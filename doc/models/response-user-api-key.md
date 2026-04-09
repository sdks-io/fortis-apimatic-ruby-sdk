
# Response User Api Key

## Structure

`ResponseUserApiKey`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type128Enum`](../../doc/models/type-128-enum.md) | Optional | Resource Type<br><br>**Default**: `Type128Enum::USERAPIKEY` |
| `data` | [`Data33`](../../doc/models/data-33.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "UserApiKey",
  "data": {
    "user_api_key": "user_api_key2"
  }
}
```

