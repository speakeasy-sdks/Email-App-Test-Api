<!-- Start SDK Example Usage -->
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