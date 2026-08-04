# User Admin

```python
user_admin_api = client.user_admin
```

## Class Name

`UserAdminApi`

## Methods

* [Admin Get Users](../../doc/controllers/user-admin.md#admin-get-users)
* [Admin Post User](../../doc/controllers/user-admin.md#admin-post-user)
* [Admin Get User](../../doc/controllers/user-admin.md#admin-get-user)
* [Admin Put User](../../doc/controllers/user-admin.md#admin-put-user)
* [Admin Delete User](../../doc/controllers/user-admin.md#admin-delete-user)
* [Admin Put Resend Verification](../../doc/controllers/user-admin.md#admin-put-resend-verification)
* [Admin Restore User](../../doc/controllers/user-admin.md#admin-restore-user)
* [Admin Get Weekly Summaries](../../doc/controllers/user-admin.md#admin-get-weekly-summaries)


# Admin Get Users

```python
def admin_get_users(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of users

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = user_admin_api.admin_get_users()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Post User

```python
def admin_post_user(self,
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

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = user_admin_api.admin_post_user(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Get User

```python
def admin_get_user(self,
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

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '19037bb1-2d76-4602-8296-4c8e617e6d08'

result = user_admin_api.admin_get_user(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Put User

```python
def admin_put_user(self,
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

**200**: User updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '5eab8ad9-01f2-43a9-94a5-fa1f2f654acd'

result = user_admin_api.admin_put_user(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Delete User

```python
def admin_delete_user(self,
                     id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: User deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '8ea20e7d-3c45-4edb-8207-c52aace36cad'

result = user_admin_api.admin_delete_user(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Put Resend Verification

```python
def admin_put_resend_verification(self,
                                 id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Verification email resent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '64d753e3-8971-4fb8-83fd-22d2ade37377'

result = user_admin_api.admin_put_resend_verification(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Restore User

```python
def admin_restore_user(self,
                      id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: User restored

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'd731918f-8f1f-4b2e-bc4e-602166dac094'

result = user_admin_api.admin_restore_user(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Get Weekly Summaries

```python
def admin_get_weekly_summaries(self,
                              id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: List of weekly summaries

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '8fe67a3e-a425-462c-b6e5-5407166abdae'

result = user_admin_api.admin_get_weekly_summaries(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

