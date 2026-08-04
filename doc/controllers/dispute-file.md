# Dispute File

```python
dispute_file_api = client.dispute_file
```

## Class Name

`DisputeFileApi`

## Methods

* [Post Dispute File](../../doc/controllers/dispute-file.md#post-dispute-file)
* [Delete Dispute File](../../doc/controllers/dispute-file.md#delete-dispute-file)


# Post Dispute File

```python
def post_dispute_file(self,
                     file=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file` | `typing.BinaryIO` | Form, Optional | - |

## Response Type

**200**: Dispute file uploaded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = dispute_file_api.post_dispute_file()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Dispute File

```python
def delete_dispute_file(self,
                       id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Dispute file deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '82163d6a-fd6c-448d-a6b5-faf4fb5fb262'

result = dispute_file_api.delete_dispute_file(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

