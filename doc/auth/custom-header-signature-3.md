
# Custom Header Signature



Documentation for accessing and setting credentials for access-token.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| access-token | `String` | Access Token | `access_token` |



**Note:** Auth credentials can be set using `AccessTokenCredentials` object, passed in as named parameter `access_token_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ruby
require 'fortis_api'
include FortisApi

client = Client.new(
  access_token_credentials: AccessTokenCredentials.new(
    access_token: 'access-token'
  )
)
```


