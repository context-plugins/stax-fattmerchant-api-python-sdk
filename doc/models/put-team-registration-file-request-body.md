
# Put Team Registration File Request Body

*This model accepts additional fields of type Any.*

## Structure

`PutTeamRegistrationFileRequestBody`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `binary` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_team_registration_file_request_body import PutTeamRegistrationFileRequestBody

put_team_registration_file_request_body = PutTeamRegistrationFileRequestBody(
    file=None,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

