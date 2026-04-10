# Paylinks

Paylinks is a way for merchants to create a link that can be used to make a payment. The link can optionally be sent out via email/sms to a customer. Paylinks is similar to Quick Invoices but much simpler.

```ruby
paylinks_controller = client.paylinks
```

## Class Name

`PaylinksController`

## Methods

* [Createanew Paylink](../../doc/controllers/paylinks.md#createanew-paylink)
* [Listall Paylinks](../../doc/controllers/paylinks.md#listall-paylinks)
* [Delete Paylink](../../doc/controllers/paylinks.md#delete-paylink)
* [View Single Paylink](../../doc/controllers/paylinks.md#view-single-paylink)
* [Update Paylink](../../doc/controllers/paylinks.md#update-paylink)
* [Resend Paylink](../../doc/controllers/paylinks.md#resend-paylink)


# Createanew Paylink

Generate a new Paylink to be sent via email, sms or grab the payment_url to embed in you own messaging system.

```ruby
def createanew_paylink(body,
                       expand: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1PaylinksRequest`](../../doc/models/v1-paylinks-request.md) | Body, Required | - |
| `expand` | [`Array[Expand17]`](../../doc/models/expand-17.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponsePaylink`](../../doc/models/response-paylink.md).

## Example Usage

```ruby
body = V1PaylinksRequest.new(
  amount_due: 1,
  location_id: '11e95f8ec39de8fbdb0a4f1a',
  cc_product_transaction_id: '11e95f8ec39de8fbdb0a4f1a',
  email: 'email@domain.com',
  contact_id: '11e95f8ec39de8fbdb0a4f1a',
  ach_product_transaction_id: '11e95f8ec39de8fbdb0a4f1a',
  expire_date: '2021-12-01',
  display_product_transaction_receipt_details: true,
  display_billing_fields: true,
  cell_phone: '3339998822',
  description: 'Description',
  store_token: false,
  store_token_title: 'John Account',
  bank_funded_only_override: false,
  redirect_url_delay: 15
)

result = paylinks_controller.createanew_paylink(body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "Paylink",
  "data": {
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "cc_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "email": "email@domain.com",
    "amount_due": 1,
    "contact_id": "11e95f8ec39de8fbdb0a4f1a",
    "ach_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "expire_date": "2021-12-01",
    "display_product_transaction_receipt_details": true,
    "display_billing_fields": true,
    "delivery_method": 0,
    "cell_phone": "3339998822",
    "description": "Description",
    "store_token": false,
    "store_token_title": "John Account",
    "bank_funded_only_override": false,
    "tags": [
      "Tag 1"
    ],
    "redirect_url_delay": 15,
    "redirect_url_on_approve": null,
    "redirect_url_on_decline": null,
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "status_id": true,
    "status_code": 1,
    "active": true,
    "created_ts": 1422040992,
    "modified_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
    "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Listall Paylinks

Pull in all Paylinks associated with the location_id.

```ruby
def listall_paylinks(page: nil,
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
| `expand` | [`Array[Expand18]`](../../doc/models/expand-18.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |
| `format` | [`Format1`](../../doc/models/format-1.md) | Query, Optional | Reporting format, valid values: csv, tsv |
| `typeahead` | `String` | Query, Optional | You can use any `field_name` from this endpoint results to order the list using the value provided as filter for the same `field_name`. It will be ordered using the following rules: 1) Exact match, 2) Starts with, 3) Contains.<br><br>> /endpoint?filter={ "field_name": "Value" }&_typeahead=field_name |
| `fields` | [`Array[Field39]`](../../doc/models/field-39.md) | Query, Optional | You can use any `field_name` from this endpoint results to filter the list of fields returned on the response. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponsePaylinksCollection`](../../doc/models/response-paylinks-collection.md).

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

result = paylinks_controller.listall_paylinks(
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
  "type": "PaylinksCollection",
  "list": [
    {
      "location_id": "11e95f8ec39de8fbdb0a4f1a",
      "cc_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
      "email": "email@domain.com",
      "amount_due": 1,
      "contact_id": "11e95f8ec39de8fbdb0a4f1a",
      "ach_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
      "expire_date": "2021-12-01",
      "display_product_transaction_receipt_details": true,
      "display_billing_fields": true,
      "delivery_method": 0,
      "cell_phone": "3339998822",
      "description": "Description",
      "store_token": false,
      "store_token_title": "John Account",
      "bank_funded_only_override": false,
      "tags": [
        "Tag 1"
      ],
      "redirect_url_delay": 15,
      "redirect_url_on_approve": null,
      "redirect_url_on_decline": null,
      "id": "11e95f8ec39de8fbdb0a4f1a",
      "status_id": true,
      "status_code": 1,
      "active": true,
      "created_ts": 1422040992,
      "modified_ts": 1422040992,
      "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
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


# Delete Paylink

Delete an existing Paylink_id

```ruby
def delete_paylink(paylink_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paylink_id` | `String` | Template, Required | System generatedPaylink Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponsePaylink`](../../doc/models/response-paylink.md).

## Example Usage

```ruby
paylink_id = '11e95f8ec39de8fbdb0a4f1a'

result = paylinks_controller.delete_paylink(paylink_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "Paylink",
  "data": {
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "cc_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "email": "email@domain.com",
    "amount_due": 1,
    "contact_id": "11e95f8ec39de8fbdb0a4f1a",
    "ach_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "expire_date": "2021-12-01",
    "display_product_transaction_receipt_details": true,
    "display_billing_fields": true,
    "delivery_method": 0,
    "cell_phone": "3339998822",
    "description": "Description",
    "store_token": false,
    "store_token_title": "John Account",
    "bank_funded_only_override": false,
    "tags": [
      "Tag 1"
    ],
    "redirect_url_delay": 15,
    "redirect_url_on_approve": null,
    "redirect_url_on_decline": null,
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "status_id": true,
    "status_code": 1,
    "active": true,
    "created_ts": 1422040992,
    "modified_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
    "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# View Single Paylink

Use the Paylink_id obtained from the Create request to look up the status

```ruby
def view_single_paylink(paylink_id,
                        expand: nil,
                        fields: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paylink_id` | `String` | Template, Required | System generatedPaylink Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `expand` | [`Array[Expand18]`](../../doc/models/expand-18.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |
| `fields` | [`Array[Field39]`](../../doc/models/field-39.md) | Query, Optional | You can use any `field_name` from this endpoint results to filter the list of fields returned on the response. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponsePaylink`](../../doc/models/response-paylink.md).

## Example Usage

```ruby
paylink_id = '11e95f8ec39de8fbdb0a4f1a'

result = paylinks_controller.view_single_paylink(paylink_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "Paylink",
  "data": {
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "cc_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "email": "email@domain.com",
    "amount_due": 1,
    "contact_id": "11e95f8ec39de8fbdb0a4f1a",
    "ach_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "expire_date": "2021-12-01",
    "display_product_transaction_receipt_details": true,
    "display_billing_fields": true,
    "delivery_method": 0,
    "cell_phone": "3339998822",
    "description": "Description",
    "store_token": false,
    "store_token_title": "John Account",
    "bank_funded_only_override": false,
    "tags": [
      "Tag 1"
    ],
    "redirect_url_delay": 15,
    "redirect_url_on_approve": null,
    "redirect_url_on_decline": null,
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "status_id": true,
    "status_code": 1,
    "active": true,
    "created_ts": 1422040992,
    "modified_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
    "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Update Paylink

Update an existing Paylink_id

```ruby
def update_paylink(paylink_id,
                   body,
                   expand: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paylink_id` | `String` | Template, Required | System generatedPaylink Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1PaylinksRequest1`](../../doc/models/v1-paylinks-request-1.md) | Body, Required | - |
| `expand` | [`Array[Expand17]`](../../doc/models/expand-17.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponsePaylink`](../../doc/models/response-paylink.md).

## Example Usage

```ruby
paylink_id = '11e95f8ec39de8fbdb0a4f1a'

body = V1PaylinksRequest1.new(
  location_id: '11e95f8ec39de8fbdb0a4f1a',
  cc_product_transaction_id: '11e95f8ec39de8fbdb0a4f1a',
  email: 'email@domain.com',
  amount_due: 1,
  contact_id: '11e95f8ec39de8fbdb0a4f1a',
  ach_product_transaction_id: '11e95f8ec39de8fbdb0a4f1a',
  expire_date: '2021-12-01',
  display_product_transaction_receipt_details: true,
  display_billing_fields: true,
  cell_phone: '3339998822',
  description: 'Description',
  store_token: false,
  store_token_title: 'John Account',
  bank_funded_only_override: false,
  redirect_url_delay: 15
)

result = paylinks_controller.update_paylink(
  paylink_id,
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
  "type": "Paylink",
  "data": {
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "cc_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "email": "email@domain.com",
    "amount_due": 1,
    "contact_id": "11e95f8ec39de8fbdb0a4f1a",
    "ach_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "expire_date": "2021-12-01",
    "display_product_transaction_receipt_details": true,
    "display_billing_fields": true,
    "delivery_method": 0,
    "cell_phone": "3339998822",
    "description": "Description",
    "store_token": false,
    "store_token_title": "John Account",
    "bank_funded_only_override": false,
    "tags": [
      "Tag 1"
    ],
    "redirect_url_delay": 15,
    "redirect_url_on_approve": null,
    "redirect_url_on_decline": null,
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "status_id": true,
    "status_code": 1,
    "active": true,
    "created_ts": 1422040992,
    "modified_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
    "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Resend Paylink

Resend the Paylink via email or sms

```ruby
def resend_paylink(paylink_id,
                   expand: nil,
                   email: nil,
                   sms: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `paylink_id` | `String` | Template, Required | System generatedPaylink Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `expand` | [`Array[Expand17]`](../../doc/models/expand-17.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |
| `email` | [`Email`](../../doc/models/email.md) | Query, Optional | Resend Email |
| `sms` | [`Sms`](../../doc/models/sms.md) | Query, Optional | Resend SMS |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponsePaylink`](../../doc/models/response-paylink.md).

## Example Usage

```ruby
paylink_id = '11e95f8ec39de8fbdb0a4f1a'

result = paylinks_controller.resend_paylink(paylink_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "Paylink",
  "data": {
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "cc_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "email": "email@domain.com",
    "amount_due": 1,
    "contact_id": "11e95f8ec39de8fbdb0a4f1a",
    "ach_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "expire_date": "2021-12-01",
    "display_product_transaction_receipt_details": true,
    "display_billing_fields": true,
    "delivery_method": 0,
    "cell_phone": "3339998822",
    "description": "Description",
    "store_token": false,
    "store_token_title": "John Account",
    "bank_funded_only_override": false,
    "tags": [
      "Tag 1"
    ],
    "redirect_url_delay": 15,
    "redirect_url_on_approve": null,
    "redirect_url_on_decline": null,
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "status_id": true,
    "status_code": 1,
    "active": true,
    "created_ts": 1422040992,
    "modified_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
    "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |

