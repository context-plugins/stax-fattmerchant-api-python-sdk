# Team

Team/merchant management

```python
team_api = client.team
```

## Class Name

`TeamApi`

## Methods

* [Get Team](../../doc/controllers/team.md#get-team)
* [Post Merchant](../../doc/controllers/team.md#post-merchant)
* [Put Merchant](../../doc/controllers/team.md#put-merchant)
* [Get Team Gateways](../../doc/controllers/team.md#get-team-gateways)
* [Get Mobile Reader Info](../../doc/controllers/team.md#get-mobile-reader-info)
* [Clone Merchant Team](../../doc/controllers/team.md#clone-merchant-team)
* [Put Notify Email](../../doc/controllers/team.md#put-notify-email)


# Get Team

```python
def get_team(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Team info

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
result = team_api.get_team()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Merchant

```python
def post_merchant(self,
                 body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Merchant created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = team_api.post_merchant(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Merchant

```python
def put_merchant(self,
                body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Merchant updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = team_api.put_merchant(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Team Gateways

```python
def get_team_gateways(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of gateways

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[Any]`.

## Example Usage

```python
result = team_api.get_team_gateways()

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


# Get Mobile Reader Info

```python
def get_mobile_reader_info(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Mobile reader info

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = team_api.get_mobile_reader_info()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Clone Merchant Team

```python
def clone_merchant_team(self,
                       merchant_id,
                       body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Merchant cloned

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = 'c037467a-154e-4398-adb3-08b3a1d7fc24'

result = team_api.clone_merchant_team(merchant_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Notify Email

```python
def put_notify_email(self,
                    notification_type,
                    body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notification_type` | `str` | Template, Required | - |
| `body` | [`PutNotifyEmailRequestBodyJson`](../../doc/models/put-notify-email-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Notification email updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
notification_type = 'string'

body = PutNotifyEmailRequestBodyJson(
    email='user@example.com'
)

result = team_api.put_notify_email(
    notification_type,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

