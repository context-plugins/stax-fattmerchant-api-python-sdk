
# Put Unpublish Bulk Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutUnpublishBulkRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `List[uuid\|str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_unpublish_bulk_request_body_json import PutUnpublishBulkRequestBodyJson

put_unpublish_bulk_request_body_json = PutUnpublishBulkRequestBodyJson(
    ids=[
        'c6a05049-44fc-46ee-86ca-bb354bca4f45'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

