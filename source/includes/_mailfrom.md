# Mail-Froms

Mail-From email addresses are the ones that you use as a sender address in your email campaigns.

## Get All Mail-Froms

```shell
curl -X GET \
     https:/restapi.directiq.com/mailfroms/ \
     -H "user-name: your-user-name" \
     -H "api-key: your-api-key" 
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

var request = new RestRequest("mailfroms", Method.GET);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");
var response = client.Execute(request);
```

> Response:

```json
[
  {
    "Id": 2486258,
    "ClientId": 1283755,
    "FromEmail": "email@address.com",
    "CreatedAt": "2017-04-26T14:35:23.967",
    "IsConfirmed": true,
    "FromName": "John Smith"
  }
]
```

This endpoint retrieves all mail-froms of your account.

### HTTP Request

`GET https://restapi.directiq.com/mailfroms`

### Query Parameters

None