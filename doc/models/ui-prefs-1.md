
# Ui Prefs 1

*This model accepts additional fields of type Object.*

## Structure

`UiPrefs1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `entry_page` | `String` | Optional | Ui Prefs Entry Page |
| `page_size` | `Integer` | Optional | Ui Prefs Page Size<br><br>**Constraints**: `>= 0`, `<= 99` |
| `report_export_type` | `Object` | Optional | - |
| `process_method` | `Object` | Optional | - |
| `default_terminal` | `String` | Optional | Ui Prefs Default Termianl<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "entry_page": "dashboard",
  "page_size": 2,
  "default_terminal": "11e95f8ec39de8fbdb0a4f1a",
  "report_export_type": {
    "key1": "val1",
    "key2": "val2"
  },
  "process_method": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

