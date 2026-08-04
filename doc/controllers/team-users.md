# Team Users

```python
team_users_api = client.team_users
```

## Class Name

`TeamUsersApi`

## Methods

* [Get Team Users](../../doc/controllers/team-users.md#get-team-users)
* [Post Team User](../../doc/controllers/team-users.md#post-team-user)
* [Get Team User Ids](../../doc/controllers/team-users.md#get-team-user-ids)
* [Get Team User](../../doc/controllers/team-users.md#get-team-user)
* [Put Team User](../../doc/controllers/team-users.md#put-team-user)
* [Put User Merchant Option](../../doc/controllers/team-users.md#put-user-merchant-option)


# Get Team Users

```python
def get_team_users(self,
                  page=None,
                  per_page=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | Page number for pagination |
| `per_page` | `int` | Query, Optional | Number of items per page |

## Response Type

**200**: Paginated list of team users

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
page = 1

per_page = 10

result = team_users_api.get_team_users(
    page=page,
    per_page=per_page
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Team User

```python
def post_team_user(self,
                  body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: User created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = team_users_api.post_team_user(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Team User Ids

```python
def get_team_user_ids(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of user IDs

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[uuid|str]`.

## Example Usage

```python
result = team_users_api.get_team_user_ids()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

## Example Response

```
[
  "98a9d57d-b25d-47f7-9ee0-e94af9b29955"
]
```


# Get Team User

```python
def get_team_user(self,
                 id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: User details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
id = '62f95e70-66c6-461f-9f5b-bc25a310264d'

result = team_users_api.get_team_user(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Team User

```python
def put_team_user(self,
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

**200**: User updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'b4dd56cd-e3c9-4455-a03d-811da71cf380'

body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = team_users_api.put_team_user(
    id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put User Merchant Option

```python
def put_user_merchant_option(self,
                            id,
                            option,
                            body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `option` | `str` | Template, Required | - |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Option updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'fdadc07a-2012-47ba-a979-74312d647c26'

option = 'string'

result = team_users_api.put_user_merchant_option(
    id,
    option
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

