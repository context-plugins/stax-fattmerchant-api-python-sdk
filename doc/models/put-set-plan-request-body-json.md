
# Put Set Plan Request Body Json

*This model accepts additional fields of type Any.*

## Structure

`PutSetPlanRequestBodyJson`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `plan` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from staxfattmerchantapi.models.put_set_plan_request_body_json import PutSetPlanRequestBodyJson

put_set_plan_request_body_json = PutSetPlanRequestBodyJson(
    plan='string',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

