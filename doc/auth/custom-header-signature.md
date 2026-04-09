
# Custom Header Signature



Documentation for accessing and setting credentials for user-id.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| user-id | `String` | User ID | `user_id` |



**Note:** Auth credentials can be set using `UserIdCredentials` object, passed in as named parameter `user_id_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ruby
require 'fortis_api'
include FortisApi

client = Client.new(
  user_id_credentials: UserIdCredentials.new(
    user_id: 'user-id'
  )
)
```


