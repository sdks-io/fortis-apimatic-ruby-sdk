# Full Boarding

```ruby
full_boarding_controller = client.full_boarding
```

## Class Name

`FullBoardingController`


# Merchant Boarding Full

This method is used to fully board a merchant to the platform. When using this method, you must provide data for each "Required" property. See the description for each of these properties for more information about their requirement criteria.

```ruby
def merchant_boarding_full(body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1FullboardingRequest`](../../doc/models/v1-fullboarding-request.md) | Body, Required | - |

## Response Type

[`ResponseFullboarding`](../../doc/models/response-fullboarding.md)

## Example Usage

```ruby
body = V1FullboardingRequest.new(
  'email@domain.com',
  'Discount Home Goods',
  '5555551234',
  OwnershipTypeEnum::LLP,
  '0000000000',
  15,
  150,
  100,
  '7629',
  'Yard services.',
  0,
  0,
  100,
  true,
  false,
  [
    Address81.new(
      '121 E Main',
      'Dallas',
      'TX',
      '75087',
      'US',
      AddressTypeEnum::LOCATION,
      'Apt 707'
    )
  ],
  [
    Owner.new(
      'James',
      'Bond',
      'CEO',
      '2021-12-01',
      '133 S Goliad St',
      'Suite 120',
      'Rockwall',
      'TX',
      '75429',
      'US',
      '000000000',
      100,
      '9042142323',
      'james@example.com',
      true,
      true,
      'Tyler'
    )
  ],
  [
    BankAccount1.new(
      'James Bond',
      '111111111',
      '1234567',
      AccountType12Enum::CHECKING,
      true,
      []
    )
  ],
  nil,
  '1234YourTemplateCode',
  'ABC123',
  'Total Home Goods, LLP',
  'http://www.example.com',
  22,
  PreferredLanguageEnum::FRCA,
  [],
  [],
  [],
  nil,
  '192.168.0.10',
  []
)

result = full_boarding_controller.merchant_boarding_full(body)
puts result
```

## Example Response *(as JSON)*

```json
{
  "type": "Fullboarding",
  "data": {
    "result": {
      "client_app_id": "ABC123",
      "dba_name": "Discount Home Goods",
      "email": "jtodd@example.com"
    },
    "status": {
      "response_code": "Received"
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401tokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |

