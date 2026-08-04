# Verify

Card verification

```python
verify_api = client.verify
```

## Class Name

`VerifyApi`

## Methods

* [Get Verifications](../../doc/controllers/verify.md#get-verifications)
* [Post Verification](../../doc/controllers/verify.md#post-verification)


# Get Verifications

```python
def get_verifications(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of verifications

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = verify_api.get_verifications()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Verification

```python
def post_verification(self,
                     body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PostVerificationRequestBodyJson`](../../doc/models/post-verification-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Verification created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PostVerificationRequestBodyJson(
    payment_method_id='3a64f5ce-e2f7-4809-991e-45ac6e95e0ab'
)

result = verify_api.post_verification(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

