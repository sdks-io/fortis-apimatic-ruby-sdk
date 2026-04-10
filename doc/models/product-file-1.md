
# Product File 1

*This model accepts additional fields of type Object.*

## Structure

`ProductFile1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `title` | `String` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `product_file_credential_id` | `String` | Optional | Product File Credential Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `free_bytes` | `Float` | Optional | Free Bytes |
| `byte_increment` | `Float` | Optional | Byte Increment |
| `max_file_size_bytes` | `Float` | Optional | Max File Size Bytes |
| `increment_cost` | `Float` | Optional | Increment Cost |
| `monthly_fee` | `Integer` | Optional | Monthly Fee |
| `file_ext_allowed` | `String` | Optional | File Ext Allowed<br><br>**Constraints**: *Maximum Length*: `64` |
| `container` | `String` | Optional | Container<br><br>**Constraints**: *Maximum Length*: `128` |
| `id` | `String` | Optional | Product File Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `active` | `TrueClass \| FalseClass` | Optional | Active |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "title": "My terminal",
  "product_file_credential_id": "11e95f8ec39de8fbdb0a4f1a",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "active": true,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "free_bytes": 13.42,
  "byte_increment": 16.74,
  "max_file_size_bytes": 221.86,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

