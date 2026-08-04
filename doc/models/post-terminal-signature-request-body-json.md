
# Post Terminal Signature Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostTerminalSignatureRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `signature` | `str` | Optional | - |
| `transaction_id` | `uuid\|str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_terminal_signature_request_body_json import PostTerminalSignatureRequestBodyJson

post_terminal_signature_request_body_json = PostTerminalSignatureRequestBodyJson(
    signature='string',
    transaction_id='2b27b12d-62c9-4de8-837c-b2d3152f887b',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

