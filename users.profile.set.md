# users.profile.set
This method changes the profile of a user. e.g. it allows to change the first and last name
##Arguments
This method has the URL `https://slack.com/api/users.admin.invite` and follows the [Slack Web API calling conventions](https://api.slack.com/web#basics).

Argument|Example|Required|Description
--------|-------|--------|-----------
`token`|`xxxx-xxxxxxxxx-xxxx`|Required|Authentication token (Requires scope: ??)
`user`|`U1234567890`|Required|ID of user who's profile will be changed
`profile`|`{"first_name": "John"}`|Required|Subset of a user profile with elements to be changed as string in JSON format. See [user](https://api.slack.com/types/user) for a definition of all elements in a profile. Make sure to URL-encode it if you use GET.

Note that not all elements of a profile can be changed this way. These elements are reported to work:
- `first_name`
- `last_name`

##Response
You will receive a standard Slack API response in JSON as described [here](https://api.slack.com/web#basics). For example if successful you get:

```json
{
ok: true
}
```
##Errors & Warnings
Error|Description
--------|-------
`user_already_invited`|User has already received an email invitation
tbd
