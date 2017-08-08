# users.admin.setInactive
This method disables a user. A disabled user can no longer log into a Slack team.
Note: This method does not work on free tier.

## Arguments
This method has the URL `https://slack.com/api/users.admin.setInactive` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
token|xxxx-xxxxxxxxx-xxxx|Required|Authentication token (Requires scope: ??)
user|U1234567890|Required|ID of the user to be disabled

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
paid_only|Error message when used with a free Slack team
