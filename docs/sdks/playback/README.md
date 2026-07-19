# Playback

## Overview

Plex Playback operations

### Available Operations

* [getProgress](#getprogress) - Get Progress
* [removeFromContinueWatching](#removefromcontinuewatching) - Remove From Continue Watching
* [playerAudioStream](#playeraudiostream) - Player Audio Stream
* [playerMute](#playermute) - Player Mute
* [playerPause](#playerpause) - Player Pause
* [playerPlay](#playerplay) - Player Play
* [playerPlayMedia](#playerplaymedia) - Player Play Media
* [playerRefreshplayqueue](#playerrefreshplayqueue) - Player Refresh Play Queue
* [playerSeek](#playerseek) - Player Seek
* [playerSetParameters](#playersetparameters) - Player Set Parameters
* [playerSetRating](#playersetrating) - Player Set Rating
* [playerSetState](#playersetstate) - Player Set State
* [playerSetStreams](#playersetstreams) - Player Set Streams
* [playerSetTextStream](#playersettextstream) - Player Set Text Stream
* [playerSetViewOffset](#playersetviewoffset) - Player Set View Offset
* [playerSkipBy](#playerskipby) - Player Skip By
* [playerSkipTo](#playerskipto) - Player Skip To
* [playerStepback](#playerstepback) - Player Step Back
* [playerStepforward](#playerstepforward) - Player Step Forward
* [playerStop](#playerstop) - Player Stop
* [playerSubtitleStream](#playersubtitlestream) - Player Subtitle Stream
* [playerUnmute](#playerunmute) - Player Unmute
* [playerVideoStream](#playervideostream) - Player Video Stream
* [playerVolume](#playervolume) - Player Volume
* [getClientResources](#getclientresources) - Get Client Resources
* [playerPollTimeline](#playerpolltimeline) - Player Poll Timeline

## getProgress

Get or update watch progress for a media item.

### Example Usage

<!-- UsageSnippet language="java" operationID="getProgress" method="get" path="/:/progress" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetProgressRequest;
import dev.plexapi.sdk.models.operations.GetProgressResponse;
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

        GetProgressRequest req = GetProgressRequest.builder()
                .key("<key>")
                .time(181086L)
                .build();

        GetProgressResponse res = sdk.playback().getProgress()
                .request(req)
                .call();

        if (res.progressResponse().isPresent()) {
            System.out.println(res.progressResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [GetProgressRequest](../../models/operations/GetProgressRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[GetProgressResponse](../../models/operations/GetProgressResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## removeFromContinueWatching

Remove an item from the Continue Watching list.

### Example Usage

<!-- UsageSnippet language="java" operationID="removeFromContinueWatching" method="put" path="/actions/removeFromContinueWatching" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.RemoveFromContinueWatchingRequest;
import dev.plexapi.sdk.models.operations.RemoveFromContinueWatchingResponse;
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

        RemoveFromContinueWatchingRequest req = RemoveFromContinueWatchingRequest.builder()
                .key("<key>")
                .build();

        RemoveFromContinueWatchingResponse res = sdk.playback().removeFromContinueWatching()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                         | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `request`                                                                                         | [RemoveFromContinueWatchingRequest](../../models/operations/RemoveFromContinueWatchingRequest.md) | :heavy_check_mark:                                                                                | The request object to use for the request.                                                        |

### Response

**[RemoveFromContinueWatchingResponse](../../models/operations/RemoveFromContinueWatchingResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerAudioStream

Change the active audio stream.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerAudioStream" method="post" path="/player/playback/audioStream" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerAudioStreamRequest;
import dev.plexapi.sdk.models.operations.PlayerAudioStreamResponse;
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

        PlayerAudioStreamRequest req = PlayerAudioStreamRequest.builder()
                .build();

        PlayerAudioStreamResponse res = sdk.playback().playerAudioStream()
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
| `request`                                                                       | [PlayerAudioStreamRequest](../../models/operations/PlayerAudioStreamRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[PlayerAudioStreamResponse](../../models/operations/PlayerAudioStreamResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerMute

Mute the client audio

### Example Usage

<!-- UsageSnippet language="java" operationID="playerMute" method="post" path="/player/playback/mute" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerMuteRequest;
import dev.plexapi.sdk.models.operations.PlayerMuteResponse;
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

        PlayerMuteRequest req = PlayerMuteRequest.builder()
                .build();

        PlayerMuteResponse res = sdk.playback().playerMute()
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
| `request`                                                         | [PlayerMuteRequest](../../models/operations/PlayerMuteRequest.md) | :heavy_check_mark:                                                | The request object to use for the request.                        |

### Response

**[PlayerMuteResponse](../../models/operations/PlayerMuteResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerPause

Pause playback on the client

### Example Usage

<!-- UsageSnippet language="java" operationID="playerPause" method="post" path="/player/playback/pause" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerPauseRequest;
import dev.plexapi.sdk.models.operations.PlayerPauseResponse;
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

        PlayerPauseRequest req = PlayerPauseRequest.builder()
                .build();

        PlayerPauseResponse res = sdk.playback().playerPause()
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
| `request`                                                           | [PlayerPauseRequest](../../models/operations/PlayerPauseRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |

### Response

**[PlayerPauseResponse](../../models/operations/PlayerPauseResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerPlay

Start playback on the client

### Example Usage

<!-- UsageSnippet language="java" operationID="playerPlay" method="post" path="/player/playback/play" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerPlayRequest;
import dev.plexapi.sdk.models.operations.PlayerPlayResponse;
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

        PlayerPlayRequest req = PlayerPlayRequest.builder()
                .build();

        PlayerPlayResponse res = sdk.playback().playerPlay()
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
| `request`                                                         | [PlayerPlayRequest](../../models/operations/PlayerPlayRequest.md) | :heavy_check_mark:                                                | The request object to use for the request.                        |

### Response

**[PlayerPlayResponse](../../models/operations/PlayerPlayResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerPlayMedia

Play a specific media item on the client.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerPlayMedia" method="post" path="/player/playback/playMedia" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerPlayMediaRequest;
import dev.plexapi.sdk.models.operations.PlayerPlayMediaResponse;
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

        PlayerPlayMediaRequest req = PlayerPlayMediaRequest.builder()
                .build();

        PlayerPlayMediaResponse res = sdk.playback().playerPlayMedia()
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
| `request`                                                                   | [PlayerPlayMediaRequest](../../models/operations/PlayerPlayMediaRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[PlayerPlayMediaResponse](../../models/operations/PlayerPlayMediaResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerRefreshplayqueue

Refresh the play queue on the client

### Example Usage

<!-- UsageSnippet language="java" operationID="playerRefreshplayqueue" method="post" path="/player/playback/refreshPlayQueue" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerRefreshplayqueueRequest;
import dev.plexapi.sdk.models.operations.PlayerRefreshplayqueueResponse;
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

        PlayerRefreshplayqueueRequest req = PlayerRefreshplayqueueRequest.builder()
                .build();

        PlayerRefreshplayqueueResponse res = sdk.playback().playerRefreshplayqueue()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                 | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `request`                                                                                 | [PlayerRefreshplayqueueRequest](../../models/operations/PlayerRefreshplayqueueRequest.md) | :heavy_check_mark:                                                                        | The request object to use for the request.                                                |

### Response

**[PlayerRefreshplayqueueResponse](../../models/operations/PlayerRefreshplayqueueResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerSeek

Seek to a specific time in the current playback.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerSeek" method="post" path="/player/playback/seek" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerSeekRequest;
import dev.plexapi.sdk.models.operations.PlayerSeekResponse;
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

        PlayerSeekRequest req = PlayerSeekRequest.builder()
                .build();

        PlayerSeekResponse res = sdk.playback().playerSeek()
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
| `request`                                                         | [PlayerSeekRequest](../../models/operations/PlayerSeekRequest.md) | :heavy_check_mark:                                                | The request object to use for the request.                        |

### Response

**[PlayerSeekResponse](../../models/operations/PlayerSeekResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerSetParameters

Set shuffle, repeat, and volume parameters.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerSetParameters" method="post" path="/player/playback/setParameters" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerSetParametersRequest;
import dev.plexapi.sdk.models.operations.PlayerSetParametersResponse;
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

        PlayerSetParametersRequest req = PlayerSetParametersRequest.builder()
                .build();

        PlayerSetParametersResponse res = sdk.playback().playerSetParameters()
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
| `request`                                                                           | [PlayerSetParametersRequest](../../models/operations/PlayerSetParametersRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[PlayerSetParametersResponse](../../models/operations/PlayerSetParametersResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerSetRating

Rate the currently playing item.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerSetRating" method="post" path="/player/playback/setRating" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerSetRatingRequest;
import dev.plexapi.sdk.models.operations.PlayerSetRatingResponse;
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

        PlayerSetRatingRequest req = PlayerSetRatingRequest.builder()
                .build();

        PlayerSetRatingResponse res = sdk.playback().playerSetRating()
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
| `request`                                                                   | [PlayerSetRatingRequest](../../models/operations/PlayerSetRatingRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[PlayerSetRatingResponse](../../models/operations/PlayerSetRatingResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerSetState

Set the playback state directly.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerSetState" method="post" path="/player/playback/setState" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerSetStateRequest;
import dev.plexapi.sdk.models.operations.PlayerSetStateResponse;
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

        PlayerSetStateRequest req = PlayerSetStateRequest.builder()
                .build();

        PlayerSetStateResponse res = sdk.playback().playerSetState()
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
| `request`                                                                 | [PlayerSetStateRequest](../../models/operations/PlayerSetStateRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[PlayerSetStateResponse](../../models/operations/PlayerSetStateResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerSetStreams

Set active audio, subtitle, and video streams.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerSetStreams" method="post" path="/player/playback/setStreams" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerSetStreamsRequest;
import dev.plexapi.sdk.models.operations.PlayerSetStreamsResponse;
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

        PlayerSetStreamsRequest req = PlayerSetStreamsRequest.builder()
                .build();

        PlayerSetStreamsResponse res = sdk.playback().playerSetStreams()
                .request(req)
                .call();

        if (res.binaryResponse().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [PlayerSetStreamsRequest](../../models/operations/PlayerSetStreamsRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |

### Response

**[PlayerSetStreamsResponse](../../models/operations/PlayerSetStreamsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerSetTextStream

Set the active text stream.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerSetTextStream" method="post" path="/player/playback/setTextStream" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerSetTextStreamRequest;
import dev.plexapi.sdk.models.operations.PlayerSetTextStreamResponse;
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

        PlayerSetTextStreamRequest req = PlayerSetTextStreamRequest.builder()
                .build();

        PlayerSetTextStreamResponse res = sdk.playback().playerSetTextStream()
                .request(req)
                .call();

        if (res.binaryResponse().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [PlayerSetTextStreamRequest](../../models/operations/PlayerSetTextStreamRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[PlayerSetTextStreamResponse](../../models/operations/PlayerSetTextStreamResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerSetViewOffset

Set the resume offset for the current item.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerSetViewOffset" method="post" path="/player/playback/setViewOffset" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerSetViewOffsetRequest;
import dev.plexapi.sdk.models.operations.PlayerSetViewOffsetResponse;
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

        PlayerSetViewOffsetRequest req = PlayerSetViewOffsetRequest.builder()
                .build();

        PlayerSetViewOffsetResponse res = sdk.playback().playerSetViewOffset()
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
| `request`                                                                           | [PlayerSetViewOffsetRequest](../../models/operations/PlayerSetViewOffsetRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |

### Response

**[PlayerSetViewOffsetResponse](../../models/operations/PlayerSetViewOffsetResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerSkipBy

Skip forward or backward by a number of items.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerSkipBy" method="post" path="/player/playback/skipBy" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerSkipByRequest;
import dev.plexapi.sdk.models.operations.PlayerSkipByResponse;
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

        PlayerSkipByRequest req = PlayerSkipByRequest.builder()
                .build();

        PlayerSkipByResponse res = sdk.playback().playerSkipBy()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [PlayerSkipByRequest](../../models/operations/PlayerSkipByRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[PlayerSkipByResponse](../../models/operations/PlayerSkipByResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerSkipTo

Skip to a specific item in the play queue.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerSkipTo" method="post" path="/player/playback/skipTo" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerSkipToRequest;
import dev.plexapi.sdk.models.operations.PlayerSkipToResponse;
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

        PlayerSkipToRequest req = PlayerSkipToRequest.builder()
                .build();

        PlayerSkipToResponse res = sdk.playback().playerSkipTo()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [PlayerSkipToRequest](../../models/operations/PlayerSkipToRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[PlayerSkipToResponse](../../models/operations/PlayerSkipToResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerStepback

Step back one frame

### Example Usage

<!-- UsageSnippet language="java" operationID="playerStepback" method="post" path="/player/playback/stepBack" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerStepbackRequest;
import dev.plexapi.sdk.models.operations.PlayerStepbackResponse;
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

        PlayerStepbackRequest req = PlayerStepbackRequest.builder()
                .build();

        PlayerStepbackResponse res = sdk.playback().playerStepback()
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
| `request`                                                                 | [PlayerStepbackRequest](../../models/operations/PlayerStepbackRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[PlayerStepbackResponse](../../models/operations/PlayerStepbackResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerStepforward

Step forward one frame

### Example Usage

<!-- UsageSnippet language="java" operationID="playerStepforward" method="post" path="/player/playback/stepForward" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerStepforwardRequest;
import dev.plexapi.sdk.models.operations.PlayerStepforwardResponse;
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

        PlayerStepforwardRequest req = PlayerStepforwardRequest.builder()
                .build();

        PlayerStepforwardResponse res = sdk.playback().playerStepforward()
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
| `request`                                                                       | [PlayerStepforwardRequest](../../models/operations/PlayerStepforwardRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[PlayerStepforwardResponse](../../models/operations/PlayerStepforwardResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerStop

Stop playback on the client

### Example Usage

<!-- UsageSnippet language="java" operationID="playerStop" method="post" path="/player/playback/stop" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerStopRequest;
import dev.plexapi.sdk.models.operations.PlayerStopResponse;
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

        PlayerStopRequest req = PlayerStopRequest.builder()
                .build();

        PlayerStopResponse res = sdk.playback().playerStop()
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
| `request`                                                         | [PlayerStopRequest](../../models/operations/PlayerStopRequest.md) | :heavy_check_mark:                                                | The request object to use for the request.                        |

### Response

**[PlayerStopResponse](../../models/operations/PlayerStopResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerSubtitleStream

Change the active subtitle stream.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerSubtitleStream" method="post" path="/player/playback/subtitleStream" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerSubtitleStreamRequest;
import dev.plexapi.sdk.models.operations.PlayerSubtitleStreamResponse;
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

        PlayerSubtitleStreamRequest req = PlayerSubtitleStreamRequest.builder()
                .build();

        PlayerSubtitleStreamResponse res = sdk.playback().playerSubtitleStream()
                .request(req)
                .call();

        if (res.binaryResponse().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                             | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `request`                                                                             | [PlayerSubtitleStreamRequest](../../models/operations/PlayerSubtitleStreamRequest.md) | :heavy_check_mark:                                                                    | The request object to use for the request.                                            |

### Response

**[PlayerSubtitleStreamResponse](../../models/operations/PlayerSubtitleStreamResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerUnmute

Unmute the client audio

### Example Usage

<!-- UsageSnippet language="java" operationID="playerUnmute" method="post" path="/player/playback/unmute" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerUnmuteRequest;
import dev.plexapi.sdk.models.operations.PlayerUnmuteResponse;
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

        PlayerUnmuteRequest req = PlayerUnmuteRequest.builder()
                .build();

        PlayerUnmuteResponse res = sdk.playback().playerUnmute()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [PlayerUnmuteRequest](../../models/operations/PlayerUnmuteRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[PlayerUnmuteResponse](../../models/operations/PlayerUnmuteResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerVideoStream

Change the active video stream.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerVideoStream" method="post" path="/player/playback/videoStream" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerVideoStreamRequest;
import dev.plexapi.sdk.models.operations.PlayerVideoStreamResponse;
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

        PlayerVideoStreamRequest req = PlayerVideoStreamRequest.builder()
                .build();

        PlayerVideoStreamResponse res = sdk.playback().playerVideoStream()
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
| `request`                                                                       | [PlayerVideoStreamRequest](../../models/operations/PlayerVideoStreamRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |

### Response

**[PlayerVideoStreamResponse](../../models/operations/PlayerVideoStreamResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerVolume

Set the client volume.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerVolume" method="post" path="/player/playback/volume" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerVolumeRequest;
import dev.plexapi.sdk.models.operations.PlayerVolumeResponse;
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

        PlayerVolumeRequest req = PlayerVolumeRequest.builder()
                .build();

        PlayerVolumeResponse res = sdk.playback().playerVolume()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [PlayerVolumeRequest](../../models/operations/PlayerVolumeRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[PlayerVolumeResponse](../../models/operations/PlayerVolumeResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getClientResources

Get client capabilities and device info.

### Example Usage

<!-- UsageSnippet language="java" operationID="getClientResources" method="get" path="/player/resources" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetClientResourcesRequest;
import dev.plexapi.sdk.models.operations.GetClientResourcesResponse;
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

        GetClientResourcesRequest req = GetClientResourcesRequest.builder()
                .build();

        GetClientResourcesResponse res = sdk.playback().getClientResources()
                .request(req)
                .call();

        if (res.mediaContainerWithDevice().isPresent()) {
            System.out.println(res.mediaContainerWithDevice().get());
        }
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [GetClientResourcesRequest](../../models/operations/GetClientResourcesRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[GetClientResourcesResponse](../../models/operations/GetClientResourcesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## playerPollTimeline

Poll the client for current playback timeline.

### Example Usage

<!-- UsageSnippet language="java" operationID="playerPollTimeline" method="get" path="/player/timeline/poll" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PlayerPollTimelineRequest;
import dev.plexapi.sdk.models.operations.PlayerPollTimelineResponse;
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

        PlayerPollTimelineRequest req = PlayerPollTimelineRequest.builder()
                .build();

        PlayerPollTimelineResponse res = sdk.playback().playerPollTimeline()
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
| `request`                                                                         | [PlayerPollTimelineRequest](../../models/operations/PlayerPollTimelineRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[PlayerPollTimelineResponse](../../models/operations/PlayerPollTimelineResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |