# Transaction

Transaction processing and management

```python
transaction_api = client.transaction
```

## Class Name

`TransactionApi`

## Methods

* [Get Transactions](../../doc/controllers/transaction.md#get-transactions)
* [Post Transaction](../../doc/controllers/transaction.md#post-transaction)
* [Get Transaction](../../doc/controllers/transaction.md#get-transaction)
* [Put Transaction](../../doc/controllers/transaction.md#put-transaction)
* [Post Refund](../../doc/controllers/transaction.md#post-refund)
* [Post Void](../../doc/controllers/transaction.md#post-void)
* [Post Void or Refund](../../doc/controllers/transaction.md#post-void-or-refund)
* [Post Capture](../../doc/controllers/transaction.md#post-capture)
* [Get Related Transaction](../../doc/controllers/transaction.md#get-related-transaction)
* [Put Receipt](../../doc/controllers/transaction.md#put-receipt)
* [Post Receipt](../../doc/controllers/transaction.md#post-receipt)
* [Put Email Receipt](../../doc/controllers/transaction.md#put-email-receipt)
* [Post Email Receipt](../../doc/controllers/transaction.md#post-email-receipt)
* [Put Sms Receipt](../../doc/controllers/transaction.md#put-sms-receipt)
* [Post Sms Receipt](../../doc/controllers/transaction.md#post-sms-receipt)
* [Put Receipt Bulk Method](../../doc/controllers/transaction.md#put-receipt-bulk-method)
* [Put Receipt Bulk](../../doc/controllers/transaction.md#put-receipt-bulk)
* [Post Transaction Log](../../doc/controllers/transaction.md#post-transaction-log)
* [Get Transaction Funding](../../doc/controllers/transaction.md#get-transaction-funding)


# Get Transactions

```python
def get_transactions(self,
                    page=None,
                    per_page=None,
                    keywords=None,
                    start_date=None,
                    end_date=None,
                    mtype=None,
                    success=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Query, Optional | Page number for pagination |
| `per_page` | `int` | Query, Optional | Number of items per page |
| `keywords` | `str` | Query, Optional | - |
| `start_date` | `date` | Query, Optional | - |
| `end_date` | `date` | Query, Optional | - |
| `mtype` | `str` | Query, Optional | - |
| `success` | `bool` | Query, Optional | - |

## Response Type

**200**: Paginated list of transactions

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
page = 1

per_page = 10

keywords = 'string'

start_date = dateutil.parser.parse('2026-02-19').date()

end_date = dateutil.parser.parse('2026-02-19').date()

mtype = 'string'

success = True

result = transaction_api.get_transactions(
    page=page,
    per_page=per_page,
    keywords=keywords,
    start_date=start_date,
    end_date=end_date,
    mtype=mtype,
    success=success
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Transaction

```python
def post_transaction(self,
                    body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Transaction created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = transaction_api.post_transaction(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Transaction

```python
def get_transaction(self,
                   id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Transaction details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
id = '9e5a6f9d-ae83-4f4b-b89e-e376a3b7d966'

result = transaction_api.get_transaction(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Transaction

```python
def put_transaction(self,
                   id,
                   body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PutTransactionRequestBodyJson`](../../doc/models/put-transaction-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Transaction updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'b7dc6b43-45f8-4075-a4f0-5f53a7673526'

body = PutTransactionRequestBodyJson(
    meta=jsonpickle.decode('{}')
)

result = transaction_api.put_transaction(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Refund

```python
def post_refund(self,
               id,
               body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PostRefundRequestBodyJson`](../../doc/models/post-refund-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Refund created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
id = 'd5be49c9-1035-4718-8ea9-ae8642f12638'

body = PostRefundRequestBodyJson(
    total=50
)

result = transaction_api.post_refund(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Void

```python
def post_void(self,
             id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Transaction voided

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
id = 'fb65aad6-0d2e-4f5e-b269-3eddc2fc7065'

result = transaction_api.post_void(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Void or Refund

```python
def post_void_or_refund(self,
                       id,
                       body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PostVoidOrRefundRequestBodyJson`](../../doc/models/post-void-or-refund-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Transaction voided or refunded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '3e9afa46-6e98-4ceb-afee-b5d5ceb66c02'

body = PostVoidOrRefundRequestBodyJson(
    total=50
)

result = transaction_api.post_void_or_refund(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Capture

```python
def post_capture(self,
                id,
                body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PostCaptureRequestBodyJson`](../../doc/models/post-capture-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Transaction captured

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '106a3f6a-91e5-4f04-bb62-62b545983b93'

body = PostCaptureRequestBodyJson(
    total=50
)

result = transaction_api.post_capture(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Related Transaction

```python
def get_related_transaction(self,
                           id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Related transactions

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'c00ffecd-a725-445a-aa69-22ae42567f00'

result = transaction_api.get_related_transaction(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Receipt

```python
def put_receipt(self,
               id,
               method,
               body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `method` | [`PutReceiptMethod`](../../doc/models/put-receipt-method.md) | Template, Required | - |
| `body` | [`PutReceiptRequestBodyJson`](../../doc/models/put-receipt-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Receipt sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'a5dfe5e0-325f-4ada-8f3f-0e43d8008bb5'

method = PutReceiptMethod.EMAIL

body = PutReceiptRequestBodyJson(
    email='user@example.com',
    phone='string'
)

result = transaction_api.put_receipt(
    id,
    method,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Receipt

```python
def post_receipt(self,
                id,
                method,
                body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `method` | [`PutReceiptMethod`](../../doc/models/put-receipt-method.md) | Template, Required | - |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Receipt sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '23a84d63-5733-4e9e-b078-1a3e15c155f0'

method = PutReceiptMethod.EMAIL

result = transaction_api.post_receipt(
    id,
    method
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Email Receipt

```python
def put_email_receipt(self,
                     id,
                     body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PutEmailReceiptRequestBodyJson`](../../doc/models/put-email-receipt-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Email receipt sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '0c573f40-814a-49c1-973a-0998b4d49fdd'

body = PutEmailReceiptRequestBodyJson(
    email='user@example.com'
)

result = transaction_api.put_email_receipt(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Email Receipt

```python
def post_email_receipt(self,
                      id,
                      body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PostEmailReceiptRequestBodyJson`](../../doc/models/post-email-receipt-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Email receipt sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'ea1ecfc6-2cc5-41c2-a7e4-885d894aa241'

body = PostEmailReceiptRequestBodyJson(
    email='user@example.com'
)

result = transaction_api.post_email_receipt(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Sms Receipt

```python
def put_sms_receipt(self,
                   id,
                   body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PutSmsReceiptRequestBodyJson`](../../doc/models/put-sms-receipt-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: SMS receipt sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'b0e7e7cd-c3bc-468e-a52d-553205fe6266'

body = PutSmsReceiptRequestBodyJson(
    phone='string'
)

result = transaction_api.put_sms_receipt(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Sms Receipt

```python
def post_sms_receipt(self,
                    id,
                    body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PostSmsReceiptRequestBodyJson`](../../doc/models/post-sms-receipt-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: SMS receipt sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '11694b8e-b5d5-473c-b91d-914f5806bf49'

body = PostSmsReceiptRequestBodyJson(
    phone='string'
)

result = transaction_api.post_sms_receipt(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Receipt Bulk Method

```python
def put_receipt_bulk_method(self,
                           method,
                           body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `method` | [`PutReceiptMethod`](../../doc/models/put-receipt-method.md) | Template, Required | - |
| `body` | [`PutReceiptBulkMethodRequestBodyJson`](../../doc/models/put-receipt-bulk-method-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Receipts sent in bulk

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
method = PutReceiptMethod.EMAIL

body = PutReceiptBulkMethodRequestBodyJson(
    transaction_ids=[
        'c29dcf19-ff14-4e95-840e-aa9ff5c44854'
    ]
)

result = transaction_api.put_receipt_bulk_method(
    method,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Receipt Bulk

```python
def put_receipt_bulk(self,
                    body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`PutReceiptBulkRequestBodyJson`](../../doc/models/put-receipt-bulk-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Receipts sent in bulk

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = PutReceiptBulkRequestBodyJson(
    transaction_ids=[
        'f1dc205a-b708-421b-8fb7-db227a386486'
    ]
)

result = transaction_api.put_receipt_bulk(
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Transaction Log

```python
def post_transaction_log(self,
                        body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Optional | - |

## Response Type

**200**: Log created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = transaction_api.post_transaction_log()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Transaction Funding

```python
def get_transaction_funding(self,
                           id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Funding details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '97a483e2-c46f-44a6-8049-000ef8da33ee'

result = transaction_api.get_transaction_funding(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

