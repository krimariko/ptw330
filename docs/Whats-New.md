---
stoplight-id: wc1frnxdtr1j2
---

# What's New

## Breaking Changes
These changes require special attention. If your app uses these API resources and you don’t adjust your usage of affected resources according to the following instructions, your app may break or encounter unexpected errors when you update to the latest API version.

### User Object Deprecated Fields
As of API version 2.1, the following fields of the `user` object have been deprecated: 
- `middle_name` 
- `email_address`
For user email queries, please use the new `email` parameter instead. This is a continuation of our broader API cleanup efforts that began earlier this year.

## API Release Notes

### Nov. 2023 API Release Notes
The following features were added in version 2.1 of Starwipe Productions's APIs:

- We've added the `date_created` parameter to [**Delete a User**](reference/photohostingAPI.yaml/paths/~1users~1{user_id}/delete) to assist in cases where a `user_id` or `username` are missing from an account or cannot be located.
- You can now attach a reminder note to previously archived galleries by querying `archive_reason` parameter of **Archive Gallery**.
- New look and feel: Starwipe Productions’s API documentation has adopted new formatting and a higher contrast color scheme and to improve accessibility.

## Product Release Notes

### Oct. 2023 App Release Notes
Here’s what’s new in version 3.30 of Starwipe Productions
- Uploaded image attachments from emails into the Starwipe Productions app directly from the Apple Email via the share feature.
- Nine additional filters have been added which users can use to edit their photos.
- New look and feel: users will see the Starwipe Productions app has adopted a higher contrast color scheme to improve accessibility.

### Sept. 2023 App Release Notes
Bug Fixes:
- Fixed: Users no longer need to have all galleries named before creating a new gallery. Galleries unnamed at the time of creating a new gallery will be named “Unnamed (1),” “Unnamed (2),” “Unnamed (3),” etc.
- Fixed: Gallery names over 60 characters no longer truncate incorrectly.
- Fixed: When photos fail to upload, users will now see a button in the center of their screen reading “Upload Failed. Click here to try again.” This allows users to quickly attempt this upload again instead of initiating the upload process from the beginning. 