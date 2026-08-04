# Integration

Third-party integration management

```python
integration_api = client.integration
```

## Class Name

`IntegrationApi`

## Methods

* [Get Integrations](../../doc/controllers/integration.md#get-integrations)
* [Get Integration](../../doc/controllers/integration.md#get-integration)
* [Put Verify Integration Token](../../doc/controllers/integration.md#put-verify-integration-token)
* [Delete Integration](../../doc/controllers/integration.md#delete-integration)
* [Post Integration Action](../../doc/controllers/integration.md#post-integration-action)


# Get Integrations

```python
def get_integrations(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of integrations

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = integration_api.get_integrations()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Integration

```python
def get_integration(self,
                   id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Integration details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '41c344b6-bc2e-4092-a678-a1a8409a5c3d'

result = integration_api.get_integration(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Verify Integration Token

```python
def put_verify_integration_token(self,
                                id,
                                body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PutVerifyIntegrationTokenRequestBodyJson`](../../doc/models/put-verify-integration-token-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Token verified

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '1d629d0a-761e-47be-9c95-b3b05359a005'

body = PutVerifyIntegrationTokenRequestBodyJson(
    token='string'
)

result = integration_api.put_verify_integration_token(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Integration

```python
def delete_integration(self,
                      id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Integration deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'c5037cf1-72f1-43e3-8760-2b3d9eca01d9'

result = integration_api.delete_integration(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Integration Action

```python
def post_integration_action(self,
                           id,
                           action,
                           body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `action` | `str` | Template, Required | - |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Action performed

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'fc3ca542-6b3b-41df-8926-c69ebb1332bb'

action = 'string'

result = integration_api.post_integration_action(
    id,
    action
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

