
# Data 37

*This model accepts additional fields of type Object.*

## Structure

`Data37`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_session` | `String` | Optional | String formatted merchantSession object.  Needs to be passed to the session.completeMerchantValidation event in JS. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "merchantSession": "{\r\n  \"epochTimestamp\": 1689772866529,\r\n  \"expiresAt\": 1689776466529,\r\n  \"merchantSessionIdentifier\": \"SSH3D9224\",\r\n  \"nonce\": \"d70dbe8a\",\r\n  \"merchantIdentifier\": \"46A940\",\r\n  \"domainName\": \"paygistixcert.paymentlogistics.net\",\r\n  \"displayName\": \"F\",\r\n  \"signature\": \"30800609f6e2\",\r\n  \"operationalAnalyticsIdentifier\": \"F:46A4E40\",\r\n  \"retries\": 0,\r\n  \"pspId\": \"ADD36D\"\r\n}",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

