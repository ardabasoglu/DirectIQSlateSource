# Spam Complaints

Every spam complaint event is recorded when a campaign email is opened by the receiver and "Report Unsolicited" link in the footer of the email is clicked.

## Get All Spam Complaints

```shell
curl -X GET \
     https:/restapi.directiq.com/spamcomplaints/{campaingId} \
     -H "user-name: your-user-name" \
     -H "api-key: your-api-key" 
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own campaign id instead of "0101".
var request = new RestRequest("spamcomplaints/0101", Method.GET);

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
    "Id": 53517566,
    "ClientId": 1548549,
    "ContactId": 11230927558,
    "CreatedAt": "2018-04-18T19:40:00",
    "CampaignId": 47222553,
    "Source": "Footer Link"
  }
]
```

This endpoint retrieves all spam complaints of a specified campaign.

### HTTP Request

`GET https://restapi.directiq.com/spamcomplaints/{campaignId}`

### Query Parameters

Parameter | Description
--------- | -----------
campaignId | Campaign id as an integer value.