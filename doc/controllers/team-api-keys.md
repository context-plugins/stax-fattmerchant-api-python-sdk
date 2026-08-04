# Team API Keys

```python
team_api_keys_api = client.team_api_keys
```

## Class Name

`TeamApiKeysApi`

## Methods

* [Get Ephemeral Token Root](../../doc/controllers/team-api-keys.md#get-ephemeral-token-root)
* [Get Team Api Keys](../../doc/controllers/team-api-keys.md#get-team-api-keys)
* [Post Team Api Key](../../doc/controllers/team-api-keys.md#post-team-api-key)
* [Get Ephemeral Token](../../doc/controllers/team-api-keys.md#get-ephemeral-token)
* [Get Team Api Key](../../doc/controllers/team-api-keys.md#get-team-api-key)
* [Put Team Api Key](../../doc/controllers/team-api-keys.md#put-team-api-key)
* [Delete Team Api Key](../../doc/controllers/team-api-keys.md#delete-team-api-key)


# Get Ephemeral Token Root

```python
def get_ephemeral_token_root(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Ephemeral token

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`GetEphemeralTokenRootResponse200Json`](../../doc/models/get-ephemeral-token-root-response-200-json.md).

## Example Usage

```python
result = team_api_keys_api.get_ephemeral_token_root()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Team Api Keys

```python
def get_team_api_keys(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of API keys

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[Any]`.

## Example Usage

```python
result = team_api_keys_api.get_team_api_keys()

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


# Post Team Api Key

```python
def post_team_api_key(self,
                     body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: API key created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = team_api_keys_api.post_team_api_key(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Ephemeral Token

```python
def get_ephemeral_token(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Ephemeral token

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type [`GetEphemeralTokenResponse200Json`](../../doc/models/get-ephemeral-token-response-200-json.md).

## Example Usage

```python
result = team_api_keys_api.get_ephemeral_token()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Team Api Key

```python
def get_team_api_key(self,
                    id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: API key details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
id = '9d376b36-5830-4223-a19b-63332e894b5b'

result = team_api_keys_api.get_team_api_key(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Team Api Key

```python
def put_team_api_key(self,
                    id,
                    body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: API key updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '582f3004-6e54-4af8-b3ed-dfd3a7d5cb2a'

body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = team_api_keys_api.put_team_api_key(
    id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Team Api Key

```python
def delete_team_api_key(self,
                       id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: API key deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '9ab156f0-7b75-47f5-85fc-0800e7eaefb3'

result = team_api_keys_api.delete_team_api_key(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

