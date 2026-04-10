
# Response Signature

*This model accepts additional fields of type Object.*

## Structure

`ResponseSignature`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type72`](../../doc/models/type-72.md) | Optional | - |
| `data` | [`Data21`](../../doc/models/data-21.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Signature",
  "data": {
    "signature": "signature8",
    "resource": "AccountVault",
    "resource_id": "resource_id6",
    "id": "id0",
    "created_ts": 114,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

