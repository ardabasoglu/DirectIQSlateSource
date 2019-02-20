# Contacts

Contact info holds the email address and other details like first name, last name and etc.

## Get All Contacts

```shell
curl -X GET \
  https://restapi.directiq.com/contacts/view \
  -H 'api-key: your-api-key' \
  -H 'user-name: your-user-name'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

var request = new RestRequest("contacts/view", Method.GET);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");
var response = client.Execute(request);
```

> Response:

```json
{
  "Data": [
    {
      "ContactId": 29317401,
      "ClientId": 0,
      "Email": "email@address.com",
      "FirstName": "John",
      "LastName": "Smith",
      "DateAdded": "2016-12-02T19:02:39",
      "Gender": "",
      "City": "",
      "BirthDate": "",
      "Extended1": "",
      "Extended2": "",
      "Extended3": "",
      "Extended4": "",
      "Extended5": "",
      "Extended6": "",
      "Extended7": "",
      "Extended8": "",
      "Extended9": "",
      "Extended10": "",
      "Extended11": "",
      "Extended12": "",
      "Extended13": "",
      "Extended14": "",
      "Extended15": null,
      "IsActive": true,
      "IsVisible": true,
      "CanBeReactivated": true,
      "Permission": null
    }
  ]
}
```

This endpoint retrieves all of your contacts.

### HTTP Request

`GET https://restapi.directiq.com/contacts/view`

### Query Parameters

None

## Get Contact by Id

```shell
curl -X GET \
  https://restapi.directiq.com/contacts/{contactId} \
  -H 'api-key: your-api-key' \
  -H 'user-name: your-user-name'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own contact id instead of "0101".
var request = new RestRequest("contacts/0101", Method.GET);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");
var response = client.Execute(request);
```

> Response:

```json
{
  "Data": [
    {
      "ContactId": 29317401,
      "ClientId": 0,
      "Email": "email@address.com",
      "FirstName": "John",
      "LastName": "Smith",
      "DateAdded": "2016-12-02T19:02:39",
      "Gender": "",
      "City": "",
      "BirthDate": "",
      "Extended1": "",
      "Extended2": "",
      "Extended3": "",
      "Extended4": "",
      "Extended5": "",
      "Extended6": "",
      "Extended7": "",
      "Extended8": "",
      "Extended9": "",
      "Extended10": "",
      "Extended11": "",
      "Extended12": "",
      "Extended13": "",
      "Extended14": "",
      "Extended15": null,
      "IsActive": true,
      "IsVisible": true,
      "CanBeReactivated": true,
      "Permission": null
    }
  ]
}
```

This endpoint retrieves a contact info given its id.

### HTTP Request

`GET https://restapi.directiq.com/contacts/{contactId}`

### Query Parameters

Parameter | Description
--------- | -----------
contactId | Contact id as an integer value.


## Get All Contacts by List Id

```shell
curl -X GET \
  https://restapi.directiq.com/contacts/view/{listId} \
  -H 'api-key: your-api-key' \
  -H 'user-name: your-user-name'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own list id instead of "0101".
var request = new RestRequest("contacts/view/0101", Method.GET);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");
var response = client.Execute(request);
```

> Response:

```json
{
  "Data": [
    {
      "ContactId": 29317401,
      "ClientId": 0,
      "Email": "email@address.com",
      "FirstName": "John",
      "LastName": "Smith",
      "DateAdded": "2016-12-02T19:02:39",
      "Gender": "",
      "City": "",
      "BirthDate": "",
      "Extended1": "",
      "Extended2": "",
      "Extended3": "",
      "Extended4": "",
      "Extended5": "",
      "Extended6": "",
      "Extended7": "",
      "Extended8": "",
      "Extended9": "",
      "Extended10": "",
      "Extended11": "",
      "Extended12": "",
      "Extended13": "",
      "Extended14": "",
      "Extended15": null,
      "IsActive": true,
      "IsVisible": true,
      "CanBeReactivated": true,
      "Permission": null
    }
  ]
}
```

This endpoint retrieves contacts of a specified list.

### HTTP Request

`GET https://restapi.directiq.com/contacts/view/{listId}`

### Query Parameters

Parameter | Description
--------- | -----------
listId | List id as an integer value.


## Get Active Contacts by List Id

```shell
curl -X GET \
  https://restapi.directiq.com/contacts/active/view/{listId} \
  -H 'api-key: your-api-key' \
  -H 'user-name: your-user-name'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own list id instead of "0101".
var request = new RestRequest("contacts/active/view/0101", Method.GET);

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
        "ContactId": 456210,
        "ClientId": 0,
        "Email": "email@address.com",
        "FirstName": null,
        "LastName": null,
        "DateAdded": "2017-02-24T19:28:11",
        "Gender": null,
        "City": null,
        "BirthDate": null,
        "Extended1": null,
        "Extended2": null,
        "Extended3": null,
        "Extended4": null,
        "Extended5": null,
        "Extended6": null,
        "Extended7": null,
        "Extended8": null,
        "Extended9": null,
        "Extended10": null,
        "Extended11": null,
        "Extended12": null,
        "Extended13": null,
        "Extended14": null,
        "Extended15": null,
        "IsActive": false,
        "IsVisible": true,
        "CanBeReactivated": true,
        "Permission": null
    }
]
```

This endpoint retrieves all active contacts of a specified list.

### HTTP Request

`GET https://restapi.directiq.com/contacts/active/view/{listId}`

### Query Parameters

Parameter | Description
--------- | -----------
listId | List id as an integer value.

## Get Passive Contacts by List Id

```shell
curl -X GET \
  https://restapi.directiq.com/contacts/passive/view/{listId} \
  -H 'api-key: your-api-key' \
  -H 'user-name: your-user-name'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own list id instead of "0101".
var request = new RestRequest("contacts/passive/view/0101", Method.GET);

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
        "ContactId": 456210,
        "ClientId": 0,
        "Email": "email@address.com",
        "FirstName": null,
        "LastName": null,
        "DateAdded": "2017-02-24T19:28:11",
        "Gender": null,
        "City": null,
        "BirthDate": null,
        "Extended1": null,
        "Extended2": null,
        "Extended3": null,
        "Extended4": null,
        "Extended5": null,
        "Extended6": null,
        "Extended7": null,
        "Extended8": null,
        "Extended9": null,
        "Extended10": null,
        "Extended11": null,
        "Extended12": null,
        "Extended13": null,
        "Extended14": null,
        "Extended15": null,
        "IsActive": false,
        "IsVisible": true,
        "CanBeReactivated": true,
        "Permission": null
    }
]
```

This endpoint retrieves all passive contacts of a specified list.

### HTTP Request

`GET https://restapi.directiq.com/contacts/passive/view/{listId}`

### Query Parameters

Parameter | Description
--------- | -----------
listId | List id as an integer value.


## Create a Contact by List Id

```shell
curl -X POST \
  https://restapi.directiq.com/contacts/{listId} \
  -H 'api-key: your-api-key' \
  -H 'content-type: application/json' \
  -H 'user-name: your-user-name' \
  -d '{"Email": "email@address.com", "FirstName" : "John", "LastName" : "Smith"}'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own list id instead of "0101".
var request = new RestRequest("contacts/0101", Method.POST);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");

request.AddParameter("application/json", "{\"Email\": \"email@address.com\", 
   \"FirstName\" : \"John\", \"LastName\" : \"Smith\"}", ParameterType.RequestBody);

var response = client.Execute(request);
```

> Response:

```json
{
  "ContactId": 0,
  "ClientId": 0,
  "Email": "email@address.com",
  "FirstName": "John",
  "LastName": "Smith",
  "DateAdded": null,
  "Gender": null,
  "City": null,
  "BirthDate": null,
  "Extended1": null,
  "Extended2": null,
  "Extended3": null,
  "Extended4": null,
  "Extended5": null,
  "Extended6": null,
  "Extended7": null,
  "Extended8": null,
  "Extended9": null,
  "Extended10": null,
  "Extended11": null,
  "Extended12": null,
  "Extended13": null,
  "Extended14": null,
  "Extended15": null,
  "IsActive": null,
  "IsVisible": null,
  "CanBeReactivated": null,
  "Permission": null
}
```

This endpoint adds a contact to a specified list.

### HTTP Request

`POST https://restapi.directiq.com/contacts/{listId}`

### Query Parameters

Parameter | Description
--------- | -----------
listId | List id as an integer value.

## Delete a Contact From a List

```shell
curl -X DELETE \
  https://restapi.directiq.com/contacts/delete/{listId} \
  -H 'api-key: your-api-key' \
  -H 'content-type: application/json' \
  -H 'user-name: your-user-name' \
  -d '{"Email": "email@address.com"}'
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own list id instead of "0101".
var request = new RestRequest("contacts/delete/0101", Method.DELETE);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");

request.AddParameter("application/json", "{\"Email\": \"email@address.com\"}",
    ParameterType.RequestBody);

var response = client.Execute(request);
```

> Response:

```json
{
  "ContactId": 0,
  "ClientId": 0,
  "Email": "email@address.com",
  "FirstName": "null",
  "LastName": "null",
  "DateAdded": null,
  "Gender": null,
  "City": null,
  "BirthDate": null,
  "Extended1": null,
  "Extended2": null,
  "Extended3": null,
  "Extended4": null,
  "Extended5": null,
  "Extended6": null,
  "Extended7": null,
  "Extended8": null,
  "Extended9": null,
  "Extended10": null,
  "Extended11": null,
  "Extended12": null,
  "Extended13": null,
  "Extended14": null,
  "Extended15": null,
  "IsActive": null,
  "IsVisible": null,
  "CanBeReactivated": null,
  "Permission": null
}
```

This endpoint deletes a contact from a specified list.

### HTTP Request

`DELETE https://restapi.directiq.com/contacts/delete/{listId}`

### Query Parameters

Parameter | Description
--------- | -----------
listId | List id as an integer value.


## Upload File For Bulk Insert

```shell
curl -X POST \
  https://restapi.directiq.com/contacts/upload/{listId} \
  -H 'api-key: your-api-key' \
  -H 'content-type: multipart/form-data' \
  -H 'user-name: your-user-name' \
  -F FILE_TO_UPLOAD=@csvFile.csv
```

```csharp
// Simple REST and HTTP API Client for .NET
using RestSharp;

var client = new RestClient("https://restapi.directiq.com/");

// Use your own list id instead of "0101".
var request = new RestRequest("contacts/upload/0101", Method.GET);

// Use your own user name instead of "your-user-name" 
request.AddHeader("user-name", "your-user-name");

// Use your own api key instead of "your-api-key"
request.AddHeader("api-key", "your-api-key");

request.AddHeader("content-type", "multipart/form-data");

request.AddParameter("multipart/form-data", "Content-Disposition: form-data; 
        name=\"FILE_TO_UPLOAD\"; filename=\"csvFile.csv\"\r\nContent-Type: false",
        ParameterType.RequestBody);

var response = client.Execute(request);
```

> Response:

```json
200 OK
```

This endpoint adds contacts to a specified list.

###CSV File###

Use a csv file containing your contacts info and upload it to the end point. You must provide at least <b>"email"</b> as the header. This field holds the email addresses of your contacts. You can also provide the common <b>"firstname"</b> and <b>"lastname"</b> as headers.

<aside class="warning">Header names must be exactly the same as stated here.</aside>

### HTTP Request

`POST https://restapi.directiq.com/contacts/upload/{listId}`

### Query Parameters

Parameter | Description
--------- | -----------
listId    | List id as an integer value.