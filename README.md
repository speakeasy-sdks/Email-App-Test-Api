# Email-App-Test-Api

<div align="left">
    <a href="https://speakeasyapi.dev/"><img src="https://custom-icon-badges.demolab.com/badge/-Built%20By%20Speakeasy-212015?style=for-the-badge&logoColor=FBE331&logo=speakeasy&labelColor=545454" /></a>
    <a href="https://github.com/speakeasy-sdks/Email-App-Test-Api.git/actions"><img src="https://img.shields.io/github/actions/workflow/status/speakeasy-sdks/Email-App-Test-Api/speakeasy_sdk_generation.yml?style=for-the-badge" /></a>
    
</div>

<!-- Start SDK Installation -->
## SDK Installation

### NPM

```bash
npm add https://github.com/speakeasy-sdks/Email-App-Test-Api
```

### Yarn

```bash
yarn add https://github.com/speakeasy-sdks/Email-App-Test-Api
```
<!-- End SDK Installation -->

## SDK Example Usage
<!-- Start SDK Example Usage -->
### Example

```typescript
import { EmailAppTestApi } from "Email-App-Test-Api";

(async () => {
    const sdk = new EmailAppTestApi({
        bearerAuth: "",
    });

    const res = await sdk.groups.postGroupsCreate({
        groupName: "string",
    });

    if (res.statusCode == 200) {
        // handle response
    }
})();

```
<!-- End SDK Example Usage -->

<!-- Start SDK Available Operations -->
## Available Resources and Operations


### [groups](docs/sdks/groups/README.md)

* [postGroupsCreate](docs/sdks/groups/README.md#postgroupscreate) - Create a group
<!-- End SDK Available Operations -->

<!-- Start Dev Containers -->

<!-- End Dev Containers -->



<!-- Start Error Handling -->
## Error Handling

Handling errors in this SDK should largely match your expectations.  All operations return a response object or throw an error.  If Error objects are specified in your OpenAPI Spec, the SDK will throw the appropriate Error type.

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 400-600         | */*             |

Example

```typescript
import { EmailAppTestApi } from "Email-App-Test-Api";

(async () => {
    const sdk = new EmailAppTestApi({
        bearerAuth: "",
    });

    let res;
    try {
        res = await sdk.groups.postGroupsCreate({
            groupName: "string",
        });
    } catch (e) {}

    if (res.statusCode == 200) {
        // handle response
    }
})();

```
<!-- End Error Handling -->



<!-- Start Server Selection -->
## Server Selection

### Select Server by Index

You can override the default server globally by passing a server index to the `serverIdx: number` optional parameter when initializing the SDK client instance. The selected server will then be used as the default on the operations that use it. This table lists the indexes associated with the available servers:

| # | Server | Variables |
| - | ------ | --------- |
| 0 | `https://api.koldmail.com/v1` | None |

#### Example

```typescript
import { EmailAppTestApi } from "Email-App-Test-Api";

(async () => {
    const sdk = new EmailAppTestApi({
        serverIdx: 0,
        bearerAuth: "",
    });

    const res = await sdk.groups.postGroupsCreate({
        groupName: "string",
    });

    if (res.statusCode == 200) {
        // handle response
    }
})();

```


### Override Server URL Per-Client

The default server can also be overridden globally by passing a URL to the `serverURL: str` optional parameter when initializing the SDK client instance. For example:
```typescript
import { EmailAppTestApi } from "Email-App-Test-Api";

(async () => {
    const sdk = new EmailAppTestApi({
        serverURL: "https://api.koldmail.com/v1",
        bearerAuth: "",
    });

    const res = await sdk.groups.postGroupsCreate({
        groupName: "string",
    });

    if (res.statusCode == 200) {
        // handle response
    }
})();

```
<!-- End Server Selection -->



<!-- Start Custom HTTP Client -->
## Custom HTTP Client

The Typescript SDK makes API calls using the (axios)[https://axios-http.com/docs/intro] HTTP library.  In order to provide a convenient way to configure timeouts, cookies, proxies, custom headers, and other low-level configuration, you can initialize the SDK client with a custom `AxiosInstance` object.

For example, you could specify a header for every request that your sdk makes as follows:

```typescript
from Email-App-Test-Api import EmailAppTestApi;
import axios;

const httpClient = axios.create({
    headers: {'x-custom-header': 'someValue'}
})

const sdk = new EmailAppTestApi({defaultClient: httpClient});
```
<!-- End Custom HTTP Client -->



<!-- Start Authentication -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name         | Type         | Scheme       |
| ------------ | ------------ | ------------ |
| `bearerAuth` | http         | HTTP Bearer  |

To authenticate with the API the `bearerAuth` parameter must be set when initializing the SDK client instance. For example:
```typescript
import { EmailAppTestApi } from "Email-App-Test-Api";

(async () => {
    const sdk = new EmailAppTestApi({
        bearerAuth: "",
    });

    const res = await sdk.groups.postGroupsCreate({
        groupName: "string",
    });

    if (res.statusCode == 200) {
        // handle response
    }
})();

```
<!-- End Authentication -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically.
Feel free to open a PR or a Github issue as a proof of concept and we'll do our best to include it in a future release!

### SDK Created by [Speakeasy](https://docs.speakeasyapi.dev/docs/using-speakeasy/client-sdks)
