# channels.delete
This method deletes a public channel

## Arguments
This method has the URL `https://slack.com/api/channels.delete` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
token|xxxx-xxxxxxxxx-xxxx|Required|Authentication token (Requires scope: `'client'`)
channel|C1234567890|Required|ID for channel to be deleted

## Response
You will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics). For example if successful you get:

```json
{
   "ok": true
}
```
## Errors & Warnings
Error|Description
--------|-------
`channel_not_found`|Provided channel ID does not match a real channel
`missing_scope`|Using an access_token with insufficient permissions
tbd.
