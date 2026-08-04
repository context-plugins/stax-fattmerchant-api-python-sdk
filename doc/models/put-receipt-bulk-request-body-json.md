
# Put Receipt Bulk Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutReceiptBulkRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transaction_ids` | `List[uuid\|str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_receipt_bulk_request_body_json import PutReceiptBulkRequestBodyJson

put_receipt_bulk_request_body_json = PutReceiptBulkRequestBodyJson(
    transaction_ids=[
        'f1dc205a-b708-421b-8fb7-db227a386486'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

