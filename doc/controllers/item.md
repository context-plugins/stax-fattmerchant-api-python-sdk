# Item

Item/product catalog management

```python
item_api = client.item
```

## Class Name

`ItemApi`

## Methods

* [Get Items](../../doc/controllers/item.md#get-items)
* [Post Item](../../doc/controllers/item.md#post-item)
* [Get Item Codes](../../doc/controllers/item.md#get-item-codes)
* [Get Item Categories](../../doc/controllers/item.md#get-item-categories)
* [Put Publish Bulk](../../doc/controllers/item.md#put-publish-bulk)
* [Put Unpublish Bulk](../../doc/controllers/item.md#put-unpublish-bulk)
* [Delete Item Bulk](../../doc/controllers/item.md#delete-item-bulk)
* [Get Item](../../doc/controllers/item.md#get-item)
* [Put Item](../../doc/controllers/item.md#put-item)
* [Delete Item](../../doc/controllers/item.md#delete-item)
* [Post Item Thumbnail](../../doc/controllers/item.md#post-item-thumbnail)
* [Put Item Increment](../../doc/controllers/item.md#put-item-increment)
* [Put Item Decrement](../../doc/controllers/item.md#put-item-decrement)


# Get Items

```python
def get_items(self,
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

**200**: Paginated list of items

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
page = 1

per_page = 10

result = item_api.get_items(
    page=page,
    per_page=per_page
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Item

```python
def post_item(self,
             body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Item created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = item_api.post_item(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Item Codes

```python
def get_item_codes(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of item codes

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = item_api.get_item_codes()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Item Categories

```python
def get_item_categories(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of categories

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = item_api.get_item_categories()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Publish Bulk

```python
def put_publish_bulk(self,
                    body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PutPublishBulkRequestBodyJson`](../../doc/models/put-publish-bulk-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Items published

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PutPublishBulkRequestBodyJson(
    ids=[
        '57c6352a-aabf-4ead-9f60-cf7df39abdc9'
    ]
)

result = item_api.put_publish_bulk(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Unpublish Bulk

```python
def put_unpublish_bulk(self,
                      body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PutUnpublishBulkRequestBodyJson`](../../doc/models/put-unpublish-bulk-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Items unpublished

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PutUnpublishBulkRequestBodyJson(
    ids=[
        'c6a05049-44fc-46ee-86ca-bb354bca4f45'
    ]
)

result = item_api.put_unpublish_bulk(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Item Bulk

```python
def delete_item_bulk(self,
                    body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`DeleteItemBulkRequestBodyJson`](../../doc/models/delete-item-bulk-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Items deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = DeleteItemBulkRequestBodyJson(
    ids=[
        '1d75b6bb-9353-4237-89b1-4a1e1a93b40a'
    ]
)

result = item_api.delete_item_bulk(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Item

```python
def get_item(self,
            id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Item details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'a81f05d3-2300-4479-af58-7c8f05fca455'

result = item_api.get_item(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Item

```python
def put_item(self,
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

**200**: Item updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'b354c5c3-2419-4765-b26e-fb96b9d45232'

body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = item_api.put_item(
    id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Item

```python
def delete_item(self,
               id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Item deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'c55080d9-f2dd-4ccf-b48a-04c1ef52b877'

result = item_api.delete_item(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Item Thumbnail

```python
def post_item_thumbnail(self,
                       id,
                       file=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `file` | `typing.BinaryIO` | Form, Optional | - |

## Response Type

**200**: Thumbnail uploaded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'd0cdc89e-8e50-4234-a04d-6ca438ca9611'

result = item_api.post_item_thumbnail(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Item Increment

```python
def put_item_increment(self,
                      id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Stock incremented

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'e63c2153-0e5d-45fa-8b4e-0c4bce5361b8'

result = item_api.put_item_increment(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Item Decrement

```python
def put_item_decrement(self,
                      id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Stock decremented

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '985a2b2a-9f48-4a0c-b0d7-ba0cfad70faf'

result = item_api.put_item_decrement(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

