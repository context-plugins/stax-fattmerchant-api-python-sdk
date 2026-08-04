
# Post Cache Test Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostCacheTestRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `key` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_cache_test_request_body_json import PostCacheTestRequestBodyJson

post_cache_test_request_body_json = PostCacheTestRequestBodyJson(
    key='string',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

