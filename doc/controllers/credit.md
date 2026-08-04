# Credit

Credit operations

```python
credit_api = client.credit
```

## Class Name

`CreditApi`


# Post Credit

```python
def post_credit(self,
               body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PostCreditRequestBodyJson`](../../doc/models/post-credit-request-body-json.md) | Body, Required | - |

## Response Type

**200**: Credit issued

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PostCreditRequestBodyJson(
    payment_method_id='c00a2852-cac9-48b2-ac7f-7a22243caae6',
    total=50,
    meta=jsonpickle.decode('{}')
)

result = credit_api.post_credit(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

