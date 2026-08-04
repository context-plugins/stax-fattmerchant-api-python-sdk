
# Put Verify Integration Token Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutVerifyIntegrationTokenRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_verify_integration_token_request_body_json import PutVerifyIntegrationTokenRequestBodyJson

put_verify_integration_token_request_body_json = PutVerifyIntegrationTokenRequestBodyJson(
    token='string',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

