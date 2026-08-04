# Invoice

Invoice management

```python
invoice_api = client.invoice
```

## Class Name

`InvoiceApi`

## Methods

* [Get Invoices](../../doc/controllers/invoice.md#get-invoices)
* [Post Invoice](../../doc/controllers/invoice.md#post-invoice)
* [Get Invoice](../../doc/controllers/invoice.md#get-invoice)
* [Put Invoice](../../doc/controllers/invoice.md#put-invoice)
* [Delete Invoice](../../doc/controllers/invoice.md#delete-invoice)
* [Put Send Invoice](../../doc/controllers/invoice.md#put-send-invoice)
* [Put Send Invoice Bulk](../../doc/controllers/invoice.md#put-send-invoice-bulk)
* [Put Test Attachment](../../doc/controllers/invoice.md#put-test-attachment)
* [Post Send Later](../../doc/controllers/invoice.md#post-send-later)
* [Post Invoice Payment](../../doc/controllers/invoice.md#post-invoice-payment)
* [Post Invoice Manual Payment](../../doc/controllers/invoice.md#post-invoice-manual-payment)


# Get Invoices

```python
def get_invoices(self,
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

**200**: Paginated list of invoices

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
page = 1

per_page = 10

result = invoice_api.get_invoices(
    page=page,
    per_page=per_page
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Invoice

```python
def post_invoice(self,
                body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Invoice created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = invoice_api.post_invoice(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Invoice

```python
def get_invoice(self,
               id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Invoice details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `Any`.

## Example Usage

```python
id = '81151595-7c10-4299-be43-7704793ef793'

result = invoice_api.get_invoice(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Invoice

```python
def put_invoice(self,
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

**200**: Invoice updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'c9a88204-db77-49b2-8c2c-f889023c6f8d'

body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = invoice_api.put_invoice(
    id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Invoice

```python
def delete_invoice(self,
                  id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Invoice deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '40e95c07-2473-4600-ad82-f3b3b8cd53a7'

result = invoice_api.delete_invoice(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Send Invoice

```python
def put_send_invoice(self,
                    id,
                    method)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `method` | [`PutReceiptMethod`](../../doc/models/put-receipt-method.md) | Template, Required | - |

## Response Type

**200**: Invoice sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '3986a8a3-de88-4639-a4df-b23909a8328e'

method = PutReceiptMethod.EMAIL

result = invoice_api.put_send_invoice(
    id,
    method
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Send Invoice Bulk

```python
def put_send_invoice_bulk(self,
                         method,
                         body=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `method` | [`PutReceiptMethod`](../../doc/models/put-receipt-method.md) | Template, Required | - |
| `body` | [`PutSendInvoiceBulkRequestBodyJson`](../../doc/models/put-send-invoice-bulk-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Invoices sent

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
method = PutReceiptMethod.EMAIL

body = PutSendInvoiceBulkRequestBodyJson(
    invoice_ids=[
        'b2306869-442a-421c-8b1e-87e1077724fe'
    ]
)

result = invoice_api.put_send_invoice_bulk(
    method,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Put Test Attachment

```python
def put_test_attachment(self,
                       id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Attachment tested

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '40b10596-acc0-4112-a792-6ee66a974760'

result = invoice_api.put_test_attachment(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Send Later

```python
def post_send_later(self,
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
| `body` | [`PostSendLaterRequestBodyJson`](../../doc/models/post-send-later-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Invoice scheduled

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '8c4fc874-5b49-48f1-b281-9a32d6c6fe1f'

method = PutReceiptMethod.EMAIL

body = PostSendLaterRequestBodyJson(
    send_at=dateutil.parser.parse('2026-02-19T11:30:08.0367268Z')
)

result = invoice_api.post_send_later(
    id,
    method,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Invoice Payment

```python
def post_invoice_payment(self,
                        id,
                        body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `uuid\|str` | Template, Required | - |
| `body` | [`PostInvoicePaymentRequestBodyJson`](../../doc/models/post-invoice-payment-request-body-json.md) | Body, Required | - |

## Response Type

**200**: Payment applied

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = 'd2bd0f69-cfbc-46b4-b6ca-7437a6b397aa'

body = PostInvoicePaymentRequestBodyJson(
    payment_method_id='00aa237f-4511-4727-b657-6f13f8497a82',
    apply_balance=True
)

result = invoice_api.post_invoice_payment(
    id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Invoice Manual Payment

```python
def post_invoice_manual_payment(self,
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
| `method` | [`PostInvoiceManualPaymentMethod`](../../doc/models/post-invoice-manual-payment-method.md) | Template, Required | - |
| `body` | [`PostInvoiceManualPaymentRequestBodyJson`](../../doc/models/post-invoice-manual-payment-request-body-json.md) | Body, Optional | - |

## Response Type

**200**: Manual payment applied

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
id = '2ece5d32-0d05-473b-b017-8ab6354a7515'

method = PostInvoiceManualPaymentMethod.GIFTCARD

body = PostInvoiceManualPaymentRequestBodyJson(
    total=50
)

result = invoice_api.post_invoice_manual_payment(
    id,
    method,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

