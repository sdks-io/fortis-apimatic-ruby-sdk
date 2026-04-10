
# Terminal Timeouts 1

*This model accepts additional fields of type Object.*

## Structure

`TerminalTimeouts1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `card_entry_timeout` | `Integer` | Optional | How long to wait for input from cardholder.<br><br>> Message on timeout:<br>> Card Entry Timeout<br><br>**Default**: `120`<br><br>**Constraints**: `>= 20`, `<= 120` |
| `device_terms_prompt_timeout` | `Integer` | Optional | How long the terms will be displayed on the device.<br><br>> Message on timeout:<br>> Timeout waiting for Customer<br><br>**Default**: `60`<br><br>**Constraints**: `>= 5`, `<= 300` |
| `overall_timeout` | `Integer` | Optional | How long to wait for response from /v2/routertransactions endpoint.<br><br>> Message on timeout:<br>> Overall Request Timeout<br><br>**Default**: `300`<br><br>**Constraints**: `>= 30`, `<= 300` |
| `pin_entry_timeout` | `Integer` | Optional | How long to wait for pin entry by cardholder.<br><br>> Message on timeout:<br>> Pin Entry Timeout<br><br>**Default**: `30`<br><br>**Constraints**: `>= 20`, `<= 50` |
| `signature_input_timeout` | `Integer` | Optional | How long to wait for first "touch" to signature.<br><br>> Message on timeout:<br>> Signature Input Timeout<br><br>**Default**: `10`<br><br>**Constraints**: `>= 10`, `<= 50` |
| `signature_submit_timeout` | `Integer` | Optional | How long to wait for signature to be submitted.<br><br>> Message on timeout:<br>> Signature Storage Timeout<br><br>**Default**: `30`<br><br>**Constraints**: `>= 20`, `<= 50` |
| `status_display_time` | `Integer` | Optional | How long the approve/decline status message stays on screen.<br><br>> Message on timeout:<br>> N/A - Not actually a "timeout".  This is a time to display the status on the screen.<br><br>**Default**: `7`<br><br>**Constraints**: `>= 1`, `<= 30` |
| `tip_cashback_timeout` | `Integer` | Optional | How long to wait for input on a tip or cashback screen.<br><br>> Message on timeout:<br>> Tip/Cashback Timeout<br><br>**Default**: `30`<br><br>**Constraints**: `>= 20`, `<= 50` |
| `transaction_timeout` | `Integer` | Optional | How long to wait for response from the processor.<br><br>> Message on timeout:<br>> Transaction Timeout<br><br>**Default**: `10`<br><br>**Constraints**: `>= 10`, `<= 20` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "card_entry_timeout": 47,
  "device_terms_prompt_timeout": 30,
  "overall_timeout": 125,
  "pin_entry_timeout": 40,
  "signature_input_timeout": 35,
  "signature_submit_timeout": 38,
  "status_display_time": 12,
  "tip_cashback_timeout": 25,
  "transaction_timeout": 17,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

