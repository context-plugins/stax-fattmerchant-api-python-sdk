
# Put Terminal Signature Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutTerminalSignatureRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `signature` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_terminal_signature_request_body_json import PutTerminalSignatureRequestBodyJson

put_terminal_signature_request_body_json = PutTerminalSignatureRequestBodyJson(
    signature='string',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

