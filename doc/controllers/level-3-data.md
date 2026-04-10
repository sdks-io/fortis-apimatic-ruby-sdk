# Level 3 Data

```ruby
level3_data_controller = client.level3_data
```

## Class Name

`Level3DataController`

## Methods

* [Createanew Level 3 Entryfora Master Card](../../doc/controllers/level-3-data.md#createanew-level-3-entryfora-master-card)
* [Createanew Level 3 Entryfora Visa](../../doc/controllers/level-3-data.md#createanew-level-3-entryfora-visa)
* [Deleteasinglelevel 3 Record](../../doc/controllers/level-3-data.md#deleteasinglelevel-3-record)
* [Viewsinglelevel 3 Record](../../doc/controllers/level-3-data.md#viewsinglelevel-3-record)


# Createanew Level 3 Entryfora Master Card

```ruby
def createanew_level3entryfora_master_card(transaction_id,
                                           body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transaction_id` | `String` | Template, Required | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1TransactionsLevel3MasterCardRequest`](../../doc/models/v1-transactions-level-3-master-card-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseTransactionLevel3Master`](../../doc/models/response-transaction-level-3-master.md).

## Example Usage

```ruby
transaction_id = '11e95f8ec39de8fbdb0a4f1a'

body = V1TransactionsLevel3MasterCardRequest.new(
  level3_data: Level3Data3.new(
    line_items: [
      LineItem19.new(
        description: 'cool drink',
        product_code: 'coke12345678',
        unit_code: 'gll',
        unit_cost: 10,
        alternate_tax_id: '1234',
        discount_amount: 10,
        discount_rate: 11,
        quantity: 5,
        tax_amount: 3,
        tax_rate: 0,
        tax_type_applied: '22',
        tax_type_id: 'a1'
      )
    ],
    destination_country_code: '840',
    duty_amount: 0,
    freight_amount: 0,
    national_tax: 2,
    sales_tax: 200,
    shipfrom_zip_code: 'AZ12345',
    shipto_zip_code: 'MI48335',
    tax_amount: 0
  )
)

result = level_3_data_controller.createanew_level3entryfora_master_card(
  transaction_id,
  body
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "TransactionLevel3Master",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "level3_data": {
      "destination_country_code": "840",
      "duty_amount": 0,
      "freight_amount": 0,
      "national_tax": 2,
      "sales_tax": 200,
      "shipfrom_zip_code": "AZ1234",
      "shipto_zip_code": "FL1234",
      "tax_amount": 10,
      "tax_exempt": "0",
      "customer_vat_registration": "12345678",
      "merchant_vat_registration": "123456",
      "order_date": "171006",
      "summary_commodity_code": "C1K2",
      "tax_rate": 0,
      "unique_vat_ref_number": "vat1234",
      "line_items": [
        {
          "description": "cool drink",
          "commodity_code": "cc123456",
          "discount_amount": 0,
          "other_tax_amount": 0,
          "product_code": "fanta123456",
          "quantity": 12,
          "tax_amount": 4,
          "tax_rate": 0,
          "unit_code": "gll",
          "unit_cost": 3,
          "alternate_tax_id": "1234",
          "debit_credit": "C",
          "discount_rate": 11,
          "tax_type_applied": "22",
          "tax_type_id": "11"
        }
      ]
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Createanew Level 3 Entryfora Visa

```ruby
def createanew_level3entryfora_visa(transaction_id,
                                    body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transaction_id` | `String` | Template, Required | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1TransactionsLevel3VisaRequest`](../../doc/models/v1-transactions-level-3-visa-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseTransactionLevel3Visa`](../../doc/models/response-transaction-level-3-visa.md).

## Example Usage

```ruby
transaction_id = '11e95f8ec39de8fbdb0a4f1a'

body = V1TransactionsLevel3VisaRequest.new(
  level3_data: Level3Data4.new(
    line_items: [
      LineItem20.new(
        description: 'cool drink',
        commodity_code: 'cc123456',
        product_code: 'fanta123456',
        unit_code: 'gll',
        unit_cost: 3,
        discount_amount: 0,
        other_tax_amount: 0,
        quantity: 12,
        tax_amount: 4,
        tax_rate: 0
      )
    ],
    destination_country_code: '840',
    duty_amount: 0,
    freight_amount: 0,
    national_tax: 2,
    sales_tax: 200,
    shipfrom_zip_code: 'AZ1234',
    shipto_zip_code: 'FL1234',
    tax_amount: 10,
    customer_vat_registration: '12345678',
    merchant_vat_registration: '123456',
    order_date: '171006',
    summary_commodity_code: 'C1K2',
    tax_rate: 0,
    unique_vat_ref_number: 'vat1234'
  )
)

result = level_3_data_controller.createanew_level3entryfora_visa(
  transaction_id,
  body
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "TransactionLevel3Visa",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "level3_data": {
      "destination_country_code": "840",
      "duty_amount": 0,
      "freight_amount": 0,
      "national_tax": 2,
      "sales_tax": 200,
      "shipfrom_zip_code": "AZ1234",
      "shipto_zip_code": "FL1234",
      "tax_amount": 10,
      "tax_exempt": "0",
      "customer_vat_registration": "12345678",
      "merchant_vat_registration": "123456",
      "order_date": "171006",
      "summary_commodity_code": "C1K2",
      "tax_rate": 0,
      "unique_vat_ref_number": "vat1234",
      "line_items": [
        {
          "description": "cool drink",
          "commodity_code": "cc123456",
          "discount_amount": 0,
          "other_tax_amount": 0,
          "product_code": "fanta123456",
          "quantity": 12,
          "tax_amount": 4,
          "tax_rate": 0,
          "unit_code": "gll",
          "unit_cost": 3,
          "alternate_tax_id": "1234",
          "debit_credit": "C",
          "discount_rate": 11,
          "tax_type_applied": "22",
          "tax_type_id": "11"
        }
      ]
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Deleteasinglelevel 3 Record

```ruby
def deleteasinglelevel3record(transaction_id,
                              level3_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transaction_id` | `String` | Template, Required | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `level_3_id` | `String` | Template, Required | Level 3 ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseTransactionLevel3`](../../doc/models/response-transaction-level-3.md).

## Example Usage

```ruby
transaction_id = '11e95f8ec39de8fbdb0a4f1a'

level3_id = '11e95f8ec39de8fbdb0a4f1a'

result = level_3_data_controller.deleteasinglelevel3record(
  transaction_id,
  level3_id
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "TransactionLevel3",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "level3_data": {
      "destination_country_code": "840",
      "duty_amount": 0,
      "freight_amount": 0,
      "national_tax": 2,
      "sales_tax": 200,
      "shipfrom_zip_code": "AZ1234",
      "shipto_zip_code": "FL1234",
      "tax_amount": 10,
      "tax_exempt": "0",
      "customer_vat_registration": "12345678",
      "merchant_vat_registration": "123456",
      "order_date": "171006",
      "summary_commodity_code": "C1K2",
      "tax_rate": 0,
      "unique_vat_ref_number": "vat1234",
      "line_items": [
        {
          "description": "cool drink",
          "commodity_code": "cc123456",
          "discount_amount": 0,
          "other_tax_amount": 0,
          "product_code": "fanta123456",
          "quantity": 12,
          "tax_amount": 4,
          "tax_rate": 0,
          "unit_code": "gll",
          "unit_cost": 3,
          "alternate_tax_id": "1234",
          "debit_credit": "C",
          "discount_rate": 11,
          "tax_type_applied": "22",
          "tax_type_id": "11"
        }
      ]
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Viewsinglelevel 3 Record

```ruby
def viewsinglelevel3record(transaction_id,
                           level3_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transaction_id` | `String` | Template, Required | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `level_3_id` | `String` | Template, Required | Level 3 ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseTransactionLevel3`](../../doc/models/response-transaction-level-3.md).

## Example Usage

```ruby
transaction_id = '11e95f8ec39de8fbdb0a4f1a'

level3_id = '11e95f8ec39de8fbdb0a4f1a'

result = level_3_data_controller.viewsinglelevel3record(
  transaction_id,
  level3_id
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "TransactionLevel3",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "level3_data": {
      "destination_country_code": "840",
      "duty_amount": 0,
      "freight_amount": 0,
      "national_tax": 2,
      "sales_tax": 200,
      "shipfrom_zip_code": "AZ1234",
      "shipto_zip_code": "FL1234",
      "tax_amount": 10,
      "tax_exempt": "0",
      "customer_vat_registration": "12345678",
      "merchant_vat_registration": "123456",
      "order_date": "171006",
      "summary_commodity_code": "C1K2",
      "tax_rate": 0,
      "unique_vat_ref_number": "vat1234",
      "line_items": [
        {
          "description": "cool drink",
          "commodity_code": "cc123456",
          "discount_amount": 0,
          "other_tax_amount": 0,
          "product_code": "fanta123456",
          "quantity": 12,
          "tax_amount": 4,
          "tax_rate": 0,
          "unit_code": "gll",
          "unit_cost": 3,
          "alternate_tax_id": "1234",
          "debit_credit": "C",
          "discount_rate": 11,
          "tax_type_applied": "22",
          "tax_type_id": "11"
        }
      ]
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |

