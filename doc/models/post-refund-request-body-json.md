
# Post Refund Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostRefundRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `total` | `float` | Optional | Partial refund amount (omit for full refund) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_refund_request_body_json import PostRefundRequestBodyJson

post_refund_request_body_json = PostRefundRequestBodyJson(
    total=50,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

