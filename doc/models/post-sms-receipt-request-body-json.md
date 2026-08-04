
# Post Sms Receipt Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostSmsReceiptRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `phone` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_sms_receipt_request_body_json import PostSmsReceiptRequestBodyJson

post_sms_receipt_request_body_json = PostSmsReceiptRequestBodyJson(
    phone='string',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

