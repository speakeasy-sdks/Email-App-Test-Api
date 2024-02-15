# Groups
(*groups*)

## Overview

Start create groups.

### Available Operations

* [postGroupsCreate](#postgroupscreate) - Create a group

## postGroupsCreate

Create a group

### Example Usage

```typescript
import { EmailAppTestApi } from "Email-App-Test-Api";

async function run() {
  const sdk = new EmailAppTestApi({
    bearerAuth: "<YOUR_BEARER_TOKEN_HERE>",
  });

  const res = await sdk.groups.postGroupsCreate({
    groupName: "<value>",
  });

  if (res.statusCode == 200) {
    // handle response
  }
}

run();
```

### Parameters

| Parameter                                                                  | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `request`                                                                  | [shared.CreateGroupRequest](../../sdk/models/shared/creategrouprequest.md) | :heavy_check_mark:                                                         | The request object to use for the request.                                 |
| `config`                                                                   | [AxiosRequestConfig](https://axios-http.com/docs/req_config)               | :heavy_minus_sign:                                                         | Available config options for making requests.                              |


### Response

**Promise<[operations.PostGroupsCreateResponse](../../sdk/models/operations/postgroupscreateresponse.md)>**
### Errors

| Error Object    | Status Code     | Content Type    |
| --------------- | --------------- | --------------- |
| errors.SDKError | 4xx-5xx         | */*             |
