
# Cardholder Account

Contains information for the Cardholder Account.

## Structure

`CardholderAccount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `expire_date` | `String` | Optional | Expiry date of the PAN or token supplied to the 3DS Requestor by the Cardholder. The field has 4 characters in a format YYMM.<br>The requirements of the presence of this field are DS specific. |
| `account_info` | [`AccountInfo`](../../doc/models/account-info.md) | Optional | This field contains additional information about the Cardholder's account provided by the 3DS Requestor. The field is optional but recommended to include. |
| `account_number` | `String` | Required | Account number that will be used in the authorization request for payment transactions. May be represented by PAN or token. |
| `scheme_id` | [`SchemeIdEnum`](../../doc/models/scheme-id-enum.md) | Required | ID for the scheme to which the Cardholder's acctNumber belongs to. It will be used to identify the Scheme from the 3DS Server configuration. |
| `account_id` | `String` | Optional | Additional information about the account optionally provided by the 3DS Requestor. |
| `cvv` | `String` | Optional | Three or four-digit security code printed on the card. This field is required depending on the rules provided by the Directory Server. Available for supporting EMV 3DS 2.3.1 and later versions.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `4` |

## Example (as JSON)

```json
{
  "expire_date": "2508",
  "account_number": "5454545454545454",
  "scheme_id": "Visa",
  "account_info": {
    "ch_acc_age_ind": "02",
    "ch_acc_date": "ch_acc_date4",
    "ch_acc_change_ind": "03",
    "ch_acc_change": "ch_acc_change2",
    "ch_acc_pw_change_ind": "02"
  },
  "account_id": "account_id8",
  "cvv": "cvv4"
}
```

