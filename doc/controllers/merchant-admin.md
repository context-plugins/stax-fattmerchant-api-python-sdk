# Merchant Admin

```python
merchant_admin_api = client.merchant_admin
```

## Class Name

`MerchantAdminApi`

## Methods

* [Admin Get Merchants](../../doc/controllers/merchant-admin.md#admin-get-merchants)
* [Admin Post Merchant](../../doc/controllers/merchant-admin.md#admin-post-merchant)
* [Admin Get Merchant](../../doc/controllers/merchant-admin.md#admin-get-merchant)
* [Admin Put Merchant](../../doc/controllers/merchant-admin.md#admin-put-merchant)
* [Admin Delete Merchant](../../doc/controllers/merchant-admin.md#admin-delete-merchant)
* [Post Unassume Merchant](../../doc/controllers/merchant-admin.md#post-unassume-merchant)
* [Post Assume Merchant](../../doc/controllers/merchant-admin.md#post-assume-merchant)
* [Send Merchant Welcome](../../doc/controllers/merchant-admin.md#send-merchant-welcome)
* [Send Merchant ACH Rejection](../../doc/controllers/merchant-admin.md#send-merchant-ach-rejection)
* [Get Merchant Users](../../doc/controllers/merchant-admin.md#get-merchant-users)
* [Post Attach User](../../doc/controllers/merchant-admin.md#post-attach-user)
* [Put Attach User](../../doc/controllers/merchant-admin.md#put-attach-user)
* [Delete Unattach User](../../doc/controllers/merchant-admin.md#delete-unattach-user)
* [Admin Put User Merchant Option](../../doc/controllers/merchant-admin.md#admin-put-user-merchant-option)
* [Delete All Scheduled Invoices](../../doc/controllers/merchant-admin.md#delete-all-scheduled-invoices)


# Admin Get Merchants

```python
def admin_get_merchants(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of merchants

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = merchant_admin_api.admin_get_merchants()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Post Merchant

```python
def admin_post_merchant(self,
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

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = merchant_admin_api.admin_post_merchant(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Get Merchant

```python
def admin_get_merchant(self,
                      merchant_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Merchant details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = '272ca3e7-f600-4565-866d-6d86abc3134b'

result = merchant_admin_api.admin_get_merchant(merchant_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Put Merchant

```python
def admin_put_merchant(self,
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

**200**: Merchant updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = 'd5bd3583-c466-4920-bc29-d9a79add866e'

result = merchant_admin_api.admin_put_merchant(merchant_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Delete Merchant

```python
def admin_delete_merchant(self,
                         merchant_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Merchant deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = '8e0a07c0-8d1c-4983-bb5f-312d2a13e573'

result = merchant_admin_api.admin_delete_merchant(merchant_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Unassume Merchant

```python
def post_unassume_merchant(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Merchant unassumed

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = merchant_admin_api.post_unassume_merchant()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Assume Merchant

```python
def post_assume_merchant(self,
                        merchant_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Now assuming merchant

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = '0a2bbe76-d32e-45a4-ac7b-c3be73c5c48a'

result = merchant_admin_api.post_assume_merchant(merchant_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Send Merchant Welcome

```python
def send_merchant_welcome(self,
                         merchant_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Welcome email sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = 'e73074cc-d032-4741-866b-f74884d5bf83'

result = merchant_admin_api.send_merchant_welcome(merchant_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Send Merchant ACH Rejection

```python
def send_merchant_ach_rejection(self,
                               merchant_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Rejection email sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = 'eb8ed02e-8702-4a41-b49a-e8e2e12292f6'

result = merchant_admin_api.send_merchant_ach_rejection(merchant_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Merchant Users

```python
def get_merchant_users(self,
                      merchant_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: List of users

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = '330f952b-52d1-428a-bab9-80327fdaa913'

result = merchant_admin_api.get_merchant_users(merchant_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Attach User

```python
def post_attach_user(self,
                    merchant_id,
                    id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: User attached

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = 'd0ef00bb-77de-459a-9138-e5755e06e39b'

id = '5a240a2d-ed9b-443a-ab39-8666de63e8b9'

result = merchant_admin_api.post_attach_user(
    merchant_id,
    id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Attach User

```python
def put_attach_user(self,
                   merchant_id,
                   id,
                   body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Attachment updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = 'ae192046-cdca-4dc8-8af9-9da2031a4057'

id = '1901ef23-b035-43ec-bb7c-a5db17827257'

result = merchant_admin_api.put_attach_user(
    merchant_id,
    id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Unattach User

```python
def delete_unattach_user(self,
                        merchant_id,
                        id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: User detached

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = '8d206040-53d4-4e2c-b5cd-439b445b8500'

id = '32f93731-3052-4771-abc0-a087b7f4bfce'

result = merchant_admin_api.delete_unattach_user(
    merchant_id,
    id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Admin Put User Merchant Option

```python
def admin_put_user_merchant_option(self,
                                  merchant_id,
                                  id,
                                  option)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |
| `id` | `uuid\|str` | Template, Required | - |
| `option` | `str` | Template, Required | - |

## Response Type

**200**: Option updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = '1781409f-287d-45d9-af5d-08708d0da58a'

id = 'bc260bdc-3e15-4c3d-abbd-bdba7df8dc6b'

option = 'string'

result = merchant_admin_api.admin_put_user_merchant_option(
    merchant_id,
    id,
    option
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete All Scheduled Invoices

```python
def delete_all_scheduled_invoices(self,
                                 merchant_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Scheduled invoices deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
merchant_id = '8e0a07c0-8d1c-4983-bb5f-312d2a13e573'

result = merchant_admin_api.delete_all_scheduled_invoices(merchant_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

