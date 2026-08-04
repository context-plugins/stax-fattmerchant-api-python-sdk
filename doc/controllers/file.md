# File

File management

```python
file_api = client.file
```

## Class Name

`FileApi`

## Methods

* [Get Files](../../doc/controllers/file.md#get-files)
* [Post File](../../doc/controllers/file.md#post-file)
* [Get File Tags](../../doc/controllers/file.md#get-file-tags)
* [Get File](../../doc/controllers/file.md#get-file)
* [Put File](../../doc/controllers/file.md#put-file)
* [Delete File](../../doc/controllers/file.md#delete-file)


# Get Files

```python
def get_files(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of files

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = file_api.get_files()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post File

```python
def post_file(self,
             file=None,
             tag=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `typing.BinaryIO` | Form, Optional | - |
| `tag` | `str` | Form, Optional | - |

## Response Type

**200**: File uploaded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
tag = 'string'

result = file_api.post_file(
    tag=tag
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get File Tags

```python
def get_file_tags(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of tags

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = file_api.get_file_tags()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get File

```python
def get_file(self,
            id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: File details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'dd3c3b8c-5e0e-41ac-95be-dc0a109c6df0'

result = file_api.get_file(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put File

```python
def put_file(self,
            id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: File updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'c5cb4536-371a-4267-8b35-d4657799c4d4'

result = file_api.put_file(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete File

```python
def delete_file(self,
               id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: File deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '8c88111b-bb59-444a-b21c-0808b5858d1b'

result = file_api.delete_file(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

