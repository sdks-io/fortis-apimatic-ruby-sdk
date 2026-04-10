
# Merchant Risk Indicator 1

*This model accepts additional fields of type Object.*

## Structure

`MerchantRiskIndicator1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ship_indicator` | [`ShipIndicator`](../../doc/models/ship-indicator.md) | Optional | - |
| `delivery_timeframe` | [`DeliveryTimeframe`](../../doc/models/delivery-timeframe.md) | Optional | - |
| `delivery_email_address` | `String` | Optional | For electronic delivery, the email address to which the merchandise was delivered. |
| `reorder_items_ind` | [`ReorderItemsInd`](../../doc/models/reorder-items-ind.md) | Optional | - |
| `pre_order_purchase_ind` | [`PreOrderPurchaseInd`](../../doc/models/pre-order-purchase-ind.md) | Optional | - |
| `pre_order_date` | `String` | Optional | For a pre-ordered purchase, the expected date that the merchandise will be available. Date format must be YYYYMMDD. |
| `gift_card_amount` | `Integer` | Optional | For prepaid or gift card purchase, the purchase amount total of prepaid or gift card(s) in major units (for example, USD 123.45 is 123). |
| `gift_card_curr` | `String` | Optional | For prepaid or gift card purchase, the currency code of the card as defined in ISO 4217 except 955 - 964 and 999. |
| `gift_card_count` | `Integer` | Optional | For prepaid or gift card purchase, total count of individual prepaid or gift cards/codes purchased.<br><br>**Constraints**: `>= 0`, `<= 99` |
| `trans_char` | [`Array[TransChar]`](../../doc/models/trans-char.md) | Optional | Available starting in EMV 3DS 2.3.1.1.  Indicates to the ACS specific transactions identified by the Merchant.<br><br>> 01 - Cryptocurrency transaction<br>> <br>> 02 - NFT transaction<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `2` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "delivery_email_address": "fortis@example.com",
  "ship_indicator": "01",
  "delivery_timeframe": "01",
  "reorder_items_ind": "01",
  "pre_order_purchase_ind": "01",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

