
# Post Verification Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostVerificationRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `payment_method_id` | `uuid\|str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_verification_request_body_json import PostVerificationRequestBodyJson

post_verification_request_body_json = PostVerificationRequestBodyJson(
    payment_method_id='3a64f5ce-e2f7-4809-991e-45ac6e95e0ab',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

