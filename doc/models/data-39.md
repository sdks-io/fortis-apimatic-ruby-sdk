
# Data 39

*This model accepts additional fields of type Object.*

## Structure

`Data39`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `attempt_interval` | `Integer` | Optional | Number of seconds before another retry is submitted<br><br>**Default**: `300`<br><br>**Constraints**: `>= 300`, `<= 86400` |
| `basic_auth_username` | `String` | Optional | Basic Auth Username Information on `expand` |
| `basic_auth_password` | `String` | Optional | Basic Auth Password Information on `expand` |
| `expands` | `String` | Optional | An option list of expanded data to send with base data. (i.e. set this field to “contact,account_vault” to get the contact an accountvault used to run a transaction.)<br><br>**Constraints**: *Maximum Length*: `512` |
| `format` | `Object` | Optional | - |
| `is_active` | `TrueClass \| FalseClass` | Optional | Flag to indicate whether configuration is active (in effect). |
| `location_id` | `String` | Optional | The location identifier of the resource you want to recieve postbacks from.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `location_api_id` | `String` | Optional | Location Api ID |
| `on_create` | `TrueClass \| FalseClass` | Optional | To receive postbacks on the creation of a resource |
| `on_update` | `TrueClass \| FalseClass` | Optional | To receive postbacks on the updating of a resource |
| `on_delete` | `TrueClass \| FalseClass` | Optional | To receive postbacks when the record is deleted |
| `legacy` | `TrueClass \| FalseClass` | Optional | Prefer the legacy api format.<br><br>**Default**: `true` |
| `postback_config_id` | `String` | Optional | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `product_transaction_id` | `String` | Optional | Required when using 'transaction' or 'transactionbatch' resource<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `resource` | [`Resource12`](../../doc/models/resource-12.md) | Optional | **Constraints**: *Maximum Length*: `128` |
| `number_of_attempts` | `Integer` | Optional | Maximum number of attempts on failure<br><br>**Constraints**: `>= 1`, `<= 5` |
| `url` | `String` | Optional | The URL where the postback will be submitted<br><br>**Constraints**: *Maximum Length*: `512` |
| `id` | `String` | Optional | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `postback_logs` | [`Array[PostbackLog]`](../../doc/models/postback-log.md) | Optional | Postback Log Information on `expand` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "attempt_interval": 300,
  "basic_auth_username": "username",
  "basic_auth_password": "password",
  "expands": "changelogs,tags",
  "is_active": true,
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "on_create": true,
  "on_update": true,
  "on_delete": true,
  "legacy": true,
  "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "number_of_attempts": 1,
  "url": "https://127.0.0.1/receiver",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "format": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

