# Webhooks

```ruby
webhooks_controller = client.webhooks
```

## Class Name

`WebhooksController`

## Methods

* [Createanewtransactionbatchpostbackconfig](../../doc/controllers/webhooks.md#createanewtransactionbatchpostbackconfig)
* [Createanewcontactpostbackconfig](../../doc/controllers/webhooks.md#createanewcontactpostbackconfig)
* [Createanewtransactionpostbackconfig](../../doc/controllers/webhooks.md#createanewtransactionpostbackconfig)
* [Deleteapostbackconfig](../../doc/controllers/webhooks.md#deleteapostbackconfig)
* [Updatetransactionbatchpostbackconfig](../../doc/controllers/webhooks.md#updatetransactionbatchpostbackconfig)
* [Updatecontactpostbackconfig](../../doc/controllers/webhooks.md#updatecontactpostbackconfig)
* [Updatetransactionpostbackconfig](../../doc/controllers/webhooks.md#updatetransactionpostbackconfig)


# Createanewtransactionbatchpostbackconfig

```ruby
def createanewtransactionbatchpostbackconfig(body,
                                             expand: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1WebhooksBatchRequest`](../../doc/models/v1-webhooks-batch-request.md) | Body, Required | - |
| `expand` | [`Array[Expand123]`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseWebhook`](../../doc/models/response-webhook.md).

## Example Usage

```ruby
body = V1WebhooksBatchRequest.new(
  is_active: true,
  location_id: '11e95f8ec39de8fbdb0a4f1a',
  on_create: true,
  on_update: true,
  on_delete: true,
  product_transaction_id: '11e95f8ec39de8fbdb0a4f1a',
  number_of_attempts: 1,
  url: 'https://127.0.0.1/receiver',
  attempt_interval: 300,
  basic_auth_username: 'tester',
  basic_auth_password: 'Test@522',
  expands: 'changelogs,tags',
  legacy: true,
  postback_config_id: '11e95f8ec39de8fbdb0a4f1a'
)

result = webhooks_controller.createanewtransactionbatchpostbackconfig(body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Createanewcontactpostbackconfig

```ruby
def createanewcontactpostbackconfig(body,
                                    expand: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1WebhooksContactRequest`](../../doc/models/v1-webhooks-contact-request.md) | Body, Required | - |
| `expand` | [`Array[Expand123]`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseWebhook`](../../doc/models/response-webhook.md).

## Example Usage

```ruby
body = V1WebhooksContactRequest.new(
  is_active: true,
  location_id: '11e95f8ec39de8fbdb0a4f1a',
  on_create: true,
  on_update: true,
  on_delete: true,
  number_of_attempts: 1,
  url: 'https://127.0.0.1/receiver',
  attempt_interval: 300,
  basic_auth_username: 'tester',
  basic_auth_password: 'Test@522',
  expands: 'changelogs,tags',
  legacy: true,
  postback_config_id: '11e95f8ec39de8fbdb0a4f1a',
  product_transaction_id: '11e95f8ec39de8fbdb0a4f1a'
)

result = webhooks_controller.createanewcontactpostbackconfig(body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Createanewtransactionpostbackconfig

```ruby
def createanewtransactionpostbackconfig(body,
                                        expand: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1WebhooksTransactionRequest`](../../doc/models/v1-webhooks-transaction-request.md) | Body, Required | - |
| `expand` | [`Array[Expand123]`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseWebhook`](../../doc/models/response-webhook.md).

## Example Usage

```ruby
body = V1WebhooksTransactionRequest.new(
  is_active: true,
  location_id: '11e95f8ec39de8fbdb0a4f1a',
  on_create: true,
  on_update: true,
  on_delete: true,
  product_transaction_id: '11e95f8ec39de8fbdb0a4f1a',
  number_of_attempts: 1,
  url: 'https://127.0.0.1/receiver',
  attempt_interval: 300,
  basic_auth_username: 'tester',
  basic_auth_password: 'Test@522',
  expands: 'changelogs,tags',
  legacy: true,
  postback_config_id: '11e95f8ec39de8fbdb0a4f1a'
)

result = webhooks_controller.createanewtransactionpostbackconfig(body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Deleteapostbackconfig

```ruby
def deleteapostbackconfig(webhook_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhook_id` | `String` | Template, Required | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseWebhook`](../../doc/models/response-webhook.md).

## Example Usage

```ruby
webhook_id = '11e95f8ec39de8fbdb0a4f1a'

result = webhooks_controller.deleteapostbackconfig(webhook_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Updatetransactionbatchpostbackconfig

```ruby
def updatetransactionbatchpostbackconfig(webhook_id,
                                         body,
                                         expand: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhook_id` | `String` | Template, Required | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1WebhooksBatchRequest1`](../../doc/models/v1-webhooks-batch-request-1.md) | Body, Required | - |
| `expand` | [`Array[Expand123]`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseWebhook`](../../doc/models/response-webhook.md).

## Example Usage

```ruby
webhook_id = '11e95f8ec39de8fbdb0a4f1a'

body = V1WebhooksBatchRequest1.new(
  attempt_interval: 300,
  basic_auth_username: 'tester',
  basic_auth_password: 'Test@522',
  expands: 'changelogs,tags',
  is_active: true,
  location_id: '11e95f8ec39de8fbdb0a4f1a',
  on_create: true,
  on_update: true,
  on_delete: true,
  legacy: true,
  postback_config_id: '11e95f8ec39de8fbdb0a4f1a',
  product_transaction_id: '11e95f8ec39de8fbdb0a4f1a',
  number_of_attempts: 1,
  url: 'https://127.0.0.1/receiver'
)

result = webhooks_controller.updatetransactionbatchpostbackconfig(
  webhook_id,
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
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Updatecontactpostbackconfig

```ruby
def updatecontactpostbackconfig(webhook_id,
                                body,
                                expand: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhook_id` | `String` | Template, Required | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1WebhooksContactRequest1`](../../doc/models/v1-webhooks-contact-request-1.md) | Body, Required | - |
| `expand` | [`Array[Expand123]`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseWebhook`](../../doc/models/response-webhook.md).

## Example Usage

```ruby
webhook_id = '11e95f8ec39de8fbdb0a4f1a'

body = V1WebhooksContactRequest1.new(
  attempt_interval: 300,
  basic_auth_username: 'tester',
  basic_auth_password: 'Test@522',
  expands: 'changelogs,tags',
  is_active: true,
  location_id: '11e95f8ec39de8fbdb0a4f1a',
  on_create: true,
  on_update: true,
  on_delete: true,
  legacy: true,
  postback_config_id: '11e95f8ec39de8fbdb0a4f1a',
  product_transaction_id: '11e95f8ec39de8fbdb0a4f1a',
  number_of_attempts: 1,
  url: 'https://127.0.0.1/receiver'
)

result = webhooks_controller.updatecontactpostbackconfig(
  webhook_id,
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
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Updatetransactionpostbackconfig

```ruby
def updatetransactionpostbackconfig(webhook_id,
                                    body,
                                    expand: nil)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhook_id` | `String` | Template, Required | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1WebhooksTransactionRequest1`](../../doc/models/v1-webhooks-transaction-request-1.md) | Body, Required | - |
| `expand` | [`Array[Expand123]`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseWebhook`](../../doc/models/response-webhook.md).

## Example Usage

```ruby
webhook_id = '11e95f8ec39de8fbdb0a4f1a'

body = V1WebhooksTransactionRequest1.new(
  attempt_interval: 300,
  basic_auth_username: 'tester',
  basic_auth_password: 'Test@522',
  expands: 'changelogs,tags',
  is_active: true,
  location_id: '11e95f8ec39de8fbdb0a4f1a',
  on_create: true,
  on_update: true,
  on_delete: true,
  legacy: true,
  postback_config_id: '11e95f8ec39de8fbdb0a4f1a',
  product_transaction_id: '11e95f8ec39de8fbdb0a4f1a',
  number_of_attempts: 1,
  url: 'https://127.0.0.1/receiver'
)

result = webhooks_controller.updatetransactionpostbackconfig(
  webhook_id,
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
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |

