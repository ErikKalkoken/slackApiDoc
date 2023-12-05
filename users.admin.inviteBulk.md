# users.admin.inviteBulk
This method sends invitation to a new user by email.
This endpoint uses a [legacy token](https://api.slack.com/custom-integrations/legacy-tokens) to authenticate. Please make sure you are using this token type and not one of the newer types.

## Arguments
This method has the URL `https://slack.com/api/users.admin.inviteBulk` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
token|xoxs-xxxxxxxxx-xxxx|Required|Authentication token (Requires scope: `'client'`)
invites|[ { email: email, type: 'ultra_restricted', mode: 'manual' } ]|Required|An array of objects that contains email/type/mode.
channels|C1234567890,G12345678|Optional|Comma-separated list of IDs (not names!) for channels, which the new user will auto-join. Both channel IDs for public channels and group IDs for private chanels work. 
restricted|true|Optional|Invite a guest that can use multiple channels
ultra_restricted|true|Optional|Invite a guest that can use one channel only
expiration_ts|1510863690|Optional|Set the expiration timestamp for when the guest account will automatically be disabled

## Hints
- Please make sure to use a [legacy token](https://api.slack.com/custom-integrations/legacy-tokens) with this API method. It will not work with any other token type.
- Sending an invite to an email address will only work once. Additional requests to the same email address will be ignored. However, if the invite is still pending you can remove it (through the admin interface) and sent another one.

## Response
You will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics). For example if successful you get:

```json
{
  "ok": true,
  invites: [ { "ok": true }, ... ],
}
```

Note that `invites` is an array - for each invitation specified, you receive a corresponding result.

## Errors & Warnings

Error|Description
--------|-------
`already_in_team`|User is already part of the team
`already_invited`|User has already received an email invitation
`already_in_team_invited_user`|User is already part of the team (?? - more info needed on when this error occurs)
`channel_not_found`|Provided channel ID does not match a real channel
`expiration_requires_restricted` | `expiration_ts` can only be used with guest accounts
`invalid_email`|Invalid email address (e.g. "qwe"). Note that Slack does not recognize some email addresses even though they are technically valid. This is a known issue.
`invite_limit_reached`|The maximum number of invites is reached
`missing_scope`|Using an access_token not authorized for `'client'` scope. Note that you need a [legacy token](https://api.slack.com/custom-integrations/legacy-tokens) for this API method.
`not_allowed`|When SSO is enabled, this method can not be used to invite new users except guests. The [SCIM API](https://api.slack.com/scim) needs to be used instead to invite new users. For inviting guests the `restricted` or 
`not_allowed_token_type`|Token type is invalid. Workspace tokens do not seem to be compatible with this method
`not_authed`| 	No authentication token provided.
`requires_one_channel`| When ultra_restricted is true and no channel is provided. A single channel must be provided.
`sent_recently`|When using resend=true, the email has been sent recently already
`ultra_restricted`| property needs to be provided
`user_disabled`|User account has been deactivated
