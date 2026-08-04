# Sandbox

```python
sandbox_api = client.sandbox
```

## Class Name

`SandboxApi`

## Methods

* [Post Quick Demo](../../doc/controllers/sandbox.md#post-quick-demo)
* [Post Sandbox](../../doc/controllers/sandbox.md#post-sandbox)


# Post Quick Demo

```python
def post_quick_demo(self,
                   body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Quick demo created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = sandbox_api.post_quick_demo()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Sandbox

```python
def post_sandbox(self,
                body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Sandbox created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = sandbox_api.post_sandbox()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

