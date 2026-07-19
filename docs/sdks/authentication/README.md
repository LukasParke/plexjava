# Authentication

## Overview

Plex Authentication operations

### Available Operations

* [registerDeviceJWK](#registerdevicejwk) - Register Device JWK
* [getAuthKeys](#getauthkeys) - Get Auth Keys
* [getAuthNonce](#getauthnonce) - Get Auth Nonce
* [exchangeJWTToken](#exchangejwttoken) - Exchange JWT Token
* [getClaimToken](#getclaimtoken) - Get Claim Token
* [getFeatures](#getfeatures) - Get Features
* [ping](#ping) - Ping the server
* [createOAuthPin](#createoauthpin) - Create OAuth PIN
* [createLegacyPin](#createlegacypin) - Create Legacy PIN
* [linkOAuthPin](#linkoauthpin) - Link OAuth PIN
* [getServerAccessTokens](#getserveraccesstokens) - Get Server Access Tokens
* [getTokenDetails](#gettokendetails) - Get Token Details
* [changePassword](#changepassword) - Change Password
* [postUsersSignInData](#postuserssignindata) - Get User Sign In Data
* [signOut](#signout) - Sign Out
* [switchHomeUser](#switchhomeuser) - Switch Home User
* [getOAuthPin](#getoauthpin) - Get OAuth PIN Status

## registerDeviceJWK

Register a device public key (JWK) for JWT-based authentication.

### Example Usage

<!-- UsageSnippet language="java" operationID="registerDeviceJWK" method="post" path="/auth/jwk" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.RegisterDeviceJWKRequest;
import dev.plexapi.sdk.models.operations.RegisterDeviceJWKResponse;
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

        RegisterDeviceJWKRequest req = RegisterDeviceJWKRequest.builder()
                .jwkRegistrationRequest(JWKRegistrationRequest.builder()
                    .jwk(Jwk.builder()
                        .crv("string value")
                        .kid("string value")
                        .kty("string value")
                        .x("string value")
                        .build())
                    .build())
                .build();

        RegisterDeviceJWKResponse res = sdk.authentication().registerDeviceJWK()
                .request(req)
                .call();

        if (res.authTokenResponse().isPresent()) {
            System.out.println(res.authTokenResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                       | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `request`                                                                       | [RegisterDeviceJWKRequest](../../models/operations/RegisterDeviceJWKRequest.md) | :heavy_check_mark:                                                              | The request object to use for the request.                                      |
| `serverURL`                                                                     | *String*                                                                        | :heavy_minus_sign:                                                              | An optional server URL to use.                                                  |

### Response

**[RegisterDeviceJWKResponse](../../models/operations/RegisterDeviceJWKResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getAuthKeys

Get Plex public JWKs for signature verification.

### Example Usage

<!-- UsageSnippet language="java" operationID="getAuthKeys" method="get" path="/auth/keys" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetAuthKeysRequest;
import dev.plexapi.sdk.models.operations.GetAuthKeysResponse;
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

        GetAuthKeysRequest req = GetAuthKeysRequest.builder()
                .build();

        GetAuthKeysResponse res = sdk.authentication().getAuthKeys()
                .request(req)
                .call();

        if (res.authKeysResponse().isPresent()) {
            System.out.println(res.authKeysResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                           | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `request`                                                           | [GetAuthKeysRequest](../../models/operations/GetAuthKeysRequest.md) | :heavy_check_mark:                                                  | The request object to use for the request.                          |
| `serverURL`                                                         | *String*                                                            | :heavy_minus_sign:                                                  | An optional server URL to use.                                      |

### Response

**[GetAuthKeysResponse](../../models/operations/GetAuthKeysResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getAuthNonce

Get a nonce to sign in client JWT authentication flow.

### Example Usage

<!-- UsageSnippet language="java" operationID="getAuthNonce" method="get" path="/auth/nonce" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetAuthNonceRequest;
import dev.plexapi.sdk.models.operations.GetAuthNonceResponse;
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

        GetAuthNonceRequest req = GetAuthNonceRequest.builder()
                .build();

        GetAuthNonceResponse res = sdk.authentication().getAuthNonce()
                .request(req)
                .call();

        if (res.authNonceResponse().isPresent()) {
            System.out.println(res.authNonceResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                             | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `request`                                                             | [GetAuthNonceRequest](../../models/operations/GetAuthNonceRequest.md) | :heavy_check_mark:                                                    | The request object to use for the request.                            |
| `serverURL`                                                           | *String*                                                              | :heavy_minus_sign:                                                    | An optional server URL to use.                                        |

### Response

**[GetAuthNonceResponse](../../models/operations/GetAuthNonceResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## exchangeJWTToken

Exchange a signed client JWT for a Plex JWT token.

### Example Usage

<!-- UsageSnippet language="java" operationID="exchangeJWTToken" method="post" path="/auth/token" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.ExchangeJWTTokenRequest;
import dev.plexapi.sdk.models.operations.ExchangeJWTTokenResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import dev.plexapi.sdk.models.shared.TokenExchangeRequest;
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

        ExchangeJWTTokenRequest req = ExchangeJWTTokenRequest.builder()
                .tokenExchangeRequest(TokenExchangeRequest.builder()
                    .clientIdentifier("string value")
                    .jwt("string value")
                    .scope("string value")
                    .build())
                .build();

        ExchangeJWTTokenResponse res = sdk.authentication().exchangeJWTToken()
                .request(req)
                .call();

        if (res.authTokenResponse().isPresent()) {
            System.out.println(res.authTokenResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                     | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `request`                                                                     | [ExchangeJWTTokenRequest](../../models/operations/ExchangeJWTTokenRequest.md) | :heavy_check_mark:                                                            | The request object to use for the request.                                    |
| `serverURL`                                                                   | *String*                                                                      | :heavy_minus_sign:                                                            | An optional server URL to use.                                                |

### Response

**[ExchangeJWTTokenResponse](../../models/operations/ExchangeJWTTokenResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getClaimToken

Get a claim token for new server setup.

### Example Usage

<!-- UsageSnippet language="java" operationID="getClaimToken" method="get" path="/claim/token.json" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetClaimTokenRequest;
import dev.plexapi.sdk.models.operations.GetClaimTokenResponse;
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

        GetClaimTokenRequest req = GetClaimTokenRequest.builder()
                .build();

        GetClaimTokenResponse res = sdk.authentication().getClaimToken()
                .request(req)
                .call();

        if (res.claimTokenResponse().isPresent()) {
            System.out.println(res.claimTokenResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                               | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `request`                                                               | [GetClaimTokenRequest](../../models/operations/GetClaimTokenRequest.md) | :heavy_check_mark:                                                      | The request object to use for the request.                              |
| `serverURL`                                                             | *String*                                                                | :heavy_minus_sign:                                                      | An optional server URL to use.                                          |

### Response

**[GetClaimTokenResponse](../../models/operations/GetClaimTokenResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getFeatures

Get Plex Pass feature flags for the logged-in user.

### Example Usage

<!-- UsageSnippet language="java" operationID="getFeatures" method="get" path="/features" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetFeaturesResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        GetFeaturesResponse res = sdk.authentication().getFeatures()
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                      | Type                           | Required                       | Description                    |
| ------------------------------ | ------------------------------ | ------------------------------ | ------------------------------ |
| `serverURL`                    | *String*                       | :heavy_minus_sign:             | An optional server URL to use. |

### Response

**[GetFeaturesResponse](../../models/operations/GetFeaturesResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## ping

Health / latency check. No authentication required.

### Example Usage

<!-- UsageSnippet language="java" operationID="ping" method="get" path="/ping" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.PingResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
            .build();

        PingResponse res = sdk.authentication().ping()
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                      | Type                           | Required                       | Description                    |
| ------------------------------ | ------------------------------ | ------------------------------ | ------------------------------ |
| `serverURL`                    | *String*                       | :heavy_minus_sign:             | An optional server URL to use. |

### Response

**[PingResponse](../../models/operations/PingResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## createOAuthPin

Create a 4-character PIN for device linking via OAuth. The user must visit https://plex.tv/link and enter the PIN to authorize the device.

### Example Usage

<!-- UsageSnippet language="java" operationID="createOAuthPin" method="post" path="/pins" -->
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
            .build();

        CreateOAuthPinRequest req = CreateOAuthPinRequest.builder()
                .build();

        CreateOAuthPinResponse res = sdk.authentication().createOAuthPin()
                .request(req)
                .security(CreateOAuthPinSecurity.builder()
                    .clientIdentifier(System.getenv().getOrDefault("CLIENT_IDENTIFIER", ""))
                    .build())
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                                     | Type                                                                                                          | Required                                                                                                      | Description                                                                                                   |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| `request`                                                                                                     | [CreateOAuthPinRequest](../../models/operations/CreateOAuthPinRequest.md)                                     | :heavy_check_mark:                                                                                            | The request object to use for the request.                                                                    |
| `security`                                                                                                    | [dev.plexapi.sdk.models.operations.CreateOAuthPinSecurity](../../models/operations/CreateOAuthPinSecurity.md) | :heavy_check_mark:                                                                                            | The security requirements to use for the request.                                                             |
| `serverURL`                                                                                                   | *String*                                                                                                      | :heavy_minus_sign:                                                                                            | An optional server URL to use.                                                                                |

### Response

**[CreateOAuthPinResponse](../../models/operations/CreateOAuthPinResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## createLegacyPin

Legacy PIN creation (XML).

### Example Usage

<!-- UsageSnippet language="java" operationID="createLegacyPin" method="post" path="/pins.xml" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.CreateLegacyPinResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        CreateLegacyPinResponse res = sdk.authentication().createLegacyPin()
                .call();

        if (res.body().isPresent()) {
            System.out.println(res.body().get());
        }
    }
}
```

### Parameters

| Parameter                      | Type                           | Required                       | Description                    |
| ------------------------------ | ------------------------------ | ------------------------------ | ------------------------------ |
| `serverURL`                    | *String*                       | :heavy_minus_sign:             | An optional server URL to use. |

### Response

**[CreateLegacyPinResponse](../../models/operations/CreateLegacyPinResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## linkOAuthPin

Link a PIN to an account (OAuth completion).

### Example Usage

<!-- UsageSnippet language="java" operationID="linkOAuthPin" method="put" path="/pins/link" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.LinkOAuthPinAuthenticationRequestBody;
import dev.plexapi.sdk.models.operations.LinkOAuthPinResponse;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws Error, Exception {

        PlexAPI sdk = PlexAPI.builder()
                .token(System.getenv().getOrDefault("TOKEN", ""))
            .build();

        LinkOAuthPinAuthenticationRequestBody req = LinkOAuthPinAuthenticationRequestBody.builder()
                .authToken("example")
                .pin("example")
                .build();

        LinkOAuthPinResponse res = sdk.authentication().linkOAuthPin()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                                 | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `request`                                                                                                 | [LinkOAuthPinAuthenticationRequestBody](../../models/operations/LinkOAuthPinAuthenticationRequestBody.md) | :heavy_check_mark:                                                                                        | The request object to use for the request.                                                                |
| `serverURL`                                                                                               | *String*                                                                                                  | :heavy_minus_sign:                                                                                        | An optional server URL to use.                                                                            |

### Response

**[LinkOAuthPinResponse](../../models/operations/LinkOAuthPinResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getServerAccessTokens

List access tokens for the server.

### Example Usage

<!-- UsageSnippet language="java" operationID="getServerAccessTokens" method="get" path="/server/access_tokens" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.GetServerAccessTokensRequest;
import dev.plexapi.sdk.models.operations.GetServerAccessTokensResponse;
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

        GetServerAccessTokensRequest req = GetServerAccessTokensRequest.builder()
                .build();

        GetServerAccessTokensResponse res = sdk.authentication().getServerAccessTokens()
                .request(req)
                .call();

        if (res.serverAccessTokensResponse().isPresent()) {
            System.out.println(res.serverAccessTokensResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                                               | Type                                                                                    | Required                                                                                | Description                                                                             |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `request`                                                                               | [GetServerAccessTokensRequest](../../models/operations/GetServerAccessTokensRequest.md) | :heavy_check_mark:                                                                      | The request object to use for the request.                                              |
| `serverURL`                                                                             | *String*                                                                                | :heavy_minus_sign:                                                                      | An optional server URL to use.                                                          |

### Response

**[GetServerAccessTokensResponse](../../models/operations/GetServerAccessTokensResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getTokenDetails

Get the User data from the provided X-Plex-Token

### Example Usage

<!-- UsageSnippet language="java" operationID="getTokenDetails" method="get" path="/user" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.BadRequest;
import dev.plexapi.sdk.models.errors.Unauthorized;
import dev.plexapi.sdk.models.operations.GetTokenDetailsRequest;
import dev.plexapi.sdk.models.operations.GetTokenDetailsResponse;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws BadRequest, Unauthorized, Exception {

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

        GetTokenDetailsRequest req = GetTokenDetailsRequest.builder()
                .build();

        GetTokenDetailsResponse res = sdk.authentication().getTokenDetails()
                .request(req)
                .call();

        if (res.userPlexAccount().isPresent()) {
            System.out.println(res.userPlexAccount().get());
        }
    }
}
```

### Parameters

| Parameter                                                                   | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `request`                                                                   | [GetTokenDetailsRequest](../../models/operations/GetTokenDetailsRequest.md) | :heavy_check_mark:                                                          | The request object to use for the request.                                  |
| `serverURL`                                                                 | *String*                                                                    | :heavy_minus_sign:                                                          | An optional server URL to use.                                              |

### Response

**[GetTokenDetailsResponse](../../models/operations/GetTokenDetailsResponse.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models/errors/BadRequest   | 400                        | application/json           |
| models/errors/Unauthorized | 401                        | application/json           |
| models/errors/SDKError     | 4XX, 5XX                   | \*/\*                      |

## changePassword

Change or reset the logged-in user's password.

### Example Usage

<!-- UsageSnippet language="java" operationID="changePassword" method="post" path="/users/password" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.ChangePasswordRequest;
import dev.plexapi.sdk.models.operations.ChangePasswordResponse;
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

        ChangePasswordRequest req = ChangePasswordRequest.builder()
                .build();

        ChangePasswordResponse res = sdk.authentication().changePassword()
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
| `request`                                                                 | [ChangePasswordRequest](../../models/operations/ChangePasswordRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |
| `serverURL`                                                               | *String*                                                                  | :heavy_minus_sign:                                                        | An optional server URL to use.                                            |

### Response

**[ChangePasswordResponse](../../models/operations/ChangePasswordResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## postUsersSignInData

Sign in user with username and password and return user data with Plex authentication token

### Example Usage

<!-- UsageSnippet language="java" operationID="postUsersSignInData" method="post" path="/users/signin" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.BadRequest;
import dev.plexapi.sdk.models.errors.Unauthorized;
import dev.plexapi.sdk.models.operations.*;
import dev.plexapi.sdk.models.shared.Accepts;
import java.lang.Exception;

public class Application {

    public static void main(String[] args) throws BadRequest, Unauthorized, Exception {

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
            .build();

        PostUsersSignInDataRequest req = PostUsersSignInDataRequest.builder()
                .requestBody(PostUsersSignInDataRequestBody.builder()
                    .login("username@email.com")
                    .password("password123")
                    .rememberMe(true)
                    .verificationCode("123456")
                    .build())
                .build();

        PostUsersSignInDataResponse res = sdk.authentication().postUsersSignInData()
                .request(req)
                .call();

        if (res.userPlexAccount().isPresent()) {
            System.out.println(res.userPlexAccount().get());
        }
    }
}
```

### Parameters

| Parameter                                                                           | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `request`                                                                           | [PostUsersSignInDataRequest](../../models/operations/PostUsersSignInDataRequest.md) | :heavy_check_mark:                                                                  | The request object to use for the request.                                          |
| `serverURL`                                                                         | *String*                                                                            | :heavy_minus_sign:                                                                  | An optional server URL to use.                                                      |

### Response

**[PostUsersSignInDataResponse](../../models/operations/PostUsersSignInDataResponse.md)**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| models/errors/BadRequest   | 400                        | application/json           |
| models/errors/Unauthorized | 401                        | application/json           |
| models/errors/SDKError     | 4XX, 5XX                   | \*/\*                      |

## signOut

Invalidate the current authentication token.

### Example Usage

<!-- UsageSnippet language="java" operationID="signOut" method="delete" path="/users/signout" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.operations.SignOutRequest;
import dev.plexapi.sdk.models.operations.SignOutResponse;
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

        SignOutRequest req = SignOutRequest.builder()
                .build();

        SignOutResponse res = sdk.authentication().signOut()
                .request(req)
                .call();

        if (res.successResponse().isPresent()) {
            System.out.println(res.successResponse().get());
        }
    }
}
```

### Parameters

| Parameter                                                   | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `request`                                                   | [SignOutRequest](../../models/operations/SignOutRequest.md) | :heavy_check_mark:                                          | The request object to use for the request.                  |
| `serverURL`                                                 | *String*                                                    | :heavy_minus_sign:                                          | An optional server URL to use.                              |

### Response

**[SignOutResponse](../../models/operations/SignOutResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## switchHomeUser

Switch to a Plex Home user and return a new auth token.

### Example Usage

<!-- UsageSnippet language="java" operationID="switchHomeUser" method="post" path="/home/users/{id}/switch" -->
```java
package hello.world;

import dev.plexapi.sdk.PlexAPI;
import dev.plexapi.sdk.models.errors.Error;
import dev.plexapi.sdk.models.operations.SwitchHomeUserRequest;
import dev.plexapi.sdk.models.operations.SwitchHomeUserResponse;
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

        SwitchHomeUserRequest req = SwitchHomeUserRequest.builder()
                .id(135337L)
                .build();

        SwitchHomeUserResponse res = sdk.authentication().switchHomeUser()
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
| `request`                                                                 | [SwitchHomeUserRequest](../../models/operations/SwitchHomeUserRequest.md) | :heavy_check_mark:                                                        | The request object to use for the request.                                |
| `serverURL`                                                               | *String*                                                                  | :heavy_minus_sign:                                                        | An optional server URL to use.                                            |

### Response

**[SwitchHomeUserResponse](../../models/operations/SwitchHomeUserResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |

## getOAuthPin

Poll the PIN status. Returns authToken when the user has linked the device.

### Example Usage

<!-- UsageSnippet language="java" operationID="getOAuthPin" method="get" path="/pins/{pinId}" -->
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
            .build();

        GetOAuthPinRequest req = GetOAuthPinRequest.builder()
                .pinId(876892L)
                .build();

        GetOAuthPinResponse res = sdk.authentication().getOAuthPin()
                .request(req)
                .security(GetOAuthPinSecurity.builder()
                    .clientIdentifier(System.getenv().getOrDefault("CLIENT_IDENTIFIER", ""))
                    .build())
                .call();

        if (res.object().isPresent()) {
            System.out.println(res.object().get());
        }
    }
}
```

### Parameters

| Parameter                                                                                               | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `request`                                                                                               | [GetOAuthPinRequest](../../models/operations/GetOAuthPinRequest.md)                                     | :heavy_check_mark:                                                                                      | The request object to use for the request.                                                              |
| `security`                                                                                              | [dev.plexapi.sdk.models.operations.GetOAuthPinSecurity](../../models/operations/GetOAuthPinSecurity.md) | :heavy_check_mark:                                                                                      | The security requirements to use for the request.                                                       |
| `serverURL`                                                                                             | *String*                                                                                                | :heavy_minus_sign:                                                                                      | An optional server URL to use.                                                                          |

### Response

**[GetOAuthPinResponse](../../models/operations/GetOAuthPinResponse.md)**

### Errors

| Error Type             | Status Code            | Content Type           |
| ---------------------- | ---------------------- | ---------------------- |
| models/errors/Error    | 401                    | application/json       |
| models/errors/SDKError | 4XX, 5XX               | \*/\*                  |