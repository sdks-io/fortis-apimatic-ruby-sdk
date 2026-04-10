
# Log Email

*This model accepts additional fields of type Object.*

## Structure

`LogEmail`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `subject` | `String` | Optional | Subject<br><br>**Constraints**: *Maximum Length*: `256` |
| `body` | `String` | Optional | Body |
| `source_address` | `String` | Optional | Source Address<br><br>**Constraints**: *Maximum Length*: `64` |
| `return_path` | `String` | Optional | Return Path<br><br>**Constraints**: *Maximum Length*: `64` |
| `provider_id` | `String` | Optional | Provider<br><br>**Constraints**: *Maximum Length*: `60` |
| `domain_id` | `String` | Optional | Domain<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `reason_sent` | `String` | Optional | Reason Sent<br><br>**Constraints**: *Maximum Length*: `36` |
| `reason_model` | `Object` | Optional | - |
| `reason_model_id` | `String` | Optional | Reason Model<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `reply_to` | `String` | Optional | Reply To<br><br>**Constraints**: *Maximum Length*: `520` |
| `id` | `String` | Optional | Log Email Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "subject": "Payment Receipt - 12skiestech",
  "body": "This email is being sent from a server.",
  "source_address": "\"12skiestech A7t3qi\" <noreply@zeamster.email>",
  "return_path": "\"12skiestech A7t3qi\" <noreply@zeamster.email>",
  "provider_id": "0100017e67bcc530-e1dd23b4-8a39-4a5b-8d5d-68d51c4c942f-000000",
  "domain_id": "11e95f8ec39de8fbdb0a4f1a",
  "reason_sent": "Contact Email",
  "reason_model_id": "11e95f8ec39de8fbdb0a4f1a",
  "reply_to": "\"Zeamster\" <emma.p@zeamster.com>",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

