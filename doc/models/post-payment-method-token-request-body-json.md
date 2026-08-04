
# Post Payment Method Token Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostPaymentMethodTokenRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `str` | Optional | - |
| `customer_id` | `uuid\|str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_payment_method_token_request_body_json import PostPaymentMethodTokenRequestBodyJson

post_payment_method_token_request_body_json = PostPaymentMethodTokenRequestBodyJson(
    token='string',
    customer_id='4d607326-71f7-4c23-b1ef-9856a6d63d5e',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

