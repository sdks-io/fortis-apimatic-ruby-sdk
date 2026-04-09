
# Response Transaction Bin Info

## Structure

`ResponseTransactionBinInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type113Enum`](../../doc/models/type-113-enum.md) | Optional | Resource Type<br><br>**Default**: `Type113Enum::TRANSACTIONBININFO` |
| `data` | [`Data28`](../../doc/models/data-28.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "TransactionBinInfo",
  "data": {
    "issuer_bank_name": "issuer_bank_name6",
    "country_code": "country_code0",
    "detail_card_product": "detail_card_product2",
    "detail_card_indicator": "detail_card_indicator2",
    "fsa_indicator": "fsa_indicator8"
  }
}
```

