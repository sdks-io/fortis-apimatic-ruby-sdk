
# Response User Api Key

*This model accepts additional fields of type Object.*

## Structure

`ResponseUserApiKey`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type128`](../../doc/models/type-128.md) | Optional | - |
| `data` | [`Data33`](../../doc/models/data-33.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "UserApiKey",
  "data": {
    "user_api_key": "user_api_key2",
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

