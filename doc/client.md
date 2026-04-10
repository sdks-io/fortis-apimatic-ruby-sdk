
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| connection | `Faraday::Connection` | The Faraday connection object passed by the SDK user for making requests |
| adapter | `Faraday::Adapter` | The Faraday adapter object passed by the SDK user for performing http requests |
| timeout | `Float` | The value to use for connection timeout. <br> **Default: 60** |
| max_retries | `Integer` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| retry_interval | `Float` | Pause in seconds between retries. <br> **Default: 1** |
| backoff_factor | `Float` | The amount to multiply each successive retry's interval amount by in order to provide backoff. <br> **Default: 2** |
| retry_statuses | `Array` | A list of HTTP statuses to retry. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array` | A list of HTTP methods to retry. <br> **Default: %i[get put]** |
| http_callback | `HttpCallBack` | The Http CallBack allows defining callables for pre and post API calls. |
| proxy_settings | [`ProxySettings`](../doc/proxy-settings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](../doc/logging-configuration.md) | The SDK logging configuration for API calls |
| user_id_credentials | [`UserIdCredentials`](auth/custom-header-signature.md) | The credential object for Custom Header Signature |
| user_api_key_credentials | [`UserApiKeyCredentials`](auth/custom-header-signature-1.md) | The credential object for Custom Header Signature |
| developer_id_credentials | [`DeveloperIdCredentials`](auth/custom-header-signature-2.md) | The credential object for Custom Header Signature |
| access_token_credentials | [`AccessTokenCredentials`](auth/custom-header-signature-3.md) | The credential object for Custom Header Signature |

The API client can be initialized as follows:

## Code-Based Client Initialization

```ruby
require 'fortis_api'
include FortisApi

client = Client.new(
  user_id_credentials: UserIdCredentials.new(
    user_id: 'user-id'
  ),
  user_api_key_credentials: UserApiKeyCredentials.new(
    user_api_key: 'user-api-key'
  ),
  developer_id_credentials: DeveloperIdCredentials.new(
    developer_id: 'developer-id'
  ),
  access_token_credentials: AccessTokenCredentials.new(
    access_token: 'access-token'
  ),
  environment: Environment::PRODUCTION,
  logging_configuration: LoggingConfiguration.new(
    log_level: Logger::INFO,
    request_logging_config: RequestLoggingConfiguration.new(
      log_body: true
    ),
    response_logging_config: ResponseLoggingConfiguration.new(
      log_headers: true
    )
  )
)
```

## Environment-Based Client Initialization

```ruby
require 'fortis_api'
include FortisApi

# Create client from environment
client = Client.from_env
```

See the [`Environment-Based Client Initialization`](../doc/environment-based-client-initialization.md) section for details.

## Fortis API Client

The gateway for the SDK. This class acts as a factory for the Controllers and also holds the configuration of the SDK.

## Controllers

| Name | Description |
|  --- | --- |
| async_processing | Gets AsyncProcessingController |
| batches | Gets BatchesController |
| contacts | Gets ContactsController |
| declined_recurring_transactions | Gets DeclinedRecurringTransactionsController |
| device_terms | Gets DeviceTermsController |
| elements | Gets ElementsController |
| full_boarding | Gets FullBoardingController |
| locations | Gets LocationsController |
| m_3_ds_authentication | Gets M3DsAuthenticationController |
| m_3_ds_transactions | Gets M3DsTransactionsController |
| merchant_deposits | Gets MerchantDepositsController |
| on_boarding | Gets OnBoardingController |
| paylinks | Gets PaylinksController |
| payment_card_reader_token | Gets PaymentCardReaderTokenController |
| quick_invoices | Gets QuickInvoicesController |
| recurring | Gets RecurringController |
| signatures | Gets SignaturesController |
| tags | Gets TagsController |
| terminals | Gets TerminalsController |
| tickets | Gets TicketsController |
| tokens | Gets TokensController |
| transaction_ach_retries | Gets TransactionAchRetriesController |
| transactions_ach | Gets TransactionsAchController |
| transactions_cash | Gets TransactionsCashController |
| transactions_credit_card | Gets TransactionsCreditCardController |
| transactions_ebt_card | Gets TransactionsEbtCardController |
| transactions_read | Gets TransactionsReadController |
| level_3_data | Gets Level3DataController |
| transactions_updates | Gets TransactionsUpdatesController |
| user_verifications | Gets UserVerificationsController |
| users | Gets UsersController |
| apple_pay_validate_merchant | Gets ApplePayValidateMerchantController |
| merchant_details | Gets MerchantDetailsController |
| webhooks | Gets WebhooksController |

