# Authentication

> Use your DirectiQ user name and API key in headers to authorize:

```shell
curl -X GET \
  https:/restapi.directiq.com/campaigns \
  -H 'api-key: your-api-key' \
  -H 'user-name: your-user-name'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own campaign id istead of "0101".
var request = new RestRequest("clicks/0101", Method.GET);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");
```

> Make sure to replace `your-api-key` with your API key, and `your-user-name` with your DirectIQ user name.

All you need to do is to use your DirectIQ <b>user name</b> and <b>API key</b> and pass them as headers with each call to our API endpoints.

You can access your API key from <b>My Account > Social Media & Integrations > API Integration</b> in your DirectIQ dashboard.

If you are not a registered DirectIQ user, you can [register here](https://www.directiq.com).