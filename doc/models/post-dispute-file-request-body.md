
# Post Dispute File Request Body

*This model accepts additional fields of type Any.*

## Structure

`PostDisputeFileRequestBody`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `binary` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_dispute_file_request_body import PostDisputeFileRequestBody

post_dispute_file_request_body = PostDisputeFileRequestBody(
    file=None,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

