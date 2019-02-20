# Stats

Stats includes statistics about recepients, bounces, delivers, reads, clicks, spams, unsubscribes, hardbounces, readsUnique, forwards of the specified campaign.

## Get Stats

```shell
curl -X GET \
     https:/restapi.directiq.com/stats/{campaingId} \
     -H "user-name: your-user-name" \
     -H "api-key: your-api-key" 
      
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own campaign id instead of "0101".
var request = new RestRequest("stats/0101", Method.GET);

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
    "CampaignId": 47312249,
    "Recepients": 1183,
    "Bounces": 54,
    "Delivers": 1129,
    "Reads": 451,
    "Clicks": 40,
    "Spams": 1,
    "Unsubscribes": 2,
    "Hardbounces": 9,
    "ReadsUnique": 165,
    "Forwards": 0
  }
]
```

This endpoint retrieves stats of a specified campaign.

### HTTP Request

`GET https://restapi.directiq.com/stats/{campaignId}`

### Query Parameters

Parameter | Description
--------- | -----------
campaignId | Campaign id as an integer value.