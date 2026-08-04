
# Post Invoice Payment Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostInvoicePaymentRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `payment_method_id` | `uuid\|str` | Optional | - |
| `apply_balance` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_invoice_payment_request_body_json import PostInvoicePaymentRequestBodyJson

post_invoice_payment_request_body_json = PostInvoicePaymentRequestBodyJson(
    payment_method_id='00aa237f-4511-4727-b657-6f13f8497a82',
    apply_balance=True,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

