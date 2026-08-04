
# Post Void or Refund Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostVoidOrRefundRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `total` | `float` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_void_or_refund_request_body_json import PostVoidOrRefundRequestBodyJson

post_void_or_refund_request_body_json = PostVoidOrRefundRequestBodyJson(
    total=50,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

