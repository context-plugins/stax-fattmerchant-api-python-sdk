
# Put Receipt Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutReceiptRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `email` | `str` | Optional | - |
| `phone` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_receipt_request_body_json import PutReceiptRequestBodyJson

put_receipt_request_body_json = PutReceiptRequestBodyJson(
    email='user@example.com',
    phone='string',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

