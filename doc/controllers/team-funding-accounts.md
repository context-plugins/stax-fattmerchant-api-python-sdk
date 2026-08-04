# Team Funding Accounts

```python
team_funding_accounts_api = client.team_funding_accounts
```

## Class Name

`TeamFundingAccountsApi`

## Methods

* [Get Team Funding Accounts](../../doc/controllers/team-funding-accounts.md#get-team-funding-accounts)
* [Create Team Funding Account](../../doc/controllers/team-funding-accounts.md#create-team-funding-account)
* [Get Team Funding Account](../../doc/controllers/team-funding-accounts.md#get-team-funding-account)
* [Update Team Funding Account](../../doc/controllers/team-funding-accounts.md#update-team-funding-account)
* [Delete Team Funding Account](../../doc/controllers/team-funding-accounts.md#delete-team-funding-account)
* [Post Team Funding Account File](../../doc/controllers/team-funding-accounts.md#post-team-funding-account-file)
* [Delete Team Funding Account File](../../doc/controllers/team-funding-accounts.md#delete-team-funding-account-file)
* [Get Team Funding Account Files](../../doc/controllers/team-funding-accounts.md#get-team-funding-account-files)


# Get Team Funding Accounts

```python
def get_team_funding_accounts(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: List of funding accounts

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `body` property of this instance returns the response data which is of type `List[Any]`.

## Example Usage

```python
result = team_funding_accounts_api.get_team_funding_accounts()

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


# Create Team Funding Account

```python
def create_team_funding_account(self,
                               body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Funding account created

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = team_funding_accounts_api.create_team_funding_account(body)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Team Funding Account

```python
def get_team_funding_account(self,
                            account_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Funding account details

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
account_id = 'c154d109-b3d2-42b1-bede-f4f799ff5aba'

result = team_funding_accounts_api.get_team_funding_account(account_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Update Team Funding Account

```python
def update_team_funding_account(self,
                               account_id,
                               body)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_id` | `uuid\|str` | Template, Required | - |
| `body` | `Any` | Body, Required | - |

## Response Type

**200**: Funding account updated

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
account_id = '461ba183-9c75-4c18-afe7-1e056f8b0c51'

body = jsonpickle.decode('{"key1":"val1","key2":"val2"}')

result = team_funding_accounts_api.update_team_funding_account(
    account_id,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Team Funding Account

```python
def delete_team_funding_account(self,
                               account_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: Funding account deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
account_id = '9ec20974-2e06-4a10-a450-48d7beba69c5'

result = team_funding_accounts_api.delete_team_funding_account(account_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Post Team Funding Account File

```python
def post_team_funding_account_file(self,
                                  account_id,
                                  file=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_id` | `uuid\|str` | Template, Required | - |
| `file` | `typing.BinaryIO` | Form, Optional | - |

## Response Type

**200**: File uploaded

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
account_id = '97278b3b-aae5-4030-9b48-dae874ed92ec'

result = team_funding_accounts_api.post_team_funding_account_file(account_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Delete Team Funding Account File

```python
def delete_team_funding_account_file(self,
                                    account_id,
                                    file_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_id` | `uuid\|str` | Template, Required | - |
| `file_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: File deleted

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
account_id = '1601cfa4-894c-4e97-b5a0-df16d59393a8'

file_id = 'af2008a7-9a87-4494-a096-cd4eab14079b'

result = team_funding_accounts_api.delete_team_funding_account_file(
    account_id,
    file_id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Team Funding Account Files

```python
def get_team_funding_account_files(self,
                                  account_id)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_id` | `uuid\|str` | Template, Required | - |

## Response Type

**200**: List of files

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
account_id = '48a386e9-192c-4b04-a3b2-0cd43650d865'

result = team_funding_accounts_api.get_team_funding_account_files(account_id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

