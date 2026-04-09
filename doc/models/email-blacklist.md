
# Email Blacklist

Email Blacklist Information on `expand`

## Structure

`EmailBlacklist`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | Blacklist ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `is_blacklisted` | `TrueClass \| FalseClass` | Optional | isBlacklisted |
| `detail` | `TrueClass \| FalseClass` | Optional | Contact Id |
| `created_ts` | `Integer` | Optional | Created Time Stamp |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "isBlacklisted": true,
  "detail": true,
  "created_ts": 1422040992
}
```

