# Terminal

Terminal signature operations

```python
terminal_api = client.terminal
```

## Class Name

`TerminalApi`

## Methods

* [Post Terminal Signature](../../doc/controllers/terminal.md#post-terminal-signature)
* [Get Terminal Signature](../../doc/controllers/terminal.md#get-terminal-signature)
* [Put Terminal Signature](../../doc/controllers/terminal.md#put-terminal-signature)


# Post Terminal Signature

```python
def post_terminal_signature(self,
                           body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PostTerminalSignatureRequestBodyJson`](../../doc/models/post-terminal-signature-request-body-json.md) | Body, Required | - |

## Response Type

**200**: Signature stored

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PostTerminalSignatureRequestBodyJson(
    signature='string',
    transaction_id='2b27b12d-62c9-4de8-837c-b2d3152f887b'
)

result = terminal_api.post_terminal_signature(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Terminal Signature

```python
def get_terminal_signature(self,
                          id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Signature details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'fb540612-06e6-42d6-ad42-ace30430040e'

result = terminal_api.get_terminal_signature(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Terminal Signature

```python
def put_terminal_signature(self,
                          id,
                          body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PutTerminalSignatureRequestBodyJson`](../../doc/models/put-terminal-signature-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Signature updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'e185fda8-bda6-444c-8345-b9916317daed'

body = PutTerminalSignatureRequestBodyJson(
    signature='string'
)

result = terminal_api.put_terminal_signature(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

