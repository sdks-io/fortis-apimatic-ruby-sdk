# Merchant Deposits

```ruby
merchant_deposits_controller = client.merchant_deposits
```

## Class Name

`MerchantDepositsController`

## Methods

* [View Single Merchant Deposit](../../doc/controllers/merchant-deposits.md#view-single-merchant-deposit)
* [List All Merchant Deposits](../../doc/controllers/merchant-deposits.md#list-all-merchant-deposits)


# View Single Merchant Deposit

```ruby
def view_single_merchant_deposit(deposit_id,
                                 page: nil,
                                 order: nil,
                                 filter_by: nil,
                                 expand: nil,
                                 format: nil,
                                 typeahead: nil,
                                 fields: nil,
                                 keyword: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deposit_id` | `String` | Template, Required | Deposit Id |
| `page` | [`Page`](../../doc/models/page.md) | Query, Optional | Use this field to specify paginate your results, by using page size and number. You can use one of the following methods:<br><br>> /endpoint?page={ "number": 1, "size": 50 }<br>> <br>> /endpoint?page[number]=1&page[size]=50 |
| `order` | [`Array[Order21]`](../../doc/models/order-21.md) | Query, Optional | Criteria used in query string parameters to order results.  Most fields from the endpoint results can be used as a `key`.  Unsupported fields or operators will return a `412`.  Must be encoded, or use syntax that does not require encoding.<br><br>> /endpoint?order[0][key]=created_ts&order[0][operator]=asc<br>> <br>> /endpoint?order=[{ "key": "created_ts", "operator": "asc"}]<br>> <br>> /endpoint?order=[{ "key": "balance", "operator": "desc"},{ "key": "created_ts", "operator": "asc"}]<br><br>**Constraints**: *Minimum Items*: `1` |
| `filter_by` | [`Array[FilterBy]`](../../doc/models/filter-by.md) | Query, Optional | Filter criteria that can be used in query string parameters.  Most fields from the endpoint results can be used as a `key`.  Unsupported fields or operators will return a `412`. Must be encoded, or use syntax that does not require encoding.<br><br>> ?filter_by[0][key]=first_name&filter_by[0][operator]==&filter_by[0][value]=Steve<br>> <br>> /endpoint?filter_by=[{ "key": "first_name", "operator": "=", "value": "Fred" }]<br>> <br>> /endpoint?filter_by=[{ "key": "account_type", "operator": "=", "value": "VISA" }]<br>> <br>> /endpoint?filter_by=[{ "key": "created_ts", "operator": ">=", "value": "946702799" }, { "key": "created_ts", "operator": "<=", value: "1695061891" }]<br>> <br>> /endpoint?filter_by=[{ "key": "last_name", "operator": "IN", "value": "Williams,Brown,Allman" }]<br><br>**Constraints**: *Minimum Items*: `1` |
| `expand` | [`Array[Expand15Enum]`](../../doc/models/expand-15-enum.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required*, *Pattern*: `^[\w]+$` |
| `format` | [`Format1Enum`](../../doc/models/format-1-enum.md) | Query, Optional | Reporting format, valid values: csv, tsv |
| `typeahead` | `String` | Query, Optional | You can use any `field_name` from this endpoint results to order the list using the value provided as filter for the same `field_name`. It will be ordered using the following rules: 1) Exact match, 2) Starts with, 3) Contains.<br><br>> /endpoint?filter={ "field_name": "Value" }&_typeahead=field_name |
| `fields` | [`Array[Field37Enum]`](../../doc/models/field-37-enum.md) | Query, Optional | You can use any `field_name` from this endpoint results to filter the list of fields returned on the response. |
| `keyword` | String \| Float \| nil | Query, Optional | This is a container for any-of cases. |

## Response Type

[`ResponseMerchantDeposit`](../../doc/models/response-merchant-deposit.md)

## Example Usage

```ruby
deposit_id = 'deposit_id0'

page = Page.new(
  1,
  50
)

order = [
  Order21.new(
    'first_name',
    OperatorEnum::ASC
  )
]

filter_by = [
  FilterBy.new(
    'first_name',
    Operator1Enum::ENUM_1,
    'Fred'
  )
]

result = merchant_deposits_controller.view_single_merchant_deposit(
  deposit_id,
  page: page,
  order: order,
  filter_by: filter_by
)
puts result
```

## Example Response *(as JSON)*

```json
{
  "type": "MerchantDeposit",
  "data": {
    "company_id": "8410111",
    "merchant_id": "88441",
    "deposit_types": [
      "deposit"
    ],
    "deposit_amount": 2487.24,
    "batch_amount": 2487.24,
    "adjustment_amount": 2487.24,
    "retained_amount": 2487.24,
    "conveyed_amount": 2487.24,
    "fee_amount": 2487.24,
    "reference_number": "400000",
    "trace_number": "400000",
    "currency": "USD",
    "created_ts": 1422040992,
    "reported_date": "2021-12-01",
    "transaction_date": "2021-12-01",
    "details": [
      {
        "amount": 2487.24,
        "reported_date": "2021-12-01",
        "settled_date": "2021-12-01"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401tokenException`](../../doc/models/response-401-token-exception.md) |


# List All Merchant Deposits

```ruby
def list_all_merchant_deposits(page: nil,
                               order: nil,
                               filter_by: nil,
                               expand: nil,
                               format: nil,
                               typeahead: nil,
                               fields: nil,
                               keyword: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | [`Page`](../../doc/models/page.md) | Query, Optional | Use this field to specify paginate your results, by using page size and number. You can use one of the following methods:<br><br>> /endpoint?page={ "number": 1, "size": 50 }<br>> <br>> /endpoint?page[number]=1&page[size]=50 |
| `order` | [`Array[Order21]`](../../doc/models/order-21.md) | Query, Optional | Criteria used in query string parameters to order results.  Most fields from the endpoint results can be used as a `key`.  Unsupported fields or operators will return a `412`.  Must be encoded, or use syntax that does not require encoding.<br><br>> /endpoint?order[0][key]=created_ts&order[0][operator]=asc<br>> <br>> /endpoint?order=[{ "key": "created_ts", "operator": "asc"}]<br>> <br>> /endpoint?order=[{ "key": "balance", "operator": "desc"},{ "key": "created_ts", "operator": "asc"}]<br><br>**Constraints**: *Minimum Items*: `1` |
| `filter_by` | [`Array[FilterBy]`](../../doc/models/filter-by.md) | Query, Optional | Filter criteria that can be used in query string parameters.  Most fields from the endpoint results can be used as a `key`.  Unsupported fields or operators will return a `412`. Must be encoded, or use syntax that does not require encoding.<br><br>> ?filter_by[0][key]=first_name&filter_by[0][operator]==&filter_by[0][value]=Steve<br>> <br>> /endpoint?filter_by=[{ "key": "first_name", "operator": "=", "value": "Fred" }]<br>> <br>> /endpoint?filter_by=[{ "key": "account_type", "operator": "=", "value": "VISA" }]<br>> <br>> /endpoint?filter_by=[{ "key": "created_ts", "operator": ">=", "value": "946702799" }, { "key": "created_ts", "operator": "<=", value: "1695061891" }]<br>> <br>> /endpoint?filter_by=[{ "key": "last_name", "operator": "IN", "value": "Williams,Brown,Allman" }]<br><br>**Constraints**: *Minimum Items*: `1` |
| `expand` | [`Array[Expand15Enum]`](../../doc/models/expand-15-enum.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required*, *Pattern*: `^[\w]+$` |
| `format` | [`Format1Enum`](../../doc/models/format-1-enum.md) | Query, Optional | Reporting format, valid values: csv, tsv |
| `typeahead` | `String` | Query, Optional | You can use any `field_name` from this endpoint results to order the list using the value provided as filter for the same `field_name`. It will be ordered using the following rules: 1) Exact match, 2) Starts with, 3) Contains.<br><br>> /endpoint?filter={ "field_name": "Value" }&_typeahead=field_name |
| `fields` | [`Array[Field38Enum]`](../../doc/models/field-38-enum.md) | Query, Optional | You can use any `field_name` from this endpoint results to filter the list of fields returned on the response. |
| `keyword` | String \| Float \| nil | Query, Optional | This is a container for any-of cases. |

## Response Type

[`ResponseMerchantDepositsCollection`](../../doc/models/response-merchant-deposits-collection.md)

## Example Usage

```ruby
page = Page.new(
  1,
  50
)

order = [
  Order21.new(
    'first_name',
    OperatorEnum::ASC
  )
]

filter_by = [
  FilterBy.new(
    'first_name',
    Operator1Enum::ENUM_1,
    'Fred'
  )
]

result = merchant_deposits_controller.list_all_merchant_deposits(
  page: page,
  order: order,
  filter_by: filter_by
)
puts result
```

## Example Response *(as JSON)*

```json
{
  "type": "MerchantDepositsCollection",
  "list": [
    {
      "company_id": "8410111",
      "merchant_id": "88441",
      "deposit_types": [
        "deposit"
      ],
      "deposit_amount": 2487.24,
      "batch_amount": 2487.24,
      "adjustment_amount": 2487.24,
      "retained_amount": 2487.24,
      "conveyed_amount": 2487.24,
      "fee_amount": 2487.24,
      "reference_number": "400000",
      "trace_number": "400000",
      "currency": "USD",
      "created_ts": 1422040992,
      "reported_date": "2021-12-01",
      "transaction_date": "2021-12-01",
      "details": [
        {
          "amount": 2487.24,
          "reported_date": "2021-12-01",
          "settled_date": "2021-12-01"
        }
      ]
    }
  ],
  "links": {
    "type": "Links",
    "first": "/v1/endpoint?page[size]=10&page[number]=1",
    "previous": "/v1/endpoint?page[size]=10&page[number]=5",
    "next": "/v1/endpoint?page[size]=10&page[number]=7",
    "last": "/v1/endpoint?page[size]=10&page[number]=42"
  },
  "pagination": {
    "type": "Pagination",
    "total_count": 423,
    "page_count": 42,
    "page_number": 6,
    "page_size": 10
  },
  "sort": {
    "type": "Sorting",
    "fields": [
      {
        "field": "last_name",
        "order": "asc"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401tokenException`](../../doc/models/response-401-token-exception.md) |

