# users.profile.set
This method changes the profile of a user. e.g. it allows to change the first and last name
## Arguments
This method has the URL `https://slack.com/api/users.profile.set` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
`token`|`xxxx-xxxxxxxxx-xxxx`|Required|Authentication token (Requires scope: users.profile:write)
`user`|`U1234567890`|Required|ID of user who's profile will be changed
`profile`|`{"first_name": "John"}`|Required|Subset of a user profile with elements to be changed as string in JSON format. See [user](https://api.slack.com/types/user) for a definition of all elements in a profile. Make sure to URL-encode it if you use GET.

Note that not all attributes of a profile can be changed this way. These attributes can be changed:
- `first_name`
- `last_name`
- `title`
- `phone`
- `skype`

## Response
If successful you will receive the updates [file object](https://api.slack.com/types/file) as JSON.

```json
{
	"id": "U12345678",
	"team_id": "T12345678",
	"name": "erik.kalkoken",
	"deleted": false,
	"status": null,
	"color": "9f69e7",
	"real_name": "Erik Kalkoken",
	"tz": "America/Chicago",
	"tz_label": "Central Daylight Time",
	"tz_offset": 3600,
	"profile": 
	{
		"avatar_hash": "XXX",
		"first_name": "Erik",
		"last_name": "Kalkoken",
		"title": "",
		"phone": "",
		"skype": "",
		"image_24": "https://avatars.slack-edge.com/2016-03-19/XXX_24.jpg",
		"image_32": "https://avatars.slack-edge.com/2016-03-19/XXX_32.jpg",
		"image_48": "https://avatars.slack-edge.com/2016-03-19/XXX_48.jpg",
		"image_72": "https://avatars.slack-edge.com/2016-03-19/XXX_72.jpg",
		"image_192": "https://avatars.slack-edge.com/2016-03-19/XXX_192.jpg",
		"image_512": "https://avatars.slack-edge.com/2016-03-19/XXX_512.jpg",
		"image_1024": "https://avatars.slack-edge.com/2016-03-19/XXX_512.jpg",
		"image_original": "https://avatars.slack-edge.com/2016-03-19/XXX_original.jpg",
		"real_name": "Erik Kalkoken",
		"real_name_normalized": "Erik Kalkoken",
		"email": "test@email.com"
	},
	"is_admin": false,
	"is_owner": false,
	"is_primary_owner": false,
	"is_restricted": false,
	"is_ultra_restricted": false,
	"is_bot": false,
	"has_2fa": false
}
```

## Errors & Warnings
In case of errors you will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics).

Error|Description
--------|-------
tbd
