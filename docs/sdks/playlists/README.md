# Playlists

## Overview

Plex Playlists operations

### Available Operations

* [deletePlaylistByRatingKey](#deleteplaylistbyratingkey) - Delete Playlist

## deletePlaylistByRatingKey

Delete a playlist.

### Example Usage

<!-- UsageSnippet language="java" operationID="deletePlaylistByRatingKey" method="delete" path="/playlists" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DeletePlaylistByRatingKeyRequest;
import dev.plexapi.sdk.models.operations.DeletePlaylistByRatingKeyResponse;
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

        DeletePlaylistByRatingKeyRequest req = DeletePlaylistByRatingKeyRequest.builder()
                .ratingKey(499749L)
                .build();

        DeletePlaylistByRatingKeyResponse res = sdk.playlists().deletePlaylistByRatingKey()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                       | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `request`                                                                                       | [DeletePlaylistByRatingKeyRequest](../../models/operations/DeletePlaylistByRatingKeyRequest.md) | :heavy_check_mark:                                                                              | The request object to use for the request.                                                      |

### Response

**[DeletePlaylistByRatingKeyResponse](../../models/operations/DeletePlaylistByRatingKeyResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |