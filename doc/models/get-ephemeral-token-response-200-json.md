
# Get Ephemeral Token Response 200 Json

*This model accepts additional fields of type Any.*

## Structure

`GetEphemeralTokenResponse200Json`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `token` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.get_ephemeral_token_response_200_json import GetEphemeralTokenResponse200Json

get_ephemeral_token_response_200_json = GetEphemeralTokenResponse200Json(
    token='string',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

