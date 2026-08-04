
# Put Restore Customer Bulk Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutRestoreCustomerBulkRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `List[uuid\|str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_restore_customer_bulk_request_body_json import PutRestoreCustomerBulkRequestBodyJson

put_restore_customer_bulk_request_body_json = PutRestoreCustomerBulkRequestBodyJson(
    ids=[
        '162e114c-e700-4bf6-a82b-e896e9189445'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

