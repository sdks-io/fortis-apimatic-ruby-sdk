
# Custom Header Signature



Documentation for accessing and setting credentials for user-api-key.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| user-api-key | `String` | User API Key | `user_api_key` |



**Note:** Auth credentials can be set using `UserApiKeyCredentials` object, passed in as named parameter `user_api_key_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ruby
require 'fortis_api'
include FortisApi

client = Client.new(
  user_api_key_credentials: UserApiKeyCredentials.new(
    user_api_key: 'user-api-key'
  )
)
```


