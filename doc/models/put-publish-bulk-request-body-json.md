
# Put Publish Bulk Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutPublishBulkRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `List[uuid\|str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_publish_bulk_request_body_json import PutPublishBulkRequestBodyJson

put_publish_bulk_request_body_json = PutPublishBulkRequestBodyJson(
    ids=[
        '57c6352a-aabf-4ead-9f60-cf7df39abdc9'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

