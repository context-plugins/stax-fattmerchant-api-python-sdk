# Team Options

```python
team_options_api = client.team_options
```

## Class Name

`TeamOptionsApi`

## Methods

* [Get Team Option](../../doc/controllers/team-options.md#get-team-option)
* [Put Team Option](../../doc/controllers/team-options.md#put-team-option)
* [Put Team Options Batch](../../doc/controllers/team-options.md#put-team-options-batch)
* [Post Team Branding](../../doc/controllers/team-options.md#post-team-branding)
* [Put Set Plan](../../doc/controllers/team-options.md#put-set-plan)
* [Put Set Gateway](../../doc/controllers/team-options.md#put-set-gateway)
* [Put Invoice Reference Numbers](../../doc/controllers/team-options.md#put-invoice-reference-numbers)


# Get Team Option

```python
def get_team_option(self,
                   option)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `option` | `str` | Template, Required | - |

## Response Type

**200**: Option value

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
option = 'string'

result = team_options_api.get_team_option(option)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Team Option

```python
def put_team_option(self,
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

result = team_options_api.put_team_option(option)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Team Options Batch

```python
def put_team_options_batch(self,
                          body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Options updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = team_options_api.put_team_options_batch()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Team Branding

```python
def post_team_branding(self,
                      file=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `typing.BinaryIO` | Form, Optional | - |

## Response Type

**200**: Branding uploaded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = team_options_api.post_team_branding()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Set Plan

```python
def put_set_plan(self,
                body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PutSetPlanRequestBodyJson`](../../doc/models/put-set-plan-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Plan set

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PutSetPlanRequestBodyJson(
    plan='string'
)

result = team_options_api.put_set_plan(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Set Gateway

```python
def put_set_gateway(self,
                   body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Gateway option set

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = team_options_api.put_set_gateway()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Invoice Reference Numbers

```python
def put_invoice_reference_numbers(self,
                                 body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Option updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = team_options_api.put_invoice_reference_numbers()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

