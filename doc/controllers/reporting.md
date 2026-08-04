# Reporting

Reporting and summaries

```python
reporting_api = client.reporting
```

## Class Name

`ReportingApi`

## Methods

* [Get Report](../../doc/controllers/reporting.md#get-report)
* [Get Team Summary](../../doc/controllers/reporting.md#get-team-summary)


# Get Report

```python
def get_report(self,
              start_date=None,
              end_date=None)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `start_date` | `date` | Query, Optional | - |
| `end_date` | `date` | Query, Optional | - |

## Response Type

**200**: Report data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
start_date = dateutil.parser.parse('2026-02-19').date()

end_date = dateutil.parser.parse('2026-02-19').date()

result = reporting_api.get_report(
    start_date=start_date,
    end_date=end_date
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Get Team Summary

```python
def get_team_summary(self)
```

## Authentication

This endpoint requires [bearerAuth](../../doc/auth/oauth-2-bearer-token.md)

## Response Type

**200**: Team summary data

This method returns an [`ApiResponse`](../../doc/api-response.md) instance.

## Example Usage

```python
result = reporting_api.get_team_summary()

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```

