
# Terminal Cvm

Terminal Cvm Information on `expand`

## Structure

`TerminalCvm`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `terminal_manufacturer_code` | `Float` | Optional | Terminal Manufacturer Code |
| `title` | `String` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `32` |
| `contact_data` | `String` | Optional | Contact Data<br><br>**Constraints**: *Maximum Length*: `100000` |
| `contactless_data` | `String` | Optional | Contactless Data<br><br>**Constraints**: *Maximum Length*: `100000` |
| `id` | `String` | Optional | Terminal Manufacturer Cvms Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Example (as JSON)

```json
{
  "terminal_manufacturer_code": 4.0,
  "title": "CVM One",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "contact_data": "contact_data8",
  "contactless_data": "contactless_data0"
}
```

