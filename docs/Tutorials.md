---
stoplight-id: 3n5kpy07jjotc
---

# Tutorials

<!-- theme: info -->
>If you are not already authorized as a developer with the Starwipe API, you must login to your [developer dashboard](https://developer.starwipecom/dashboard) and register for an API key before making any requests. For more information, see [Authentication](Authentication.md).

## Making a Request

To make a request, first find the HTTP method and endpoint for the operation that you want to use. For example, the [Create User](../reference/photohostingAPI.yaml/paths/~1users/post) operation uses the `POST` method and the `/users` endpoint. 

For the full list of endpoints and operations, see the [API Reference](../reference/photohostingAPI.yaml) section.

### Example: Create a New User

Here is an example request using cURL that creates a new user. To test out this request, replace the API key in the example code with your own unique API key.
```cURL
curl --request POST \
  --url https://api.starwipe.com/v2/users \
  --header 'Accept: application/json' \
  --header 'Content-Type: application/json' \
  --header 'X-API-KEY: 9Ii7kjBFSEczqen0hdARvU5XytVHJQ' \
  --data '{
  "username": "whitelodge23",
  "email": "dbcooper@fbi.gov",
  "first_name": "Dale",
  "last_name": "Cooper",
  "privacy_enabled": true
}'
```

Continue reading to learn how to send parameters and use the response.

#### *More video and written tutorials coming soon!*
