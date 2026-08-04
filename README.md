
# Getting Started with Stax (FattMerchant) API

## Introduction

API specification auto-generated from Laravel route definitions.
Base URL: https://apiprod.fattlabs.com
All routes require JWT authentication unless otherwise noted.

## Building

You must have Python `3.7+` installed on your system to install and run this SDK. This SDK package depends on other Python packages like pytest, etc. These dependencies are defined in the `requirements.txt` file that comes with the SDK. To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type `pip --version`. This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including `requirements.txt`) for the SDK.
* Run the command `pip install -r requirements.txt`. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Staxfattmerchantapi-Python&step=installDependencies)

## Installation

The following section explains how to use the staxfattmerchantapi library in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Staxfattmerchantapi-Python&step=pyCharm)

Click on `Open` in PyCharm to browse to your generated SDK directory and then click `OK`.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=Staxfattmerchantapi-Python&step=openProject0)

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=Staxfattmerchantapi-Python&projectName=staxfattmerchantapi&step=openProject1)

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Staxfattmerchantapi-Python&projectName=staxfattmerchantapi&step=createDirectory)

Name the directory as "test".

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?workspaceFolder=Staxfattmerchantapi-Python&step=nameDirectory)

Add a python file to this project.

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?workspaceFolder=Staxfattmerchantapi-Python&projectName=staxfattmerchantapi&step=createFile)

Name it "testSDK".

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?workspaceFolder=Staxfattmerchantapi-Python&projectName=staxfattmerchantapi&step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```python
from staxfattmerchantapi.staxfattmerchantapi_client import StaxfattmerchantapiClient
```

![Add a new project in PyCharm - Step 5](https://apidocs.io/illustration/python?workspaceFolder=Staxfattmerchantapi-Python&projectName=staxfattmerchantapi&libraryName=staxfattmerchantapi.staxfattmerchantapi_client&className=StaxfattmerchantapiClient&step=projectFiles)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on `Run`

![Run Test Project - Step 1](https://apidocs.io/illustration/python?workspaceFolder=Staxfattmerchantapi-Python&projectName=staxfattmerchantapi&libraryName=staxfattmerchantapi.staxfattmerchantapi_client&className=StaxfattmerchantapiClient&step=runProject)

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](README.md#environments) | The API environment. <br> **Default: `Environment.PRODUCTION`** |
| http_client_instance | `Union[Session, HttpClientProvider]` | The Http Client passed from the sdk user for making requests |
| override_http_client_configuration | `bool` | The value which determines to override properties of the passed Http Client from the sdk user |
| http_call_back | `HttpCallBack` | The callback value that is invoked before and after an HTTP call is made to an endpoint |
| timeout | `float` | The value to use for connection timeout. <br> **Default: 30** |
| max_retries | `int` | The number of times to retry an endpoint call if it fails. <br> **Default: 0** |
| backoff_factor | `float` | A backoff factor to apply between attempts after the second try. <br> **Default: 2** |
| retry_statuses | `Array of int` | The http statuses on which retry is to be done. <br> **Default: [408, 413, 429, 500, 502, 503, 504, 521, 522, 524, 408, 413, 429, 500, 502, 503, 504, 521, 522, 524]** |
| retry_methods | `Array of string` | The http methods on which retry is to be done. <br> **Default: ["GET", "PUT", "GET", "PUT"]** |
| proxy_settings | [`ProxySettings`](doc/proxy-settings.md) | Optional proxy configuration to route HTTP requests through a proxy server. |
| logging_configuration | [`LoggingConfiguration`](doc/logging-configuration.md) | The SDK logging configuration for API calls |
| bearer_auth_credentials | [`BearerAuthCredentials`](doc/auth/oauth-2-bearer-token.md) | The credential object for OAuth 2 Bearer token |

The API client can be initialized as follows:

### Code-Based Client Initialization

```python
import logging

from staxfattmerchantapi.configuration import Environment
from staxfattmerchantapi.http.auth.oauth_2 import BearerAuthCredentials
from staxfattmerchantapi.logging.configuration.api_logging_configuration import LoggingConfiguration
from staxfattmerchantapi.logging.configuration.api_logging_configuration import RequestLoggingConfiguration
from staxfattmerchantapi.logging.configuration.api_logging_configuration import ResponseLoggingConfiguration
from staxfattmerchantapi.staxfattmerchantapi_client import StaxfattmerchantapiClient

client = StaxfattmerchantapiClient(
    bearer_auth_credentials=BearerAuthCredentials(
        access_token='AccessToken'
    ),
    environment=Environment.PRODUCTION,
    logging_configuration=LoggingConfiguration(
        log_level=logging.INFO,
        request_logging_config=RequestLoggingConfiguration(
            log_body=True
        ),
        response_logging_config=ResponseLoggingConfiguration(
            log_headers=True
        )
    )
)
```

### Environment-Based Client Initialization

```python
from staxfattmerchantapi.staxfattmerchantapi_client import StaxfattmerchantapiClient

# Specify the path to your .env file if it’s located outside the project’s root directory.
client = StaxfattmerchantapiClient.from_environment(dotenv_path='/path/to/.env')
```

See the [Environment-Based Client Initialization](doc/environment-based-client-initialization.md) section for details.

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| PRODUCTION | **Default** Production |
| ENVIRONMENT2 | Development |

## Authorization

This API uses the following authentication schemes.

* [`bearerAuth (OAuth 2 Bearer token)`](doc/auth/oauth-2-bearer-token.md)

## List of APIs

* [Team Users](doc/controllers/team-users.md)
* [Team API Keys](doc/controllers/team-api-keys.md)
* [Team Options](doc/controllers/team-options.md)
* [Team Registration](doc/controllers/team-registration.md)
* [Team Funding Accounts](doc/controllers/team-funding-accounts.md)
* [Invoice Schedule](doc/controllers/invoice-schedule.md)
* [Dispute File](doc/controllers/dispute-file.md)
* [Payment Method](doc/controllers/payment-method.md)
* [Merchant Admin](doc/controllers/merchant-admin.md)
* [User Admin](doc/controllers/user-admin.md)
* [Web Payment](doc/controllers/web-payment.md)
* [Self](doc/controllers/self.md)
* [Team](doc/controllers/team.md)
* [Webhook](doc/controllers/webhook.md)
* [Transaction](doc/controllers/transaction.md)
* [Invoice](doc/controllers/invoice.md)
* [Customer](doc/controllers/customer.md)
* [Item](doc/controllers/item.md)
* [File](doc/controllers/file.md)
* [Integration](doc/controllers/integration.md)
* [Hello Sign](doc/controllers/hello-sign.md)
* [Reporting](doc/controllers/reporting.md)
* [Charge](doc/controllers/charge.md)
* [Credit](doc/controllers/credit.md)
* [Verify](doc/controllers/verify.md)
* [Terminal](doc/controllers/terminal.md)
* [Sandbox](doc/controllers/sandbox.md)
* [Cache](doc/controllers/cache.md)

## SDK Infrastructure

### Configuration

* [ProxySettings](doc/proxy-settings.md)
* [Environment-Based Client Initialization](doc/environment-based-client-initialization.md)
* [AbstractLogger](doc/abstract-logger.md)
* [LoggingConfiguration](doc/logging-configuration.md)
* [RequestLoggingConfiguration](doc/request-logging-configuration.md)
* [ResponseLoggingConfiguration](doc/response-logging-configuration.md)

### HTTP

* [HttpResponse](doc/http-response.md)
* [HttpRequest](doc/http-request.md)

### Utilities

* [ApiResponse](doc/api-response.md)
* [ApiHelper](doc/api-helper.md)
* [HttpDateTime](doc/http-date-time.md)
* [RFC3339DateTime](doc/rfc3339-date-time.md)
* [UnixDateTime](doc/unix-date-time.md)

