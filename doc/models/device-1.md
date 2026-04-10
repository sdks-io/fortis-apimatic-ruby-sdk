
# Device 1

*This model accepts additional fields of type Object.*

## Structure

`Device1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `device_binding_status` | [`DeviceBindingStatus`](../../doc/models/device-binding-status.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "device_binding_status": "01",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

