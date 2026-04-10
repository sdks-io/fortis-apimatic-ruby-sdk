
# Resources 1

*This model accepts additional fields of type Object.*

## Structure

`Resources1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `title` | `String` | Optional | Resource Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `priv` | `String` | Optional | Priv<br><br>**Constraints**: *Maximum Length*: `64` |
| `resource_name` | `String` | Optional | Resource Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `id` | `Integer` | Optional | Resource ID |
| `last_used_date` | `Integer` | Optional | Last Used Date |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "title": "My terminal",
  "resource_name": "v2.addons.iframe.get",
  "id": 5693,
  "last_used_date": 1422040992,
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "priv": "priv0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

