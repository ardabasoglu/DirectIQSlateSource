# Clicks

Every click event is recorded when a campaign email is opened and the receiver clicks on any link on that email.

## Get All Clicks

```shell
curl -X GET  \
     https:/restapi.directiq.com/clicks/{campaingId} \
     -H "user-name: your-user-name" \
     -H "api-key: your-api-key" 
     
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own campaign id instead of "0101".
var request = new RestRequest("clicks/0101", Method.GET);

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
    "Id": 23435670,
    "ClientId": 1538491,
    "CampaignId": 46873723,
    "Link": "http://www.directiq10.com/FORWARD/NDY4NzcyLTExMzA5Mjc1OA==",
    "CreatedAt": "2018-03-20T18:14:00",
    "IpAddrees": "23.226.128.51",
    "IpLong": "400719923",
    "CountryCode": "US",
    "CountryName": "United States",
    "City": "Jacksonville",
    "LinkId": 4,
    "Region": "Florida",
    "UserAgent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) 
        AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.186 Safari/537.36",
    "Device": "PC"
  }
]
```

This endpoint retrieves all clicks of a specified campaign.

### HTTP Request

`GET https://restapi.directiq.com/clicks/{campaignId}`

### Query Parameters

Parameter | Description
--------- | -----------
campaignId | Campaign id as an integer value.