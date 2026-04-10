
# Terminal Application

Terminal Application Information on `expand`

*This model accepts additional fields of type Object.*

## Structure

`TerminalApplication`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `standalone` | `TrueClass \| FalseClass` | Optional | Standalone |
| `emv_capable` | `TrueClass \| FalseClass` | Optional | Emv Capable |
| `nfc_capable` | `TrueClass \| FalseClass` | Optional | Nfc Capable |
| `pin_capable` | `TrueClass \| FalseClass` | Optional | Pin Capable |
| `print_capable` | `TrueClass \| FalseClass` | Optional | Print Capable |
| `msr_capable` | `TrueClass \| FalseClass` | Optional | Msr Capable |
| `sig_capture_capable` | `TrueClass \| FalseClass` | Optional | Sig Capture Capable |
| `mpos_terminal` | `TrueClass \| FalseClass` | Optional | Mpos Terminal |
| `title` | `String` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `48` |
| `description` | `String` | Optional | Description<br><br>**Constraints**: *Maximum Length*: `256` |
| `id` | `String` | Optional | Terminal Application Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "standalone": true,
  "emv_capable": true,
  "nfc_capable": false,
  "pin_capable": true,
  "print_capable": false,
  "msr_capable": true,
  "sig_capture_capable": false,
  "mpos_terminal": false,
  "title": "Ingenico Link2500",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

