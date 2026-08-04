# Hello Sign

HelloSign e-signature integration

```python
hello_sign_api = client.hello_sign
```

## Class Name

`HelloSignApi`

## Methods

* [Post Hello Sign Send Email](../../doc/controllers/hello-sign.md#post-hello-sign-send-email)
* [Get Hello Sign Templates](../../doc/controllers/hello-sign.md#get-hello-sign-templates)
* [Get Hello Sign Template](../../doc/controllers/hello-sign.md#get-hello-sign-template)
* [Post Hello Sign Signature Url](../../doc/controllers/hello-sign.md#post-hello-sign-signature-url)
* [Get Hello Sign Signatures](../../doc/controllers/hello-sign.md#get-hello-sign-signatures)


# Post Hello Sign Send Email

```python
def post_hello_sign_send_email(self,
                              body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Email sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = hello_sign_api.post_hello_sign_send_email()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Hello Sign Templates

```python
def get_hello_sign_templates(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of templates

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = hello_sign_api.get_hello_sign_templates()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Hello Sign Template

```python
def get_hello_sign_template(self,
                           template_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `template_id` | `str` | Template, Required | - |

## Response Type

**200**: Template details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
template_id = 'string'

result = hello_sign_api.get_hello_sign_template(template_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Hello Sign Signature Url

```python
def post_hello_sign_signature_url(self,
                                 template_id,
                                 body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `template_id` | `str` | Template, Required | - |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Signature URL created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
template_id = 'string'

result = hello_sign_api.post_hello_sign_signature_url(template_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Hello Sign Signatures

```python
def get_hello_sign_signatures(self,
                             merchant_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: List of signature URLs

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = '27b43713-39b9-41d7-93cf-d5919bd75de9'

result = hello_sign_api.get_hello_sign_signatures(merchant_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

