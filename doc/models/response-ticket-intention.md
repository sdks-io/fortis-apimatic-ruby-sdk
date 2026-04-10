
# Response Ticket Intention

*This model accepts additional fields of type Object.*

## Structure

`ResponseTicketIntention`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type27`](../../doc/models/type-27.md) | Optional | - |
| `data` | [`Data7`](../../doc/models/data-7.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "TicketIntention",
  "data": {
    "contact_id": "contact_id4",
    "contact_api_id": "contact_api_id4",
    "location_id": "location_id4",
    "product_transaction_id": "product_transaction_id4",
    "message": "message0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

