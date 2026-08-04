
# Post Team Registration File Request Body

*This model accepts additional fields of type Any.*

## Structure

`PostTeamRegistrationFileRequestBody`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `binary` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_team_registration_file_request_body import PostTeamRegistrationFileRequestBody

post_team_registration_file_request_body = PostTeamRegistrationFileRequestBody(
    file=None,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

