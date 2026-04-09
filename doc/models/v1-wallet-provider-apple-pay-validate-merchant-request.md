
# V1 Wallet Provider Apple Pay Validate Merchant Request

## Structure

`V1WalletProviderApplePayValidateMerchantRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `String` | Required | Url obtained in the ApplePay button click event. Apple's URL that needs to be called to validate merchant. |
| `merchant_id` | `String` | Required | Merchant ID |
| `domain_name` | `String` | Required | Domain Name |
| `display_name` | `String` | Required | Title |

## Example (as JSON)

```json
{
  "url": "https://apple-pay-gateway-cert.apple.com/paymentservices/startSession",
  "merchantId": "abc1234",
  "domainName": "website.domain.com",
  "displayName": "Sandwich Market"
}
```

