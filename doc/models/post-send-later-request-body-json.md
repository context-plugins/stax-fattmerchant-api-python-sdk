
# Post Send Later Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PostSendLaterRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `send_at` | `datetime` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from staxfattmerchantapi.models.post_send_later_request_body_json import PostSendLaterRequestBodyJson

post_send_later_request_body_json = PostSendLaterRequestBodyJson(
    send_at=dateutil.parser.parse('2026-02-19T11:30:08.0367268Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

