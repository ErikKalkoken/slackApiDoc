# users.admin.invite
This method sends invitation to a new user by email
##Arguments
This method has the URL `https://slack.com/api/users.admin.invite` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
token|xxxx-xxxxxxxxx-xxxx|Required|Authentication token (Requires scope: ??)
email|john.doe@email.com|Required|Email address of the new user
channels|C1234567890|Optional|Comma-separated list of channel names or IDs which the new user will auto-join
first_name|John|Optional|Prefilled input for the "First name" field on the "new user registration" page.
last_name|Doe|Optional|Prefilled input for the "Last name" field on the "new user registration" page.

##Response
You will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics). For example if successful you get:

```json
{
ok: true
}
```
##Errors & Warnings
Error|Description
--------|-------
`already_invited`|User has already received an email invitation
`already_in_team`|User is already part of the team
tbd
