# Declined Recurring Transactions

```ruby
declined_recurring_transactions_controller = client.declined_recurring_transactions
```

## Class Name

`DeclinedRecurringTransactionsController`

## Methods

* [Getone Declined Recurring Transaction](../../doc/controllers/declined-recurring-transactions.md#getone-declined-recurring-transaction)
* [Listall Declined Recurring Transactions](../../doc/controllers/declined-recurring-transactions.md#listall-declined-recurring-transactions)
* [Createapayment](../../doc/controllers/declined-recurring-transactions.md#createapayment)
* [Rerunthetransaction](../../doc/controllers/declined-recurring-transactions.md#rerunthetransaction)
* [Resendthetransaction](../../doc/controllers/declined-recurring-transactions.md#resendthetransaction)


# Getone Declined Recurring Transaction

```ruby
def getone_declined_recurring_transaction(declined_recurring_transaction_id,
                                          expand: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `declined_recurring_transaction_id` | `String` | Template, Required | Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `expand` | [`Array[Expand5]`](../../doc/models/expand-5.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseDeclinedRecurringTransaction`](../../doc/models/response-declined-recurring-transaction.md).

## Example Usage

```ruby
declined_recurring_transaction_id = '11e95f8ec39de8fbdb0a4f1a'

result = declined_recurring_transactions_controller.getone_declined_recurring_transaction(declined_recurring_transaction_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "DeclinedRecurringTransaction",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "status": "paid",
    "recurring_id": "11e95f8ec39de8fbdb0a4f1a",
    "created_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
    "modified_ts": 1422040992,
    "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Listall Declined Recurring Transactions

```ruby
def listall_declined_recurring_transactions(page: nil,
                                            order: nil,
                                            filter_by: nil,
                                            expand: nil,
                                            format: nil,
                                            typeahead: nil,
                                            fields: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | [`Page1`](../../doc/models/page-1.md) | Query, Optional | Use this field to specify paginate your results, by using page size and number. You can use one of the following methods:<br><br>> /endpoint?page={ "number": 1, "size": 50 }<br>> <br>> /endpoint?page[number]=1&page[size]=50 |
| `order` | [`Array[Order21]`](../../doc/models/order-21.md) | Query, Optional | Criteria used in query string parameters to order results.  Most fields from the endpoint results can be used as a `key`.  Unsupported fields or operators will return a `412`.  Must be encoded, or use syntax that does not require encoding.<br><br>> /endpoint?order[0][key]=created_ts&order[0][operator]=asc<br>> <br>> /endpoint?order=[{ "key": "created_ts", "operator": "asc"}]<br>> <br>> /endpoint?order=[{ "key": "balance", "operator": "desc"},{ "key": "created_ts", "operator": "asc"}]<br><br>**Constraints**: *Minimum Items*: `1` |
| `filter_by` | [`Array[FilterBy]`](../../doc/models/filter-by.md) | Query, Optional | Filter criteria that can be used in query string parameters.  Most fields from the endpoint results can be used as a `key`.  Unsupported fields or operators will return a `412`. Must be encoded, or use syntax that does not require encoding.<br><br>> ?filter_by[0][key]=first_name&filter_by[0][operator]==&filter_by[0][value]=Steve<br>> <br>> /endpoint?filter_by=[{ "key": "first_name", "operator": "=", "value": "Fred" }]<br>> <br>> /endpoint?filter_by=[{ "key": "account_type", "operator": "=", "value": "VISA" }]<br>> <br>> /endpoint?filter_by=[{ "key": "created_ts", "operator": ">=", "value": "946702799" }, { "key": "created_ts", "operator": "<=", value: "1695061891" }]<br>> <br>> /endpoint?filter_by=[{ "key": "last_name", "operator": "IN", "value": "Williams,Brown,Allman" }]<br><br>**Constraints**: *Minimum Items*: `1` |
| `expand` | [`Array[Expand5]`](../../doc/models/expand-5.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |
| `format` | [`Format1`](../../doc/models/format-1.md) | Query, Optional | Reporting format, valid values: csv, tsv |
| `typeahead` | `String` | Query, Optional | You can use any `field_name` from this endpoint results to order the list using the value provided as filter for the same `field_name`. It will be ordered using the following rules: 1) Exact match, 2) Starts with, 3) Contains.<br><br>> /endpoint?filter={ "field_name": "Value" }&_typeahead=field_name |
| `fields` | [`Array[Field30]`](../../doc/models/field-30.md) | Query, Optional | You can use any `field_name` from this endpoint results to filter the list of fields returned on the response. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseDeclinedRecurringTransactionsCollection`](../../doc/models/response-declined-recurring-transactions-collection.md).

## Example Usage

```ruby
page = Page1.new(
  number: 1,
  size: 50
)

order = [
  Order21.new(
    key: 'first_name',
    operator: Operator::ASC
  )
]

filter_by = [
  FilterBy.new(
    key: 'first_name',
    operator: Operator1::ENUM_1,
    value: 'Fred'
  )
]

result = declined_recurring_transactions_controller.listall_declined_recurring_transactions(
  page: page,
  order: order,
  filter_by: filter_by
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
  "type": "DeclinedRecurringTransactionsCollection",
  "list": [
    {
      "id": "11e95f8ec39de8fbdb0a4f1a",
      "status": "paid",
      "recurring_id": "11e95f8ec39de8fbdb0a4f1a",
      "created_ts": 1422040992,
      "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
      "modified_ts": 1422040992,
      "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
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
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Createapayment

```ruby
def createapayment(body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1DeclinedRecurringTransactionPaymentsRequest`](../../doc/models/v1-declined-recurring-transaction-payments-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseDeclinedRecurringTransactionPayment`](../../doc/models/response-declined-recurring-transaction-payment.md).

## Example Usage

```ruby
body = V1DeclinedRecurringTransactionPaymentsRequest.new(
  declined_recurring_transaction_id: '11e95f8ec39de8fbdb0a4f1a',
  account_number: '5454545454545454',
  exp_date: '0722',
  transaction_amount: 0,
  account_holder_name: 'John Doe',
  description: 'Description',
  save_account_title: 'John Account',
  subtotal_amount: 599,
  surcharge_amount: 599
)

result = declined_recurring_transactions_controller.createapayment(body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "DeclinedRecurringTransactionPayment",
  "data": {
    "declined_recurring_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "account_number": "5454545454545454",
    "account_holder_name": "John Doe",
    "exp_date": "0722",
    "transaction_amount": 0,
    "description": "Description",
    "billing_address": {
      "postal_code": "48375",
      "city": "Novi",
      "state": "Michigan",
      "phone": "3339998822",
      "country": "USA"
    },
    "tags": [
      "Walk-in Customer"
    ],
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "first_six": "700953",
    "last_four": "3657",
    "routing": null,
    "reason_code_id": 1000,
    "created_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Rerunthetransaction

```ruby
def rerunthetransaction(declined_recurring_transaction_id,
                        expand: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `declined_recurring_transaction_id` | `String` | Template, Required | Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `expand` | [`Array[Expand5]`](../../doc/models/expand-5.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseDeclinedRecurringTransaction`](../../doc/models/response-declined-recurring-transaction.md).

## Example Usage

```ruby
declined_recurring_transaction_id = '11e95f8ec39de8fbdb0a4f1a'

result = declined_recurring_transactions_controller.rerunthetransaction(declined_recurring_transaction_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "DeclinedRecurringTransaction",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "status": "paid",
    "recurring_id": "11e95f8ec39de8fbdb0a4f1a",
    "created_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
    "modified_ts": 1422040992,
    "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Resendthetransaction

```ruby
def resendthetransaction(declined_recurring_transaction_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `declined_recurring_transaction_id` | `String` | Template, Required | Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseDeclinedRecurringTransactionResend`](../../doc/models/response-declined-recurring-transaction-resend.md).

## Example Usage

```ruby
declined_recurring_transaction_id = '11e95f8ec39de8fbdb0a4f1a'

result = declined_recurring_transactions_controller.resendthetransaction(declined_recurring_transaction_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "DeclinedRecurringTransactionResend",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "email_log_id": "11e95f8ec39de8fbdb0a4f1a",
    "email": "email@domain.com"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |

