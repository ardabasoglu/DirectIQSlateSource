# Campaigns

Campaigns are the heart of the DirectIQ system. They hold many important information like your email template, delivery email lists and schedules for sending.

## Get All Campaigns

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

var request = new RestRequest("campaigns", Method.GET);

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
        "Id": 45365632222,
        "Name": "Auto Test",
        "Subject": "Auto Test",
        "TemplateId": 52563563,
        "ListIds": null,
        "TimeToSend": "2018-04-05T07:00:09",
        "SenderEmailId": 0
    }
]
```

This endpoint retrieves all of your campaigns.

### HTTP Request

`GET https://restapi.directiq.com/campaigns`

### Query Parameters

None

## Create a Campaign

```shell
curl -X POST \
  https://restapi.directiq.com/campaigns \
  -H 'api-key: your-api-key' \
  -H 'content-type: application/json' \
  -H 'user-name: your-user-name' \
  -d '{"Name" : "My Campaign","Subject" : "My Subject","TemplateId" : 534453,
     "ListIds" : [132664564576], "TimeToSend" : "4/11/2018 2:00:00 PM",
     "SenderEmailId" : 28312378}'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

var request = new RestRequest("campaigns", Method.POST);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");

request.AddParameter("application/json", "{\"Name\" : \"My Campaign\",
    \"Subject\" : \"My Subject\",\"TemplateId\" : 534453,\"ListIds\" : [132664564576],
    \"TimeToSend\" : \"4/11/2018 2:00:00 PM\",\"SenderEmailId\" : 28312378}",
    ParameterType.RequestBody);

var response = client.Execute(request);
```

> Response:

```json
{
    "Id": 0,
    "Name": "My Campaign",
    "Subject": "My Subject",
    "TemplateId": 534453,
    "ListIds": [
        132664564576
    ],
    "TimeToSend": "2018-04-11T14:00:00",
    "SenderEmailId": 28312378
}
```

This endpoint creates a campaign.

### HTTP Request

`POST https://restapi.directiq.com/campaigns`

### Query Parameters

None