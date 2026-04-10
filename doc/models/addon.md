
# Addon

*This model accepts additional fields of type Object.*

## Structure

`Addon`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `title` | `String` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `24` |
| `secret` | `String` | Optional | Secret<br><br>**Constraints**: *Maximum Length*: `36` |
| `iframe_url` | `String` | Optional | Iframe URL<br><br>**Constraints**: *Maximum Length*: `512` |
| `location_setup_url` | `String` | Optional | Location Setup URL<br><br>**Constraints**: *Maximum Length*: `512` |
| `user_setup_url` | `String` | Optional | User Setup URL<br><br>**Constraints**: *Maximum Length*: `512` |
| `encrypt_url_params` | `TrueClass \| FalseClass` | Optional | Encrypt URL Params |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "encrypt_url_params": true,
  "title": "title4",
  "secret": "secret4",
  "iframe_url": "iframe_url4",
  "location_setup_url": "location_setup_url0",
  "user_setup_url": "user_setup_url6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

