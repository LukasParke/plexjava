# Plex

## Overview

Plex Plex operations

### Available Operations

* [getServerResources](#getserverresources) - Get Server Resources

## getServerResources

Get Plex server access tokens and server connections

### Example Usage

<!-- UsageSnippet language="java" operationID="getServerResources" method="get" path="/resources" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Unauthorized;
import dev.plexapi.sdk.models.operations.*;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Unauthorized, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .accepts(Accepts.APPLICATION_XML)
                .clientIdentifier("abc123")
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetServerResourcesRequest req = GetServerResourcesRequest.builder()
                .includeHttps(IncludeHttps.True)
                .includeRelay(IncludeRelay.True)
                .includeIPv6(IncludeIPv6.True)
                .build();

        GetServerResourcesResponse res = sdk.plex().getServerResources()
                .request(req)
                .call();

        if (res.plexDevices().isPresent()) {
            System.out.println(res.plexDevices().get());
        }
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [GetServerResourcesRequest](../../models/operations/GetServerResourcesRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |
| `serverURL`                                                                       | *String*                                                                          | :heavy_minus_sign:                                                                | An optional server URL to use.                                                    |

### Response

**[GetServerResourcesResponse](../../models/operations/GetServerResourcesResponse.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models/errors/Unauthorized | 401                        | application/json           |
| models/errors/SDKError     | 4XX, 5XX                   | \*/\*                      |