# files.delete
This method deletes a file

## Arguments
This method has the URL `https://slack.com/api/files.delete` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
token|xxxx-xxxxxxxxx-xxxx|Required|Authentication token (Requires scope: `files:write`) ??
file|F2147483862|Required|Specify a file by providing its ID.

## Response
You will receive a standard Slack API response in JSON. If successful you get:

```json
{
"ok": true
}
```
## Errors & Warnings
I would assume you get similar errors and warnings as with [files.upload](https://api.slack.com/methods/files.upload) and [files.info](https://api.slack.com/methods/files.info)


