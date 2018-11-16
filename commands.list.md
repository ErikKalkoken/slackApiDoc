# commands.list
This method returns a list of all available slash command for a workspace including custom slash commands.

## Arguments
This method has the URL `https://slack.com/api/commands.list` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
`token`|`xxxx-xxxxxxxxx-xxxx`|Required|Authentication token (Requires scope: `post`)

## Response
Returns a list of slash command objects.

Typical success response
```json
{
  "ok": true,
  "commands": 
  {
    "/feed": 
    {
      "canonical_name": "/feed",
      "usage": "help [or subscribe, list, remove…]",
      "desc": "Manage RSS subscriptions",
      "name": "/feed",
      "type": "core"
    },
    "/evetime": 
    {
      "usage": "[about]",
      "desc": "Shows the current Eve Online time",
      "name": "/evetime",
      "type": "app",
      "app": "A12345678"
    },
    "/eveprice": 
    {
      "usage": "[name of item to display the current price for, e.g. Merlin]",
      "desc": "Shows current Jita prices for an item",
      "name": "/eveprice",
      "type": "app",
      "app": "A22345678"
    },
    "/evestatus": 
    {
      "usage": "[about]",
      "desc": "Shows the current status of the Eve Online server",
      "name": "/evestatus",
      "type": "app",
      "app": "A32345678"
    },
    "/evestruct": 
    {
      "usage": "[name of solar system]",
      "desc": "Shows list of public structures in a solar system",
      "name": "/evestruct",
      "type": "app",
      "app": "A42345678"
    }
}
```
In case of errors you will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics). 

## Chat command type
The slash command object can be on of two types indicated by the `type` property:
- `core`: a core slash command provided by Slack
- `app`: a custom slash command provided by a Slack app. For app types you will also find the corresponding `app_id` in the slash command object.


## Errors & Warnings
Error|Description
--------|-------
`missing_scope`|The method requires the scope `post`. Since this scope does not seam to be availble in the app config window you need to provide a legacy token for this to work.

tbd
