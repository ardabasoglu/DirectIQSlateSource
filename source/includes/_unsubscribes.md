# Unsubscribes

Every unsubscribe event is recorded when a campaign email is opened by the receiver and "Unsubscribe" link in the footer of the email is clicked.

## Get All Unsubscribes

```shell
curl -X GET \
     https:/restapi.directiq.com/unsubscribes/{campaingId} \
     -H "user-name: your-user-name" \
     -H "api-key: your-api-key" 
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own campaign id instead of "0101".
var request = new RestRequest("unsubscribes/0101", Method.GET);

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
    "Id": 23159386,
    "ClientId": 1837355,
    "CampaignId": 47315229,
    "ContactId": 124652349787,
    "CreatedAt": "2018-04-10T10:35:00",
    "Email": "someone@someaddress.com",
    "FirstName": "John",
    "LastName": "Smith"
  }
]
```

This endpoint retrieves all unsubscribes of a specified campaign.

### HTTP Request

`GET https://restapi.directiq.com/unsubscribes/{campaignId}`

### Query Parameters

Parameter | Description
--------- | -----------
campaignId | Campaign id as an integer value.