
# Post Credit Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostCreditRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `payment_method_id` | `uuid\|str` | Optional | - |
| `total` | `float` | Optional | - |
| `meta` | `Any` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_credit_request_body_json import PostCreditRequestBodyJson

post_credit_request_body_json = PostCreditRequestBodyJson(
    payment_method_id='c00a2852-cac9-48b2-ac7f-7a22243caae6',
    total=50,
    meta=jsonpickle.decode('{}'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

