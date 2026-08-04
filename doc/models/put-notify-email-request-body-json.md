
# Put Notify Email Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutNotifyEmailRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `email` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_notify_email_request_body_json import PutNotifyEmailRequestBodyJson

put_notify_email_request_body_json = PutNotifyEmailRequestBodyJson(
    email='user@example.com',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

