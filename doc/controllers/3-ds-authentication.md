# 3 DS Authentication

```ruby
m3_ds_authentication_controller = client.m3_ds_authentication
```

## Class Name

`M3DSAuthenticationController`


# 3 DS Authentication Request

Makes a 3DS Authentication request to authenticate a card or begin the challenge flow.  If a challenge is required, a POST should be made to acs_url using the value of base64_encoded_challenge_request for the value of "creq" using x-www-form-urlencoded for the challenge request to the ACS.

```ruby
def m3_ds_authentication_request(body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1MerchantThreedsecureAuthenticationRequest`](../../doc/models/v1-merchant-threedsecure-authentication-request.md) | Body, Required | - |

## Response Type

[`ResponseThreeDSAuthentication`](../../doc/models/response-three-ds-authentication.md)

## Example Usage

```ruby
body = V1MerchantThreedsecureAuthenticationRequest.new(
  '11ee3860e2fc7f5ea67d36b3',
  DeviceChannelEnum::ENUM_02,
  MessageCategoryEnum::ENUM_01,
  ThreeDsRequestor.new(
    ThreeDsRequestorAuthenticationIndEnum::ENUM_01,
    [],
    [
      ThreeDsRequestorChallengeIndEnum::ENUM_03
    ],
    [],
    envrr,
    nil,
    envrr
  ),
  CardholderAccount.new(
    '5454545454545454',
    SchemeIdEnum::VISA,
    '2508',
    AccountInfo.new(
      envrr,
      nil,
      envrr,
      nil,
      envrr,
      nil,
      envrr,
      nil,
      nil,
      nil,
      nil,
      nil,
      envrr,
      envrr,
      envrr
    )
  ),
  PreferredProtocolVersionEnum::ENUM_220,
  true,
  'Y',
  nil,
  nil,
  nil,
  Cardholder.new(
    envrr,
    BillingAddress24.new,
    nil,
    HomePhone.new,
    MobilePhone.new,
    WorkPhone.new,
    nil,
    ShippingAddress.new
  ),
  Purchase.new(
    nil,
    MerchantRiskIndicator.new(
      envrr,
      envrr,
      nil,
      envrr,
      envrr,
      nil,
      nil,
      nil,
      nil,
      []
    ),
    nil,
    nil,
    nil,
    nil,
    nil,
    nil,
    envrr,
    nil,
    nil,
    nil,
    nil,
    envrr
  ),
  BroadInfo.new(
    envrr,
    nil,
    nil,
    envrr,
    envrr,
    envrr
  ),
  [],
  [],
  BrowserInformation.new(
    nil,
    nil,
    nil,
    nil,
    nil,
    nil,
    nil,
    nil,
    envrr,
    nil,
    []
  ),
  nil,
  Device.new(
    envrr
  ),
  MultiTransaction.new(
    []
  )
)

result = m3_ds_authentication_controller.m3_ds_authentication_request(body)
puts result
```

## Example Response *(as JSON)*

```json
{
  "type": "ThreeDSAuthentication",
  "data": {
    "three_ds_server_trans_id": "ea0c9973-4cd0-4f9f-83b3-609bf22c69e7",
    "acs_url": "https://api.sandbox.fortis.tech/v1/acs/challenge",
    "transaction_status": "C",
    "ds_trans_id": "278c7508-cac6-4233-902d-b90f31f741c6",
    "acs_trans_id": "d7c1ee99-9478-44a6-b1f2-391e29c6b340",
    "message_version": "2.2.0",
    "acs_challenge_mandated": "Y",
    "purchase_date": "20240509111532",
    "base64_encoded_challenge_request": "eyJtZXNzYWdlVHlwZSI6IkNSZXEiLCJ0aHJlZURTU2VydmVyVHJhbnNJRCI6ImVhMGM5OTczLTRjZDAtNGY5Zi04M2IzLTYwOWJmMjJjNjllNyIsImFjc1RyYW5zSUQiOiIwNWViNTE2OS02ZTFkLTQ5NTMtYWQ3NC1hZWU5YmQ4ZTc1YmIiLCJjaGFsbGVuZ2VXaW5kb3dTaXplIjoiMDEiLCJtZXNzYWdlVmVyc2lvbiI6IjIuMi4wIn0="
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`ResponseErrorException`](../../doc/models/response-error-exception.md) |
| 401 | Unauthorized | [`Response401tokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |

