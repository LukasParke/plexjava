# LibraryCollections

## Overview

Endpoints for manipulating collections.  In addition to these endpoints, `/library/collections/:collectionId/X` will be rerouted to `/library/metadata/:collectionId/X` and respond to those endpoints as well.

### Available Operations

* [addCollectionItems](#addcollectionitems) - Add items to a collection
* [updateCollectionItem](#updatecollectionitem) - Update an item in a collection
* [moveCollectionItem](#movecollectionitem) - Reorder an item in the collection

## addCollectionItems

Add items to a collection by uri

### Example Usage

<!-- UsageSnippet language="java" operationID="addCollectionItems" method="put" path="/library/collections/{collectionId}/items" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.AddCollectionItemsRequest;
import dev.plexapi.sdk.models.operations.AddCollectionItemsResponse;
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

        AddCollectionItemsRequest req = AddCollectionItemsRequest.builder()
                .collectionId(338144L)
                .uri("https://expensive-bakeware.com")
                .build();

        AddCollectionItemsResponse res = sdk.libraryCollections().addCollectionItems()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [AddCollectionItemsRequest](../../models/operations/AddCollectionItemsRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[AddCollectionItemsResponse](../../models/operations/AddCollectionItemsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## updateCollectionItem

Delete an item from a collection

### Example Usage

<!-- UsageSnippet language="java" operationID="updateCollectionItem" method="put" path="/library/collections/{collectionId}/items/{itemId}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.UpdateCollectionItemRequest;
import dev.plexapi.sdk.models.operations.UpdateCollectionItemResponse;
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

        UpdateCollectionItemRequest req = UpdateCollectionItemRequest.builder()
                .collectionId(640014L)
                .itemId(2136L)
                .build();

        UpdateCollectionItemResponse res = sdk.libraryCollections().updateCollectionItem()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                             | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `request`                                                                             | [UpdateCollectionItemRequest](../../models/operations/UpdateCollectionItemRequest.md) | :heavy_check_mark:                                                                    | The request object to use for the request.                                            |

### Response

**[UpdateCollectionItemResponse](../../models/operations/UpdateCollectionItemResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## moveCollectionItem

Reorder items in a collection with one item after another

### Example Usage

<!-- UsageSnippet language="java" operationID="moveCollectionItem" method="put" path="/library/collections/{collectionId}/items/{itemId}/move" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.MoveCollectionItemRequest;
import dev.plexapi.sdk.models.operations.MoveCollectionItemResponse;
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

        MoveCollectionItemRequest req = MoveCollectionItemRequest.builder()
                .collectionId(239532L)
                .itemId(513864L)
                .build();

        MoveCollectionItemResponse res = sdk.libraryCollections().moveCollectionItem()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [MoveCollectionItemRequest](../../models/operations/MoveCollectionItemRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[MoveCollectionItemResponse](../../models/operations/MoveCollectionItemResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |