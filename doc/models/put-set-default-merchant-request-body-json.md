
# Put Set Default Merchant Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutSetDefaultMerchantRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_set_default_merchant_request_body_json import PutSetDefaultMerchantRequestBodyJson

put_set_default_merchant_request_body_json = PutSetDefaultMerchantRequestBodyJson(
    merchant_id='195b4ff0-2c81-45b0-b052-698ee00a5291',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

