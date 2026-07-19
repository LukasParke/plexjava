# Library

## Overview

Library endpoints which are outside of the Media Provider API.  Typically this is manipulation of the library (adding/removing sections, modifying preferences, etc).

### Available Operations

* [getRootLibrary](#getrootlibrary) - Get Root Library
* [getLibraryItems](#getlibraryitems) - Get all items in library
* [deleteCaches](#deletecaches) - Delete library caches
* [cleanBundles](#cleanbundles) - Clean bundles
* [ingestTransientItem](#ingesttransientitem) - Ingest a transient item
* [getLibraryMatches](#getlibrarymatches) - Get library matches
* [optimizeLibrary](#optimizelibrary) - Get Optimize Library
* [optimizeLibraryPost](#optimizelibrarypost) - Optimize Library
* [optimizeDatabase](#optimizedatabase) - Optimize the Database
* [getRandomArtwork](#getrandomartwork) - Get random artwork
* [getRecentlyAddedGlobal](#getrecentlyaddedglobal) - Get Global Recently Added
* [getLibrarySectionsFallback](#getlibrarysectionsfallback) - Get Library Sections (Fallback)
* [getSections](#getsections) - Get library sections (main Media Provider Only)
* [addSection](#addsection) - Add a library section
* [stopAllRefreshes](#stopallrefreshes) - Stop refresh
* [getSectionsPrefs](#getsectionsprefs) - Get section prefs
* [refreshSectionsMetadata](#refreshsectionsmetadata) - Refresh all sections
* [getTags](#gettags) - Get all library tags of a type
* [uploadArt](#uploadart) - Upload media art Art
* [getMetadataChildren](#getmetadatachildren) - Get Metadata Children
* [computeSonicPath](#computesonicpath) - Compute Sonic Path
* [getMetadataGrandchildren](#getmetadatagrandchildren) - Get Metadata Grandchildren
* [getMetadataGrandparent](#getmetadatagrandparent) - Get Metadata Grandparent
* [getNearestMetadata](#getnearestmetadata) - Get Nearest Metadata
* [getMetadataOnDeck](#getmetadataondeck) - Get Metadata On Deck
* [getMetadataParent](#getmetadataparent) - Get Metadata Parent
* [uploadPoster](#uploadposter) - Upload media art Poster
* [getMetadataReviews](#getmetadatareviews) - Get Metadata Reviews
* [deleteMetadataItem](#deletemetadataitem) - Delete a metadata item
* [editMetadataItem](#editmetadataitem) - Edit a metadata item
* [detectAds](#detectads) - Ad-detect an item
* [getAllItemLeaves](#getallitemleaves) - Get the leaves of an item
* [analyzeMetadata](#analyzemetadata) - Analyze an item
* [generateThumbs](#generatethumbs) - Generate thumbs of chapters for an item
* [detectCredits](#detectcredits) - Credit detect a metadata item
* [getExtras](#getextras) - Get an item's extras
* [addExtras](#addextras) - Add to an item's extras
* [getFile](#getfile) - Get a file from a metadata or media bundle
* [startBifGeneration](#startbifgeneration) - Start BIF generation of an item
* [detectIntros](#detectintros) - Intro detect an item
* [createMarker](#createmarker) - Create a marker
* [matchItem](#matchitem) - Match a metadata item
* [listMatches](#listmatches) - Get metadata matches for an item
* [mergeItems](#mergeitems) - Merge a metadata item
* [setItemPreferences](#setitempreferences) - Set metadata preferences
* [refreshItemsMetadata](#refreshitemsmetadata) - Refresh a metadata item
* [getRelatedItems](#getrelateditems) - Get related items
* [listSimilar](#listsimilar) - Get similar items
* [splitItem](#splititem) - Split a metadata item
* [getSubtitles](#getsubtitles) - Get subtitles
* [getItemTree](#getitemtree) - Get metadata items as a tree
* [unmatch](#unmatch) - Unmatch a metadata item
* [listTopUsers](#listtopusers) - Get metadata top users
* [detectVoiceActivity](#detectvoiceactivity) - Detect voice activity
* [getAugmentationStatus](#getaugmentationstatus) - Get augmentation status
* [setStreamSelection](#setstreamselection) - Set stream selection
* [getPerson](#getperson) - Get person details
* [listPersonMedia](#listpersonmedia) - Get media for a person
* [deleteLibrarySection](#deletelibrarysection) - Delete a library section
* [getLibraryDetails](#getlibrarydetails) - Get a library section by id
* [editSection](#editsection) - Edit a library section
* [getSectionAgents](#getsectionagents) - Get Section Agents
* [updateItems](#updateitems) - Set the fields of the filtered items
* [startAnalysis](#startanalysis) - Analyze a section
* [getSectionArtists](#getsectionartists) - Get Section Artists
* [autocomplete](#autocomplete) - Get autocompletions for search
* [getByContentRating](#getbycontentrating) - Get By Content Rating
* [getByDecade](#getbydecade) - Get By Decade
* [getByFolder](#getbyfolder) - Get By Folder
* [getByResolution](#getbyresolution) - Get By Resolution
* [getByYear](#getbyyear) - Get By Year
* [getSectionClips](#getsectionclips) - Get Section Clips
* [getCollections](#getcollections) - Get collections in a section
* [getCommon](#getcommon) - Get common fields for items
* [getSectionEdit](#getsectionedit) - Edit Section
* [editLibrarySection](#editlibrarysection) - Edit Section
* [emptyTrash](#emptytrash) - Get Empty Trash
* [emptyTrashPost](#emptytrashpost) - Empty Trash
* [emptyTrashPut](#emptytrashput) - Empty section trash
* [getSectionEpisodes](#getsectionepisodes) - Get Section Episodes
* [getSectionFilters](#getsectionfilters) - Get section filters
* [getFirstCharacters](#getfirstcharacters) - Get list of first characters
* [getLibrarySectionHubs](#getlibrarysectionhubs) - Get Section Hubs
* [deleteIndexes](#deleteindexes) - Delete section indexes
* [deleteIntros](#deleteintros) - Delete section intro markers
* [getSectionLabels](#getsectionlabels) - Get Section Labels
* [matchSectionItems](#matchsectionitems) - Match Section Items
* [moveSection](#movesection) - Move Section
* [getSectionMovies](#getsectionmovies) - Get Section Movies
* [getNewestForSection](#getnewestforsection) - Get Newest for Section
* [getOnDeckForSection](#getondeckforsection) - Get On Deck for Section
* [optimizeSection](#optimizesection) - Get Optimize Section
* [optimizeSectionPost](#optimizesectionpost) - Optimize Section
* [getSectionPhotos](#getsectionphotos) - Get Section Photos
* [getSectionPlaylists](#getsectionplaylists) - Get Section Playlists
* [getSectionPreferences](#getsectionpreferences) - Get section prefs
* [setSectionPreferences](#setsectionpreferences) - Set section prefs
* [getRecentlyAddedForSection](#getrecentlyaddedforsection) - Get Recently Added for Section
* [cancelRefresh](#cancelrefresh) - Cancel section refresh
* [refreshSection](#refreshsection) - Get Refresh Section
* [refreshSectionPost](#refreshsectionpost) - Refresh Section
* [searchSection](#searchsection) - Search Section
* [getSectionSettings](#getsectionsettings) - Get Section Settings
* [getSectionShows](#getsectionshows) - Get Section Shows
* [getAvailableSorts](#getavailablesorts) - Get a section sorts
* [getSectionTags](#getsectiontags) - Get Section Tags
* [getSectionTimeline](#getsectiontimeline) - Get Section Timeline
* [unmatchSectionItems](#unmatchsectionitems) - Unmatch Section Items
* [getUnwatchedForSection](#getunwatchedforsection) - Get Unwatched for Section
* [getStreamLevels](#getstreamlevels) - Get loudness about a stream in json
* [getStreamLoudness](#getstreamloudness) - Get loudness about a stream
* [getChapterImage](#getchapterimage) - Get a chapter image
* [setItemArtwork](#setitemartwork) - Set an item's artwork, theme, etc
* [updateItemArtwork](#updateitemartwork) - Set an item's artwork, theme, etc
* [deleteMarker](#deletemarker) - Delete a marker
* [editMarker](#editmarker) - Edit a marker
* [deleteMediaItem](#deletemediaitem) - Delete a media item
* [getPartIndex](#getpartindex) - Get BIF index for a part
* [deleteCollection](#deletecollection) - Delete a collection
* [getSectionImage](#getsectionimage) - Get a section composite image
* [deleteStream](#deletestream) - Delete a stream
* [getStream](#getstream) - Get a stream
* [setStreamOffset](#setstreamoffset) - Set a stream offset
* [getItemArtwork](#getitemartwork) - Get an item's artwork, theme, etc
* [getMediaPart](#getmediapart) - Get a media part
* [getImageFromBif](#getimagefrombif) - Get an image from part BIF

## getRootLibrary

Get the root library object.

### Example Usage

<!-- UsageSnippet language="java" operationID="getRootLibrary" method="get" path="/library" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetRootLibraryResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetRootLibraryResponse res = sdk.library().getRootLibrary()
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Response

**[GetRootLibraryResponse](../../models/operations/GetRootLibraryResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getLibraryItems

Request all metadata items according to a query.

### Example Usage

<!-- UsageSnippet language="java" operationID="getLibraryItems" method="get" path="/library/all" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetLibraryItemsRequest;
import dev.plexapi.sdk.models.operations.GetLibraryItemsResponse;
import dev.plexapi.sdk.models.shared.*;
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

        GetLibraryItemsRequest req = GetLibraryItemsRequest.builder()
                .mediaQuery(MediaQuery.builder()
                    .type(MediaType.Episode)
                    .sort("duration:desc,index")
                    .sourceType(2L)
                    .build())
                .build();

        GetLibraryItemsResponse res = sdk.library().getLibraryItems()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetLibraryItemsRequest](../../models/operations/GetLibraryItemsRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[GetLibraryItemsResponse](../../models/operations/GetLibraryItemsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## deleteCaches

Delete the hub caches so they are recomputed on next request

### Example Usage

<!-- UsageSnippet language="java" operationID="deleteCaches" method="delete" path="/library/caches" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DeleteCachesResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        DeleteCachesResponse res = sdk.library().deleteCaches()
                .call();

        // handle response
    }
}
```

### Response

**[DeleteCachesResponse](../../models/operations/DeleteCachesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## cleanBundles

Clean out any now unused bundles. Bundles can become unused when media is deleted

### Example Usage

<!-- UsageSnippet language="java" operationID="cleanBundles" method="put" path="/library/clean/bundles" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.CleanBundlesResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        CleanBundlesResponse res = sdk.library().cleanBundles()
                .call();

        // handle response
    }
}
```

### Response

**[CleanBundlesResponse](../../models/operations/CleanBundlesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## ingestTransientItem

This endpoint takes a file path specified in the `url` parameter, matches it using the scanner's match mechanism, downloads rich metadata, and then ingests the item as a transient item (without a library section). In the case where the file represents an episode, the entire tree (show, season, and episode) is added as transient items. At this time, movies and episodes are the only supported types, which are gleaned automatically from the file path.
Note that any of the parameters passed to the metadata details endpoint (e.g. `includeExtras=1`) work here.

### Example Usage

<!-- UsageSnippet language="java" operationID="ingestTransientItem" method="post" path="/library/file" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.IngestTransientItemRequest;
import dev.plexapi.sdk.models.operations.IngestTransientItemResponse;
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

        IngestTransientItemRequest req = IngestTransientItemRequest.builder()
                .url("file:///storage%2Femulated%2F0%2FArcher-S01E01.mkv")
                .virtualFilePath("/Avatar.mkv")
                .computeHashes(BoolInt.True)
                .ingestNonMatches(BoolInt.True)
                .build();

        IngestTransientItemResponse res = sdk.library().ingestTransientItem()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [IngestTransientItemRequest](../../models/operations/IngestTransientItemRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[IngestTransientItemResponse](../../models/operations/IngestTransientItemResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getLibraryMatches

The matches endpoint is used to match content external to the library with content inside the library. This is done by passing a series of semantic "hints" about the content (its type, name, or release year). Each type (e.g. movie) has a canonical set of minimal required hints.
This ability to match content is useful in a variety of scenarios. For example, in the DVR, the EPG uses the endpoint to match recording rules against airing content. And in the cloud, the UMP uses the endpoint to match up a piece of media with rich metadata.
The endpoint response can including multiple matches, if there is ambiguity, each one containing a `score` from 0 to 100. For somewhat historical reasons, anything over 85 is considered a positive match (we prefer false negatives over false positives in general for matching).
The `guid` hint is somewhat special, in that it generally represents a unique identity for a piece of media (e.g. the IMDB `ttXXX`) identifier, in contrast with other hints which can be much more ambiguous (e.g. a title of `Jane Eyre`, which could refer to the 1943 or the 2011 version).
Episodes require either a season/episode pair, or an air date (or both). Either the path must be sent, or the show title

### Example Usage

<!-- UsageSnippet language="java" operationID="getLibraryMatches" method="get" path="/library/matches" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetLibraryMatchesRequest;
import dev.plexapi.sdk.models.operations.GetLibraryMatchesResponse;
import dev.plexapi.sdk.models.shared.*;
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

        GetLibraryMatchesRequest req = GetLibraryMatchesRequest.builder()
                .type(MediaType.TvShow)
                .includeFullMetadata(BoolInt.True)
                .includeAncestorMetadata(BoolInt.True)
                .includeAlternateMetadataSources(BoolInt.True)
                .build();

        GetLibraryMatchesResponse res = sdk.library().getLibraryMatches()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [GetLibraryMatchesRequest](../../models/operations/GetLibraryMatchesRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetLibraryMatchesResponse](../../models/operations/GetLibraryMatchesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## optimizeLibrary

Optimize the database globally across all library sections.

### Example Usage

<!-- UsageSnippet language="java" operationID="optimizeLibrary" method="get" path="/library/optimize" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.OptimizeLibraryRequest;
import dev.plexapi.sdk.models.operations.OptimizeLibraryResponse;
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

        OptimizeLibraryRequest req = OptimizeLibraryRequest.builder()
                .build();

        OptimizeLibraryResponse res = sdk.library().optimizeLibrary()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [OptimizeLibraryRequest](../../models/operations/OptimizeLibraryRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[OptimizeLibraryResponse](../../models/operations/OptimizeLibraryResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## optimizeLibraryPost

Optimize the database globally across all library sections.

### Example Usage

<!-- UsageSnippet language="java" operationID="optimizeLibraryPost" method="post" path="/library/optimize" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.OptimizeLibraryPostRequest;
import dev.plexapi.sdk.models.operations.OptimizeLibraryPostResponse;
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

        OptimizeLibraryPostRequest req = OptimizeLibraryPostRequest.builder()
                .build();

        OptimizeLibraryPostResponse res = sdk.library().optimizeLibraryPost()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [OptimizeLibraryPostRequest](../../models/operations/OptimizeLibraryPostRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[OptimizeLibraryPostResponse](../../models/operations/OptimizeLibraryPostResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## optimizeDatabase

Initiate optimize on the database.

### Example Usage

<!-- UsageSnippet language="java" operationID="optimizeDatabase" method="put" path="/library/optimize" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.OptimizeDatabaseRequest;
import dev.plexapi.sdk.models.operations.OptimizeDatabaseResponse;
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

        OptimizeDatabaseRequest req = OptimizeDatabaseRequest.builder()
                .async(BoolInt.True)
                .build();

        OptimizeDatabaseResponse res = sdk.library().optimizeDatabase()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [OptimizeDatabaseRequest](../../models/operations/OptimizeDatabaseRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[OptimizeDatabaseResponse](../../models/operations/OptimizeDatabaseResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getRandomArtwork

Get random artwork across sections.  This is commonly used for a screensaver.

This retrieves 100 random artwork paths in the specified sections and returns them.  Restrictions are put in place to not return artwork for items the user is not allowed to access.  Artwork will be for Movies, Shows, and Artists only.

### Example Usage

<!-- UsageSnippet language="java" operationID="getRandomArtwork" method="get" path="/library/randomArtwork" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetRandomArtworkRequest;
import dev.plexapi.sdk.models.operations.GetRandomArtworkResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;
import java.util.List;

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

        GetRandomArtworkRequest req = GetRandomArtworkRequest.builder()
                .sections(List.of(
                    5L,
                    6L))
                .build();

        GetRandomArtworkResponse res = sdk.library().getRandomArtwork()
                .request(req)
                .call();

        if (res.mediaContainerWithArtwork().isPresent()) {
            System.out.println(res.mediaContainerWithArtwork().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [GetRandomArtworkRequest](../../models/operations/GetRandomArtworkRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[GetRandomArtworkResponse](../../models/operations/GetRandomArtworkResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getRecentlyAddedGlobal

Get recently added items across all library sections.

### Example Usage

<!-- UsageSnippet language="java" operationID="getRecentlyAddedGlobal" method="get" path="/library/recentlyAdded" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetRecentlyAddedGlobalRequest;
import dev.plexapi.sdk.models.operations.GetRecentlyAddedGlobalResponse;
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

        GetRecentlyAddedGlobalRequest req = GetRecentlyAddedGlobalRequest.builder()
                .build();

        GetRecentlyAddedGlobalResponse res = sdk.library().getRecentlyAddedGlobal()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                 | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `request`                                                                                 | [GetRecentlyAddedGlobalRequest](../../models/operations/GetRecentlyAddedGlobalRequest.md) | :heavy_check_mark:                                                                        | The request object to use for the request.                                                |

### Response

**[GetRecentlyAddedGlobalResponse](../../models/operations/GetRecentlyAddedGlobalResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getLibrarySectionsFallback

Fallback for non-owners to list library sections.

### Example Usage

<!-- UsageSnippet language="java" operationID="getLibrarySectionsFallback" method="get" path="/library/sections/" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetLibrarySectionsFallbackResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetLibrarySectionsFallbackResponse res = sdk.library().getLibrarySectionsFallback()
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Response

**[GetLibrarySectionsFallbackResponse](../../models/operations/GetLibrarySectionsFallbackResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSections

A library section (commonly referred to as just a library) is a collection of media. Libraries are typed, and depending on their type provide either a flat or a hierarchical view of the media. For example, a music library has an artist > albums > tracks structure, whereas a movie library is flat.
Libraries have features beyond just being a collection of media; for starters, they include information about supported types, filters and sorts. This allows a client to provide a rich interface around the media (e.g. allow sorting movies by release year).

### Example Usage

<!-- UsageSnippet language="java" operationID="getSections" method="get" path="/library/sections/all" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionsResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetSectionsResponse res = sdk.library().getSections()
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Response

**[GetSectionsResponse](../../models/operations/GetSectionsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## addSection

Add a new library section to the server

### Example Usage

<!-- UsageSnippet language="java" operationID="addSection" method="post" path="/library/sections/all" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.*;
import dev.plexapi.sdk.models.shared.Accepts;
import dev.plexapi.sdk.models.shared.BoolInt;
import java.lang.Exception;
import java.util.List;

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

        AddSectionRequest req = AddSectionRequest.builder()
                .name("<value>")
                .mediaType(39544L)
                .agent("<value>")
                .language("<value>")
                .locations(List.of(
                    "O:\\fatboy\\Media\\Ripped\\Music",
                    "O:\\fatboy\\Media\\My Music"))
                .prefs(QueryParamPrefs.builder()
                    .build())
                .relative(BoolInt.True)
                .importFromiTunes(BoolInt.True)
                .build();

        AddSectionResponse res = sdk.library().addSection()
                .request(req)
                .call();

        if (res.slashGetResponses200().isPresent()) {
            System.out.println(res.slashGetResponses200().get());
        }
    }
}
```

### Parameters

| Parameter                                                         | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `request`                                                         | [AddSectionRequest](../../models/operations/AddSectionRequest.md) | :heavy_check_mark:                                                | The request object to use for the request.                        |

### Response

**[AddSectionResponse](../../models/operations/AddSectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## stopAllRefreshes

Stop all refreshes across all sections

### Example Usage

<!-- UsageSnippet language="java" operationID="stopAllRefreshes" method="delete" path="/library/sections/all/refresh" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.StopAllRefreshesResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        StopAllRefreshesResponse res = sdk.library().stopAllRefreshes()
                .call();

        if (res.librarySections().isPresent()) {
            System.out.println(res.librarySections().get());
        }
    }
}
```

### Response

**[StopAllRefreshesResponse](../../models/operations/StopAllRefreshesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionsPrefs

Get a section's preferences for a metadata type

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionsPrefs" method="get" path="/library/sections/prefs" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.GetSectionsPrefsRequest;
import dev.plexapi.sdk.models.operations.GetSectionsPrefsResponse;
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

        GetSectionsPrefsRequest req = GetSectionsPrefsRequest.builder()
                .mediaType(460221L)
                .build();

        GetSectionsPrefsResponse res = sdk.library().getSectionsPrefs()
                .request(req)
                .call();

        if (res.librarySections().isPresent()) {
            System.out.println(res.librarySections().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [GetSectionsPrefsRequest](../../models/operations/GetSectionsPrefsRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[GetSectionsPrefsResponse](../../models/operations/GetSectionsPrefsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## refreshSectionsMetadata

Tell PMS to refresh all section metadata

### Example Usage

<!-- UsageSnippet language="java" operationID="refreshSectionsMetadata" method="post" path="/library/sections/refresh" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.RefreshSectionsMetadataRequest;
import dev.plexapi.sdk.models.operations.RefreshSectionsMetadataResponse;
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

        RefreshSectionsMetadataRequest req = RefreshSectionsMetadataRequest.builder()
                .build();

        RefreshSectionsMetadataResponse res = sdk.library().refreshSectionsMetadata()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                                   | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `request`                                                                                   | [RefreshSectionsMetadataRequest](../../models/operations/RefreshSectionsMetadataRequest.md) | :heavy_check_mark:                                                                          | The request object to use for the request.                                                  |

### Response

**[RefreshSectionsMetadataResponse](../../models/operations/RefreshSectionsMetadataResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getTags

Get all library tags of a type

### Example Usage

<!-- UsageSnippet language="java" operationID="getTags" method="get" path="/library/tags" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetTagsRequest;
import dev.plexapi.sdk.models.operations.GetTagsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import dev.plexapi.sdk.models.shared.MediaType;
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

        GetTagsRequest req = GetTagsRequest.builder()
                .type(MediaType.TvShow)
                .build();

        GetTagsResponse res = sdk.library().getTags()
                .request(req)
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                   | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `request`                                                   | [GetTagsRequest](../../models/operations/GetTagsRequest.md) | :heavy_check_mark:                                          | The request object to use for the request.                  |

### Response

**[GetTagsResponse](../../models/operations/GetTagsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## uploadArt

Upload custom background art for a metadata item.

### Example Usage

<!-- UsageSnippet language="java" operationID="uploadArt" method="post" path="/library/metadata/{id}/arts" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.*;
import dev.plexapi.sdk.models.shared.Accepts;
import dev.plexapi.sdk.utils.Utils;
import java.io.FileInputStream;
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

        UploadArtRequest req = UploadArtRequest.builder()
                .id(996758L)
                .requestBody(UploadArtRequestBody.builder()
                    .file(File.builder()
                        .fileName("example.file")
                        .content(Utils.readBytesAndClose(new FileInputStream("example.file")))
                        .build())
                    .build())
                .build();

        UploadArtResponse res = sdk.library().uploadArt()
                .request(req)
                .call();

    }
}
```

### Parameters

| Parameter                                                       | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `request`                                                       | [UploadArtRequest](../../models/operations/UploadArtRequest.md) | :heavy_check_mark:                                              | The request object to use for the request.                      |

### Response

**[UploadArtResponse](../../models/operations/UploadArtResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getMetadataChildren

Get children of a show, season, artist, or album.

### Example Usage: include-stream

<!-- UsageSnippet language="java" operationID="getMetadataChildren" method="get" path="/library/metadata/{id}/children" example="include-stream" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetMetadataChildrenRequest;
import dev.plexapi.sdk.models.operations.GetMetadataChildrenResponse;
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

        GetMetadataChildrenRequest req = GetMetadataChildrenRequest.builder()
                .id(240367L)
                .build();

        GetMetadataChildrenResponse res = sdk.library().getMetadataChildren()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```
### Example Usage: include-stream-otheritem

<!-- UsageSnippet language="java" operationID="getMetadataChildren" method="get" path="/library/metadata/{id}/children" example="include-stream-otheritem" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetMetadataChildrenRequest;
import dev.plexapi.sdk.models.operations.GetMetadataChildrenResponse;
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

        GetMetadataChildrenRequest req = GetMetadataChildrenRequest.builder()
                .id(240367L)
                .build();

        GetMetadataChildrenResponse res = sdk.library().getMetadataChildren()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```
### Example Usage: include-stream-otheritem-anotheritem

<!-- UsageSnippet language="java" operationID="getMetadataChildren" method="get" path="/library/metadata/{id}/children" example="include-stream-otheritem-anotheritem" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetMetadataChildrenRequest;
import dev.plexapi.sdk.models.operations.GetMetadataChildrenResponse;
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

        GetMetadataChildrenRequest req = GetMetadataChildrenRequest.builder()
                .id(240367L)
                .build();

        GetMetadataChildrenResponse res = sdk.library().getMetadataChildren()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [GetMetadataChildrenRequest](../../models/operations/GetMetadataChildrenRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[GetMetadataChildrenResponse](../../models/operations/GetMetadataChildrenResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## computeSonicPath

Compute a sonic adventure path from a starting track.

### Example Usage

<!-- UsageSnippet language="java" operationID="computeSonicPath" method="get" path="/library/metadata/{id}/computePath" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.ComputeSonicPathRequest;
import dev.plexapi.sdk.models.operations.ComputeSonicPathResponse;
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

        ComputeSonicPathRequest req = ComputeSonicPathRequest.builder()
                .id(622554L)
                .build();

        ComputeSonicPathResponse res = sdk.library().computeSonicPath()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [ComputeSonicPathRequest](../../models/operations/ComputeSonicPathRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[ComputeSonicPathResponse](../../models/operations/ComputeSonicPathResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getMetadataGrandchildren

Get grandchildren (e.g. episodes under a show).

### Example Usage

<!-- UsageSnippet language="java" operationID="getMetadataGrandchildren" method="get" path="/library/metadata/{id}/grandchildren" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetMetadataGrandchildrenRequest;
import dev.plexapi.sdk.models.operations.GetMetadataGrandchildrenResponse;
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

        GetMetadataGrandchildrenRequest req = GetMetadataGrandchildrenRequest.builder()
                .id(679910L)
                .build();

        GetMetadataGrandchildrenResponse res = sdk.library().getMetadataGrandchildren()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                     | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `request`                                                                                     | [GetMetadataGrandchildrenRequest](../../models/operations/GetMetadataGrandchildrenRequest.md) | :heavy_check_mark:                                                                            | The request object to use for the request.                                                    |

### Response

**[GetMetadataGrandchildrenResponse](../../models/operations/GetMetadataGrandchildrenResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getMetadataGrandparent

Get grandparent metadata shortcut.

### Example Usage

<!-- UsageSnippet language="java" operationID="getMetadataGrandparent" method="get" path="/library/metadata/{id}/grandparent" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetMetadataGrandparentRequest;
import dev.plexapi.sdk.models.operations.GetMetadataGrandparentResponse;
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

        GetMetadataGrandparentRequest req = GetMetadataGrandparentRequest.builder()
                .id(191152L)
                .build();

        GetMetadataGrandparentResponse res = sdk.library().getMetadataGrandparent()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                 | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `request`                                                                                 | [GetMetadataGrandparentRequest](../../models/operations/GetMetadataGrandparentRequest.md) | :heavy_check_mark:                                                                        | The request object to use for the request.                                                |

### Response

**[GetMetadataGrandparentResponse](../../models/operations/GetMetadataGrandparentResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getNearestMetadata

Get sonically similar items for a music track.

### Example Usage

<!-- UsageSnippet language="java" operationID="getNearestMetadata" method="get" path="/library/metadata/{id}/nearest" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetNearestMetadataRequest;
import dev.plexapi.sdk.models.operations.GetNearestMetadataResponse;
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

        GetNearestMetadataRequest req = GetNearestMetadataRequest.builder()
                .id(62697L)
                .build();

        GetNearestMetadataResponse res = sdk.library().getNearestMetadata()
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
| `request`                                                                         | [GetNearestMetadataRequest](../../models/operations/GetNearestMetadataRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[GetNearestMetadataResponse](../../models/operations/GetNearestMetadataResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getMetadataOnDeck

Get On Deck status for a show or season.

### Example Usage

<!-- UsageSnippet language="java" operationID="getMetadataOnDeck" method="get" path="/library/metadata/{id}/onDeck" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetMetadataOnDeckRequest;
import dev.plexapi.sdk.models.operations.GetMetadataOnDeckResponse;
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

        GetMetadataOnDeckRequest req = GetMetadataOnDeckRequest.builder()
                .id(883975L)
                .build();

        GetMetadataOnDeckResponse res = sdk.library().getMetadataOnDeck()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [GetMetadataOnDeckRequest](../../models/operations/GetMetadataOnDeckRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetMetadataOnDeckResponse](../../models/operations/GetMetadataOnDeckResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getMetadataParent

Get parent metadata shortcut.

### Example Usage

<!-- UsageSnippet language="java" operationID="getMetadataParent" method="get" path="/library/metadata/{id}/parent" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetMetadataParentRequest;
import dev.plexapi.sdk.models.operations.GetMetadataParentResponse;
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

        GetMetadataParentRequest req = GetMetadataParentRequest.builder()
                .id(352555L)
                .build();

        GetMetadataParentResponse res = sdk.library().getMetadataParent()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [GetMetadataParentRequest](../../models/operations/GetMetadataParentRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetMetadataParentResponse](../../models/operations/GetMetadataParentResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## uploadPoster

Upload a custom poster image for a metadata item.

### Example Usage

<!-- UsageSnippet language="java" operationID="uploadPoster" method="post" path="/library/metadata/{id}/posters" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.*;
import dev.plexapi.sdk.models.shared.Accepts;
import dev.plexapi.sdk.utils.Utils;
import java.io.FileInputStream;
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

        UploadPosterRequest req = UploadPosterRequest.builder()
                .id(316927L)
                .requestBody(UploadPosterRequestBody.builder()
                    .file(UploadPosterFile.builder()
                        .fileName("example.file")
                        .content(Utils.readBytesAndClose(new FileInputStream("example.file")))
                        .build())
                    .build())
                .build();

        UploadPosterResponse res = sdk.library().uploadPoster()
                .request(req)
                .call();

    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [UploadPosterRequest](../../models/operations/UploadPosterRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[UploadPosterResponse](../../models/operations/UploadPosterResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getMetadataReviews

Get user reviews for a metadata item.

### Example Usage

<!-- UsageSnippet language="java" operationID="getMetadataReviews" method="get" path="/library/metadata/{id}/reviews" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetMetadataReviewsRequest;
import dev.plexapi.sdk.models.operations.GetMetadataReviewsResponse;
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

        GetMetadataReviewsRequest req = GetMetadataReviewsRequest.builder()
                .id(146091L)
                .build();

        GetMetadataReviewsResponse res = sdk.library().getMetadataReviews()
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
| `request`                                                                         | [GetMetadataReviewsRequest](../../models/operations/GetMetadataReviewsRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[GetMetadataReviewsResponse](../../models/operations/GetMetadataReviewsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## deleteMetadataItem

Delete a single metadata item from the library, deleting media as well

### Example Usage

<!-- UsageSnippet language="java" operationID="deleteMetadataItem" method="delete" path="/library/metadata/{ids}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.DeleteMetadataItemRequest;
import dev.plexapi.sdk.models.operations.DeleteMetadataItemResponse;
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

        DeleteMetadataItemRequest req = DeleteMetadataItemRequest.builder()
                .ids("<value>")
                .proxy(BoolInt.True)
                .build();

        DeleteMetadataItemResponse res = sdk.library().deleteMetadataItem()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [DeleteMetadataItemRequest](../../models/operations/DeleteMetadataItemRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[DeleteMetadataItemResponse](../../models/operations/DeleteMetadataItemResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## editMetadataItem

Edit metadata items setting fields

### Example Usage

<!-- UsageSnippet language="java" operationID="editMetadataItem" method="put" path="/library/metadata/{ids}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.EditMetadataItemRequest;
import dev.plexapi.sdk.models.operations.EditMetadataItemResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;
import java.util.List;

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

        EditMetadataItemRequest req = EditMetadataItemRequest.builder()
                .ids(List.of(
                    "<value 1>",
                    "<value 2>"))
                .build();

        EditMetadataItemResponse res = sdk.library().editMetadataItem()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [EditMetadataItemRequest](../../models/operations/EditMetadataItemRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[EditMetadataItemResponse](../../models/operations/EditMetadataItemResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## detectAds

Start the detection of ads in a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="detectAds" method="put" path="/library/metadata/{ids}/addetect" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DetectAdsRequest;
import dev.plexapi.sdk.models.operations.DetectAdsResponse;
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

        DetectAdsRequest req = DetectAdsRequest.builder()
                .ids("<value>")
                .build();

        DetectAdsResponse res = sdk.library().detectAds()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                       | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `request`                                                       | [DetectAdsRequest](../../models/operations/DetectAdsRequest.md) | :heavy_check_mark:                                              | The request object to use for the request.                      |

### Response

**[DetectAdsResponse](../../models/operations/DetectAdsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getAllItemLeaves

Get the leaves for a metadata item such as the episodes in a show

### Example Usage

<!-- UsageSnippet language="java" operationID="getAllItemLeaves" method="get" path="/library/metadata/{ids}/allLeaves" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetAllItemLeavesRequest;
import dev.plexapi.sdk.models.operations.GetAllItemLeavesResponse;
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

        GetAllItemLeavesRequest req = GetAllItemLeavesRequest.builder()
                .ids("<value>")
                .build();

        GetAllItemLeavesResponse res = sdk.library().getAllItemLeaves()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [GetAllItemLeavesRequest](../../models/operations/GetAllItemLeavesRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[GetAllItemLeavesResponse](../../models/operations/GetAllItemLeavesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## analyzeMetadata

Start the analysis of a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="analyzeMetadata" method="put" path="/library/metadata/{ids}/analyze" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.AnalyzeMetadataRequest;
import dev.plexapi.sdk.models.operations.AnalyzeMetadataResponse;
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

        AnalyzeMetadataRequest req = AnalyzeMetadataRequest.builder()
                .ids("<value>")
                .build();

        AnalyzeMetadataResponse res = sdk.library().analyzeMetadata()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [AnalyzeMetadataRequest](../../models/operations/AnalyzeMetadataRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[AnalyzeMetadataResponse](../../models/operations/AnalyzeMetadataResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## generateThumbs

Start the chapter thumb generation for an item

### Example Usage

<!-- UsageSnippet language="java" operationID="generateThumbs" method="put" path="/library/metadata/{ids}/chapterThumbs" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GenerateThumbsRequest;
import dev.plexapi.sdk.models.operations.GenerateThumbsResponse;
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

        GenerateThumbsRequest req = GenerateThumbsRequest.builder()
                .ids("<value>")
                .force(BoolInt.True)
                .build();

        GenerateThumbsResponse res = sdk.library().generateThumbs()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                 | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `request`                                                                 | [GenerateThumbsRequest](../../models/operations/GenerateThumbsRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[GenerateThumbsResponse](../../models/operations/GenerateThumbsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## detectCredits

Start credit detection on a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="detectCredits" method="put" path="/library/metadata/{ids}/credits" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DetectCreditsRequest;
import dev.plexapi.sdk.models.operations.DetectCreditsResponse;
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

        DetectCreditsRequest req = DetectCreditsRequest.builder()
                .ids("<value>")
                .force(BoolInt.True)
                .manual(BoolInt.True)
                .build();

        DetectCreditsResponse res = sdk.library().detectCredits()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `request`                                                               | [DetectCreditsRequest](../../models/operations/DetectCreditsRequest.md) | :heavy_check_mark:                                                      | The request object to use for the request.                              |

### Response

**[DetectCreditsResponse](../../models/operations/DetectCreditsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getExtras

Get the extras for a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="getExtras" method="get" path="/library/metadata/{ids}/extras" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetExtrasRequest;
import dev.plexapi.sdk.models.operations.GetExtrasResponse;
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

        GetExtrasRequest req = GetExtrasRequest.builder()
                .ids("<value>")
                .build();

        GetExtrasResponse res = sdk.library().getExtras()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                       | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `request`                                                       | [GetExtrasRequest](../../models/operations/GetExtrasRequest.md) | :heavy_check_mark:                                              | The request object to use for the request.                      |

### Response

**[GetExtrasResponse](../../models/operations/GetExtrasResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## addExtras

Add an extra to a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="addExtras" method="post" path="/library/metadata/{ids}/extras" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.AddExtrasRequest;
import dev.plexapi.sdk.models.operations.AddExtrasResponse;
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

        AddExtrasRequest req = AddExtrasRequest.builder()
                .ids("<value>")
                .url("https://super-mortise.biz/")
                .build();

        AddExtrasResponse res = sdk.library().addExtras()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                       | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `request`                                                       | [AddExtrasRequest](../../models/operations/AddExtrasRequest.md) | :heavy_check_mark:                                              | The request object to use for the request.                      |

### Response

**[AddExtrasResponse](../../models/operations/AddExtrasResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getFile

Get a bundle file for a metadata or media item.  This is either an image or a mp3 (for a show's theme)

### Example Usage

<!-- UsageSnippet language="java" operationID="getFile" method="get" path="/library/metadata/{ids}/file" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetFileRequest;
import dev.plexapi.sdk.models.operations.GetFileResponse;
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

        GetFileRequest req = GetFileRequest.builder()
                .ids("<value>")
                .build();

        GetFileResponse res = sdk.library().getFile()
                .request(req)
                .call();

        if (res.twoHundredAudioMpeg3ResponseStream().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                   | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `request`                                                   | [GetFileRequest](../../models/operations/GetFileRequest.md) | :heavy_check_mark:                                          | The request object to use for the request.                  |

### Response

**[GetFileResponse](../../models/operations/GetFileResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## startBifGeneration

Start the indexing (BIF generation) of an item

### Example Usage

<!-- UsageSnippet language="java" operationID="startBifGeneration" method="put" path="/library/metadata/{ids}/index" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.StartBifGenerationRequest;
import dev.plexapi.sdk.models.operations.StartBifGenerationResponse;
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

        StartBifGenerationRequest req = StartBifGenerationRequest.builder()
                .ids("<value>")
                .force(BoolInt.True)
                .build();

        StartBifGenerationResponse res = sdk.library().startBifGeneration()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [StartBifGenerationRequest](../../models/operations/StartBifGenerationRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[StartBifGenerationResponse](../../models/operations/StartBifGenerationResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## detectIntros

Start the detection of intros in a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="detectIntros" method="put" path="/library/metadata/{ids}/intro" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DetectIntrosRequest;
import dev.plexapi.sdk.models.operations.DetectIntrosResponse;
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

        DetectIntrosRequest req = DetectIntrosRequest.builder()
                .ids("<value>")
                .force(BoolInt.True)
                .build();

        DetectIntrosResponse res = sdk.library().detectIntros()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [DetectIntrosRequest](../../models/operations/DetectIntrosRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[DetectIntrosResponse](../../models/operations/DetectIntrosResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## createMarker

Create a marker for this user on the metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="createMarker" method="post" path="/library/metadata/{ids}/marker" -->
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

        CreateMarkerRequest req = CreateMarkerRequest.builder()
                .ids("<value>")
                .mediaType(248391L)
                .startTimeOffset(535191L)
                .attributes(Attributes.builder()
                    .build())
                .build();

        CreateMarkerResponse res = sdk.library().createMarker()
                .request(req)
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [CreateMarkerRequest](../../models/operations/CreateMarkerRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[CreateMarkerResponse](../../models/operations/CreateMarkerResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## matchItem

Match a metadata item to a guid

### Example Usage

<!-- UsageSnippet language="java" operationID="matchItem" method="put" path="/library/metadata/{ids}/match" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.MatchItemRequest;
import dev.plexapi.sdk.models.operations.MatchItemResponse;
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

        MatchItemRequest req = MatchItemRequest.builder()
                .ids("<value>")
                .build();

        MatchItemResponse res = sdk.library().matchItem()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                       | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `request`                                                       | [MatchItemRequest](../../models/operations/MatchItemRequest.md) | :heavy_check_mark:                                              | The request object to use for the request.                      |

### Response

**[MatchItemResponse](../../models/operations/MatchItemResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## listMatches

Get the list of metadata matches for a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="listMatches" method="put" path="/library/metadata/{ids}/matches" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.ListMatchesRequest;
import dev.plexapi.sdk.models.operations.ListMatchesResponse;
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

        ListMatchesRequest req = ListMatchesRequest.builder()
                .ids("<value>")
                .manual(BoolInt.True)
                .build();

        ListMatchesResponse res = sdk.library().listMatches()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [ListMatchesRequest](../../models/operations/ListMatchesRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[ListMatchesResponse](../../models/operations/ListMatchesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## mergeItems

Merge a metadata item with other items

### Example Usage

<!-- UsageSnippet language="java" operationID="mergeItems" method="put" path="/library/metadata/{ids}/merge" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.MergeItemsRequest;
import dev.plexapi.sdk.models.operations.MergeItemsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;
import java.util.List;

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

        MergeItemsRequest req = MergeItemsRequest.builder()
                .idsPathParameter("<value>")
                .idsQueryParameter(List.of(
                    "<",
                    "v",
                    "a",
                    "l",
                    "u",
                    "e",
                    ">"))
                .build();

        MergeItemsResponse res = sdk.library().mergeItems()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                         | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `request`                                                         | [MergeItemsRequest](../../models/operations/MergeItemsRequest.md) | :heavy_check_mark:                                                | The request object to use for the request.                        |

### Response

**[MergeItemsResponse](../../models/operations/MergeItemsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## setItemPreferences

Set the preferences on a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="setItemPreferences" method="put" path="/library/metadata/{ids}/prefs" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.SetItemPreferencesRequest;
import dev.plexapi.sdk.models.operations.SetItemPreferencesResponse;
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

        SetItemPreferencesRequest req = SetItemPreferencesRequest.builder()
                .ids("<value>")
                .build();

        SetItemPreferencesResponse res = sdk.library().setItemPreferences()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [SetItemPreferencesRequest](../../models/operations/SetItemPreferencesRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[SetItemPreferencesResponse](../../models/operations/SetItemPreferencesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## refreshItemsMetadata

Refresh a metadata item from the agent

### Example Usage

<!-- UsageSnippet language="java" operationID="refreshItemsMetadata" method="put" path="/library/metadata/{ids}/refresh" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.RefreshItemsMetadataRequest;
import dev.plexapi.sdk.models.operations.RefreshItemsMetadataResponse;
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

        RefreshItemsMetadataRequest req = RefreshItemsMetadataRequest.builder()
                .ids("<value>")
                .markUpdated(BoolInt.True)
                .skipRefresh(BoolInt.True)
                .build();

        RefreshItemsMetadataResponse res = sdk.library().refreshItemsMetadata()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                             | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `request`                                                                             | [RefreshItemsMetadataRequest](../../models/operations/RefreshItemsMetadataRequest.md) | :heavy_check_mark:                                                                    | The request object to use for the request.                                            |

### Response

**[RefreshItemsMetadataResponse](../../models/operations/RefreshItemsMetadataResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getRelatedItems

Get a hub of related items to a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="getRelatedItems" method="get" path="/library/metadata/{ids}/related" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetRelatedItemsRequest;
import dev.plexapi.sdk.models.operations.GetRelatedItemsResponse;
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

        GetRelatedItemsRequest req = GetRelatedItemsRequest.builder()
                .ids("<value>")
                .build();

        GetRelatedItemsResponse res = sdk.library().getRelatedItems()
                .request(req)
                .call();

        if (res.mediaContainerWithHubs().isPresent()) {
            System.out.println(res.mediaContainerWithHubs().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetRelatedItemsRequest](../../models/operations/GetRelatedItemsRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[GetRelatedItemsResponse](../../models/operations/GetRelatedItemsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## listSimilar

Get a list of similar items to a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="listSimilar" method="get" path="/library/metadata/{ids}/similar" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.ListSimilarRequest;
import dev.plexapi.sdk.models.operations.ListSimilarResponse;
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

        ListSimilarRequest req = ListSimilarRequest.builder()
                .ids("<value>")
                .build();

        ListSimilarResponse res = sdk.library().listSimilar()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [ListSimilarRequest](../../models/operations/ListSimilarRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[ListSimilarResponse](../../models/operations/ListSimilarResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## splitItem

Split a metadata item into multiple items

### Example Usage

<!-- UsageSnippet language="java" operationID="splitItem" method="put" path="/library/metadata/{ids}/split" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.SplitItemRequest;
import dev.plexapi.sdk.models.operations.SplitItemResponse;
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

        SplitItemRequest req = SplitItemRequest.builder()
                .ids("<value>")
                .build();

        SplitItemResponse res = sdk.library().splitItem()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                       | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `request`                                                       | [SplitItemRequest](../../models/operations/SplitItemRequest.md) | :heavy_check_mark:                                              | The request object to use for the request.                      |

### Response

**[SplitItemResponse](../../models/operations/SplitItemResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSubtitles

Add a subtitle to a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="getSubtitles" method="get" path="/library/metadata/{ids}/subtitles" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSubtitlesRequest;
import dev.plexapi.sdk.models.operations.GetSubtitlesResponse;
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

        GetSubtitlesRequest req = GetSubtitlesRequest.builder()
                .ids("<value>")
                .forced(BoolInt.True)
                .hearingImpaired(BoolInt.True)
                .build();

        GetSubtitlesResponse res = sdk.library().getSubtitles()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [GetSubtitlesRequest](../../models/operations/GetSubtitlesRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[GetSubtitlesResponse](../../models/operations/GetSubtitlesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getItemTree

Get a tree of metadata items, such as the seasons/episodes of a show

### Example Usage

<!-- UsageSnippet language="java" operationID="getItemTree" method="get" path="/library/metadata/{ids}/tree" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetItemTreeRequest;
import dev.plexapi.sdk.models.operations.GetItemTreeResponse;
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

        GetItemTreeRequest req = GetItemTreeRequest.builder()
                .ids("<value>")
                .build();

        GetItemTreeResponse res = sdk.library().getItemTree()
                .request(req)
                .call();

        if (res.mediaContainerWithNestedMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithNestedMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [GetItemTreeRequest](../../models/operations/GetItemTreeRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[GetItemTreeResponse](../../models/operations/GetItemTreeResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## unmatch

Unmatch a metadata item to info fetched from the agent

### Example Usage

<!-- UsageSnippet language="java" operationID="unmatch" method="put" path="/library/metadata/{ids}/unmatch" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.UnmatchRequest;
import dev.plexapi.sdk.models.operations.UnmatchResponse;
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

        UnmatchRequest req = UnmatchRequest.builder()
                .ids("<value>")
                .build();

        UnmatchResponse res = sdk.library().unmatch()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                   | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `request`                                                   | [UnmatchRequest](../../models/operations/UnmatchRequest.md) | :heavy_check_mark:                                          | The request object to use for the request.                  |

### Response

**[UnmatchResponse](../../models/operations/UnmatchResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## listTopUsers

Get the list of users which have played this item starting with the most

### Example Usage

<!-- UsageSnippet language="java" operationID="listTopUsers" method="get" path="/library/metadata/{ids}/users/top" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.ListTopUsersRequest;
import dev.plexapi.sdk.models.operations.ListTopUsersResponse;
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

        ListTopUsersRequest req = ListTopUsersRequest.builder()
                .ids("<value>")
                .build();

        ListTopUsersResponse res = sdk.library().listTopUsers()
                .request(req)
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [ListTopUsersRequest](../../models/operations/ListTopUsersRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[ListTopUsersResponse](../../models/operations/ListTopUsersResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## detectVoiceActivity

Start the detection of voice in a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="detectVoiceActivity" method="put" path="/library/metadata/{ids}/voiceActivity" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DetectVoiceActivityRequest;
import dev.plexapi.sdk.models.operations.DetectVoiceActivityResponse;
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

        DetectVoiceActivityRequest req = DetectVoiceActivityRequest.builder()
                .ids("<value>")
                .force(BoolInt.True)
                .manual(BoolInt.True)
                .build();

        DetectVoiceActivityResponse res = sdk.library().detectVoiceActivity()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [DetectVoiceActivityRequest](../../models/operations/DetectVoiceActivityRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[DetectVoiceActivityResponse](../../models/operations/DetectVoiceActivityResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getAugmentationStatus

Get augmentation status and potentially wait for completion

### Example Usage

<!-- UsageSnippet language="java" operationID="getAugmentationStatus" method="get" path="/library/metadata/augmentations/{augmentationId}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.GetAugmentationStatusRequest;
import dev.plexapi.sdk.models.operations.GetAugmentationStatusResponse;
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

        GetAugmentationStatusRequest req = GetAugmentationStatusRequest.builder()
                .augmentationId("<id>")
                .wait_(BoolInt.True)
                .build();

        GetAugmentationStatusResponse res = sdk.library().getAugmentationStatus()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                               | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `request`                                                                               | [GetAugmentationStatusRequest](../../models/operations/GetAugmentationStatusRequest.md) | :heavy_check_mark:                                                                      | The request object to use for the request.                                              |

### Response

**[GetAugmentationStatusResponse](../../models/operations/GetAugmentationStatusResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## setStreamSelection

Set which streams (audio/subtitle) are selected by this user

### Example Usage

<!-- UsageSnippet language="java" operationID="setStreamSelection" method="put" path="/library/parts/{partId}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.SetStreamSelectionRequest;
import dev.plexapi.sdk.models.operations.SetStreamSelectionResponse;
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

        SetStreamSelectionRequest req = SetStreamSelectionRequest.builder()
                .partId(360489L)
                .allParts(BoolInt.True)
                .build();

        SetStreamSelectionResponse res = sdk.library().setStreamSelection()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [SetStreamSelectionRequest](../../models/operations/SetStreamSelectionRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[SetStreamSelectionResponse](../../models/operations/SetStreamSelectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getPerson

Get details for a single actor.

### Example Usage

<!-- UsageSnippet language="java" operationID="getPerson" method="get" path="/library/people/{personId}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.GetPersonRequest;
import dev.plexapi.sdk.models.operations.GetPersonResponse;
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

        GetPersonRequest req = GetPersonRequest.builder()
                .personId("<id>")
                .build();

        GetPersonResponse res = sdk.library().getPerson()
                .request(req)
                .call();

        if (res.mediaContainerWithTags().isPresent()) {
            System.out.println(res.mediaContainerWithTags().get());
        }
    }
}
```

### Parameters

| Parameter                                                       | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `request`                                                       | [GetPersonRequest](../../models/operations/GetPersonRequest.md) | :heavy_check_mark:                                              | The request object to use for the request.                      |

### Response

**[GetPersonResponse](../../models/operations/GetPersonResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## listPersonMedia

Get all the media for a single actor.

### Example Usage

<!-- UsageSnippet language="java" operationID="listPersonMedia" method="get" path="/library/people/{personId}/media" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.ListPersonMediaRequest;
import dev.plexapi.sdk.models.operations.ListPersonMediaResponse;
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

        ListPersonMediaRequest req = ListPersonMediaRequest.builder()
                .personId("<id>")
                .build();

        ListPersonMediaResponse res = sdk.library().listPersonMedia()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [ListPersonMediaRequest](../../models/operations/ListPersonMediaRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[ListPersonMediaResponse](../../models/operations/ListPersonMediaResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## deleteLibrarySection

Delete a library section by id

### Example Usage

<!-- UsageSnippet language="java" operationID="deleteLibrarySection" method="delete" path="/library/sections/{sectionId}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DeleteLibrarySectionRequest;
import dev.plexapi.sdk.models.operations.DeleteLibrarySectionResponse;
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

        DeleteLibrarySectionRequest req = DeleteLibrarySectionRequest.builder()
                .sectionId("<id>")
                .async(BoolInt.True)
                .build();

        DeleteLibrarySectionResponse res = sdk.library().deleteLibrarySection()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                             | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `request`                                                                             | [DeleteLibrarySectionRequest](../../models/operations/DeleteLibrarySectionRequest.md) | :heavy_check_mark:                                                                    | The request object to use for the request.                                            |

### Response

**[DeleteLibrarySectionResponse](../../models/operations/DeleteLibrarySectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getLibraryDetails

Returns details for the library. This can be thought of as an interstitial endpoint because it contains information about the library, rather than content itself. It often contains a list of `Directory` metadata objects: These used to be used by clients to build a menuing system.

### Example Usage

<!-- UsageSnippet language="java" operationID="getLibraryDetails" method="get" path="/library/sections/{sectionId}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetLibraryDetailsRequest;
import dev.plexapi.sdk.models.operations.GetLibraryDetailsResponse;
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

        GetLibraryDetailsRequest req = GetLibraryDetailsRequest.builder()
                .sectionId("<id>")
                .includeDetails(BoolInt.True)
                .build();

        GetLibraryDetailsResponse res = sdk.library().getLibraryDetails()
                .request(req)
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [GetLibraryDetailsRequest](../../models/operations/GetLibraryDetailsRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetLibraryDetailsResponse](../../models/operations/GetLibraryDetailsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## editSection

Edit a library section by id setting parameters

### Example Usage

<!-- UsageSnippet language="java" operationID="editSection" method="put" path="/library/sections/{sectionId}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.*;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;
import java.util.List;

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

        EditSectionRequest req = EditSectionRequest.builder()
                .sectionId("<id>")
                .agent("<value>")
                .locations(List.of(
                    "O:\\fatboy\\Media\\Ripped\\Music",
                    "O:\\fatboy\\Media\\My Music"))
                .prefs(EditSectionQueryParamPrefs.builder()
                    .build())
                .build();

        EditSectionResponse res = sdk.library().editSection()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [EditSectionRequest](../../models/operations/EditSectionRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[EditSectionResponse](../../models/operations/EditSectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionAgents

Get available metadata agents for a library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionAgents" method="get" path="/library/sections/{sectionId}/agents" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionAgentsRequest;
import dev.plexapi.sdk.models.operations.GetSectionAgentsResponse;
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

        GetSectionAgentsRequest req = GetSectionAgentsRequest.builder()
                .sectionId(757906L)
                .build();

        GetSectionAgentsResponse res = sdk.library().getSectionAgents()
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
| `request`                                                                     | [GetSectionAgentsRequest](../../models/operations/GetSectionAgentsRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[GetSectionAgentsResponse](../../models/operations/GetSectionAgentsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## updateItems

This endpoint takes an large possible set of values.  Here are some examples.
- **Parameters, extra documentation**
  - artist.title.value
      - When used with track, both artist.title.value and album.title.value need to be specified
  - title.value usage
      - Summary
          - Tracks always rename and never merge
          - Albums and Artists
              - if single item and item without title does not exist, it is renamed.
              - if single item and item with title does exist they are merged.
              - if multiple they are always merged.
      - Tracks
          - Works as expected will update the track's title
          - Single track:    `/library/sections/{id}/all?type=10&id=42&title.value=NewName`
          - Multiple tracks: `/library/sections/{id}/all?type=10&id=42,43,44&title.value=NewName`
          - All tracks:      `/library/sections/{id}/all?type=10&title.value=NewName`
      - Albums
          - Functionality changes depending on the existence of an album with the same title
          - Album exists
              - Single album: `/library/sections/{id}/all?type=9&id=42&title.value=Album 2`
                  - Album with id 42 is merged into album titled "Album 2"
              - Multiple/All albums: `/library/sections/{id}/all?type=9&title.value=Moo Album`
                  - All albums are merged into the existing album titled "Moo Album"
          - Album does not exist
              - Single album: `/library/sections/{id}/all?type=9&id=42&title.value=NewAlbumTitle`
                  - Album with id 42 has title modified to "NewAlbumTitle"
              - Multiple/All albums: `/library/sections/{id}/all?type=9&title.value=NewAlbumTitle`
                  - All albums are merged into a new album with title="NewAlbumTitle"
      - Artists
          - Functionaly changes depending on the existence of an artist with the same title.
          - Artist exists
              - Single artist: `/library/sections/{id}/all?type=8&id=42&title.value=Artist 2`
                  - Artist with id 42 is merged into existing artist titled "Artist 2"
              - Multiple/All artists: `/library/sections/{id}/all?type=8&title.value=Artist 3`
                  - All artists are merged into the existing artist titled "Artist 3"
          - Artist does not exist
              - Single artist: `/library/sections/{id}/all?type=8&id=42&title.value=NewArtistTitle`
                  - Artist with id 42 has title modified to "NewArtistTitle"
              - Multiple/All artists: `/library/sections/{id}/all?type=8&title.value=NewArtistTitle`
                  - All artists are merged into a new artist with title="NewArtistTitle"

- **Notes**
    - Technically square brackets are not allowed in an URI except the Internet Protocol Literal Address
    - RFC3513: A host identified by an Internet Protocol literal address, version 6 [RFC3513] or later, is distinguished by enclosing the IP literal within square brackets ("[" and "]"). This is the only place where square bracket characters are allowed in the URI syntax.
    - Escaped square brackets are allowed, but don't render well

### Example Usage

<!-- UsageSnippet language="java" operationID="updateItems" method="put" path="/library/sections/{sectionId}/all" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.UpdateItemsRequest;
import dev.plexapi.sdk.models.operations.UpdateItemsResponse;
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

        UpdateItemsRequest req = UpdateItemsRequest.builder()
                .sectionId("<id>")
                .fieldLocked(BoolInt.True)
                .build();

        UpdateItemsResponse res = sdk.library().updateItems()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [UpdateItemsRequest](../../models/operations/UpdateItemsRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[UpdateItemsResponse](../../models/operations/UpdateItemsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## startAnalysis

Start analysis of all items in a section.  If BIF generation is enabled, this will also be started on this section

### Example Usage

<!-- UsageSnippet language="java" operationID="startAnalysis" method="put" path="/library/sections/{sectionId}/analyze" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.StartAnalysisRequest;
import dev.plexapi.sdk.models.operations.StartAnalysisResponse;
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

        StartAnalysisRequest req = StartAnalysisRequest.builder()
                .sectionId(158829L)
                .build();

        StartAnalysisResponse res = sdk.library().startAnalysis()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `request`                                                               | [StartAnalysisRequest](../../models/operations/StartAnalysisRequest.md) | :heavy_check_mark:                                                      | The request object to use for the request.                              |

### Response

**[StartAnalysisResponse](../../models/operations/StartAnalysisResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionArtists

Get artists for a music library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionArtists" method="get" path="/library/sections/{sectionId}/artists" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionArtistsRequest;
import dev.plexapi.sdk.models.operations.GetSectionArtistsResponse;
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

        GetSectionArtistsRequest req = GetSectionArtistsRequest.builder()
                .sectionId(716398L)
                .build();

        GetSectionArtistsResponse res = sdk.library().getSectionArtists()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [GetSectionArtistsRequest](../../models/operations/GetSectionArtistsRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetSectionArtistsResponse](../../models/operations/GetSectionArtistsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## autocomplete

The field to autocomplete on is specified by the `{field}.query` parameter. For example `genre.query` or `title.query`.
Returns a set of items from the filtered items whose `{field}` starts with `{field}.query`.  In the results, a `{field}.queryRange` will be present to express the range of the match

### Example Usage

<!-- UsageSnippet language="java" operationID="autocomplete" method="get" path="/library/sections/{sectionId}/autocomplete" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.AutocompleteRequest;
import dev.plexapi.sdk.models.operations.AutocompleteResponse;
import dev.plexapi.sdk.models.shared.*;
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

        AutocompleteRequest req = AutocompleteRequest.builder()
                .sectionId(942007L)
                .mediaQuery(MediaQuery.builder()
                    .type(MediaType.Episode)
                    .sort("duration:desc,index")
                    .sourceType(2L)
                    .build())
                .build();

        AutocompleteResponse res = sdk.library().autocomplete()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [AutocompleteRequest](../../models/operations/AutocompleteRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[AutocompleteResponse](../../models/operations/AutocompleteResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getByContentRating

Browse items in a library section grouped by content rating.

### Example Usage

<!-- UsageSnippet language="java" operationID="getByContentRating" method="get" path="/library/sections/{sectionId}/byContentRating" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetByContentRatingRequest;
import dev.plexapi.sdk.models.operations.GetByContentRatingResponse;
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

        GetByContentRatingRequest req = GetByContentRatingRequest.builder()
                .sectionId(586837L)
                .build();

        GetByContentRatingResponse res = sdk.library().getByContentRating()
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
| `request`                                                                         | [GetByContentRatingRequest](../../models/operations/GetByContentRatingRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[GetByContentRatingResponse](../../models/operations/GetByContentRatingResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getByDecade

Browse items in a library section grouped by decade.

### Example Usage

<!-- UsageSnippet language="java" operationID="getByDecade" method="get" path="/library/sections/{sectionId}/byDecade" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetByDecadeRequest;
import dev.plexapi.sdk.models.operations.GetByDecadeResponse;
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

        GetByDecadeRequest req = GetByDecadeRequest.builder()
                .sectionId(212187L)
                .build();

        GetByDecadeResponse res = sdk.library().getByDecade()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [GetByDecadeRequest](../../models/operations/GetByDecadeRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[GetByDecadeResponse](../../models/operations/GetByDecadeResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getByFolder

Browse items in a library section by underlying filesystem folder.

### Example Usage

<!-- UsageSnippet language="java" operationID="getByFolder" method="get" path="/library/sections/{sectionId}/byFolder" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetByFolderRequest;
import dev.plexapi.sdk.models.operations.GetByFolderResponse;
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

        GetByFolderRequest req = GetByFolderRequest.builder()
                .sectionId(352088L)
                .build();

        GetByFolderResponse res = sdk.library().getByFolder()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [GetByFolderRequest](../../models/operations/GetByFolderRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[GetByFolderResponse](../../models/operations/GetByFolderResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getByResolution

Browse items in a library section grouped by resolution.

### Example Usage

<!-- UsageSnippet language="java" operationID="getByResolution" method="get" path="/library/sections/{sectionId}/byResolution" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetByResolutionRequest;
import dev.plexapi.sdk.models.operations.GetByResolutionResponse;
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

        GetByResolutionRequest req = GetByResolutionRequest.builder()
                .sectionId(139174L)
                .build();

        GetByResolutionResponse res = sdk.library().getByResolution()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetByResolutionRequest](../../models/operations/GetByResolutionRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[GetByResolutionResponse](../../models/operations/GetByResolutionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getByYear

Browse items in a library section grouped by year.

### Example Usage

<!-- UsageSnippet language="java" operationID="getByYear" method="get" path="/library/sections/{sectionId}/byYear" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetByYearRequest;
import dev.plexapi.sdk.models.operations.GetByYearResponse;
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

        GetByYearRequest req = GetByYearRequest.builder()
                .sectionId(14634L)
                .build();

        GetByYearResponse res = sdk.library().getByYear()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                       | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `request`                                                       | [GetByYearRequest](../../models/operations/GetByYearRequest.md) | :heavy_check_mark:                                              | The request object to use for the request.                      |

### Response

**[GetByYearResponse](../../models/operations/GetByYearResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionClips

Get clips for a library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionClips" method="get" path="/library/sections/{sectionId}/clips" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionClipsRequest;
import dev.plexapi.sdk.models.operations.GetSectionClipsResponse;
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

        GetSectionClipsRequest req = GetSectionClipsRequest.builder()
                .sectionId(407860L)
                .build();

        GetSectionClipsResponse res = sdk.library().getSectionClips()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetSectionClipsRequest](../../models/operations/GetSectionClipsRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[GetSectionClipsResponse](../../models/operations/GetSectionClipsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getCollections

Get all collections in a section

### Example Usage

<!-- UsageSnippet language="java" operationID="getCollections" method="get" path="/library/sections/{sectionId}/collections" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetCollectionsRequest;
import dev.plexapi.sdk.models.operations.GetCollectionsResponse;
import dev.plexapi.sdk.models.shared.*;
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

        GetCollectionsRequest req = GetCollectionsRequest.builder()
                .sectionId(348838L)
                .mediaQuery(MediaQuery.builder()
                    .type(MediaType.Episode)
                    .sort("duration:desc,index")
                    .sourceType(2L)
                    .build())
                .build();

        GetCollectionsResponse res = sdk.library().getCollections()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                 | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `request`                                                                 | [GetCollectionsRequest](../../models/operations/GetCollectionsRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[GetCollectionsResponse](../../models/operations/GetCollectionsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getCommon

Represents a "Common" item. It contains only the common attributes of the items selected by the provided filter
Fields which are not common will be expressed in the `mixedFields` field

### Example Usage

<!-- UsageSnippet language="java" operationID="getCommon" method="get" path="/library/sections/{sectionId}/common" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.GetCommonRequest;
import dev.plexapi.sdk.models.operations.GetCommonResponse;
import dev.plexapi.sdk.models.shared.*;
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

        GetCommonRequest req = GetCommonRequest.builder()
                .sectionId(298154L)
                .mediaQuery(MediaQuery.builder()
                    .type(MediaType.Episode)
                    .sort("duration:desc,index")
                    .sourceType(2L)
                    .build())
                .build();

        GetCommonResponse res = sdk.library().getCommon()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                       | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `request`                                                       | [GetCommonRequest](../../models/operations/GetCommonRequest.md) | :heavy_check_mark:                                              | The request object to use for the request.                      |

### Response

**[GetCommonResponse](../../models/operations/GetCommonResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionEdit

Get library section metadata.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionEdit" method="get" path="/library/sections/{sectionId}/edit" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionEditRequest;
import dev.plexapi.sdk.models.operations.GetSectionEditResponse;
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

        GetSectionEditRequest req = GetSectionEditRequest.builder()
                .sectionId(223075L)
                .build();

        GetSectionEditResponse res = sdk.library().getSectionEdit()
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
| `request`                                                                 | [GetSectionEditRequest](../../models/operations/GetSectionEditRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[GetSectionEditResponse](../../models/operations/GetSectionEditResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## editLibrarySection

Update library section metadata.

### Example Usage

<!-- UsageSnippet language="java" operationID="editLibrarySection" method="put" path="/library/sections/{sectionId}/edit" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.EditLibrarySectionRequest;
import dev.plexapi.sdk.models.operations.EditLibrarySectionResponse;
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

        EditLibrarySectionRequest req = EditLibrarySectionRequest.builder()
                .sectionId(834094L)
                .build();

        EditLibrarySectionResponse res = sdk.library().editLibrarySection()
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
| `request`                                                                         | [EditLibrarySectionRequest](../../models/operations/EditLibrarySectionRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[EditLibrarySectionResponse](../../models/operations/EditLibrarySectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## emptyTrash

Permanently remove items from the trash for a library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="emptyTrash" method="get" path="/library/sections/{sectionId}/emptyTrash" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.EmptyTrashRequest;
import dev.plexapi.sdk.models.operations.EmptyTrashResponse;
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

        EmptyTrashRequest req = EmptyTrashRequest.builder()
                .sectionId(30052L)
                .build();

        EmptyTrashResponse res = sdk.library().emptyTrash()
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
| `request`                                                         | [EmptyTrashRequest](../../models/operations/EmptyTrashRequest.md) | :heavy_check_mark:                                                | The request object to use for the request.                        |

### Response

**[EmptyTrashResponse](../../models/operations/EmptyTrashResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## emptyTrashPost

Permanently remove items from the trash for a library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="emptyTrashPost" method="post" path="/library/sections/{sectionId}/emptyTrash" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.EmptyTrashPostRequest;
import dev.plexapi.sdk.models.operations.EmptyTrashPostResponse;
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

        EmptyTrashPostRequest req = EmptyTrashPostRequest.builder()
                .sectionId(537157L)
                .build();

        EmptyTrashPostResponse res = sdk.library().emptyTrashPost()
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
| `request`                                                                 | [EmptyTrashPostRequest](../../models/operations/EmptyTrashPostRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[EmptyTrashPostResponse](../../models/operations/EmptyTrashPostResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## emptyTrashPut

Empty trash in the section, permanently deleting media/metadata for missing media

### Example Usage

<!-- UsageSnippet language="java" operationID="emptyTrashPut" method="put" path="/library/sections/{sectionId}/emptyTrash" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.EmptyTrashPutRequest;
import dev.plexapi.sdk.models.operations.EmptyTrashPutResponse;
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

        EmptyTrashPutRequest req = EmptyTrashPutRequest.builder()
                .sectionId(642296L)
                .build();

        EmptyTrashPutResponse res = sdk.library().emptyTrashPut()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `request`                                                               | [EmptyTrashPutRequest](../../models/operations/EmptyTrashPutRequest.md) | :heavy_check_mark:                                                      | The request object to use for the request.                              |

### Response

**[EmptyTrashPutResponse](../../models/operations/EmptyTrashPutResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionEpisodes

Get episodes for a TV library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionEpisodes" method="get" path="/library/sections/{sectionId}/episodes" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionEpisodesRequest;
import dev.plexapi.sdk.models.operations.GetSectionEpisodesResponse;
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

        GetSectionEpisodesRequest req = GetSectionEpisodesRequest.builder()
                .sectionId(229495L)
                .build();

        GetSectionEpisodesResponse res = sdk.library().getSectionEpisodes()
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
| `request`                                                                         | [GetSectionEpisodesRequest](../../models/operations/GetSectionEpisodesRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[GetSectionEpisodesResponse](../../models/operations/GetSectionEpisodesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionFilters

Get common filters on a section

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionFilters" method="get" path="/library/sections/{sectionId}/filters" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionFiltersRequest;
import dev.plexapi.sdk.models.operations.GetSectionFiltersResponse;
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

        GetSectionFiltersRequest req = GetSectionFiltersRequest.builder()
                .sectionId(380557L)
                .build();

        GetSectionFiltersResponse res = sdk.library().getSectionFilters()
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
| `request`                                                                       | [GetSectionFiltersRequest](../../models/operations/GetSectionFiltersRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetSectionFiltersResponse](../../models/operations/GetSectionFiltersResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getFirstCharacters

Get list of first characters in this section

### Example Usage

<!-- UsageSnippet language="java" operationID="getFirstCharacters" method="get" path="/library/sections/{sectionId}/firstCharacters" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetFirstCharactersRequest;
import dev.plexapi.sdk.models.operations.GetFirstCharactersResponse;
import dev.plexapi.sdk.models.shared.*;
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

        GetFirstCharactersRequest req = GetFirstCharactersRequest.builder()
                .sectionId(3947L)
                .mediaQuery(MediaQuery.builder()
                    .type(MediaType.Episode)
                    .sort("duration:desc,index")
                    .sourceType(2L)
                    .build())
                .build();

        GetFirstCharactersResponse res = sdk.library().getFirstCharacters()
                .request(req)
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [GetFirstCharactersRequest](../../models/operations/GetFirstCharactersRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[GetFirstCharactersResponse](../../models/operations/GetFirstCharactersResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getLibrarySectionHubs

Get hubs for a library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getLibrarySectionHubs" method="get" path="/library/sections/{sectionId}/hubs" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetLibrarySectionHubsRequest;
import dev.plexapi.sdk.models.operations.GetLibrarySectionHubsResponse;
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

        GetLibrarySectionHubsRequest req = GetLibrarySectionHubsRequest.builder()
                .sectionId(426468L)
                .build();

        GetLibrarySectionHubsResponse res = sdk.library().getLibrarySectionHubs()
                .request(req)
                .call();

        if (res.mediaContainerWithHubs().isPresent()) {
            System.out.println(res.mediaContainerWithHubs().get());
        }
    }
}
```

### Parameters

| Parameter                                                                               | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `request`                                                                               | [GetLibrarySectionHubsRequest](../../models/operations/GetLibrarySectionHubsRequest.md) | :heavy_check_mark:                                                                      | The request object to use for the request.                                              |

### Response

**[GetLibrarySectionHubsResponse](../../models/operations/GetLibrarySectionHubsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## deleteIndexes

Delete all the indexes in a section

### Example Usage

<!-- UsageSnippet language="java" operationID="deleteIndexes" method="delete" path="/library/sections/{sectionId}/indexes" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DeleteIndexesRequest;
import dev.plexapi.sdk.models.operations.DeleteIndexesResponse;
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

        DeleteIndexesRequest req = DeleteIndexesRequest.builder()
                .sectionId(588437L)
                .build();

        DeleteIndexesResponse res = sdk.library().deleteIndexes()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `request`                                                               | [DeleteIndexesRequest](../../models/operations/DeleteIndexesRequest.md) | :heavy_check_mark:                                                      | The request object to use for the request.                              |

### Response

**[DeleteIndexesResponse](../../models/operations/DeleteIndexesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## deleteIntros

Delete all the intro markers in a section

### Example Usage

<!-- UsageSnippet language="java" operationID="deleteIntros" method="delete" path="/library/sections/{sectionId}/intros" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.DeleteIntrosRequest;
import dev.plexapi.sdk.models.operations.DeleteIntrosResponse;
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

        DeleteIntrosRequest req = DeleteIntrosRequest.builder()
                .sectionId(498656L)
                .build();

        DeleteIntrosResponse res = sdk.library().deleteIntros()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [DeleteIntrosRequest](../../models/operations/DeleteIntrosRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[DeleteIntrosResponse](../../models/operations/DeleteIntrosResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionLabels

Get labels for a library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionLabels" method="get" path="/library/sections/{sectionId}/label" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionLabelsRequest;
import dev.plexapi.sdk.models.operations.GetSectionLabelsResponse;
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

        GetSectionLabelsRequest req = GetSectionLabelsRequest.builder()
                .sectionId(705342L)
                .build();

        GetSectionLabelsResponse res = sdk.library().getSectionLabels()
                .request(req)
                .call();

        if (res.mediaContainerWithTags().isPresent()) {
            System.out.println(res.mediaContainerWithTags().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [GetSectionLabelsRequest](../../models/operations/GetSectionLabelsRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[GetSectionLabelsResponse](../../models/operations/GetSectionLabelsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## matchSectionItems

Match items in a library section against metadata providers.

### Example Usage

<!-- UsageSnippet language="java" operationID="matchSectionItems" method="get" path="/library/sections/{sectionId}/match" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.MatchSectionItemsRequest;
import dev.plexapi.sdk.models.operations.MatchSectionItemsResponse;
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

        MatchSectionItemsRequest req = MatchSectionItemsRequest.builder()
                .sectionId(31032L)
                .build();

        MatchSectionItemsResponse res = sdk.library().matchSectionItems()
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
| `request`                                                                       | [MatchSectionItemsRequest](../../models/operations/MatchSectionItemsRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[MatchSectionItemsResponse](../../models/operations/MatchSectionItemsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## moveSection

Move library section paths.

### Example Usage

<!-- UsageSnippet language="java" operationID="moveSection" method="put" path="/library/sections/{sectionId}/move" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.MoveSectionRequest;
import dev.plexapi.sdk.models.operations.MoveSectionResponse;
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

        MoveSectionRequest req = MoveSectionRequest.builder()
                .sectionId(483061L)
                .build();

        MoveSectionResponse res = sdk.library().moveSection()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [MoveSectionRequest](../../models/operations/MoveSectionRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[MoveSectionResponse](../../models/operations/MoveSectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionMovies

Get movies for a movie library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionMovies" method="get" path="/library/sections/{sectionId}/movies" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionMoviesRequest;
import dev.plexapi.sdk.models.operations.GetSectionMoviesResponse;
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

        GetSectionMoviesRequest req = GetSectionMoviesRequest.builder()
                .sectionId(530892L)
                .build();

        GetSectionMoviesResponse res = sdk.library().getSectionMovies()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [GetSectionMoviesRequest](../../models/operations/GetSectionMoviesRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[GetSectionMoviesResponse](../../models/operations/GetSectionMoviesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getNewestForSection

Get the newest additions for a specific library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getNewestForSection" method="get" path="/library/sections/{sectionId}/newest" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetNewestForSectionRequest;
import dev.plexapi.sdk.models.operations.GetNewestForSectionResponse;
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

        GetNewestForSectionRequest req = GetNewestForSectionRequest.builder()
                .sectionId(73900L)
                .build();

        GetNewestForSectionResponse res = sdk.library().getNewestForSection()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [GetNewestForSectionRequest](../../models/operations/GetNewestForSectionRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[GetNewestForSectionResponse](../../models/operations/GetNewestForSectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getOnDeckForSection

Get the On Deck items for a specific library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getOnDeckForSection" method="get" path="/library/sections/{sectionId}/onDeck" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetOnDeckForSectionRequest;
import dev.plexapi.sdk.models.operations.GetOnDeckForSectionResponse;
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

        GetOnDeckForSectionRequest req = GetOnDeckForSectionRequest.builder()
                .sectionId(331089L)
                .build();

        GetOnDeckForSectionResponse res = sdk.library().getOnDeckForSection()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [GetOnDeckForSectionRequest](../../models/operations/GetOnDeckForSectionRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[GetOnDeckForSectionResponse](../../models/operations/GetOnDeckForSectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## optimizeSection

Optimize the database for a specific library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="optimizeSection" method="get" path="/library/sections/{sectionId}/optimize" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.OptimizeSectionRequest;
import dev.plexapi.sdk.models.operations.OptimizeSectionResponse;
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

        OptimizeSectionRequest req = OptimizeSectionRequest.builder()
                .sectionId(721290L)
                .build();

        OptimizeSectionResponse res = sdk.library().optimizeSection()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [OptimizeSectionRequest](../../models/operations/OptimizeSectionRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[OptimizeSectionResponse](../../models/operations/OptimizeSectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## optimizeSectionPost

Optimize the database for a specific library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="optimizeSectionPost" method="post" path="/library/sections/{sectionId}/optimize" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.OptimizeSectionPostRequest;
import dev.plexapi.sdk.models.operations.OptimizeSectionPostResponse;
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

        OptimizeSectionPostRequest req = OptimizeSectionPostRequest.builder()
                .sectionId(876391L)
                .build();

        OptimizeSectionPostResponse res = sdk.library().optimizeSectionPost()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [OptimizeSectionPostRequest](../../models/operations/OptimizeSectionPostRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[OptimizeSectionPostResponse](../../models/operations/OptimizeSectionPostResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionPhotos

Get photos for a photo library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionPhotos" method="get" path="/library/sections/{sectionId}/photos" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionPhotosRequest;
import dev.plexapi.sdk.models.operations.GetSectionPhotosResponse;
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

        GetSectionPhotosRequest req = GetSectionPhotosRequest.builder()
                .sectionId(622466L)
                .build();

        GetSectionPhotosResponse res = sdk.library().getSectionPhotos()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [GetSectionPhotosRequest](../../models/operations/GetSectionPhotosRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[GetSectionPhotosResponse](../../models/operations/GetSectionPhotosResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionPlaylists

Get playlists belonging to a library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionPlaylists" method="get" path="/library/sections/{sectionId}/playlists" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionPlaylistsRequest;
import dev.plexapi.sdk.models.operations.GetSectionPlaylistsResponse;
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

        GetSectionPlaylistsRequest req = GetSectionPlaylistsRequest.builder()
                .sectionId(826184L)
                .build();

        GetSectionPlaylistsResponse res = sdk.library().getSectionPlaylists()
                .request(req)
                .call();

        if (res.mediaContainerWithPlaylistMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithPlaylistMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [GetSectionPlaylistsRequest](../../models/operations/GetSectionPlaylistsRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[GetSectionPlaylistsResponse](../../models/operations/GetSectionPlaylistsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionPreferences

Get the prefs for a section by id and potentially overriding the agent

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionPreferences" method="get" path="/library/sections/{sectionId}/prefs" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionPreferencesRequest;
import dev.plexapi.sdk.models.operations.GetSectionPreferencesResponse;
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

        GetSectionPreferencesRequest req = GetSectionPreferencesRequest.builder()
                .sectionId(754869L)
                .build();

        GetSectionPreferencesResponse res = sdk.library().getSectionPreferences()
                .request(req)
                .call();

        if (res.mediaContainerWithSettings().isPresent()) {
            System.out.println(res.mediaContainerWithSettings().get());
        }
    }
}
```

### Parameters

| Parameter                                                                               | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `request`                                                                               | [GetSectionPreferencesRequest](../../models/operations/GetSectionPreferencesRequest.md) | :heavy_check_mark:                                                                      | The request object to use for the request.                                              |

### Response

**[GetSectionPreferencesResponse](../../models/operations/GetSectionPreferencesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## setSectionPreferences

Set the prefs for a section by id

### Example Usage

<!-- UsageSnippet language="java" operationID="setSectionPreferences" method="put" path="/library/sections/{sectionId}/prefs" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.*;
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

        SetSectionPreferencesRequest req = SetSectionPreferencesRequest.builder()
                .sectionId(349936L)
                .prefs(SetSectionPreferencesQueryParamPrefs.builder()
                    .build())
                .build();

        SetSectionPreferencesResponse res = sdk.library().setSectionPreferences()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                               | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `request`                                                                               | [SetSectionPreferencesRequest](../../models/operations/SetSectionPreferencesRequest.md) | :heavy_check_mark:                                                                      | The request object to use for the request.                                              |

### Response

**[SetSectionPreferencesResponse](../../models/operations/SetSectionPreferencesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getRecentlyAddedForSection

Get recently added items for a specific library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getRecentlyAddedForSection" method="get" path="/library/sections/{sectionId}/recentlyAdded" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetRecentlyAddedForSectionRequest;
import dev.plexapi.sdk.models.operations.GetRecentlyAddedForSectionResponse;
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

        GetRecentlyAddedForSectionRequest req = GetRecentlyAddedForSectionRequest.builder()
                .sectionId(46283L)
                .build();

        GetRecentlyAddedForSectionResponse res = sdk.library().getRecentlyAddedForSection()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                         | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `request`                                                                                         | [GetRecentlyAddedForSectionRequest](../../models/operations/GetRecentlyAddedForSectionRequest.md) | :heavy_check_mark:                                                                                | The request object to use for the request.                                                        |

### Response

**[GetRecentlyAddedForSectionResponse](../../models/operations/GetRecentlyAddedForSectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## cancelRefresh

Cancel the refresh of a section

### Example Usage

<!-- UsageSnippet language="java" operationID="cancelRefresh" method="delete" path="/library/sections/{sectionId}/refresh" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.CancelRefreshRequest;
import dev.plexapi.sdk.models.operations.CancelRefreshResponse;
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

        CancelRefreshRequest req = CancelRefreshRequest.builder()
                .sectionId(326852L)
                .build();

        CancelRefreshResponse res = sdk.library().cancelRefresh()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `request`                                                               | [CancelRefreshRequest](../../models/operations/CancelRefreshRequest.md) | :heavy_check_mark:                                                      | The request object to use for the request.                              |

### Response

**[CancelRefreshResponse](../../models/operations/CancelRefreshResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## refreshSection

Trigger a metadata refresh for a library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="refreshSection" method="get" path="/library/sections/{sectionId}/refresh" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.RefreshSectionRequest;
import dev.plexapi.sdk.models.operations.RefreshSectionResponse;
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

        RefreshSectionRequest req = RefreshSectionRequest.builder()
                .sectionId(450300L)
                .build();

        RefreshSectionResponse res = sdk.library().refreshSection()
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
| `request`                                                                 | [RefreshSectionRequest](../../models/operations/RefreshSectionRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[RefreshSectionResponse](../../models/operations/RefreshSectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## refreshSectionPost

Trigger a metadata refresh for a library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="refreshSectionPost" method="post" path="/library/sections/{sectionId}/refresh" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.RefreshSectionPostRequest;
import dev.plexapi.sdk.models.operations.RefreshSectionPostResponse;
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

        RefreshSectionPostRequest req = RefreshSectionPostRequest.builder()
                .sectionId(848668L)
                .force(BoolInt.True)
                .build();

        RefreshSectionPostResponse res = sdk.library().refreshSectionPost()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [RefreshSectionPostRequest](../../models/operations/RefreshSectionPostRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[RefreshSectionPostResponse](../../models/operations/RefreshSectionPostResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## searchSection

Search within a specific library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="searchSection" method="get" path="/library/sections/{sectionId}/search" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.SearchSectionRequest;
import dev.plexapi.sdk.models.operations.SearchSectionResponse;
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

        SearchSectionRequest req = SearchSectionRequest.builder()
                .sectionId(925380L)
                .build();

        SearchSectionResponse res = sdk.library().searchSection()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `request`                                                               | [SearchSectionRequest](../../models/operations/SearchSectionRequest.md) | :heavy_check_mark:                                                      | The request object to use for the request.                              |

### Response

**[SearchSectionResponse](../../models/operations/SearchSectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionSettings

Get section-specific settings.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionSettings" method="get" path="/library/sections/{sectionId}/settings" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionSettingsRequest;
import dev.plexapi.sdk.models.operations.GetSectionSettingsResponse;
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

        GetSectionSettingsRequest req = GetSectionSettingsRequest.builder()
                .sectionId(100390L)
                .build();

        GetSectionSettingsResponse res = sdk.library().getSectionSettings()
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
| `request`                                                                         | [GetSectionSettingsRequest](../../models/operations/GetSectionSettingsRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[GetSectionSettingsResponse](../../models/operations/GetSectionSettingsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionShows

Get shows for a TV library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionShows" method="get" path="/library/sections/{sectionId}/shows" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionShowsRequest;
import dev.plexapi.sdk.models.operations.GetSectionShowsResponse;
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

        GetSectionShowsRequest req = GetSectionShowsRequest.builder()
                .sectionId(9583L)
                .build();

        GetSectionShowsResponse res = sdk.library().getSectionShows()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetSectionShowsRequest](../../models/operations/GetSectionShowsRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[GetSectionShowsResponse](../../models/operations/GetSectionShowsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getAvailableSorts

Get the sort mechanisms available in a section

### Example Usage

<!-- UsageSnippet language="java" operationID="getAvailableSorts" method="get" path="/library/sections/{sectionId}/sorts" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetAvailableSortsRequest;
import dev.plexapi.sdk.models.operations.GetAvailableSortsResponse;
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

        GetAvailableSortsRequest req = GetAvailableSortsRequest.builder()
                .sectionId(212498L)
                .build();

        GetAvailableSortsResponse res = sdk.library().getAvailableSorts()
                .request(req)
                .call();

        if (res.mediaContainerWithSorts().isPresent()) {
            System.out.println(res.mediaContainerWithSorts().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [GetAvailableSortsRequest](../../models/operations/GetAvailableSortsRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetAvailableSortsResponse](../../models/operations/GetAvailableSortsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionTags

Get tags in a library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionTags" method="get" path="/library/sections/{sectionId}/tags" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionTagsRequest;
import dev.plexapi.sdk.models.operations.GetSectionTagsResponse;
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

        GetSectionTagsRequest req = GetSectionTagsRequest.builder()
                .sectionId(787543L)
                .build();

        GetSectionTagsResponse res = sdk.library().getSectionTags()
                .request(req)
                .call();

        if (res.mediaContainerWithTags().isPresent()) {
            System.out.println(res.mediaContainerWithTags().get());
        }
    }
}
```

### Parameters

| Parameter                                                                 | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `request`                                                                 | [GetSectionTagsRequest](../../models/operations/GetSectionTagsRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[GetSectionTagsResponse](../../models/operations/GetSectionTagsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionTimeline

Get section timeline data.

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionTimeline" method="get" path="/library/sections/{sectionId}/timeline" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionTimelineRequest;
import dev.plexapi.sdk.models.operations.GetSectionTimelineResponse;
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

        GetSectionTimelineRequest req = GetSectionTimelineRequest.builder()
                .sectionId(670370L)
                .build();

        GetSectionTimelineResponse res = sdk.library().getSectionTimeline()
                .request(req)
                .call();

        if (res.mediaContainerWithDirectory().isPresent()) {
            System.out.println(res.mediaContainerWithDirectory().get());
        }
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [GetSectionTimelineRequest](../../models/operations/GetSectionTimelineRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[GetSectionTimelineResponse](../../models/operations/GetSectionTimelineResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## unmatchSectionItems

Unmatch items in a library section from metadata providers.

### Example Usage

<!-- UsageSnippet language="java" operationID="unmatchSectionItems" method="get" path="/library/sections/{sectionId}/unmatch" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.UnmatchSectionItemsRequest;
import dev.plexapi.sdk.models.operations.UnmatchSectionItemsResponse;
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

        UnmatchSectionItemsRequest req = UnmatchSectionItemsRequest.builder()
                .sectionId(209342L)
                .build();

        UnmatchSectionItemsResponse res = sdk.library().unmatchSectionItems()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [UnmatchSectionItemsRequest](../../models/operations/UnmatchSectionItemsRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[UnmatchSectionItemsResponse](../../models/operations/UnmatchSectionItemsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getUnwatchedForSection

Get unwatched items for a specific library section.

### Example Usage

<!-- UsageSnippet language="java" operationID="getUnwatchedForSection" method="get" path="/library/sections/{sectionId}/unwatched" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetUnwatchedForSectionRequest;
import dev.plexapi.sdk.models.operations.GetUnwatchedForSectionResponse;
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

        GetUnwatchedForSectionRequest req = GetUnwatchedForSectionRequest.builder()
                .sectionId(483590L)
                .build();

        GetUnwatchedForSectionResponse res = sdk.library().getUnwatchedForSection()
                .request(req)
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                 | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `request`                                                                                 | [GetUnwatchedForSectionRequest](../../models/operations/GetUnwatchedForSectionRequest.md) | :heavy_check_mark:                                                                        | The request object to use for the request.                                                |

### Response

**[GetUnwatchedForSectionResponse](../../models/operations/GetUnwatchedForSectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getStreamLevels

The the loudness of a stream in db, one entry per 100ms

### Example Usage

<!-- UsageSnippet language="java" operationID="getStreamLevels" method="get" path="/library/streams/{streamId}/levels" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.GetStreamLevelsRequest;
import dev.plexapi.sdk.models.operations.GetStreamLevelsResponse;
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

        GetStreamLevelsRequest req = GetStreamLevelsRequest.builder()
                .streamId(447611L)
                .build();

        GetStreamLevelsResponse res = sdk.library().getStreamLevels()
                .request(req)
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetStreamLevelsRequest](../../models/operations/GetStreamLevelsRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[GetStreamLevelsResponse](../../models/operations/GetStreamLevelsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getStreamLoudness

The the loudness of a stream in db, one number per line, one entry per 100ms

### Example Usage

<!-- UsageSnippet language="java" operationID="getStreamLoudness" method="get" path="/library/streams/{streamId}/loudness" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.GetStreamLoudnessRequest;
import dev.plexapi.sdk.models.operations.GetStreamLoudnessResponse;
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

        GetStreamLoudnessRequest req = GetStreamLoudnessRequest.builder()
                .streamId(277271L)
                .build();

        GetStreamLoudnessResponse res = sdk.library().getStreamLoudness()
                .request(req)
                .call();

        if (res.res().isPresent()) {
            System.out.println(res.res().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [GetStreamLoudnessRequest](../../models/operations/GetStreamLoudnessRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[GetStreamLoudnessResponse](../../models/operations/GetStreamLoudnessResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getChapterImage

Get a single chapter image for a piece of media

### Example Usage

<!-- UsageSnippet language="java" operationID="getChapterImage" method="get" path="/library/media/{mediaId}/chapterImages/{chapter}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.GetChapterImageRequest;
import dev.plexapi.sdk.models.operations.GetChapterImageResponse;
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

        GetChapterImageRequest req = GetChapterImageRequest.builder()
                .mediaId(892563L)
                .chapter(48348L)
                .build();

        GetChapterImageResponse res = sdk.library().getChapterImage()
                .request(req)
                .call();

        if (res.responseStream().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetChapterImageRequest](../../models/operations/GetChapterImageRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[GetChapterImageResponse](../../models/operations/GetChapterImageResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## setItemArtwork

Set the artwork, thumb, element for a metadata item
Generally only the admin can perform this action.  The exception is if the metadata is a playlist created by the user

### Example Usage

<!-- UsageSnippet language="java" operationID="setItemArtwork" method="post" path="/library/metadata/{ids}/{element}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.*;
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

        SetItemArtworkRequest req = SetItemArtworkRequest.builder()
                .ids("<value>")
                .element(Element.BANNER)
                .build();

        SetItemArtworkResponse res = sdk.library().setItemArtwork()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                 | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `request`                                                                 | [SetItemArtworkRequest](../../models/operations/SetItemArtworkRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[SetItemArtworkResponse](../../models/operations/SetItemArtworkResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## updateItemArtwork

Set the artwork, thumb, element for a metadata item
Generally only the admin can perform this action.  The exception is if the metadata is a playlist created by the user

### Example Usage

<!-- UsageSnippet language="java" operationID="updateItemArtwork" method="put" path="/library/metadata/{ids}/{element}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.*;
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

        UpdateItemArtworkRequest req = UpdateItemArtworkRequest.builder()
                .ids("<value>")
                .element(PathParamElement.CLEAR_LOGO)
                .build();

        UpdateItemArtworkResponse res = sdk.library().updateItemArtwork()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [UpdateItemArtworkRequest](../../models/operations/UpdateItemArtworkRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[UpdateItemArtworkResponse](../../models/operations/UpdateItemArtworkResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## deleteMarker

Delete a marker for this user on the metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="deleteMarker" method="delete" path="/library/metadata/{ids}/marker/{marker}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.DeleteMarkerRequest;
import dev.plexapi.sdk.models.operations.DeleteMarkerResponse;
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

        DeleteMarkerRequest req = DeleteMarkerRequest.builder()
                .ids("<value>")
                .marker("<value>")
                .build();

        DeleteMarkerResponse res = sdk.library().deleteMarker()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [DeleteMarkerRequest](../../models/operations/DeleteMarkerRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[DeleteMarkerResponse](../../models/operations/DeleteMarkerResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## editMarker

Edit a marker for this user on the metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="editMarker" method="put" path="/library/metadata/{ids}/marker/{marker}" -->
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

        EditMarkerRequest req = EditMarkerRequest.builder()
                .ids("<value>")
                .marker("<value>")
                .mediaType(884347L)
                .startTimeOffset(517251L)
                .attributes(QueryParamAttributes.builder()
                    .build())
                .build();

        EditMarkerResponse res = sdk.library().editMarker()
                .request(req)
                .call();

        if (res.postResponses200().isPresent()) {
            System.out.println(res.postResponses200().get());
        }
    }
}
```

### Parameters

| Parameter                                                         | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `request`                                                         | [EditMarkerRequest](../../models/operations/EditMarkerRequest.md) | :heavy_check_mark:                                                | The request object to use for the request.                        |

### Response

**[EditMarkerResponse](../../models/operations/EditMarkerResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## deleteMediaItem

Delete a single media from a metadata item in the library

### Example Usage

<!-- UsageSnippet language="java" operationID="deleteMediaItem" method="delete" path="/library/metadata/{ids}/media/{mediaItem}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.DeleteMediaItemRequest;
import dev.plexapi.sdk.models.operations.DeleteMediaItemResponse;
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

        DeleteMediaItemRequest req = DeleteMediaItemRequest.builder()
                .ids("<value>")
                .mediaItem("<value>")
                .proxy(BoolInt.True)
                .build();

        DeleteMediaItemResponse res = sdk.library().deleteMediaItem()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [DeleteMediaItemRequest](../../models/operations/DeleteMediaItemRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[DeleteMediaItemResponse](../../models/operations/DeleteMediaItemResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getPartIndex

Get BIF index for a part by index type

### Example Usage

<!-- UsageSnippet language="java" operationID="getPartIndex" method="get" path="/library/parts/{partId}/indexes/{index}" -->
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

        GetPartIndexRequest req = GetPartIndexRequest.builder()
                .partId(724750L)
                .index(Index.SD)
                .build();

        GetPartIndexResponse res = sdk.library().getPartIndex()
                .request(req)
                .call();

        if (res.responseStream().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [GetPartIndexRequest](../../models/operations/GetPartIndexRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[GetPartIndexResponse](../../models/operations/GetPartIndexResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## deleteCollection

Delete a library collection from the PMS

### Example Usage

<!-- UsageSnippet language="java" operationID="deleteCollection" method="delete" path="/library/sections/{sectionId}/collection/{collectionId}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.DeleteCollectionRequest;
import dev.plexapi.sdk.models.operations.DeleteCollectionResponse;
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

        DeleteCollectionRequest req = DeleteCollectionRequest.builder()
                .sectionId(283619L)
                .collectionId(680895L)
                .build();

        DeleteCollectionResponse res = sdk.library().deleteCollection()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [DeleteCollectionRequest](../../models/operations/DeleteCollectionRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[DeleteCollectionResponse](../../models/operations/DeleteCollectionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getSectionImage

Get a composite image of images in this section

### Example Usage

<!-- UsageSnippet language="java" operationID="getSectionImage" method="get" path="/library/sections/{sectionId}/composite/{updatedAt}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetSectionImageRequest;
import dev.plexapi.sdk.models.operations.GetSectionImageResponse;
import dev.plexapi.sdk.models.shared.*;
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

        GetSectionImageRequest req = GetSectionImageRequest.builder()
                .sectionId(925611L)
                .updatedAt(117413L)
                .mediaQuery(MediaQuery.builder()
                    .type(MediaType.Episode)
                    .sort("duration:desc,index")
                    .sourceType(2L)
                    .build())
                .build();

        GetSectionImageResponse res = sdk.library().getSectionImage()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetSectionImageRequest](../../models/operations/GetSectionImageRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[GetSectionImageResponse](../../models/operations/GetSectionImageResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## deleteStream

Delete a stream.  Only applies to downloaded subtitle streams or a sidecar subtitle when media deletion is enabled.

### Example Usage

<!-- UsageSnippet language="java" operationID="deleteStream" method="delete" path="/library/streams/{streamId}.{ext}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.DeleteStreamRequest;
import dev.plexapi.sdk.models.operations.DeleteStreamResponse;
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

        DeleteStreamRequest req = DeleteStreamRequest.builder()
                .streamId(841510L)
                .ext("<value>")
                .build();

        DeleteStreamResponse res = sdk.library().deleteStream()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [DeleteStreamRequest](../../models/operations/DeleteStreamRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[DeleteStreamResponse](../../models/operations/DeleteStreamResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getStream

Get a stream (such as a sidecar subtitle stream)

### Example Usage

<!-- UsageSnippet language="java" operationID="getStream" method="get" path="/library/streams/{streamId}.{ext}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.GetStreamRequest;
import dev.plexapi.sdk.models.operations.GetStreamResponse;
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

        GetStreamRequest req = GetStreamRequest.builder()
                .streamId(314506L)
                .ext("<value>")
                .autoAdjustSubtitle(BoolInt.True)
                .build();

        GetStreamResponse res = sdk.library().getStream()
                .request(req)
                .call();

        if (res.binaryResponse().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                       | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `request`                                                       | [GetStreamRequest](../../models/operations/GetStreamRequest.md) | :heavy_check_mark:                                              | The request object to use for the request.                      |

### Response

**[GetStreamResponse](../../models/operations/GetStreamResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## setStreamOffset

Set a stream offset in ms.  This may not be respected by all clients

### Example Usage

<!-- UsageSnippet language="java" operationID="setStreamOffset" method="put" path="/library/streams/{streamId}.{ext}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.SetStreamOffsetRequest;
import dev.plexapi.sdk.models.operations.SetStreamOffsetResponse;
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

        SetStreamOffsetRequest req = SetStreamOffsetRequest.builder()
                .streamId(606295L)
                .ext("<value>")
                .build();

        SetStreamOffsetResponse res = sdk.library().setStreamOffset()
                .request(req)
                .call();

        if (res.binaryResponse().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [SetStreamOffsetRequest](../../models/operations/SetStreamOffsetRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[SetStreamOffsetResponse](../../models/operations/SetStreamOffsetResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getItemArtwork

Get the artwork, thumb, element for a metadata item

### Example Usage

<!-- UsageSnippet language="java" operationID="getItemArtwork" method="get" path="/library/metadata/{ids}/{element}/{timestamp}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.*;
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

        GetItemArtworkRequest req = GetItemArtworkRequest.builder()
                .ids("<value>")
                .element(GetItemArtworkPathParamElement.POSTER)
                .timestamp(999555L)
                .build();

        GetItemArtworkResponse res = sdk.library().getItemArtwork()
                .request(req)
                .call();

        if (res.twoHundredAudioMpeg3ResponseStream().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                 | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `request`                                                                 | [GetItemArtworkRequest](../../models/operations/GetItemArtworkRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[GetItemArtworkResponse](../../models/operations/GetItemArtworkResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getMediaPart

Get a media part for streaming or download.
  - streaming: This is the default scenario.  Bandwidth usage on this endpoint will be guaranteed (on the server's end) to be at least the bandwidth reservation given in the decision.  If no decision exists, an ad-hoc decision will be created if sufficient bandwidth exists.  Clients should not rely on ad-hoc decisions being made as this may be removed in the future.
  - download: Indicated if the query parameter indicates this is a download.  Bandwidth will be prioritized behind playbacks and will get a fair share of what remains.

### Example Usage

<!-- UsageSnippet language="java" operationID="getMediaPart" method="get" path="/library/parts/{partId}/{changestamp}/{filename}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.GetMediaPartRequest;
import dev.plexapi.sdk.models.operations.GetMediaPartResponse;
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

        GetMediaPartRequest req = GetMediaPartRequest.builder()
                .partId(877105L)
                .changestamp(970622L)
                .filename("example.file")
                .download(BoolInt.True)
                .build();

        GetMediaPartResponse res = sdk.library().getMediaPart()
                .request(req)
                .call();

        if (res.binaryResponse().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [GetMediaPartRequest](../../models/operations/GetMediaPartRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[GetMediaPartResponse](../../models/operations/GetMediaPartResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getImageFromBif

Extract an image from the BIF for a part at a particular offset

### Example Usage

<!-- UsageSnippet language="java" operationID="getImageFromBif" method="get" path="/library/parts/{partId}/indexes/{index}/{offset}" -->
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

        GetImageFromBifRequest req = GetImageFromBifRequest.builder()
                .partId(304273L)
                .index(PathParamIndex.SD)
                .offset(939569L)
                .build();

        GetImageFromBifResponse res = sdk.library().getImageFromBif()
                .request(req)
                .call();

        if (res.responseStream().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetImageFromBifRequest](../../models/operations/GetImageFromBifRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[GetImageFromBifResponse](../../models/operations/GetImageFromBifResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |