
# V1 Quick Invoices Request

## Structure

`V1QuickInvoicesRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `title` | `String` | Required | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `cc_product_transaction_id` | `String` | Optional | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ach_product_transaction_id` | `String` | Optional | ACH Product Transaction Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `due_date` | `String` | Required | Due Date, Format: Y-m-d<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `item_list` | [`Array[ItemList4]`](../../doc/models/item-list-4.md) | Required | Item List<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `300`, *Unique Items Required* |
| `allow_overpayment` | `TrueClass \| FalseClass` | Optional | Allow Overpayment. |
| `bank_funded_only_override` | `TrueClass \| FalseClass` | Optional | Bank Funded Only override |
| `email` | `String` | Optional | Email<br><br>**Constraints**: *Maximum Length*: `128` |
| `contact_id` | `String` | Optional | Contact ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `contact_api_id` | `String` | Optional | Contact API Id<br><br>**Constraints**: *Maximum Length*: `64` |
| `quick_invoice_api_id` | `String` | Optional | Quick Invoice API Id<br><br>**Constraints**: *Maximum Length*: `64` |
| `customer_id` | `String` | Optional | Customer Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `expire_date` | `String` | Optional | Expire Date.<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `allow_partial_pay` | `TrueClass \| FalseClass` | Optional | Allow partial pay |
| `attach_files_to_email` | `TrueClass \| FalseClass` | Optional | Attach Files to Email |
| `send_email` | `TrueClass \| FalseClass` | Optional | Send Email |
| `invoice_number` | `String` | Optional | Invoice number<br><br>**Constraints**: *Maximum Length*: `64` |
| `item_header` | `String` | Optional | Item Header<br><br>**Constraints**: *Maximum Length*: `250` |
| `item_footer` | `String` | Optional | Item footer<br><br>**Constraints**: *Maximum Length*: `250` |
| `amount_due` | `Integer` | Optional | Amount Due |
| `notification_email` | `String` | Optional | Notification email<br><br>**Constraints**: *Maximum Length*: `640` |
| `status_id` | `Integer` | Optional | (DEPRECATED) Status Id<br><br>**Constraints**: `>= 0`, `<= 1` |
| `status_code` | `Integer` | Optional | Status Code<br><br>**Constraints**: `>= 0`, `<= 1` |
| `note` | `String` | Optional | Note<br><br>**Constraints**: *Maximum Length*: `200` |
| `notification_days_before_due_date` | `Integer` | Optional | Notification days before due date<br><br>**Constraints**: `>= 0`, `<= 60` |
| `notification_days_after_due_date` | `Integer` | Optional | Notification days after due date<br><br>**Constraints**: `>= 0`, `<= 60` |
| `notification_on_due_date` | `TrueClass \| FalseClass` | Optional | Notification on due date |
| `send_text_to_pay` | `TrueClass \| FalseClass` | Optional | Send Text To Pay |
| `files` | [`Array[File2]`](../../doc/models/file-2.md) | Optional | Files<br><br>> Maximum of 4 files & maximum size of 5MB per file.<br><br>**Constraints**: *Maximum Items*: `4` |
| `remaining_balance` | `Integer` | Optional | Remaining Balance<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `single_payment_min_amount` | `Integer` | Optional | Single Payment Min Amount |
| `single_payment_max_amount` | `Integer` | Optional | Single Payment Max Amount<br><br>**Default**: `999999999` |
| `cell_phone` | `String` | Optional | Cell Phone<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{10}$` |
| `tags` | `Array[String]` | Optional | Tags |
| `quick_invoice_c_1` | `String` | Optional | Custom field 1 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `quick_invoice_c_2` | `String` | Optional | Custom field 2 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `quick_invoice_c_3` | `String` | Optional | Custom field 1 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `auto_reopen` | `TrueClass \| FalseClass` | Optional | Auto Reopen. If set to true, a void, refund or detachment of a Transaction Payment will cause the QuickInvoice to be opened again |

## Example (as JSON)

```json
{
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "title": "My terminal",
  "cc_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "ach_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "due_date": "2021-12-01",
  "item_list": [
    {
      "name": "Bread",
      "amount": 2015
    }
  ],
  "allow_overpayment": true,
  "bank_funded_only_override": true,
  "email": "email@domain.com",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "contact_api_id": "contact12345",
  "quick_invoice_api_id": "quickinvoice12345",
  "customer_id": "11e95f8ec39de8fbdb0a4f1a",
  "expire_date": "2021-12-01",
  "allow_partial_pay": true,
  "attach_files_to_email": true,
  "send_email": true,
  "invoice_number": "invoice12345",
  "item_header": "Quick invoice header sample",
  "item_footer": "Thank you",
  "amount_due": 24536,
  "notification_email": "email@domain.com",
  "status_id": 1,
  "status_code": 1,
  "note": "some note",
  "notification_days_before_due_date": 3,
  "notification_days_after_due_date": 7,
  "notification_on_due_date": true,
  "send_text_to_pay": true,
  "remaining_balance": 24536,
  "single_payment_min_amount": 500,
  "single_payment_max_amount": 500000,
  "cell_phone": "3339998822",
  "quick_invoice_c1": "custom-data-1",
  "quick_invoice_c2": "custom-data-2",
  "quick_invoice_c3": "custom-data-3",
  "auto_reopen": true
}
```

