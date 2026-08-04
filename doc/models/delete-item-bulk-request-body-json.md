
# Delete Item Bulk Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`DeleteItemBulkRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `List[uuid\|str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.delete_item_bulk_request_body_json import DeleteItemBulkRequestBodyJson

delete_item_bulk_request_body_json = DeleteItemBulkRequestBodyJson(
    ids=[
        '1d75b6bb-9353-4237-89b1-4a1e1a93b40a'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

