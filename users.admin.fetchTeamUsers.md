# users.admin.fetchTeamUsers

This method queries all users in a Slack team. It's the API that backed "Manage members" UI.

Note: In my tests, it only works with `xoxs-` token, which can be captured with browser devtool.

## Arguments

This method has the URL `https://slack.com/api/users.admin.setInactive` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
token|xoxs-xxxxxxxxx-xxxx|Required|Authentication token
query|{"type":"and","clauses":[{"type":"is","value":"user"},{"type":"fuzzy_with_email","value":"john"}]}|Required|The query that matches users
count|100|Optional|Max returned users count
include_bots|0|Optional|Include bot users
exclude_slackbot|true|Optional|Exclude slackbot
include_deleted|0|Optional|Show deactivated accounts
sort_dir|asc|Optional|Sorting direction
sort|real_name|Optional|Sorting field

## Response

You will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics). For example if successful you get:

```json
{
  "ok": true,
  "items": [
    {
      "id": "U12345678",
      "team_id": "T12345678",
      "name": "john",
      "deleted": false,
      "color": "ffffff",
      "real_name": "john",
      "tz": "Asia/Chongqing",
      "tz_label": "China Standard Time",
      "tz_offset": 28800,
      "profile": {
        "title": "",
        "phone": "",
        "skype": "",
        "real_name": "john",
        "real_name_normalized": "john",
        "display_name": "john",
        "display_name_normalized": "john",
        "fields": null,
        "status_text": "",
        "status_emoji": "",
        "status_expiration": 0,
        "avatar_hash": "a1b2c3",
        "image_original": "https://avatars.slack-edge.com/xxx/xxx_original.png",
        "email": "john.doe@email.com",
        "first_name": "john",
        "last_name": "",
        "image_24": "https://avatars.slack-edge.com/xxx/xxx_24.png",
        "image_32": "https://avatars.slack-edge.com/xxx/xxx_32.png",
        "image_48": "https://avatars.slack-edge.com/xxx/xxx_48.png",
        "image_72": "https://avatars.slack-edge.com/xxx/xxx_72.png",
        "image_192": "https://avatars.slack-edge.com/xxx/xxx_192.png",
        "image_512": "https://avatars.slack-edge.com/xxx/xxx_512.png",
        "image_1024": "https://avatars.slack-edge.com/xxx/xxx_1024.png",
        "status_text_canonical": "",
        "team": "T12345678",
        "is_custom_image": true
      },
      "is_admin": false,
      "is_owner": false,
      "is_primary_owner": false,
      "is_restricted": false,
      "is_ultra_restricted": false,
      "is_bot": false,
      "is_app_user": false,
      "updated": 1427028409,
      "created": 1406714043,
      "is_inactive": 1,
      "username_is_editable": true,
      "email_is_editable": true,
      "two_factor_auth_enabled": false
    }
  ],
  "teams": [],
  "num_found": 1,
  "next_cursor_mark": "xxxxxxx=="
}
```

## Errors & Warnings

Error|Description
--------|-------
not_allowed_token_type|Error message when accessed with a wrong type of token
missing_query|Error message when query is not provided
