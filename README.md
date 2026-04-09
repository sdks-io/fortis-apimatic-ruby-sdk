
# Getting Started with Fortis API

## Install the Package

Install the gem from the command line:

```bash
gem install fortis-apimatic-sdk -v 1.0.0
```

Or add the gem to your Gemfile and run `bundle`:

```ruby
gem 'fortis-apimatic-sdk', '1.0.0'
```

For additional gem details, see the [RubyGems page for the fortis-apimatic-sdk gem](https://rubygems.org/gems/fortis-apimatic-sdk/versions/1.0.0).

## IRB Console Usage

You can explore the SDK interactively using IRB in two ways

### 1. Use IRB with Installed Gem

Open your system terminal (Command Prompt, Git Bash or macOS Terminal) and type the following command to start the irb console.

```bash
irb
```

Now you can load the SDK in the IRB

```ruby
require 'fortis_api'
include FortisApi
```

### 2. Use IRB within SDK

Open your system terminal (Command Prompt, Git Bash or macOS Terminal) and navigate to the root folder of SDK.

```
cd path/to/fortis_api
```

Now you can start the preconfigured irb console by running the following command

```bash
ruby bin/console
```

**_Note:_** This automatically loads the SDK from lib/

## Test the SDK

To run the tests, navigate to the root directory of the SDK in your terminal and execute the following command:

```
rake
```

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/README.md#environments) | The API environment. <br> **Default: `Environment.SANDBOX`** |
| connection | `Faraday::Connection` | The Faraday connection object passed by the SDK user for making requests |
| adapter | `Faraday::Adapter` | The Faraday adapter object passed by the SDK user for performing http requests |
| timeout | `Float` | The value to use for connection timeout. <br> **Default: 60** |
| max_retries | `Integer` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| retry_interval | `Float` | Pause in seconds between retries. <br> **Default: 1** |
| backoff_factor | `Float` | The amount to multiply each successive retry's interval amount by in order to provide backoff. <br> **Default: 2** |
| retry_statuses | `Array` | A list of HTTP statuses to retry. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array` | A list of HTTP methods to retry. <br> **Default: %i[get put]** |
| http_callback | `HttpCallBack` | The Http CallBack allows defining callables for pre and post API calls. |
| proxy_settings | [`ProxySettings`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/proxy-settings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| user_id_credentials | [`UserIdCredentials`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/auth/custom-header-signature.md) | The credential object for Custom Header Signature |
| user_api_key_credentials | [`UserApiKeyCredentials`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/auth/custom-header-signature-1.md) | The credential object for Custom Header Signature |
| developer_id_credentials | [`DeveloperIdCredentials`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/auth/custom-header-signature-2.md) | The credential object for Custom Header Signature |
| access_token_credentials | [`AccessTokenCredentials`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/auth/custom-header-signature-3.md) | The credential object for Custom Header Signature |

The API client can be initialized as follows:

### Code-Based Client Initialization

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
  environment: Environment::SANDBOX
)
```

### Environment-Based Client Initialization

```ruby
require 'fortis_api'
include FortisApi

# Create client from environment
client = Client.from_env
```

See the [`Environment-Based Client Initialization`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/environment-based-client-initialization.md) section for details.

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| SANDBOX | **Default** |
| PRODUCTION | - |

## Authorization

This API uses the following authentication schemes.

* [`user-id (Custom Header Signature)`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/auth/custom-header-signature.md)
* [`user-api-key (Custom Header Signature)`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/auth/custom-header-signature-1.md)
* [`developer-id (Custom Header Signature)`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/auth/custom-header-signature-2.md)
* [`access-token (Custom Header Signature)`](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/auth/custom-header-signature-3.md)

## List of APIs

* [Async Processing](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/async-processing.md)
* [Declined Recurring Transactions](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/declined-recurring-transactions.md)
* [Device Terms](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/device-terms.md)
* [Full Boarding](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/full-boarding.md)
* [3 DS Authentication](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/3-ds-authentication.md)
* [3 DS Transactions](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/3-ds-transactions.md)
* [Merchant Deposits](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/merchant-deposits.md)
* [On Boarding](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/on-boarding.md)
* [Payment Card Reader Token](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/payment-card-reader-token.md)
* [Quick Invoices](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/quick-invoices.md)
* [Transaction ACH Retries](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/transaction-ach-retries.md)
* [Transactions-ACH](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/transactions-ach.md)
* [Transactions-Cash](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/transactions-cash.md)
* [Transactions-Credit Card](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/transactions-credit-card.md)
* [Transactions-EBT Card](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/transactions-ebt-card.md)
* [Transactions-Read](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/transactions-read.md)
* [Level 3 Data](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/level-3-data.md)
* [Transactions-Updates](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/transactions-updates.md)
* [User Verifications](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/user-verifications.md)
* [Apple Pay Validate Merchant](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/apple-pay-validate-merchant.md)
* [Merchant Details](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/merchant-details.md)
* [Batches](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/batches.md)
* [Contacts](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/contacts.md)
* [Elements](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/elements.md)
* [Locations](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/locations.md)
* [Paylinks](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/paylinks.md)
* [Recurring](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/recurring.md)
* [Signatures](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/signatures.md)
* [Tags](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/tags.md)
* [Terminals](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/terminals.md)
* [Tickets](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/tickets.md)
* [Tokens](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/tokens.md)
* [Users](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/users.md)
* [Webhooks](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/controllers/webhooks.md)

## SDK Infrastructure

### Configuration

* [ProxySettings](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/proxy-settings.md)
* [Environment-Based Client Initialization](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/environment-based-client-initialization.md)

### HTTP

* [HttpResponse](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/http-response.md)
* [HttpRequest](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/http-request.md)

### Utilities

* [ApiHelper](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/api-helper.md)
* [DateTimeHelper](https://www.github.com/sdks-io/fortis-apimatic-ruby-sdk/tree/1.0.0/doc/date-time-helper.md)

