
# Post Item Thumbnail Request Body

*This model accepts additional fields of type Any.*

## Structure

`PostItemThumbnailRequestBody`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `binary` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_item_thumbnail_request_body import PostItemThumbnailRequestBody

post_item_thumbnail_request_body = PostItemThumbnailRequestBody(
    file=None,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

