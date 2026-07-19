# Transcoder

## Overview

API Operations against the Transcoder

### Available Operations

* [transcodeMusic](#transcodemusic) - Transcode Music
* [transcodeImage](#transcodeimage) - Transcode an image
* [getTranscodeSessions](#gettranscodesessions) - Get Transcode Sessions
* [makeDecision](#makedecision) - Make a decision on media playback
* [triggerFallback](#triggerfallback) - Manually trigger a transcoder fallback
* [transcodeSubtitles](#transcodesubtitles) - Transcode subtitles
* [startTranscodeSession](#starttranscodesession) - Start A Transcoding Session
* [getDASHSegment](#getdashsegment) - Get DASH Segment
* [getHLSSegment](#gethlssegment) - Get HLS Segment

## transcodeMusic

Audio transcode endpoint for music playback.

### Example Usage

<!-- UsageSnippet language="java" operationID="transcodeMusic" method="get" path="/music/:/transcode" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.TranscodeMusicRequest;
import dev.plexapi.sdk.models.operations.TranscodeMusicResponse;
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

        TranscodeMusicRequest req = TranscodeMusicRequest.builder()
                .build();

        TranscodeMusicResponse res = sdk.transcoder().transcodeMusic()
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
| `request`                                                                 | [TranscodeMusicRequest](../../models/operations/TranscodeMusicRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[TranscodeMusicResponse](../../models/operations/TranscodeMusicResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## transcodeImage

Transcode an image, possibly changing format or size

### Example Usage

<!-- UsageSnippet language="java" operationID="transcodeImage" method="get" path="/photo/:/transcode" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.TranscodeImageRequest;
import dev.plexapi.sdk.models.operations.TranscodeImageResponse;
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

        TranscodeImageRequest req = TranscodeImageRequest.builder()
                .url("/library/metadata/265/thumb/1715112705")
                .background("#ff5522")
                .upscale(BoolInt.True)
                .minSize(BoolInt.True)
                .rotate(BoolInt.True)
                .blendColor("#ff5522")
                .build();

        TranscodeImageResponse res = sdk.transcoder().transcodeImage()
                .request(req)
                .call();

        if (res.twoHundredImageJpegResponseStream().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                 | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `request`                                                                 | [TranscodeImageRequest](../../models/operations/TranscodeImageRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[TranscodeImageResponse](../../models/operations/TranscodeImageResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getTranscodeSessions

Get active transcode sessions.

### Example Usage

<!-- UsageSnippet language="java" operationID="getTranscodeSessions" method="get" path="/transcode/sessions" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetTranscodeSessionsResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetTranscodeSessionsResponse res = sdk.transcoder().getTranscodeSessions()
                .call();

        if (res.mediaContainerWithMetadata().isPresent()) {
            System.out.println(res.mediaContainerWithMetadata().get());
        }
    }
}
```

### Response

**[GetTranscodeSessionsResponse](../../models/operations/GetTranscodeSessionsResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## makeDecision

Make a decision on media playback based on client profile, and requested settings such as bandwidth and resolution.

### Example Usage

<!-- UsageSnippet language="java" operationID="makeDecision" method="get" path="/{transcodeType}/:/transcode/universal/decision" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.*;
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

        MakeDecisionRequest req = MakeDecisionRequest.builder()
                .transcodeType(TranscodeType.MUSIC)
                .advancedSubtitles(AdvancedSubtitles.BURN)
                .audioBoost(50L)
                .audioChannelCount(5L)
                .autoAdjustQuality(BoolInt.True)
                .autoAdjustSubtitle(BoolInt.True)
                .directPlay(BoolInt.True)
                .directStream(BoolInt.True)
                .directStreamAudio(BoolInt.True)
                .disableResolutionRotation(BoolInt.True)
                .hasMDE(BoolInt.True)
                .location(Location.WAN)
                .mediaBufferSize(102400L)
                .mediaIndex(0L)
                .musicBitrate(5000L)
                .offset(90.5)
                .partIndex(0L)
                .path("/library/metadata/151671")
                .peakBitrate(12000L)
                .photoResolution("1080x1080")
                .protocol(QueryParamProtocol.DASH)
                .secondsPerSegment(5L)
                .subtitleSize(50L)
                .subtitles(Subtitles.BURN)
                .videoResolution("1080x1080")
                .copyts(BoolInt.True)
                .videoBitrate(12000L)
                .videoQuality(50L)
                .xPlexClientProfileExtra("add-limitation(scope=videoCodec&scopeName=*&type=upperBound&name=video.frameRate&value=60&replace=true)+append-transcode-target-codec(type=videoProfile&context=streaming&videoCodec=h264%2Chevc&audioCodec=aac&protocol=dash)")
                .xPlexClientProfileName("generic")
                .build();

        MakeDecisionResponse res = sdk.transcoder().makeDecision()
                .request(req)
                .call();

        if (res.mediaContainerWithDecision().isPresent()) {
            System.out.println(res.mediaContainerWithDecision().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [MakeDecisionRequest](../../models/operations/MakeDecisionRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |

### Response

**[MakeDecisionResponse](../../models/operations/MakeDecisionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## triggerFallback

Manually trigger a transcoder fallback ex: HEVC to h.264 or hw to sw

### Example Usage

<!-- UsageSnippet language="java" operationID="triggerFallback" method="post" path="/{transcodeType}/:/transcode/universal/fallback" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.TriggerFallbackRequest;
import dev.plexapi.sdk.models.operations.TriggerFallbackResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import dev.plexapi.sdk.models.shared.TranscodeType;
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

        TriggerFallbackRequest req = TriggerFallbackRequest.builder()
                .transcodeType(TranscodeType.AUDIO)
                .build();

        TriggerFallbackResponse res = sdk.transcoder().triggerFallback()
                .request(req)
                .call();

        // handle response
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [TriggerFallbackRequest](../../models/operations/TriggerFallbackRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |

### Response

**[TriggerFallbackResponse](../../models/operations/TriggerFallbackResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## transcodeSubtitles

Only transcode subtitle streams.

### Example Usage

<!-- UsageSnippet language="java" operationID="transcodeSubtitles" method="get" path="/{transcodeType}/:/transcode/universal/subtitles" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.*;
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

        TranscodeSubtitlesRequest req = TranscodeSubtitlesRequest.builder()
                .transcodeType(TranscodeType.AUDIO)
                .advancedSubtitles(AdvancedSubtitles.BURN)
                .audioBoost(50L)
                .audioChannelCount(5L)
                .autoAdjustQuality(BoolInt.True)
                .autoAdjustSubtitle(BoolInt.True)
                .directPlay(BoolInt.True)
                .directStream(BoolInt.True)
                .directStreamAudio(BoolInt.True)
                .disableResolutionRotation(BoolInt.True)
                .hasMDE(BoolInt.True)
                .location(QueryParamLocation.WAN)
                .mediaBufferSize(102400L)
                .mediaIndex(0L)
                .musicBitrate(5000L)
                .offset(90.5)
                .partIndex(0L)
                .path("/library/metadata/151671")
                .peakBitrate(12000L)
                .photoResolution("1080x1080")
                .protocol(TranscodeSubtitlesQueryParamProtocol.DASH)
                .secondsPerSegment(5L)
                .subtitleSize(50L)
                .subtitles(QueryParamSubtitles.BURN)
                .videoResolution("1080x1080")
                .copyts(BoolInt.True)
                .videoBitrate(12000L)
                .videoQuality(50L)
                .xPlexClientProfileExtra("add-limitation(scope=videoCodec&scopeName=*&type=upperBound&name=video.frameRate&value=60&replace=true)+append-transcode-target-codec(type=videoProfile&context=streaming&videoCodec=h264%2Chevc&audioCodec=aac&protocol=dash)")
                .xPlexClientProfileName("generic")
                .build();

        TranscodeSubtitlesResponse res = sdk.transcoder().transcodeSubtitles()
                .request(req)
                .call();

        if (res.binaryResponse().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                         | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `request`                                                                         | [TranscodeSubtitlesRequest](../../models/operations/TranscodeSubtitlesRequest.md) | :heavy_check_mark:                                                                | The request object to use for the request.                                        |

### Response

**[TranscodeSubtitlesResponse](../../models/operations/TranscodeSubtitlesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## startTranscodeSession

Starts the transcoder and returns the corresponding streaming resource document.

### Example Usage

<!-- UsageSnippet language="java" operationID="startTranscodeSession" method="get" path="/{transcodeType}/:/transcode/universal/start.{extension}" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.*;
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

        StartTranscodeSessionRequest req = StartTranscodeSessionRequest.builder()
                .transcodeType(TranscodeType.MUSIC)
                .extension(Extension.MPD)
                .advancedSubtitles(AdvancedSubtitles.BURN)
                .audioBoost(50L)
                .audioChannelCount(5L)
                .autoAdjustQuality(BoolInt.True)
                .autoAdjustSubtitle(BoolInt.True)
                .directPlay(BoolInt.True)
                .directStream(BoolInt.True)
                .directStreamAudio(BoolInt.True)
                .disableResolutionRotation(BoolInt.True)
                .hasMDE(BoolInt.True)
                .location(StartTranscodeSessionQueryParamLocation.WAN)
                .mediaBufferSize(102400L)
                .mediaIndex(0L)
                .musicBitrate(5000L)
                .offset(90.5)
                .partIndex(0L)
                .path("/library/metadata/151671")
                .peakBitrate(12000L)
                .photoResolution("1080x1080")
                .protocol(StartTranscodeSessionQueryParamProtocol.DASH)
                .secondsPerSegment(5L)
                .subtitleSize(50L)
                .subtitles(StartTranscodeSessionQueryParamSubtitles.BURN)
                .videoResolution("1080x1080")
                .copyts(BoolInt.True)
                .videoBitrate(12000L)
                .videoQuality(50L)
                .xPlexClientProfileExtra("add-limitation(scope=videoCodec&scopeName=*&type=upperBound&name=video.frameRate&value=60&replace=true)+append-transcode-target-codec(type=videoProfile&context=streaming&videoCodec=h264%2Chevc&audioCodec=aac&protocol=dash)")
                .xPlexClientProfileName("generic")
                .build();

        StartTranscodeSessionResponse res = sdk.transcoder().startTranscodeSession()
                .request(req)
                .call();

        if (res.twoHundredApplicationVndAppleMpegurlBinaryResponse().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                               | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `request`                                                                               | [StartTranscodeSessionRequest](../../models/operations/StartTranscodeSessionRequest.md) | :heavy_check_mark:                                                                      | The request object to use for the request.                                              |

### Response

**[StartTranscodeSessionResponse](../../models/operations/StartTranscodeSessionResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getDASHSegment

DASH segment delivery for adaptive streaming.

### Example Usage

<!-- UsageSnippet language="java" operationID="getDASHSegment" method="get" path="/{transcodeType}/:/transcode/universal/session/{sessionId}/{segmentId}.m4s" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetDASHSegmentRequest;
import dev.plexapi.sdk.models.operations.GetDASHSegmentResponse;
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

        GetDASHSegmentRequest req = GetDASHSegmentRequest.builder()
                .transcodeType("<value>")
                .sessionId("<id>")
                .segmentId("<id>")
                .build();

        GetDASHSegmentResponse res = sdk.transcoder().getDASHSegment()
                .request(req)
                .call();

        if (res.responseStream().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                                 | Type                                                                      | Required                                                                  | Description                                                               |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| `request`                                                                 | [GetDASHSegmentRequest](../../models/operations/GetDASHSegmentRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |

### Response

**[GetDASHSegmentResponse](../../models/operations/GetDASHSegmentResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getHLSSegment

HLS TS segment delivery for adaptive streaming.

### Example Usage

<!-- UsageSnippet language="java" operationID="getHLSSegment" method="get" path="/{transcodeType}/:/transcode/universal/session/{sessionId}/{segmentId}.ts" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetHLSSegmentRequest;
import dev.plexapi.sdk.models.operations.GetHLSSegmentResponse;
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

        GetHLSSegmentRequest req = GetHLSSegmentRequest.builder()
                .transcodeType("<value>")
                .sessionId("<id>")
                .segmentId("<id>")
                .build();

        GetHLSSegmentResponse res = sdk.transcoder().getHLSSegment()
                .request(req)
                .call();

        if (res.responseStream().isPresent()) {
            // handle response
        }
    }
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `request`                                                               | [GetHLSSegmentRequest](../../models/operations/GetHLSSegmentRequest.md) | :heavy_check_mark:                                                      | The request object to use for the request.                              |

### Response

**[GetHLSSegmentResponse](../../models/operations/GetHLSSegmentResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |