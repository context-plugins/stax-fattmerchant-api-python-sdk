# Self

Current authenticated user operations

```python
mself_api = client.mself
```

## Class Name

`SelfApi`

## Methods

* [Get Self Root](../../doc/controllers/self.md#get-self-root)
* [Get Self](../../doc/controllers/self.md#get-self)
* [Put Self User](../../doc/controllers/self.md#put-self-user)
* [Get Self List](../../doc/controllers/self.md#get-self-list)
* [Put Resend Email Verification](../../doc/controllers/self.md#put-resend-email-verification)
* [Put Acknowledgment](../../doc/controllers/self.md#put-acknowledgment)
* [Put Set Default Merchant](../../doc/controllers/self.md#put-set-default-merchant)
* [Put Self Merchant Option](../../doc/controllers/self.md#put-self-merchant-option)
* [Get Fee Statement Messages](../../doc/controllers/self.md#get-fee-statement-messages)
* [Get Saasquatch Token](../../doc/controllers/self.md#get-saasquatch-token)


# Get Self Root

```python
def get_self_root(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Current user info

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
result = mself_api.get_self_root()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized - Invalid or missing authentication token | `ApiException` |


# Get Self

```python
def get_self(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Current user info

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
result = mself_api.get_self()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized - Invalid or missing authentication token | `ApiException` |


# Put Self User

```python
def put_self_user(self,
                 body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Updated user

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = mself_api.put_self_user(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Self List

```python
def get_self_list(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of self records

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[Any]`.

## Example Usage

```python
result = mself_api.get_self_list()

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


# Put Resend Email Verification

```python
def put_resend_email_verification(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Verification email resent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = mself_api.put_resend_email_verification()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Acknowledgment

```python
def put_acknowledgment(self,
                      key)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `key` | `str` | Template, Required | - |

## Response Type

**200**: Acknowledgment recorded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
key = 'string'

result = mself_api.put_acknowledgment(key)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Set Default Merchant

```python
def put_set_default_merchant(self,
                            body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PutSetDefaultMerchantRequestBodyJson`](../../doc/models/put-set-default-merchant-request-body-json.md) | Body, Required | - |

## Response Type

**200**: Default merchant set

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PutSetDefaultMerchantRequestBodyJson(
    merchant_id='195b4ff0-2c81-45b0-b052-698ee00a5291'
)

result = mself_api.put_set_default_merchant(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Self Merchant Option

```python
def put_self_merchant_option(self,
                            option,
                            body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `option` | `str` | Template, Required | - |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Option updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
option = 'string'

result = mself_api.put_self_merchant_option(option)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Fee Statement Messages

```python
def get_fee_statement_messages(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Fee statement messages

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[Any]`.

## Example Usage

```python
result = mself_api.get_fee_statement_messages()

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


# Get Saasquatch Token

```python
def get_saasquatch_token(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Saasquatch token

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = mself_api.get_saasquatch_token()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

