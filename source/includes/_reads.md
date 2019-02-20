# Reads

Every read event is recorded when a campaign email is opened by the reciever.

## Get All Reads

```shell
curl -X GET \
     https:/restapi.directiq.com/reads/{campaingId} \
     -H "user-name: your-user-name" \
     -H "api-key: your-api-key" 
     
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own campaign id instead of "0101".
var request = new RestRequest("reads/0101", Method.GET);

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
    "Id": 197403757,
    "ClientId": 55849,
    "CampaignId": 54668772,
    "ContactId": 11304932758,
    "CreatedAt": "2018-03-20T18:13:00",
    "IpAddress": "61.101.18.144",
    "IpLong": 11131343020,
    "CountryCode": "US",
    "CountryName": "United States",
    "City": "",
    "Device": "PC",
    "Region": "Florida",
    "UserAgent": "Mozilla/5.0 (Windows NT 5.1; rv:11.0) 
        Gecko Firefox/11.0 (via ggpht.com GoogleImageProxy)"
  }
]
```

This endpoint retrieves all reads of a specified campaign.

### HTTP Request

`GET https://restapi.directiq.com/reads/{campaignId}`

### Query Parameters

Parameter | Description
--------- | -----------
campaignId | Campaign id as an integer value.