
# Data 28

*This model accepts additional fields of type Object.*

## Structure

`Data28`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `issuer_bank_name` | `String` | Optional | The Issuer Bank name for the BIN<br><br>**Constraints**: *Maximum Length*: `60` |
| `country_code` | `String` | Optional | VISA - Three character alpha country code<br>MC - Three character alpha country code<br>Maestro - Three character alpha country code<br>Amex - Space Filled<br>Discover - Three character alpha country code or spaces when Discover doesn't share issuer country.<br><br>**Constraints**: *Maximum Length*: `2` |
| `detail_card_product` | `String` | Optional | V - Visa<br>M - MasterCard<br>A - American Express<br>D - Discover<br>N - PIN Only (Non-Visa/MasterCard/AMEX/Discover<br><br>**Constraints**: *Maximum Length*: `1` |
| `detail_card_indicator` | `String` | Optional | Left justified, Space filled<br><br>**Constraints**: *Maximum Length*: `2` |
| `fsa_indicator` | `String` | Optional | Left justified, Space filled<br><br>**Constraints**: *Maximum Length*: `1` |
| `prepaid_indicator` | `String` | Optional | P = Prepaid Card<br>Default: Space filled<br><br>**Constraints**: *Maximum Length*: `1` |
| `product_id` | `String` | Optional | P = Prepaid Card<br>Default: Space filled<br><br>**Constraints**: *Maximum Length*: `3` |
| `regulator_indicator` | `String` | Optional | P = Prepaid Card<br>Default: Space filled<br><br>**Constraints**: *Maximum Length*: `1` |
| `visa_product_sub_type` | `String` | Optional | This is used to identify product sub-types, i.e. further classification of product.<br><br>**Constraints**: *Maximum Length*: `2` |
| `visa_large_ticket_indicator` | `String` | Optional | L = Visa Large Ticket.<br>Default: Space filled<br><br>**Constraints**: *Maximum Length*: `1` |
| `account_fund_source` | `String` | Optional | For Visa, MasterCard, and Discover.  Identifies the source of the funds associated with the primary account for the card.<br><br>**Constraints**: *Maximum Length*: `1` |
| `card_class` | `String` | Optional | Categorizes the BIN as a Business card, Corporate T&E card, Purchase card or Consumer card. Assists the POS device with prompting decisions – to collect addenda or not.  Visa, MasterCard and Discover only.<br><br>**Constraints**: *Maximum Length*: `1` |
| `token_ind` | `String` | Optional | Token Indicator values:<br>Y = Token BIN<br>Default: Space filled<br>VISA, MC, and Discover Only<br><br>**Constraints**: *Maximum Length*: `1` |
| `issuing_network` | `String` | Optional | For Discover card types<br>00 - Discover<br>01 - Diners<br>02 - JCB (Japanese Credit Bank)<br>03 - CUP (China Union Pay)<br>04 PayPal<br><br>**Constraints**: *Maximum Length*: `2` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "issuer_bank_name": "Cartasi S.P.A.",
  "country_code": "US",
  "detail_card_product": "V",
  "detail_card_indicator": "X",
  "fsa_indicator": "F",
  "prepaid_indicator": "P",
  "product_id": "G",
  "regulator_indicator": "N",
  "account_fund_source": "C",
  "card_class": "B",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

