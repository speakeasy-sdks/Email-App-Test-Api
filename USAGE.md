<!-- Start SDK Example Usage [usage] -->
```typescript
import { EmailAppTestApi } from "Email-App-Test-Api";

async function run() {
    const sdk = new EmailAppTestApi({
        bearerAuth: "<YOUR_BEARER_TOKEN_HERE>",
    });

    const res = await sdk.groups.postGroupsCreate({
        groupName: "string",
    });

    if (res.statusCode == 200) {
        // handle response
    }
}

run();

```
<!-- End SDK Example Usage [usage] -->