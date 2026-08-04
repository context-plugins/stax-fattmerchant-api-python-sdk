
# Put Receipt Bulk Method Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutReceiptBulkMethodRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transaction_ids` | `List[uuid\|str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_receipt_bulk_method_request_body_json import PutReceiptBulkMethodRequestBodyJson

put_receipt_bulk_method_request_body_json = PutReceiptBulkMethodRequestBodyJson(
    transaction_ids=[
        'c29dcf19-ff14-4e95-840e-aa9ff5c44854'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

