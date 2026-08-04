# Cache

```python
cache_api = client.cache
```

## Class Name

`CacheApi`


# Post Cache Test

```python
def post_cache_test(self,
                   body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PostCacheTestRequestBodyJson`](../../doc/models/post-cache-test-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Cache test result

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PostCacheTestRequestBodyJson(
    key='string'
)

result = cache_api.post_cache_test(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

