# Charge

One-time charge operations

```python
charge_api = client.charge
```

## Class Name

`ChargeApi`


# Post Charge

```python
def post_charge(self,
               body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Charge created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = charge_api.post_charge(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

