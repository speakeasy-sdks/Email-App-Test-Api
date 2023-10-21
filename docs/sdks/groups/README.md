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

(async() => {
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

### Parameters

| Parameter                                                              | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `request`                                                              | [shared.CreateGroupRequest](../../models/shared/creategrouprequest.md) | :heavy_check_mark:                                                     | The request object to use for the request.                             |
| `config`                                                               | [AxiosRequestConfig](https://axios-http.com/docs/req_config)           | :heavy_minus_sign:                                                     | Available config options for making requests.                          |


### Response

**Promise<[operations.PostGroupsCreateResponse](../../models/operations/postgroupscreateresponse.md)>**

