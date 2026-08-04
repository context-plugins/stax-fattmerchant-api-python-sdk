
# Put Transaction Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutTransactionRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | `Any` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_transaction_request_body_json import PutTransactionRequestBodyJson

put_transaction_request_body_json = PutTransactionRequestBodyJson(
    meta=jsonpickle.decode('{}'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

