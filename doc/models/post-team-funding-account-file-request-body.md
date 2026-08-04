
# Post Team Funding Account File Request Body

*This model accepts additional fields of type Any.*

## Structure

`PostTeamFundingAccountFileRequestBody`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `binary` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.post_team_funding_account_file_request_body import PostTeamFundingAccountFileRequestBody

post_team_funding_account_file_request_body = PostTeamFundingAccountFileRequestBody(
    file=None,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

