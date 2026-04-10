
# V1 Transactions Void Request

*This model accepts additional fields of type Object.*

## Structure

`V1TransactionsVoidRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tags` | `Array[String]` | Optional | Tags |
| `description` | `String` | Optional | Description<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "description": "some description",
  "tags": [
    "tags5",
    "tags6",
    "tags7"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

