
# Put Registration Sign Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutRegistrationSignRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `signature` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_registration_sign_request_body_json import PutRegistrationSignRequestBodyJson

put_registration_sign_request_body_json = PutRegistrationSignRequestBodyJson(
    signature='string',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

