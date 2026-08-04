# Team Registration

```python
team_registration_api = client.team_registration
```

## Class Name

`TeamRegistrationApi`

## Methods

* [Get Team Registration](../../doc/controllers/team-registration.md#get-team-registration)
* [Put Team Registration](../../doc/controllers/team-registration.md#put-team-registration)
* [Put Registration Sign](../../doc/controllers/team-registration.md#put-registration-sign)
* [Put Auto Verification Accept](../../doc/controllers/team-registration.md#put-auto-verification-accept)
* [Post Team Registration File](../../doc/controllers/team-registration.md#post-team-registration-file)
* [Put Team Registration File](../../doc/controllers/team-registration.md#put-team-registration-file)
* [Delete Team Registration File](../../doc/controllers/team-registration.md#delete-team-registration-file)
* [Get Registration for Merchant](../../doc/controllers/team-registration.md#get-registration-for-merchant)


# Get Team Registration

```python
def get_team_registration(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Registration data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
result = team_registration_api.get_team_registration()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Team Registration

```python
def put_team_registration(self,
                         body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Registration updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = team_registration_api.put_team_registration(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Registration Sign

```python
def put_registration_sign(self,
                         body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PutRegistrationSignRequestBodyJson`](../../doc/models/put-registration-sign-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Registration signed

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PutRegistrationSignRequestBodyJson(
    signature='string'
)

result = team_registration_api.put_registration_sign(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Auto Verification Accept

```python
def put_auto_verification_accept(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Auto-verification accepted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = team_registration_api.put_auto_verification_accept()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Team Registration File

```python
def post_team_registration_file(self,
                               file=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `typing.BinaryIO` | Form, Optional | - |

## Response Type

**200**: File uploaded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = team_registration_api.post_team_registration_file()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Team Registration File

```python
def put_team_registration_file(self,
                              file_id,
                              file=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file_id` | `uuid\|str` | Template, Required | - |
| `file` | `typing.BinaryIO` | Form, Optional | - |

## Response Type

**200**: File updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
file_id = 'acbfefb7-8abe-40bf-9281-4178ba272f47'

result = team_registration_api.put_team_registration_file(file_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Team Registration File

```python
def delete_team_registration_file(self,
                                 file_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: File deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
file_id = '8164b35b-f2db-4a38-962f-90f4b1bdc6a3'

result = team_registration_api.delete_team_registration_file(file_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Registration for Merchant

```python
def get_registration_for_merchant(self,
                                 id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Registration data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '6fd1b462-554c-4fc0-8f18-334df92cdaca'

result = team_registration_api.get_registration_for_merchant(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

