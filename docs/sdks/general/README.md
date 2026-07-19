# General

## Overview

General endpoints for basic PMS operation not specific to any media provider

### Available Operations

* [getServerInfo](#getserverinfo) - Get PMS info
* [getSystemAccounts](#getsystemaccounts) - Get System Accounts
* [getUserWebhooks](#getuserwebhooks) - User Webhooks
* [addUserWebhook](#adduserwebhook) - Add User Webhook
* [getClients](#getclients) - Get Clients
* [getCloudServer](#getcloudserver) - Get Cloud Server
* [getSystemDevices](#getsystemdevices) - Get System Devices
* [getDiagnostics](#getdiagnostics) - Get Diagnostics
* [downloadDatabaseDiagnostics](#downloaddatabasediagnostics) - Download Database Diagnostics
* [downloadLogBundle](#downloadlogbundle) - Download Log Bundle
* [getGeoIP](#getgeoip) - Get GeoIP
* [getIdentity](#getidentity) - Get PMS identity
* [getIP](#getip) - Get IP
* [claimServer](#claimserver) - Claim Server
* [refreshReachability](#refreshreachability) - Refresh Reachability
* [getSourceConnectionInformation](#getsourceconnectioninformation) - Get Source Connection Information
* [createTransientToken](#createtransienttoken) - Get Transient Tokens
* [getLocalServers](#getlocalservers) - Get Local Servers
* [browseFilesystem](#browsefilesystem) - Browse Filesystem
* [getBandwidthStatistics](#getbandwidthstatistics) - Get Bandwidth Statistics
* [getResourceStatistics](#getresourcestatistics) - Get Resource Statistics
* [getSyncStatus](#getsyncstatus) - Get Sync Status
* [getSyncItems](#getsyncitems) - Get Sync Items
* [getSyncQueue](#getsyncqueue) - Get Sync Queue
* [refreshSyncContent](#refreshsynccontent) - Refresh Sync Content
* [refreshSyncLists](#refreshsynclists) - Refresh Sync Lists
* [getSyncTranscodeQueue](#getsynctranscodequeue) - Get Sync Transcode Queue
* [getMetadataAgents](#getmetadataagents) - Get Metadata Agents
* [getSystemSettings](#getsystemsettings) - Get System Settings
* [checkForSystemUpdates](#checkforsystemupdates) - Check for System Updates
* [getWebhooks](#getwebhooks) - Get Webhooks
* [addWebhook](#addwebhook) - Add Webhook
* [getPlexDownloads](#getplexdownloads) - Get Plex Downloads
* [browseFilesystemPath](#browsefilesystempath) - Browse Filesystem Path
* [getSyncItem](#getsyncitem) - Get Sync Item
* [getMetadataAgentDetails](#getmetadataagentdetails) - Get Metadata Agent Details

## getServerInfo

Information about this PMS setup and configuration

### Example Usage

<!-- UsageSnippet language="java" operationID="getServerInfo" method="get" path="/" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetServerInfoRequest;
import dev.plexapi.sdk.models.operations.GetServerInfoResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetServerInfoRequest req = GetServerInfoRequest.builder()
                .build();

        GetServerInfoResponse res = sdk.general().getServerInfo()
                .request(req)
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `request`                                                               | [GetServerInfoRequest](../../models/operations/GetServerInfoRequest.md) | :heavy_check_mark:                                                      | The request object to use for the request.                              |

### Response

**[GetServerInfoResponse](../../models/operations/GetServerInfoResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSystemAccounts

Get a list of local system accounts.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSystemAccounts" method="get" path="/accounts" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSystemAccountsRequest;
import dev.plexapi.sdk.models.operations.GetSystemAccountsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetSystemAccountsRequest req = GetSystemAccountsRequest.builder()
                .build();

        GetSystemAccountsResponse res = sdk.general().getSystemAccounts()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [GetSystemAccountsRequest](../../models/operations/GetSystemAccountsRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetSystemAccountsResponse](../../models/operations/GetSystemAccountsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getUserWebhooks

List webhook URLs for the logged-in user.

### Example Usage

<!-- UsageSnippet language="java" operationID="getUserWebhooks" method="get" path="/api/v2/user/webhooks" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetUserWebhooksResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetUserWebhooksResponse res = sdk.general().getUserWebhooks()
                .call();

        if (res.webhookPayload().isPresent()) {
            System.out.println(res.webhookPayload().get());
        }
    }
}
```

### Parameters

| Parameter                      | Type                           | Required                       | Description                    |
| ------------------------------ | ------------------------------ | ------------------------------ | ------------------------------ |
| `serverURL`                    | *String*                       | :heavy_minus_sign:             | An optional server URL to use. |

### Response

**[GetUserWebhooksResponse](../../models/operations/GetUserWebhooksResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## addUserWebhook

Add a webhook URL for the logged-in user.

### Example Usage

<!-- UsageSnippet language="java" operationID="addUserWebhook" method="post" path="/api/v2/user/webhooks" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.AddUserWebhookRequest;
import dev.plexapi.sdk.models.operations.AddUserWebhookResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        AddUserWebhookRequest req = AddUserWebhookRequest.builder()
                .build();

        AddUserWebhookResponse res = sdk.general().addUserWebhook()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                 | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `request`                                                                 | [AddUserWebhookRequest](../../models/operations/AddUserWebhookRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |
| `serverURL`                                                               | *String*                                                                  | :heavy_minus_sign:                                                        | An optional server URL to use.                                            |

### Response

**[AddUserWebhookResponse](../../models/operations/AddUserWebhookResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getClients

Get a list of connected Plex clients.

### Example Usage

<!-- UsageSnippet language="java" operationID="getClients" method="get" path="/clients" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetClientsRequest;
import dev.plexapi.sdk.models.operations.GetClientsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetClientsRequest req = GetClientsRequest.builder()
                .build();

        GetClientsResponse res = sdk.general().getClients()
                .request(req)
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                         | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `request`                                                         | [GetClientsRequest](../../models/operations/GetClientsRequest.md) | :heavy_check_mark:                                                | The request object to use for the request.                        |

### Response

**[GetClientsResponse](../../models/operations/GetClientsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getCloudServer

Get Plex Cloud server status for the logged-in user.

### Example Usage

<!-- UsageSnippet language="java" operationID="getCloudServer" method="get" path="/cloud_server" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetCloudServerRequest;
import dev.plexapi.sdk.models.operations.GetCloudServerResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetCloudServerRequest req = GetCloudServerRequest.builder()
                .build();

        GetCloudServerResponse res = sdk.general().getCloudServer()
                .request(req)
                .call();

        if (res.cloudServerResponse().isPresent()) {
            System.out.println(res.cloudServerResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                 | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `request`                                                                 | [GetCloudServerRequest](../../models/operations/GetCloudServerRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |
| `serverURL`                                                               | *String*                                                                  | :heavy_minus_sign:                                                        | An optional server URL to use.                                            |

### Response

**[GetCloudServerResponse](../../models/operations/GetCloudServerResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSystemDevices

Get a list of local system devices.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSystemDevices" method="get" path="/devices" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSystemDevicesRequest;
import dev.plexapi.sdk.models.operations.GetSystemDevicesResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetSystemDevicesRequest req = GetSystemDevicesRequest.builder()
                .build();

        GetSystemDevicesResponse res = sdk.general().getSystemDevices()
                .request(req)
                .call();

        if (res.mediaContainerWithDevice().isPresent()) {
            System.out.println(res.mediaContainerWithDevice().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [GetSystemDevicesRequest](../../models/operations/GetSystemDevicesRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[GetSystemDevicesResponse](../../models/operations/GetSystemDevicesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getDiagnostics

Get server diagnostics overview.

### Example Usage

<!-- UsageSnippet language="java" operationID="getDiagnostics" method="get" path="/diagnostics" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetDiagnosticsRequest;
import dev.plexapi.sdk.models.operations.GetDiagnosticsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetDiagnosticsRequest req = GetDiagnosticsRequest.builder()
                .build();

        GetDiagnosticsResponse res = sdk.general().getDiagnostics()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                 | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `request`                                                                 | [GetDiagnosticsRequest](../../models/operations/GetDiagnosticsRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[GetDiagnosticsResponse](../../models/operations/GetDiagnosticsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## downloadDatabaseDiagnostics

Download server database diagnostics bundle.

### Example Usage

<!-- UsageSnippet language="java" operationID="downloadDatabaseDiagnostics" method="get" path="/diagnostics/databases" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DownloadDatabaseDiagnosticsRequest;
import dev.plexapi.sdk.models.operations.DownloadDatabaseDiagnosticsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        DownloadDatabaseDiagnosticsRequest req = DownloadDatabaseDiagnosticsRequest.builder()
                .build();

        DownloadDatabaseDiagnosticsResponse res = sdk.general().downloadDatabaseDiagnostics()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                           | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `request`                                                                                           | [DownloadDatabaseDiagnosticsRequest](../../models/operations/DownloadDatabaseDiagnosticsRequest.md) | :heavy_check_mark:                                                                                  | The request object to use for the request.                                                          |

### Response

**[DownloadDatabaseDiagnosticsResponse](../../models/operations/DownloadDatabaseDiagnosticsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## downloadLogBundle

Download server logs bundle.

### Example Usage

<!-- UsageSnippet language="java" operationID="downloadLogBundle" method="get" path="/diagnostics/logs" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DownloadLogBundleRequest;
import dev.plexapi.sdk.models.operations.DownloadLogBundleResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        DownloadLogBundleRequest req = DownloadLogBundleRequest.builder()
                .build();

        DownloadLogBundleResponse res = sdk.general().downloadLogBundle()
                .request(req)
                .call();

        if (res.binaryResponse().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [DownloadLogBundleRequest](../../models/operations/DownloadLogBundleRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[DownloadLogBundleResponse](../../models/operations/DownloadLogBundleResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getGeoIP

Get GeoIP lookup information for the current request.

### Example Usage

<!-- UsageSnippet language="java" operationID="getGeoIP" method="get" path="/geoip" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetGeoIPRequest;
import dev.plexapi.sdk.models.operations.GetGeoIPResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetGeoIPRequest req = GetGeoIPRequest.builder()
                .build();

        GetGeoIPResponse res = sdk.general().getGeoIP()
                .request(req)
                .call();

        if (res.geoIPResponse().isPresent()) {
            System.out.println(res.geoIPResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                     | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `request`                                                     | [GetGeoIPRequest](../../models/operations/GetGeoIPRequest.md) | :heavy_check_mark:                                            | The request object to use for the request.                    |
| `serverURL`                                                   | *String*                                                      | :heavy_minus_sign:                                            | An optional server URL to use.                                |

### Response

**[GetGeoIPResponse](../../models/operations/GetGeoIPResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getIdentity

Get details about this PMS's identity

### Example Usage

<!-- UsageSnippet language="java" operationID="getIdentity" method="get" path="/identity" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetIdentityResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
            .build();

        GetIdentityResponse res = sdk.general().getIdentity()
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Response

**[GetIdentityResponse](../../models/operations/GetIdentityResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getIP

Get the public IP address detected by Plex.

### Example Usage

<!-- UsageSnippet language="java" operationID="getIP" method="get" path="/ip" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetIPRequest;
import dev.plexapi.sdk.models.operations.GetIPResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetIPRequest req = GetIPRequest.builder()
                .build();

        GetIPResponse res = sdk.general().getIP()
                .request(req)
                .call();

        if (res.ipResponse().isPresent()) {
            System.out.println(res.ipResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                               | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `request`                                               | [GetIPRequest](../../models/operations/GetIPRequest.md) | :heavy_check_mark:                                      | The request object to use for the request.              |
| `serverURL`                                             | *String*                                                | :heavy_minus_sign:                                      | An optional server URL to use.                          |

### Response

**[GetIPResponse](../../models/operations/GetIPResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## claimServer

Claim the local PMS server using a claim token obtained from plex.tv.

### Example Usage

<!-- UsageSnippet language="java" operationID="claimServer" method="post" path="/myplex/claim" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.ClaimServerRequest;
import dev.plexapi.sdk.models.operations.ClaimServerResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        ClaimServerRequest req = ClaimServerRequest.builder()
                .build();

        ClaimServerResponse res = sdk.general().claimServer()
                .request(req)
                .call();

        if (res.claimTokenResponse().isPresent()) {
            System.out.println(res.claimTokenResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [ClaimServerRequest](../../models/operations/ClaimServerRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[ClaimServerResponse](../../models/operations/ClaimServerResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## refreshReachability

Refresh remote access port mapping.

### Example Usage

<!-- UsageSnippet language="java" operationID="refreshReachability" method="put" path="/myplex/refreshReachability" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.RefreshReachabilityResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        RefreshReachabilityResponse res = sdk.general().refreshReachability()
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Response

**[RefreshReachabilityResponse](../../models/operations/RefreshReachabilityResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSourceConnectionInformation

If a caller requires connection details and a transient token for a source that is known to the server, for example a cloud media provider or shared PMS, then this endpoint can be called. This endpoint is only accessible with either an admin token or a valid transient token generated from an admin token.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSourceConnectionInformation" method="get" path="/security/resources" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.GetSourceConnectionInformationRequest;
import dev.plexapi.sdk.models.operations.GetSourceConnectionInformationResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import dev.plexapi.sdk.models.shared.BoolInt;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetSourceConnectionInformationRequest req = GetSourceConnectionInformationRequest.builder()
                .source("server://client-identifier")
                .refresh(BoolInt.True)
                .build();

        GetSourceConnectionInformationResponse res = sdk.general().getSourceConnectionInformation()
                .request(req)
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                                 | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `request`                                                                                                 | [GetSourceConnectionInformationRequest](../../models/operations/GetSourceConnectionInformationRequest.md) | :heavy_check_mark:                                                                                        | The request object to use for the request.                                                                |

### Response

**[GetSourceConnectionInformationResponse](../../models/operations/GetSourceConnectionInformationResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## createTransientToken

This endpoint provides the caller with a temporary token with the same access level as the caller's token. These tokens are valid for up to 48 hours and are destroyed if the server instance is restarted.
Note: This endpoint responds to all HTTP verbs but POST in preferred

### Example Usage

<!-- UsageSnippet language="java" operationID="createTransientToken" method="post" path="/security/token" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.*;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        CreateTransientTokenRequest req = CreateTransientTokenRequest.builder()
                .mediaType(QueryParamType.DELEGATION)
                .scope(Scope.ALL)
                .build();

        CreateTransientTokenResponse res = sdk.general().createTransientToken()
                .request(req)
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                                             | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `request`                                                                             | [CreateTransientTokenRequest](../../models/operations/CreateTransientTokenRequest.md) | :heavy_check_mark:                                                                    | The request object to use for the request.                                            |

### Response

**[CreateTransientTokenResponse](../../models/operations/CreateTransientTokenResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getLocalServers

Get a list of local servers.

### Example Usage

<!-- UsageSnippet language="java" operationID="getLocalServers" method="get" path="/servers" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetLocalServersRequest;
import dev.plexapi.sdk.models.operations.GetLocalServersResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetLocalServersRequest req = GetLocalServersRequest.builder()
                .build();

        GetLocalServersResponse res = sdk.general().getLocalServers()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetLocalServersRequest](../../models/operations/GetLocalServersRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[GetLocalServersResponse](../../models/operations/GetLocalServersResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## browseFilesystem

Browse filesystem paths accessible to the server.

### Example Usage

<!-- UsageSnippet language="java" operationID="browseFilesystem" method="get" path="/services/browse" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.BrowseFilesystemRequest;
import dev.plexapi.sdk.models.operations.BrowseFilesystemResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import dev.plexapi.sdk.models.shared.BoolInt;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        BrowseFilesystemRequest req = BrowseFilesystemRequest.builder()
                .includeFiles(BoolInt.True)
                .build();

        BrowseFilesystemResponse res = sdk.general().browseFilesystem()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [BrowseFilesystemRequest](../../models/operations/BrowseFilesystemRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[BrowseFilesystemResponse](../../models/operations/BrowseFilesystemResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getBandwidthStatistics

Get dashboard bandwidth data.

### Example Usage

<!-- UsageSnippet language="java" operationID="getBandwidthStatistics" method="get" path="/statistics/bandwidth" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetBandwidthStatisticsRequest;
import dev.plexapi.sdk.models.operations.GetBandwidthStatisticsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import dev.plexapi.sdk.models.shared.BoolInt;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetBandwidthStatisticsRequest req = GetBandwidthStatisticsRequest.builder()
                .timespan(4L)
                .lan(BoolInt.True)
                .build();

        GetBandwidthStatisticsResponse res = sdk.general().getBandwidthStatistics()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                 | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `request`                                                                                 | [GetBandwidthStatisticsRequest](../../models/operations/GetBandwidthStatisticsRequest.md) | :heavy_check_mark:                                                                        | The request object to use for the request.                                                |

### Response

**[GetBandwidthStatisticsResponse](../../models/operations/GetBandwidthStatisticsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getResourceStatistics

Get dashboard resource data.

### Example Usage

<!-- UsageSnippet language="java" operationID="getResourceStatistics" method="get" path="/statistics/resources" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetResourceStatisticsRequest;
import dev.plexapi.sdk.models.operations.GetResourceStatisticsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetResourceStatisticsRequest req = GetResourceStatisticsRequest.builder()
                .build();

        GetResourceStatisticsResponse res = sdk.general().getResourceStatistics()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                               | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `request`                                                                               | [GetResourceStatisticsRequest](../../models/operations/GetResourceStatisticsRequest.md) | :heavy_check_mark:                                                                      | The request object to use for the request.                                              |

### Response

**[GetResourceStatisticsResponse](../../models/operations/GetResourceStatisticsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSyncStatus

Get sync status overview.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSyncStatus" method="get" path="/sync" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSyncStatusRequest;
import dev.plexapi.sdk.models.operations.GetSyncStatusResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetSyncStatusRequest req = GetSyncStatusRequest.builder()
                .build();

        GetSyncStatusResponse res = sdk.general().getSyncStatus()
                .request(req)
                .call();

        if (res.mediaContainerWithStatus().isPresent()) {
            System.out.println(res.mediaContainerWithStatus().get());
        }
    }
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `request`                                                               | [GetSyncStatusRequest](../../models/operations/GetSyncStatusRequest.md) | :heavy_check_mark:                                                      | The request object to use for the request.                              |

### Response

**[GetSyncStatusResponse](../../models/operations/GetSyncStatusResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSyncItems

Get sync items list.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSyncItems" method="get" path="/sync/items" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSyncItemsRequest;
import dev.plexapi.sdk.models.operations.GetSyncItemsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetSyncItemsRequest req = GetSyncItemsRequest.builder()
                .build();

        GetSyncItemsResponse res = sdk.general().getSyncItems()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [GetSyncItemsRequest](../../models/operations/GetSyncItemsRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[GetSyncItemsResponse](../../models/operations/GetSyncItemsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSyncQueue

Get sync queue.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSyncQueue" method="get" path="/sync/queue" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSyncQueueRequest;
import dev.plexapi.sdk.models.operations.GetSyncQueueResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetSyncQueueRequest req = GetSyncQueueRequest.builder()
                .build();

        GetSyncQueueResponse res = sdk.general().getSyncQueue()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [GetSyncQueueRequest](../../models/operations/GetSyncQueueRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[GetSyncQueueResponse](../../models/operations/GetSyncQueueResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## refreshSyncContent

Force PMS to refresh content for known SyncLists.

### Example Usage

<!-- UsageSnippet language="java" operationID="refreshSyncContent" method="put" path="/sync/refreshContent" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.RefreshSyncContentRequest;
import dev.plexapi.sdk.models.operations.RefreshSyncContentResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        RefreshSyncContentRequest req = RefreshSyncContentRequest.builder()
                .build();

        RefreshSyncContentResponse res = sdk.general().refreshSyncContent()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [RefreshSyncContentRequest](../../models/operations/RefreshSyncContentRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[RefreshSyncContentResponse](../../models/operations/RefreshSyncContentResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## refreshSyncLists

Force PMS to download new SyncList from plex.tv.

### Example Usage

<!-- UsageSnippet language="java" operationID="refreshSyncLists" method="put" path="/sync/refreshSynclists" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.RefreshSyncListsRequest;
import dev.plexapi.sdk.models.operations.RefreshSyncListsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        RefreshSyncListsRequest req = RefreshSyncListsRequest.builder()
                .build();

        RefreshSyncListsResponse res = sdk.general().refreshSyncLists()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [RefreshSyncListsRequest](../../models/operations/RefreshSyncListsRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[RefreshSyncListsResponse](../../models/operations/RefreshSyncListsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSyncTranscodeQueue

Get sync transcode queue status.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSyncTranscodeQueue" method="get" path="/sync/transcodeQueue" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSyncTranscodeQueueRequest;
import dev.plexapi.sdk.models.operations.GetSyncTranscodeQueueResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetSyncTranscodeQueueRequest req = GetSyncTranscodeQueueRequest.builder()
                .build();

        GetSyncTranscodeQueueResponse res = sdk.general().getSyncTranscodeQueue()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                               | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `request`                                                                               | [GetSyncTranscodeQueueRequest](../../models/operations/GetSyncTranscodeQueueRequest.md) | :heavy_check_mark:                                                                      | The request object to use for the request.                                              |

### Response

**[GetSyncTranscodeQueueResponse](../../models/operations/GetSyncTranscodeQueueResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getMetadataAgents

Get a list of available metadata agents.

### Example Usage

<!-- UsageSnippet language="java" operationID="getMetadataAgents" method="get" path="/system/agents" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetMetadataAgentsRequest;
import dev.plexapi.sdk.models.operations.GetMetadataAgentsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetMetadataAgentsRequest req = GetMetadataAgentsRequest.builder()
                .build();

        GetMetadataAgentsResponse res = sdk.general().getMetadataAgents()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [GetMetadataAgentsRequest](../../models/operations/GetMetadataAgentsRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetMetadataAgentsResponse](../../models/operations/GetMetadataAgentsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSystemSettings

Get system-level settings.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSystemSettings" method="get" path="/system/settings" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSystemSettingsRequest;
import dev.plexapi.sdk.models.operations.GetSystemSettingsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetSystemSettingsRequest req = GetSystemSettingsRequest.builder()
                .build();

        GetSystemSettingsResponse res = sdk.general().getSystemSettings()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [GetSystemSettingsRequest](../../models/operations/GetSystemSettingsRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetSystemSettingsResponse](../../models/operations/GetSystemSettingsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## checkForSystemUpdates

Check for available PMS updates.

### Example Usage

<!-- UsageSnippet language="java" operationID="checkForSystemUpdates" method="get" path="/system/updates" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.CheckForSystemUpdatesRequest;
import dev.plexapi.sdk.models.operations.CheckForSystemUpdatesResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        CheckForSystemUpdatesRequest req = CheckForSystemUpdatesRequest.builder()
                .build();

        CheckForSystemUpdatesResponse res = sdk.general().checkForSystemUpdates()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                               | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `request`                                                                               | [CheckForSystemUpdatesRequest](../../models/operations/CheckForSystemUpdatesRequest.md) | :heavy_check_mark:                                                                      | The request object to use for the request.                                              |

### Response

**[CheckForSystemUpdatesResponse](../../models/operations/CheckForSystemUpdatesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getWebhooks

List configured webhook URLs for the logged-in user.

### Example Usage

<!-- UsageSnippet language="java" operationID="getWebhooks" method="get" path="/webhooks" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetWebhooksRequest;
import dev.plexapi.sdk.models.operations.GetWebhooksResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetWebhooksRequest req = GetWebhooksRequest.builder()
                .build();

        GetWebhooksResponse res = sdk.general().getWebhooks()
                .request(req)
                .call();

        if (res.webhookPayload().isPresent()) {
            System.out.println(res.webhookPayload().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [GetWebhooksRequest](../../models/operations/GetWebhooksRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |
| `serverURL`                                                         | *String*                                                            | :heavy_minus_sign:                                                  | An optional server URL to use.                                      |

### Response

**[GetWebhooksResponse](../../models/operations/GetWebhooksResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## addWebhook

Add a webhook URL for the logged-in user.

### Example Usage

<!-- UsageSnippet language="java" operationID="addWebhook" method="post" path="/webhooks" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.AddWebhookRequest;
import dev.plexapi.sdk.models.operations.AddWebhookResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        AddWebhookRequest req = AddWebhookRequest.builder()
                .build();

        AddWebhookResponse res = sdk.general().addWebhook()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                         | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `request`                                                         | [AddWebhookRequest](../../models/operations/AddWebhookRequest.md) | :heavy_check_mark:                                                | The request object to use for the request.                        |
| `serverURL`                                                       | *String*                                                          | :heavy_minus_sign:                                                | An optional server URL to use.                                    |

### Response

**[AddWebhookResponse](../../models/operations/AddWebhookResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getPlexDownloads

Get available Plex update downloads for a specific channel (e.g. `plexpass`, `public`).

### Example Usage

<!-- UsageSnippet language="java" operationID="getPlexDownloads" method="get" path="/downloads/{channel}.json" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetPlexDownloadsRequest;
import dev.plexapi.sdk.models.operations.GetPlexDownloadsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetPlexDownloadsRequest req = GetPlexDownloadsRequest.builder()
                .channel("<value>")
                .build();

        GetPlexDownloadsResponse res = sdk.general().getPlexDownloads()
                .request(req)
                .call();

        if (res.plexDownloadsResponse().isPresent()) {
            System.out.println(res.plexDownloadsResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [GetPlexDownloadsRequest](../../models/operations/GetPlexDownloadsRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |
| `serverURL`                                                                   | *String*                                                                      | :heavy_minus_sign:                                                            | An optional server URL to use.                                                |

### Response

**[GetPlexDownloadsResponse](../../models/operations/GetPlexDownloadsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## browseFilesystemPath

Browse a specific filesystem path.

### Example Usage

<!-- UsageSnippet language="java" operationID="browseFilesystemPath" method="get" path="/services/browse/{base64path}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.BrowseFilesystemPathRequest;
import dev.plexapi.sdk.models.operations.BrowseFilesystemPathResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        BrowseFilesystemPathRequest req = BrowseFilesystemPathRequest.builder()
                .base64path("<value>")
                .build();

        BrowseFilesystemPathResponse res = sdk.general().browseFilesystemPath()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                             | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `request`                                                                             | [BrowseFilesystemPathRequest](../../models/operations/BrowseFilesystemPathRequest.md) | :heavy_check_mark:                                                                    | The request object to use for the request.                                            |

### Response

**[BrowseFilesystemPathResponse](../../models/operations/BrowseFilesystemPathResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSyncItem

Get sync item details.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSyncItem" method="get" path="/sync/items/{syncId}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSyncItemRequest;
import dev.plexapi.sdk.models.operations.GetSyncItemResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetSyncItemRequest req = GetSyncItemRequest.builder()
                .syncId(761088L)
                .build();

        GetSyncItemResponse res = sdk.general().getSyncItem()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [GetSyncItemRequest](../../models/operations/GetSyncItemRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[GetSyncItemResponse](../../models/operations/GetSyncItemResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getMetadataAgentDetails

Get details and settings for a specific metadata agent.

### Example Usage

<!-- UsageSnippet language="java" operationID="getMetadataAgentDetails" method="get" path="/system/agents/{agentId}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetMetadataAgentDetailsRequest;
import dev.plexapi.sdk.models.operations.GetMetadataAgentDetailsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .product("Plex for Roku")
                .version("2.4.1")
                .platform("Roku")
                .platformVersion("4.3 build 1057")
                .device("Roku 3")
                .model("4200X")
                .deviceVendor("Roku")
                .deviceName("Living Room TV")
                .marketplace("googlePlay")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetMetadataAgentDetailsRequest req = GetMetadataAgentDetailsRequest.builder()
                .agentId("<id>")
                .build();

        GetMetadataAgentDetailsResponse res = sdk.general().getMetadataAgentDetails()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                   | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `request`                                                                                   | [GetMetadataAgentDetailsRequest](../../models/operations/GetMetadataAgentDetailsRequest.md) | :heavy_check_mark:                                                                          | The request object to use for the request.                                                  |

### Response

**[GetMetadataAgentDetailsResponse](../../models/operations/GetMetadataAgentDetailsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |