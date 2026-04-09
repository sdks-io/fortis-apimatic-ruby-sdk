
# Custom Header Signature



Documentation for accessing and setting credentials for developer-id.

## Auth Credentials

| Name | Type | Description | Getter |
|  --- | --- | --- | --- |
| developer-id | `String` | Developer ID | `developer_id` |



**Note:** Auth credentials can be set using `DeveloperIdCredentials` object, passed in as named parameter `developer_id_credentials` in the client initialization.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ruby
require 'fortis_api'
include FortisApi

client = Client.new(
  developer_id_credentials: DeveloperIdCredentials.new(
    developer_id: 'developer-id'
  )
)
```


