
# Device

Contains device information.

Available for supporting EMV 3DS 2.3.1 and later versions.

*This model accepts additional fields of type Object.*

## Structure

`Device`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `device_binding_status` | [`DeviceBindingStatus`](../../doc/models/device-binding-status.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "device_binding_status": "38",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

