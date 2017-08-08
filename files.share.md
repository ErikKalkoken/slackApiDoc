# files.share
This method changes the properties of a file object
This method has the URL `https://slack.com/api/files.share` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
`token`|`xxxx-xxxxxxxxx-xxxx`|Required|Authentication token (Requires scope: ??)
`file`|`F12345678`|Required|ID of the file to be edited
`channel`|`C12345678`|Required|ID of channel to share the file in. Works with both public (channel ID) and private channels (group ID)

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
tbd|tbd
