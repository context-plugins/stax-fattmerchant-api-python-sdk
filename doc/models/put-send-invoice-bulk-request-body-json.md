
# Put Send Invoice Bulk Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutSendInvoiceBulkRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `invoice_ids` | `List[uuid\|str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_send_invoice_bulk_request_body_json import PutSendInvoiceBulkRequestBodyJson

put_send_invoice_bulk_request_body_json = PutSendInvoiceBulkRequestBodyJson(
    invoice_ids=[
        'b2306869-442a-421c-8b1e-87e1077724fe'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

