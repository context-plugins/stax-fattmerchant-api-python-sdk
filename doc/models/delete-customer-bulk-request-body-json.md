
# Delete Customer Bulk Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`DeleteCustomerBulkRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `List[uuid\|str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.delete_customer_bulk_request_body_json import DeleteCustomerBulkRequestBodyJson

delete_customer_bulk_request_body_json = DeleteCustomerBulkRequestBodyJson(
    ids=[
        'f48f0a02-1cad-4651-8ae4-6c707231f0f3'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

