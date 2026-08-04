
# Merge Customer Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`MergeCustomerRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `duplicates` | `List[uuid\|str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.merge_customer_request_body_json import MergeCustomerRequestBodyJson

merge_customer_request_body_json = MergeCustomerRequestBodyJson(
    duplicates=[
        '7d29292f-b705-4d68-91ef-f85dc49a187b'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

