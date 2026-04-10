
# Identity Verification 5

*This model accepts additional fields of type Object.*

## Structure

`IdentityVerification5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dl_state` | `String` | Optional | Used for certain ACH transactions where Driver's License is required by the terminal being used.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` |
| `dl_number` | `String` | Optional | Used for certain ACH transactions where Driver's License is required by the terminal being used.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `50` |
| `ssn_4` | `String` | Optional | The last four of the account_holder social security number.<br><br>**Constraints**: *Maximum Length*: `4` |
| `dob_year` | `String` | Optional | Used for certain ACH transactions where Identity Verification is enabled on the terminal being used.<br><br>**Constraints**: *Minimum Length*: `4`, *Maximum Length*: `4`, *Pattern*: `^(19\d{2})\|20\d{2}$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "dl_state": "MI",
  "dl_number": "1235567",
  "ssn4": "8527",
  "dob_year": "1980",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

