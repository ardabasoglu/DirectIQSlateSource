# Contact Lists

Contact lists are containers which hold contact objects that you use for your campaigns.

## Get All Contact Lists

```shell
curl -X GET \
     https://restapi.directiq.com/contactlists \
     -H "user-name: your-user-name" \
     -H "api-key: your-api-key" 
         
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

var request = new RestRequest("contactlists", Method.GET);

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
        "Id": 587658,
        "Name": "777",
        "LastUpdate": "2018-04-19T11:23:00",
        "Count": 773,
        "ClientId": 8765786,
        "Active": 0,
        "Passive": 0,
        "HashId": "00000000-0000-0000-0000-000000000000",
        "IsLocked": 0,
        "IsVisible": true,
        "IsDoubleOptIn": false
    }
]
```

This endpoint retrieves all of your contact lists.

### HTTP Request

`GET https://restapi.directiq.com/contactlists`

### Query Parameters

None

## Get Contact List by Id

```shell
curl -X GET \
  https://restapi.directiq.com/contactlists/view/{listId} \
  -H 'api-key: your-api-key' \
  -H 'user-name: your-user-name'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own list id instead of "65767676" 
var request = new RestRequest("contactlists/view/65767676", Method.GET);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");
var response = client.Execute(request);
```

> Response:

```json
{
    "Id": 65767676,
    "Name": "777",
    "LastUpdate": "2018-04-19T11:23:00",
    "Count": 773,
    "ClientId": 7437905,
    "Active": 0,
    "Passive": 0,
    "HashId": "00000000-0000-0000-0000-000000000000",
    "IsLocked": 0,
    "IsVisible": true,
    "IsDoubleOptIn": false
}
```

This endpoint retrieves the specified contact list by its id.

### HTTP Request

`GET https://restapi.directiq.com/contactlists/view/{listId}`

### Query Parameters

Parameter | Description
--------- | -----------
listId    | List id as an integer value.

## Create a Contact List

```shell
curl -X POST \
   https://restapi.directiq.com/contactlists?name={MyListName} \
  -H 'api-key: your-api-key' \
  -H 'user-name: your-user-name'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own list name instead of "your-list-name" 
var request = new RestRequest("contactlists?name=your-list-name", Method.POST);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");
var response = client.Execute(request);
```

> Response:

```json
133718 // integer value of list id.
```

This endpoint creates a contact list given its name.

### HTTP Request

`POST https://restapi.directiq.com/contactlists?name={your-list-name}`

### Query Parameters

Parameter | Description
--------- | -----------
name      | Name as a string value.

## Delete a List

```shell
curl -X DELETE \
  https://restapi.directiq.com/contactlists/delete/{listId} \
  -H 'api-key: your-api-key' \
  -H 'user-name: your-user-name'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own list id instead of 56353 
var request = new RestRequest("contactlists/delete/56353", Method.DELETE);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");
var response = client.Execute(request);
```

> Response:

```json
56353 // integer value of list id.
```

This endpoint deletes a contact list given its id.

### HTTP Request

`DELETE https://restapi.directiq.com/contactlists/delete/{listId}`

### Query Parameters

Parameter | Description
--------- | -----------
listId    | List id as an integer value.