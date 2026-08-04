# Web Payment

```python
web_payment_api = client.web_payment
```

## Class Name

`WebPaymentApi`


# Post Web Payment Transaction

```python
def post_web_payment_transaction(self,
                                body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Web payment transaction created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = web_payment_api.post_web_payment_transaction(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

