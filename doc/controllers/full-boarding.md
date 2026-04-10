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

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `data` property of this instance returns the response data which is of type [`ResponseFullboarding`](../../doc/models/response-fullboarding.md).

## Example Usage

```ruby
body = V1FullboardingRequest.new(
  email: 'email@domain.com',
  dba_name: 'Discount Home Goods',
  phone_number: '5555551234',
  ownership_type: OwnershipType::NP,
  fed_tax_id: '0000000000',
  average_ticket: 15,
  high_ticket: 150,
  cc_monthly_volume: 100,
  mcc_code: '7629',
  business_description: 'Yard services.',
  swiped_percent: 0,
  keyed_percent: 0,
  ecommerce_percent: 100,
  is_foreign_entity: true,
  personally_guaranteed: false,
  addresses: [
    Address81.new(
      address_line_1: '121 E Main',
      city: 'Dallas',
      state_province: 'TX',
      postal_code: '75087',
      country_code: 'US',
      address_type: AddressType::CORPORATE,
      address_line_2: 'Apt 707'
    )
  ],
  owners: [
    Owner.new(
      first_name: 'James',
      last_name: 'Bond',
      title: 'CEO',
      date_of_birth: '2021-12-01',
      address_line_1: '133 S Goliad St',
      address_line_2: 'Suite 120',
      city: 'Rockwall',
      state_province: 'TX',
      postal_code: '75429',
      country_code: 'US',
      ssn: '000000000',
      ownership_percent: 100,
      phone_number: '9042142323',
      email_address: 'james@example.com',
      is_controller: true,
      is_signer: true,
      middle_name: 'Tyler'
    )
  ],
  bank_accounts: [
    BankAccount1.new(
      account_holder_name: 'James Bond',
      routing_number: '111111111',
      account_number: '1234567',
      account_type: AccountType12::CHECKING,
      is_primary: true
    )
  ],
  template_id: '1234YourTemplateCode',
  client_app_id: 'ABC123',
  legal_name: 'Total Home Goods, LLP',
  website: 'http://www.example.com',
  ec_monthly_volume: 22,
  signer_ip: '192.168.0.10'
)

result = full_boarding_controller.merchant_boarding_full(body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
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
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |

