
# V1 Merchant Threedsecure Authentication Request

*This model accepts additional fields of type Object.*

## Structure

`V1MerchantThreedsecureAuthenticationRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `product_transaction_id` | `String` | Required | Product Transaction ID to associate with this 3DS request<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `preferred_protocol_version` | `Object` | Optional | - |
| `enforce_preferred_protocol_version` | `TrueClass \| FalseClass` | Optional | Boolean flag that enforces preferred 3D Secure protocol version to be used in 3D Secure authentication. The value should be set true to enforce preferred version. If value is false or not provided, 3DS Server can fall back to next supported 3DS protocol version while initiating 3D Secure authentication. |
| `device_channel` | [`DeviceChannel`](../../doc/models/device-channel.md) | Required | - |
| `message_category` | [`MessageCategory`](../../doc/models/message-category.md) | Required | - |
| `three_ds_comp_ind` | `String` | Optional | Indicates whether the 3DS Method successfully completed. The value is used only when device_channel = 02 (Browser).<br><br>From protocol version 2.3.1 this field is required.<br><br>> Y - Successfully completed<br>> <br>> N - Did not successfully complete<br>> <br>> U - Unavailable - 3DS Method URL was not present in the PRes message data for the card range associated with the Cardholder Account Number. |
| `three_ds_method_id` | `String` | Optional | Contains the 3DS Server Transaction ID used during the previous execution of the 3DS method. Accepted value length is 36 characters. Accepted value is a Canonical format as defined in IETF RFC 4122. May utilise any of the specified versions if the output meets specified requirements.<br>This field is required if the 3DS Requestor reuses previous 3DS Method execution with device_channel = 02 (BRW). Available in EMV 3DS 2.3.1 and later versions. |
| `three_ds_requestor` | [`ThreeDsRequestor1`](../../doc/models/three-ds-requestor-1.md) | Required | - |
| `three_ds_server_trans_id` | `UUID \| String` | Optional | Universally unique transaction identifier assigned by the 3DS Server to identify a single transaction. This value has 36 characters in a format defined in IETF RFC 4122. In case 3DS Method is previously invoked, the threeDSServerTransID should be sent. If not, 3DS Server will generate a new transaction identifier.<br><br>If threeDSServerTransID is generated in versioning flow same transaction identifier should be used in Authentication flow which combines them as one transaction. |
| `three_ds_requestor_url` | `String` | Optional | Fully qualified URL of 3DS Requestor website or customer care site. |
| `cardholder_account` | [`CardholderAccount1`](../../doc/models/cardholder-account-1.md) | Required | - |
| `cardholder` | [`Cardholder1`](../../doc/models/cardholder-1.md) | Optional | - |
| `purchase` | [`Purchase1`](../../doc/models/purchase-1.md) | Optional | - |
| `broad_info` | [`BroadInfo1`](../../doc/models/broad-info-1.md) | Optional | - |
| `message_extension` | [`Array[MessageExtension]`](../../doc/models/message-extension.md) | Optional | Data necessary to support requirements not otherwise defined in the 3D Secure message are carried in a Message Extension. This field is limited to 81,920 characters and it is used in the Authentication Request.<br><br>Requirements of this field are set by each Directory Server. |
| `challenge_message_extension` | [`Array[ChallengeMessageExtension]`](../../doc/models/challenge-message-extension.md) | Optional | Data necessary to support requirements not otherwise defined in the 3D Secure message are carried in a Message Extension. This field is limited to 81,920 characters and it is used in the generating of the ChallengeRequest, if challenge is needed.<br><br>Requirements of this field are set by each Directory Server. |
| `browser_information` | [`BrowserInformation1`](../../doc/models/browser-information-1.md) | Optional | - |
| `three_ri_ind` | `Object` | Optional | - |
| `device` | [`Device1`](../../doc/models/device-1.md) | Optional | - |
| `multi_transaction` | [`MultiTransaction1`](../../doc/models/multi-transaction-1.md) | Optional | - |
| `device_id` | `String` | Optional | Unique and immutable identifier linked to a device that is consistent across 3DS transactions for the specific user device.<br><br>Available for supporting EMV 3DS 2.3.1 and later versions. |
| `user_id` | `String` | Optional | Identifier of the transacting user’s Browser Account ID.<br><br>Available for supporting EMV 3DS 2.3.1 and later versions. |
| `payee_origin` | `String` | Optional | The origin of the payee that will be provided in the SPC Transaction Data as a fully qualified URL.<br><br>**Constraints**: *Maximum Length*: `2048` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "product_transaction_id": "11ee3860e2fc7f5ea67d36b3",
  "enforce_preferred_protocol_version": true,
  "device_channel": "02",
  "message_category": "96",
  "three_ds_comp_ind": "Y",
  "three_ds_requestor": {
    "three_ds_requestor_authentication_ind": "90",
    "three_ds_requestor_challenge_ind": [
      "03"
    ],
    "three_ds_requestor_authentication_info": [
      {
        "three_ds_req_auth_method": "98",
        "three_ds_req_auth_timestamp": "three_ds_req_auth_timestamp2",
        "three_ds_req_auth_data": "three_ds_req_auth_data2",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "three_ds_req_auth_method": "98",
        "three_ds_req_auth_timestamp": "three_ds_req_auth_timestamp2",
        "three_ds_req_auth_data": "three_ds_req_auth_data2",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "three_ds_requestor_prior_authentication_info": [
      {
        "three_ds_req_prior_ref": "three_ds_req_prior_ref6",
        "three_ds_req_prior_auth_method": "90",
        "three_ds_req_prior_auth_timestamp": "three_ds_req_prior_auth_timestamp6",
        "three_ds_req_prior_auth_data": "three_ds_req_prior_auth_data0",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "three_ds_requestor_dec_req_ind": "F",
    "three_ds_requestor_dec_max_time": 246,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "cardholder_account": {
    "expire_date": "2508",
    "account_number": "5454545454545454",
    "scheme_id": "Visa",
    "account_info": {
      "ch_acc_age_ind": "02",
      "ch_acc_date": "ch_acc_date4",
      "ch_acc_change_ind": "03",
      "ch_acc_change": "ch_acc_change2",
      "ch_acc_pw_change_ind": "02",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "account_id": "account_id0",
    "cvv": "cvv6",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "preferred_protocol_version": {
    "key1": "val1",
    "key2": "val2"
  },
  "three_ds_method_id": "three_ds_method_id4",
  "three_ds_server_trans_id": "00000fa0-0000-0000-0000-000000000000",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

