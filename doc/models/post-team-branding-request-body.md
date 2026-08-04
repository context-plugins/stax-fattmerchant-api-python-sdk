
# Post Team Branding Request Body

*This model accepts additional fields of type Any.*

## Structure

`PostTeamBrandingRequestBody`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `binary` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_team_branding_request_body import PostTeamBrandingRequestBody

post_team_branding_request_body = PostTeamBrandingRequestBody(
    file=None,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

