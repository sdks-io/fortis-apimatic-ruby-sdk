
# Broad Info

Until EMV 3DS 2.2.0:

Unstructured information sent between the 3DS Server, the DS and the ACS.

This field is not required to be filled by the Requestor and the requirements for the presence of this field are DS specific.

Starting from EMV 3DS 2.3.1:

Structured information sent between the 3DS Server, the DS and the ACS. 2.3.1 structure is defined below. Accepted value length is maximum 4096 characters. This field is optional.

*This model accepts additional fields of type Object.*

## Structure

`BroadInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `category` | [`Category`](../../doc/models/category.md) | Optional | - |
| `description` | `String` | Optional | Information to be broadcasted to the recipients. Accepted value length is maximum 4000 characters. This field is optional.<br><br>**Constraints**: *Maximum Length*: `4000` |
| `expire_date` | `String` | Optional | The date after which the relevance of the broadcasted information (e.g., ceritifacte expiration dates) expires. The accepted value length is 8 characters. The accepted format is YYYYMMDD.<br><br>**Constraints**: *Maximum Length*: `8` |
| `severity` | [`Severity`](../../doc/models/severity.md) | Optional | - |
| `recipients` | [`Recipients`](../../doc/models/recipients.md) | Optional | - |
| `source` | [`Source`](../../doc/models/source.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "category": "98",
  "description": "description2",
  "expire_date": "expire_date0",
  "severity": "03",
  "recipients": "01",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

