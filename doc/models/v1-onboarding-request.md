
# V1 Onboarding Request

*This model accepts additional fields of type Object.*

## Structure

`V1OnboardingRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `parent_id` | `String` | Optional | Location ID |
| `primary_principal` | [`PrimaryPrincipal2`](../../doc/models/primary-principal-2.md) | Required | - |
| `template_code` | `String` | Required | The ID of the template to be used - this value will be provided by Fortis.<br><br>**Constraints**: *Maximum Length*: `20`, *Pattern*: `^[a-zA-Z0-9]*$` |
| `email` | `String` | Required | Merchant email address.<br><br>**Constraints**: *Maximum Length*: `100` |
| `dba_name` | `String` | Required | Merchant 'Doing Business As' name.<br><br>**Constraints**: *Maximum Length*: `100` |
| `location` | [`Location19`](../../doc/models/location-19.md) | Required | - |
| `app_delivery` | [`AppDelivery`](../../doc/models/app-delivery.md) | Required | **Constraints**: *Maximum Length*: `12` |
| `business_category` | `Object` | Optional | - |
| `business_type` | `Object` | Optional | - |
| `business_description` | `String` | Optional | Description of Goods or Services.<br><br>**Constraints**: *Maximum Length*: `200` |
| `swiped_percent` | `Integer` | Optional | Card present/swiped percentage<br><br>> The sum total of "swiped_percent", "keyed_percent" and "ecommerce_percent" must add up to 100.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `keyed_percent` | `Integer` | Optional | Card not present/keyed percentage<br><br>> The sum total of "swiped_percent", "keyed_percent" and "ecommerce_percent" must add up to 100.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `ecommerce_percent` | `Integer` | Optional | eCommerce percentage.<br><br>> The sum total of "swiped_percent", "keyed_percent" and "ecommerce_percent" must add up to 100.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `ownership_type` | `Object` | Optional | - |
| `fed_tax_id` | `String` | Optional | Federal Tax ID (EIN).<br><br>**Constraints**: *Maximum Length*: `10` |
| `cc_average_ticket_range` | `Integer` | Optional | Average Transaction Amount Range<br><br>> (Applicable when Template Application Type is 'credit_card' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `cc_monthly_volume_range` | `Integer` | Optional | Monthly Processing Volume Range<br><br>> (Applicable when Template Application Type is 'credit_card' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `cc_high_ticket` | `Integer` | Optional | Highest transaction amount rounded to the next dollar<br><br>> (No decimal and applicable when Template Application Type is 'credit_card' or 'both').<br><br>**Constraints**: `>= 0`, `<= 30000` |
| `ec_average_ticket_range` | `Integer` | Optional | Average Transaction Amount Range<br><br>> (Applicable when Template Application Type is 'echeck' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `ec_monthly_volume_range` | `Integer` | Optional | Monthly Processing Volume Range<br><br>> (Applicable when Template Application Type is 'echeck' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `ec_high_ticket` | `Integer` | Optional | Highest transaction amount rounded to the next dollar<br><br>> (No decimal and applicable when Template Application Type is 'echeck' or 'both').<br><br>**Constraints**: `>= 0`, `<= 30000` |
| `website` | `String` | Optional | Merchant's business website.<br><br>> (Required if "ecommerce_percent" is greater than 0).<br><br>**Constraints**: *Maximum Length*: `100` |
| `bank_account` | [`BankAccount3`](../../doc/models/bank-account-3.md) | Optional | - |
| `alt_bank_account` | [`AltBankAccount2`](../../doc/models/alt-bank-account-2.md) | Optional | - |
| `legal_name` | `String` | Optional | Merchant legal name.<br><br>> (leave blank if same as DBA name).<br><br>**Constraints**: *Maximum Length*: `100` |
| `contact` | [`Contact13`](../../doc/models/contact-13.md) | Required | - |
| `client_app_id` | `String` | Optional | Client Issues Id to track that can be used to track each submitted merchant application. This id should be generated and sent in the request payload, and will be returned in the response payload. If no id is submitted in the payload request, this field will be null in the response.<br><br>**Constraints**: *Maximum Length*: `50` |
| `sec_codes` | [`Array[SecCode]`](../../doc/models/sec-code.md) | Optional | Array of SEC codes that will be allowed, Only applicable for ACH. Valid values are 'PPD', 'WEB', 'TEL', 'CCD'. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "primary_principal": {
    "first_name": "Bob",
    "last_name": "Fairview",
    "middle_name": "Nathaniel",
    "title": "Dr",
    "date_of_birth": "2021-12-01",
    "address_line_1": "1354 Oak St.",
    "address_line_2": "Unit 203",
    "city": "Dover",
    "state_province": "DE",
    "postal_code": "55022",
    "ownership_percent": 100,
    "phone_number": "555-555-1234",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "template_code": "1234YourTemplateCode",
  "email": "email@domain.com",
  "dba_name": "Discount Home Goods",
  "location": {
    "address_line_1": "1200 West Hartford Pkwy",
    "address_line_2": "Suite 2000",
    "city": "Dover",
    "state_province": "DE",
    "postal_code": "55022",
    "phone_number": "555-555-1212",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "app_delivery": "direct",
  "swiped_percent": 0,
  "keyed_percent": 0,
  "ecommerce_percent": 100,
  "fed_tax_id": "0000000000",
  "cc_average_ticket_range": 5,
  "cc_monthly_volume_range": 1,
  "cc_high_ticket": 1500,
  "ec_average_ticket_range": 5,
  "ec_monthly_volume_range": 2,
  "ec_high_ticket": 1500,
  "website": "http://www.example.com",
  "legal_name": "Total Home Goods, LLP",
  "contact": {
    "first_name": "Jeffery",
    "last_name": "Todd",
    "email": "jtodd@example.com",
    "phone_number": "555-555-3456",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "client_app_id": "ABC123",
  "parent_id": "parent_id8",
  "business_category": {
    "key1": "val1",
    "key2": "val2"
  },
  "business_type": {
    "key1": "val1",
    "key2": "val2"
  },
  "business_description": "business_description0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

