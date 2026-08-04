
# Post Capture Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostCaptureRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `total` | `float` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_capture_request_body_json import PostCaptureRequestBodyJson

post_capture_request_body_json = PostCaptureRequestBodyJson(
    total=50,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

