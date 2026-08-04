
# Post File Request Body

*This model accepts additional fields of type Any.*

## Structure

`PostFileRequestBody`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `binary` | Optional | - |
| `tag` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_file_request_body import PostFileRequestBody

post_file_request_body = PostFileRequestBody(
    file=None,
    tag='string',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

