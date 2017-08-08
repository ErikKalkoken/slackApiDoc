# chat.command
This method executes a slash command in a public channel.
This method has the URL `https://slack.com/api/chat.command` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
`token`|`xxxx-xxxxxxxxx-xxxx`|Required|Authentication token (Requires scope: `post`)
`channel`|`C12345678`|Required|ID of the public channel to execute the command in
`command`|`/who`|Required|Slash command to be executed. Leading backslash is required.
`text`|`xxxx-xxxxxxxxx-xxxx`|Optional|Additional parameters provided to the slash command

## Response
You will receive a response in JSON indicating if the command has been executed successfully or not with the `ok` variable. 
For some internal commands (e.g. `/who`) the response of the slash command will be provided in the `response` variable. For most slash commands  the response will instead be produced in the channel on Slack.

```json
{
	"ok": true,
	"response": "Users here: ..."
}
```

## Errors & Warnings
In case of errors you will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics). 

Error|Description
--------|-------
`missing_scope`|The method requires the scope `post`. Since this scope does not seam to be availble in the app config window you need to provide a legacy token for this to work.

tbd

