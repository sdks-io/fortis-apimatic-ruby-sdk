
# Data 6

*This model accepts additional fields of type Object.*

## Structure

`Data6`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `terminal_id` | `String` | Optional | Terminal ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `require_signature` | `TrueClass \| FalseClass` | Optional | Set to true or 1 to require a signature from the customer |
| `device_term_api_id` | `String` | Optional | Can be used for associating record to external systems. Must be unique per location.<br><br>**Constraints**: *Maximum Length*: `64` |
| `terms_conditions` | `String` | Optional | This is the message that is displayed on the screen when prompting for a signature.<br><br>**Constraints**: *Maximum Length*: `4096` |
| `id` | `String` | Optional | Device term ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `reason_code_id` | `Integer` | Optional | Reason code ID |
| `signature` | [`Signature1`](../../doc/models/signature-1.md) | Optional | - |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | System generated id for user who created record<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_user` | [`User9`](../../doc/models/user-9.md) | Optional | - |
| `location` | [`Location18`](../../doc/models/location-18.md) | Optional | - |
| `terminal` | [`Terminal2`](../../doc/models/terminal-2.md) | Optional | - |
| `changelogs` | [`Array[Changelog]`](../../doc/models/changelog.md) | Optional | Changelog Information on `expand` |
| `reason_code` | [`ReasonCode1`](../../doc/models/reason-code-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "terminal_id": "11e95f8ec39de8fbdb0a4f1a",
  "require_signature": true,
  "device_term_api_id": "device_term134",
  "terms_conditions": "FUNgib0Vh0B9c0Wbttvr50vNtGLOkTdFL0eFmhN1RJpKhK14IENeDa8irp2dEk9thEcVHvVEyriQeZLs5NjNsCzqNj9JDA4RSJwK647IFtYjrNPN1nBb9bw6hoQ71oT5kpsiXGt8HcqBFVBVeDA7psIzKAyDveAw2o1hfjipkOtXrPgWun0rYwyyFuvqkT1egQYKfYDj",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "reason_code_id": 1000,
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

