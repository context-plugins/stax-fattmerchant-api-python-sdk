
# Post Email Receipt Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostEmailReceiptRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `email` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_email_receipt_request_body_json import PostEmailReceiptRequestBodyJson

post_email_receipt_request_body_json = PostEmailReceiptRequestBodyJson(
    email='user@example.com',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

