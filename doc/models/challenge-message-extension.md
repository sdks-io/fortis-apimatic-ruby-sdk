
# Challenge Message Extension

*This model accepts additional fields of type Object.*

## Structure

`ChallengeMessageExtension`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | A unique identifier for the extension. Payment System Registered Application Provider Identifier (RID) is required as prefix of the ID. The maximum length is 64 characters.<br><br>**Constraints**: *Maximum Length*: `64` |
| `name` | `String` | Optional | The name of the extension data set as defined by the extension owner. Maximum length is 64 characters.<br><br>**Constraints**: *Maximum Length*: `64` |
| `criticality_indicator` | `TrueClass \| FalseClass` | Optional | A boolean value indicating whether the recipient must understand the contents of the extension to interpret the entire message. |
| `data` | `Object` | Optional | The data carried in the extension as. The maximum length is 8059 characters. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "id8",
  "name": "name8",
  "criticality_indicator": false,
  "data": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

