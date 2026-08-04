
# Post Invoice Manual Payment Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostInvoiceManualPaymentRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `total` | `float` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_invoice_manual_payment_request_body_json import PostInvoiceManualPaymentRequestBodyJson

post_invoice_manual_payment_request_body_json = PostInvoiceManualPaymentRequestBodyJson(
    total=50,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

