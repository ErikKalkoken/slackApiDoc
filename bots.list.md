# bots.list
This method returns a list of all apps in the current workspace, simular to [users.list](https://api.slack.com/methods/users.list).

## Arguments
This method has the URL `https://slack.com/api/bots.list` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
token|xxxx-xxxxxxxxx-xxxx|Required|Authentication token (Requires scope: `'read'` - only works with legacy tokens)

## Response
You will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics). For example if successful you get:

```json
{
  "ok": true,
  "bots": [
    {
      "id": "B12345678",
      "deleted": false,
      "name": "magic-webhook",
      "updated": 1451148229,
      "app_id": "A12345678",
      "icons": {
        "image_36": "https://a.slack-edge.com/xxx/plugins/_skeleton/assets/service_36.png",
        "image_48": "https://a.slack-edge.com/xxx/plugins/_skeleton/assets/service_48.png",
        "image_72": "https://a.slack-edge.com/xxx/plugins/_skeleton/assets/service_72.png"
      }
    },
    {
      "id": "B12345679",
      "deleted": false,
      "name": "Slack API Tester",
      "updated": 1464779158,
      "app_id": "A02",
      "icons": {
        "image_36": "https://a.slack-edge.com/xxx/plugins/app/assets/service_36.png",
        "image_48": "https://a.slack-edge.com/xxx/plugins/app/assets/service_48.png",
        "image_72": "https://a.slack-edge.com/xxx/plugins/app/assets/service_72.png"
      }
    }
   ]
}

```
## Errors & Warnings
Error|Description
--------|-------
`missing_scope`| Tried to call the method with a token that does not have the `read` scope

