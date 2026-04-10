# Apple Pay Validate Merchant

```ruby
apple_pay_validate_merchant_controller = client.apple_pay_validate_merchant
```

## Class Name

`ApplePayValidateMerchantController`


# Apple Pay Validate Merchant

Apple Pay Validate Merchant

```ruby
def apple_pay_validate_merchant(body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1WalletProviderApplePayValidateMerchantRequest`](../../doc/models/v1-wallet-provider-apple-pay-validate-merchant-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseApplePayValidateMerchant`](../../doc/models/response-apple-pay-validate-merchant.md).

## Example Usage

```ruby
body = V1WalletProviderApplePayValidateMerchantRequest.new(
  url: 'https://apple-pay-gateway-cert.apple.com/paymentservices/startSession',
  merchant_id: 'abc1234',
  domain_name: 'website.domain.com',
  display_name: 'Sandwich Market'
)

result = apple_pay_validate_merchant_controller.apple_pay_validate_merchant(body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Example Response *(as JSON)*

```json
{
  "type": "ApplePayValidateMerchant",
  "data": {
    "merchantSession": "{\"epochTimestamp\":1689772866529,\"expiresAt\":1689776466529,\"merchantSessionIdentifier\":\"SSH3D9224\",\"nonce\":\"d70dbe8a\",\"merchantIdentifier\":\"46A940\",\"domainName\":\"paygistixcert.paymentlogistics.net\",\"displayName\":\"F\",\"signature\":\"30800609f6e2\",\"operationalAnalyticsIdentifier\":\"F:46A4E40\",\"retries\":0,\"pspId\":\"ADD36D\"}"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |

