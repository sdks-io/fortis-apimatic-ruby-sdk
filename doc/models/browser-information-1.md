
# Browser Information 1

*This model accepts additional fields of type Object.*

## Structure

`BrowserInformation1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `browser_accept_header` | `String` | Optional | Exact content of the HTTP accept headers as sent to the 3DS Requestor from the Cardholder's browser. This field is limited to maximum 2048 characters  and if the total length exceeds the limit, the 3DS Server truncates the excess portion.<br><br>This field is required for requests where device_channel=02 (BRW). |
| `browser_java_enabled` | `TrueClass \| FalseClass` | Optional | Boolean that represents the ability of the cardholder browser to execute Java. Value is returned from the navigator.javaEnabled property.<br><br>Depending on the message version, the field is required for requests:<br><br>- with message version = 2.1.0 and device_channel = 02 (BRW).<br>- with message version = 2.2.0 and device_channel = 02 (BRW) and browser_javascript_enabled = true. |
| `browser_language` | `String` | Optional | Value representing the browser language as defined in IETF BCP47.<br><br>Until EMV 3DS 2.2.0:<br>The value is limited to 1-8 characters. If the value exceeds 8 characters, it will be truncated to a semantically valid value, if possible. The value is returned from navigator.language property.<br><br>This field is required for requests where device_channel = 02 (BRW).<br>In other cases this field is optional.<br><br>Starting from EMV 3DS 2.3.1:<br>The value is limited to 35 characters. If the value exceeds 35 characters, it will be truncated to a semantically valid value, if possible. The value is returned from navigator.language property.<br><br>This field is required for requests where device_channel = 02 (BRW) and browser_javascript_enabled = true.<br>In other cases this field is optional.<br><br>**Constraints**: *Maximum Length*: `35` |
| `browser_color_depth` | `String` | Optional | Value representing the bit depth of the color palette for displaying images, in bits per pixel. Obtained from Cardholder browser using the screen.colorDepth property. The field is limited to 1-2 characters.<br><br>If the value is not in the accepted values, it will be resolved to the first accepted value lower from the one provided.<br><br>Depending on the message version, the field is required for requests:<br><br>- with message version = 2.1.0 and device_channel = 02 (BRW).<br>- with message version = 2.2.0 and device_channel = 02 (BRW) and browser_javascript_enabled = true.<br><br>> 1 - 1 bit<br>> <br>> 4 - 4 bits<br>> <br>> 8 - 8 bits<br>> <br>> 15 - 15 bits<br>> <br>> 16 - 16 bits<br>> <br>> 24 - 24 bits<br>> <br>> 32 - 32 bits<br>> <br>> 48 - 48 bits<br><br>**Constraints**: *Maximum Length*: `2`, *Pattern*: `^[a-zA-Z0-9]*$` |
| `browser_screen_height` | `Integer` | Optional | Total height of the Cardholder's screen in pixels. Value is returned from the screen.height property. The value is limited to 1-6 characters.<br><br>Depending on the message version, the field is required for requests:<br><br>- with message version = 2.1.0 and device_channel = 02 (BRW).<br>- with message version = 2.2.0 and device_channel = 02 (BRW) and browserJavascripbrowser_javascript_enabledtEnabled = true.<br><br>**Constraints**: `>= 0`, `<= 999999` |
| `browser_screen_width` | `Integer` | Optional | Total width of the Cardholder's screen in pixels. Value is returned from the screen.width property. The value is limited to 1-6 characters.<br><br>Depending on the message version, the field is required for requests:<br><br>- with message version = 2.1.0 and device_channel = 02 (BRW).<br>- with message version = 2.2.0 and device_channel = 02 (BRW) and browser_javascript_enabled = true.<br><br>**Constraints**: `>= 0`, `<= 999999` |
| `browser_tz` | `Integer` | Optional | Time difference between UTC time and the Cardholder browser local time, in minutes. The field is limited to 1-5 characters where the values is returned from the getTimezoneOffset() method.<br><br>Depending on the message version, the field is required for requests:<br><br>- with message version = 2.1.0 and device_channel = 02 (BRW).<br>- with message version = 2.2.0 and device_channel = 02 (BRW) and browser_javascript_enabled = true.<br><br>**Constraints**: `>= 0`, `<= 99999` |
| `browser_user_agent` | `String` | Optional | Exact content of the HTTP user-agent header. The field is limited to maximum 2048 caracters. If the total length of the User-Agent sent by the browser exceeds 2048 characters, the 3DS Server truncates the excess portion.<br><br>This field is required for requests where device_channel = 02 (BRW). |
| `challenge_window_size` | [`ChallengeWindowSize`](../../doc/models/challenge-window-size.md) | Optional | - |
| `browser_javascript_enabled` | `TrueClass \| FalseClass` | Optional | Boolean that represents the ability of the cardholder browser to execute JavaScript.<br><br>This field is required for requests where device_channel = 02 (BRW).<br>Available for supporting EMV 3DS 2.2.0 and later versions. |
| `accept_language` | `Array[String]` | Optional | Value representing the browser language preference present in the http header, as defined in IETF BCP 47.<br><br>The value is limited to 1-99 elements. Each element should contain a maximum of 100 characters.<br><br>This field is required for requests where device_channel = 02 (BRW).<br>Available for supporting EMV 3DS 2.3.1 and later versions.<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `99`, *Maximum Length*: `100` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "browser_accept_header": "application/json",
  "browser_java_enabled": false,
  "browser_language": "en",
  "browser_color_depth": "8",
  "browser_screen_height": 1080,
  "browser_screen_width": 1920,
  "browser_tz": 1,
  "browser_user_agent": "Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:47.0) Gecko/20100101 Firefox/47.0",
  "browser_javascript_enabled": true,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

