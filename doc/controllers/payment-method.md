# Payment Method

```python
payment_method_api = client.payment_method
```

## Class Name

`PaymentMethodApi`

## Methods

* [Get Payment Methods](../../doc/controllers/payment-method.md#get-payment-methods)
* [Post Payment Method](../../doc/controllers/payment-method.md#post-payment-method)
* [Post Payment Method Token](../../doc/controllers/payment-method.md#post-payment-method-token)
* [Get Payment Method](../../doc/controllers/payment-method.md#get-payment-method)
* [Put Payment Method](../../doc/controllers/payment-method.md#put-payment-method)
* [Delete Payment Method](../../doc/controllers/payment-method.md#delete-payment-method)


# Get Payment Methods

```python
def get_payment_methods(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of payment methods

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[Any]`.

## Example Usage

```python
result = payment_method_api.get_payment_methods()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Example Response

```
[
  null
]
```


# Post Payment Method

```python
def post_payment_method(self,
                       body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Payment method created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = payment_method_api.post_payment_method(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Payment Method Token

```python
def post_payment_method_token(self,
                             body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PostPaymentMethodTokenRequestBodyJson`](../../doc/models/post-payment-method-token-request-body-json.md) | Body, Required | - |

## Response Type

**200**: Payment method created from token

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PostPaymentMethodTokenRequestBodyJson(
    token='string',
    customer_id='4d607326-71f7-4c23-b1ef-9856a6d63d5e'
)

result = payment_method_api.post_payment_method_token(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Payment Method

```python
def get_payment_method(self,
                      id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Payment method details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
id = '459dfb57-76e9-48d7-825d-880e0f366839'

result = payment_method_api.get_payment_method(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Payment Method

```python
def put_payment_method(self,
                      id,
                      body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Payment method updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '443bed5d-301a-4a0e-b36a-a5ebf8845396'

result = payment_method_api.put_payment_method(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Payment Method

```python
def delete_payment_method(self,
                         id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Payment method deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '5aeea92a-1645-4fd1-8e7b-f7c2be31545d'

result = payment_method_api.delete_payment_method(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

