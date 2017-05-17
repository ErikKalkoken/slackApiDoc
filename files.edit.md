# files.edit
This method changes the properties of a file object
This method has the URL `https://slack.com/api/files.edit` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
`token`|`xxxx-xxxxxxxxx-xxxx`|Required|Authentication token (Requires scope: ??)
`file`|`F12345678`|Required|ID of the file to be edited
`title`|`Brand new title`|Required|New title of the file
`filetype`|`text`|Optional|New filetype of the file. See [file object](https://api.slack.com/types/file#file_types) for a list of all supported types.
##Response
If successful you will receive the updates [file object](https://api.slack.com/types/file) as JSON.

```json
{
	"id": "F12345678",
	"created": 1458346483,
	"timestamp": 1458346483,
	"name": "BBB.gif",
	"title": "test",
	"mimetype": "image/gif",
	"filetype": "gif",
	"pretty_type": "GIF",
	"user": "U12345678",
	"editable": false,
	"size": 845468,
	"mode": "hosted",
	"is_external": false,
	"external_type": "",
	"is_public": true,
	"public_url_shared": false,
	"display_as_bot": false,
	"username": "",
	"url_private": "https://files.slack.com/files-pri/TXXX/BBB.gif",
	"url_private_download": "https://files.slack.com/files-pri/TXXX/download/BBB.gif",
	"thumb_64": "https://files.slack.com/files-tmb/TXXX-YYY/ZZZ_64.png",
	"thumb_80": "https://files.slack.com/files-tmb/TXXX-YYY/ZZZ_80.png",
	"thumb_360": "https://files.slack.com/files-tmb/TXXX-YYY/ZZZ_360.png",
	"thumb_360_w": 360,
	"thumb_360_h": 86,
	"thumb_480": "https://files.slack.com/files-tmb/TXXX-YYY/ZZZ_480.png",
	"thumb_480_w": 480,
	"thumb_480_h": 115,
	"thumb_160": "https://files.slack.com/files-tmb/TXXX-YYY/ZZZ_160.png",
	"thumb_360_gif": "https://files.slack.com/files-tmb/TXXX-YYY/ZZZ_360.gif",
	"thumb_480_gif": "https://files.slack.com/files-tmb/TXXX-YYY/ZZZ_480.gif",
	"image_exif_rotation": 1,
	"original_w": 500,
	"original_h": 120,
	"permalink": "https://myslack.slack.com/files/erik.kalkoken/F0TTA9FKQ/ZZZ.gif",
	"permalink_public": "https://slack-files.com/TXXX-AAA",
	"channels": [
		"C12345678"
	],
	"groups": [ ],
	"ims": [ ],
	"comments_count": 0
}
```
In case of errors you will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics). 
##Errors & Warnings
Error|Description
--------|-------
tbd
