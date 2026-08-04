# Webhook

Webhook management

```python
webhook_api = client.webhook
```

## Class Name

`WebhookApi`

## Methods

* [Get Webhooks](../../doc/controllers/webhook.md#get-webhooks)
* [Post Webhook](../../doc/controllers/webhook.md#post-webhook)
* [Get Webhook List](../../doc/controllers/webhook.md#get-webhook-list)
* [Get Webhook](../../doc/controllers/webhook.md#get-webhook)
* [Delete Webhook](../../doc/controllers/webhook.md#delete-webhook)


# Get Webhooks

```python
def get_webhooks(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Paginated list of webhooks

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[Any]`.

## Example Usage

```python
result = webhook_api.get_webhooks()

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


# Post Webhook

```python
def post_webhook(self,
                body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Webhook created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = webhook_api.post_webhook(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Webhook List

```python
def get_webhook_list(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of webhooks

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = webhook_api.get_webhook_list()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Webhook

```python
def get_webhook(self,
               id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Webhook details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
id = '3a301e36-8577-4eb9-bb91-e3b31701f469'

result = webhook_api.get_webhook(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Webhook

```python
def delete_webhook(self,
                  id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Webhook deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'ed84dd28-fc07-4a37-860d-0e4adf63d16d'

result = webhook_api.delete_webhook(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

