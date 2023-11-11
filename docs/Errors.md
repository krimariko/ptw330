---
stoplight-id: g2583nfajuy06
---

# Errors & Troubleshooting

Recognize and respond to errors such as failure to upload images, failure to create an account, and failure to archive a gallery.


## HTTP Error Codes

Starwipe uses standard HTTP codes when responding to API calls. Response codes in the *2xx* range indicate a successful action. 

Response codes in the *4xx* range indicate that the request could not be completed due to an error with the API call such as a missing API key in the header or invalid parameter.

Codes in the *5xx* range indicate that the request could not be processed due to a problem with our servers.

Below are HTTP *4xx* errors and common explanations.


| Error                  | Description                                                                                       |
|------------------------|---------------------------------------------------------------------------------------------------|
| 400 - Bad Request      | The request was unacceptable, often due to a missing required parameter.                          |
| 401 - Unauthorized     | No valid API key provided.                                                                        |
| 402: Request Failed    | Parameters were valid but the request failed. This usually indicates a server glitch on our end. In most cases resending the request solves the issue.|
| 403: Forbidden         | The API key doesn’t have permission to perform the request.                                       |
| 404: Not Found         | Requested resource doesn’t exist.                                                                 |
| 409: Conflict          | The request conflicts with another request.                                                       |
| 429: Too Many Requests | Too many requests hit the API too quickly.                                                        |

## Error Types
Some errors, often with code *400* or *401*, return specific information about the type of error and reason it occurred. You can use this data to troubleshoot failed API calls.

The table below lists all possible error types and their descriptions.

| **Error**                       | **Error Type**                 | **Description**                                                                                                                                                                                    |
|----------------------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fail to create user              | `user_creation_error`           | New user cannot be created due to one of the following conditions: `username` already in use, `email` missing, `email` already in use, or `username` does not meet criteria.    |
| Fail to upload single photo      | `image_upload_error`       | Failed attempt at uploading a single photo. Check photo type: Starwipe only accepts JPEG and HEIC formats at this time.                                                                |
| Fail to upload a group of photos | `image_group_upload_error` | Failed attempt at uploading a group of 2 or more photos. Check photo type: Starwipe only accepts JPEG and HEIC formats at this time. Maximum group upload size is 2,000 photos.      |
| Fail to create gallery           | `gallery_creation_error`        | New gallery cannot be created due to one of the following conditions: `user_id` missing or does not exist                                                                                                                                  |
| Fail to authenticate          | `api_key_invalid`        | API key is invalid or missing. If the key appears to be valid but authentication failed, the API key is likely inactive in your account. Manage your API keys in the [developer dashboard]( https://developer.starwipe.com/dashboard).                                                                                                                                  |
| Fail to access the requested resource           | `id_invalid`        | The id used to retrieve a particular object is invalid or does not exist.                                                                                                                                  |


### Access Stored Information About Failures
Objects store information about their most recent failure. When needing to troubleshoot a past error, you can retrieve an object and examine its stored data to determine the source of the failure, then choose a response to correct it.

For example, to learn more about a failure that occurred previously when updating a user profile, you can:
1. Retrieve the relevant user by calling [Get User](../reference/photohostingAPI.yaml/paths/~1users~1{user_id}/get).
2. Note the value of `last_error_type`. (If the field is empty, the user does not have any associated errors).
3. Review the table of **Error Types** in the section above for details about the stored error.

