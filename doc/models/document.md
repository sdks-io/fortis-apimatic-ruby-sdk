
# Document

Array of document objects.

*This model accepts additional fields of type Object.*

## Structure

`Document`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `document_name` | `String` | Required | Array of bank account objects.<br><br>**Constraints**: *Maximum Length*: `32` |
| `document_data` | `String` | Required | Base64 encoded document content.<br><br>> Base64 encoded document content. |
| `mime_type` | `String` | Required | Mime type of document.<br><br>**Constraints**: *Maximum Length*: `20` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "document_name": "ImportantDoc.txt",
  "document_data": "alskj;asijia;eiom;weirj;iomj",
  "mime_type": "application/json",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

