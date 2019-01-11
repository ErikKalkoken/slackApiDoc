## Message text limits

This is a summary of all known hard limits on how Slack is rendering text in messages including attachments.
Exceeding those limits will result in text being rendered shortened, messages split into multiple messags or text becoming truncated.

### Scope
These limits apply to all known methods for sending messages:
- [Incoming Webhook](https://api.slack.com/incoming-webhooks)
- API methods, e.g. [chat.postMessage](https://api.slack.com/methods/chat.postMessage)
- Replying to a [slash command](https://api.slack.com/slash-commands) request or an [interactive message](https://api.slack.com/interactive-messages) request

### Limits
Property|Limit|Effect|Source
--|--|--|--
message text|4.000|Message will be split into multiple messages| (undocumented)
message text|40.000|Message will be truncated and a warning will be returned| [Truncating really long messages](https://api.slack.com/changelog/2018-04-truncating-really-long-messages)
attachment text|700|Attachment will be rendered shortened, but can be extended by clicking on "Show more" | ?
attachment text|8.000|Attachment will be truncated | (undocumented)

