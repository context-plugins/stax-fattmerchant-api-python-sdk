# Invoice Schedule

```python
invoice_schedule_api = client.invoice_schedule
```

## Class Name

`InvoiceScheduleApi`

## Methods

* [Get Invoice Schedules](../../doc/controllers/invoice-schedule.md#get-invoice-schedules)
* [Post Invoice Schedule](../../doc/controllers/invoice-schedule.md#post-invoice-schedule)
* [Get Invoice Schedule](../../doc/controllers/invoice-schedule.md#get-invoice-schedule)
* [Put Invoice Schedule](../../doc/controllers/invoice-schedule.md#put-invoice-schedule)
* [Delete Invoice Schedule](../../doc/controllers/invoice-schedule.md#delete-invoice-schedule)


# Get Invoice Schedules

```python
def get_invoice_schedules(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of invoice schedules

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = invoice_schedule_api.get_invoice_schedules()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Invoice Schedule

```python
def post_invoice_schedule(self,
                         body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Schedule created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = invoice_schedule_api.post_invoice_schedule(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Invoice Schedule

```python
def get_invoice_schedule(self,
                        id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Schedule details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'ce6d23af-9692-48be-a969-289b4c8abb09'

result = invoice_schedule_api.get_invoice_schedule(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Invoice Schedule

```python
def put_invoice_schedule(self,
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

**200**: Schedule updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'af0a2db2-0c94-479d-a007-a648eba1b86a'

body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = invoice_schedule_api.put_invoice_schedule(
    id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Invoice Schedule

```python
def delete_invoice_schedule(self,
                           id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Schedule deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '0dc97b8a-6b9e-4ee8-9566-71751bc1c77d'

result = invoice_schedule_api.delete_invoice_schedule(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

