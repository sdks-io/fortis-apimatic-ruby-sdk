
# Data 33

*This model accepts additional fields of type Object.*

## Structure

`Data33`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `user_api_key` | `String` | Optional | User Api Key<br><br>**Constraints**: *Minimum Length*: `16`, *Maximum Length*: `64` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "user_api_key": "234bas8dfn8238f923w2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

