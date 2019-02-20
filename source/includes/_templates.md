# Templates

Templates are the email contents generally in the HTML form that you use in your campaigns.

## Get All Templates

```shell
curl -X GET \
     https:/restapi.directiq.com/templates \
     -H "user-name: your-user-name" \
     -H "api-key: your-api-key"
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

var request = new RestRequest("templates", Method.GET);

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
    "Id": 252534,
    "Name": "Test 001",
    "Subject": "Test 001",
    "Body": "<html>\r\n<head>\r\n\t<title></title>\r\n\t\r\n</head>
        \r\n<body>\r\n<p>Template body.</p>\r\n</body>\r\n</html>\r\n",
    "TextBody": "\r\n\r\n\t\r\n\t\r\n\r\n\r\nTemplate body.\r\n\r\n\r\n",
    "UpdateDate": "2018-04-23T11:31:00"
  }
]
```

This endpoint retrieves all of your templates.

### HTTP Request

`GET https://restapi.directiq.com/templates`

### Query Parameters

None

## Create a Template

```shell
curl -X POST \
  https:/restapi.directiq.com/templates \
  -H 'api-key: your-api-key' \
  -H 'content-type: application/json' \
  -H 'user-name: your-user-name' \
  -d '{"Name":"Auto Test","Subject":"Auto Test","Body":"<html><body><p>Auto Test</p>
      </body></html>","TextBody":"Auto Test","UpdateDate":"4/5/2018 2:00:09 PM"}'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

var request = new RestRequest("templates", Method.POST);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");

request.AddParameter("application/json", "{\"Name\":\"Auto Test\",\"Subject\":\"Auto Test\",
    \"Body\":\"<html><body><p>Auto Test</p></body></html>\",
    \"TextBody\":\"Auto Test\",\"UpdateDate\":\"4/5/2018 2:00:09 PM\"}",
    ParameterType.RequestBody);

var response = client.Execute(request);
```

> Response:

```json
{
  "Id": 0,
  "Name": "Auto Test",
  "Subject": "Auto Test",
  "Body": "<html><body><p>Auto Test</p></body></html>",
  "TextBody": "Auto Test",
  "UpdateDate": "2018-04-05T14:00:09"
}
```

This endpoint creates a template.

### HTTP Request

`POST https://restapi.directiq.com/templates`

### Query Parameters

None