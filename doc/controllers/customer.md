# Customer

Customer management

```python
customer_api = client.customer
```

## Class Name

`CustomerApi`

## Methods

* [Get Customers](../../doc/controllers/customer.md#get-customers)
* [Post Customer](../../doc/controllers/customer.md#post-customer)
* [Delete Customer Bulk](../../doc/controllers/customer.md#delete-customer-bulk)
* [Put Restore Customer Bulk](../../doc/controllers/customer.md#put-restore-customer-bulk)
* [Post Find or Create Customer](../../doc/controllers/customer.md#post-find-or-create-customer)
* [Get Customer](../../doc/controllers/customer.md#get-customer)
* [Put Customer](../../doc/controllers/customer.md#put-customer)
* [Delete Customer](../../doc/controllers/customer.md#delete-customer)
* [Put Restore Customer](../../doc/controllers/customer.md#put-restore-customer)
* [Get Customer Files](../../doc/controllers/customer.md#get-customer-files)
* [Get Customer Payment Methods](../../doc/controllers/customer.md#get-customer-payment-methods)
* [Merge Customer](../../doc/controllers/customer.md#merge-customer)
* [Merge Duplicate Customers](../../doc/controllers/customer.md#merge-duplicate-customers)
* [Unmerge Customer](../../doc/controllers/customer.md#unmerge-customer)


# Get Customers

```python
def get_customers(self,
                 page=None,
                 per_page=None,
                 keywords=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | Page number for pagination |
| `per_page` | `int` | Query, Optional | Number of items per page |
| `keywords` | `str` | Query, Optional | - |

## Response Type

**200**: Paginated list of customers

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
page = 1

per_page = 10

keywords = 'string'

result = customer_api.get_customers(
    page=page,
    per_page=per_page,
    keywords=keywords
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Customer

```python
def post_customer(self,
                 body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Customer created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = customer_api.post_customer(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Customer Bulk

```python
def delete_customer_bulk(self,
                        body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`DeleteCustomerBulkRequestBodyJson`](../../doc/models/delete-customer-bulk-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Customers deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = DeleteCustomerBulkRequestBodyJson(
    ids=[
        'f48f0a02-1cad-4651-8ae4-6c707231f0f3'
    ]
)

result = customer_api.delete_customer_bulk(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Restore Customer Bulk

```python
def put_restore_customer_bulk(self,
                             body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PutRestoreCustomerBulkRequestBodyJson`](../../doc/models/put-restore-customer-bulk-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Customers restored

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PutRestoreCustomerBulkRequestBodyJson(
    ids=[
        '162e114c-e700-4bf6-a82b-e896e9189445'
    ]
)

result = customer_api.put_restore_customer_bulk(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Find or Create Customer

```python
def post_find_or_create_customer(self,
                                body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Customer found or created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = customer_api.post_find_or_create_customer(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Customer

```python
def get_customer(self,
                id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Customer details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
id = 'de697049-1950-40ea-993c-a20f21630e23'

result = customer_api.get_customer(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Customer

```python
def put_customer(self,
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

**200**: Customer updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'aafc5822-62f4-437a-9d61-ce48b0ea0bb4'

body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = customer_api.put_customer(
    id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Customer

```python
def delete_customer(self,
                   id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Customer deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '6b8eccd0-436a-4ccb-8f43-910bd91c71bf'

result = customer_api.delete_customer(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Restore Customer

```python
def put_restore_customer(self,
                        id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Customer restored

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'd03da812-92f2-4a62-ba2f-dc23cdada558'

result = customer_api.put_restore_customer(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Customer Files

```python
def get_customer_files(self,
                      id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: List of customer files

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'c267a245-f412-48aa-b7e7-2245a9f5496e'

result = customer_api.get_customer_files(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Customer Payment Methods

```python
def get_customer_payment_methods(self,
                                id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: List of payment methods

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[Any]`.

## Example Usage

```python
id = '66a8212b-ce68-420d-a961-0f845c6a7607'

result = customer_api.get_customer_payment_methods(id)

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


# Merge Customer

```python
def merge_customer(self,
                  id,
                  body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`MergeCustomerRequestBodyJson`](../../doc/models/merge-customer-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Customers merged

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'baebe10b-4bac-4358-8ab1-c86f8e5a79fb'

body = MergeCustomerRequestBodyJson(
    duplicates=[
        '7d29292f-b705-4d68-91ef-f85dc49a187b'
    ]
)

result = customer_api.merge_customer(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Merge Duplicate Customers

```python
def merge_duplicate_customers(self,
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

**200**: Duplicates merged

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'be5c8e68-449d-46ee-890e-138a4f77e22d'

result = customer_api.merge_duplicate_customers(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Unmerge Customer

```python
def unmerge_customer(self,
                    id,
                    merge_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `merge_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Customer unmerged

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '385d5325-aadd-4a9f-b31b-2a90af8e5880'

merge_id = 'bc0f1577-71e0-4199-8f94-2637605e3bf0'

result = customer_api.unmerge_customer(
    id,
    merge_id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

