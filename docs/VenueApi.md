# OpenPartyApi.VenueApi

All URIs are relative to *https://api.openparty.co/v0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**venuesGet**](VenueApi.md#venuesGet) | **GET** /venues | Retrieve Venues by Type and Date
[**venuesIdGet**](VenueApi.md#venuesIdGet) | **GET** /venues/{id} | Get Venue by a given id
[**venuesIdTablepricingGet**](VenueApi.md#venuesIdTablepricingGet) | **GET** /venues/{id}/tablepricing | Get All Bottle Service Tables by a venue in a given date


<a name="venuesGet"></a>
# **venuesGet**
> [Venue] venuesGet(type, opts)

Retrieve Venues by Type and Date

The Venue endpoint returns an array of venues filtered by date and type of venue (nightclub or poolparty). Each venue includes  information such as name, display name, type, features, logo among other details.

### Example
```javascript
var OpenPartyApi = require('open_party_api');

var apiInstance = new OpenPartyApi.VenueApi();

var type = "type_example"; // String | Type can be only 'nightclub' or 'poolparty'.

var opts = { 
  '_date': new Date("2013-10-20") // Date | Format for Date should be mm/dd/yy.
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.venuesGet(type, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **String**| Type can be only &#39;nightclub&#39; or &#39;poolparty&#39;. | 
 **_date** | **Date**| Format for Date should be mm/dd/yy. | [optional] 

### Return type

[**[Venue]**](Venue.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="venuesIdGet"></a>
# **venuesIdGet**
> [Venue] venuesIdGet(id)

Get Venue by a given id

The Venues endpoint returns information about a venue by given id. The response includes the display name and other details about the venue.

### Example
```javascript
var OpenPartyApi = require('open_party_api');

var apiInstance = new OpenPartyApi.VenueApi();

var id = 3.4; // Number | Id for the venue.


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.venuesIdGet(id, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Number**| Id for the venue. | 

### Return type

[**[Venue]**](Venue.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="venuesIdTablepricingGet"></a>
# **venuesIdTablepricingGet**
> [Event] venuesIdTablepricingGet(id, _date)

Get All Bottle Service Tables by a venue in a given date

The tablepricing endpoint returns an array with information about bottle service tables in a given date. The response includes the prices, capacity for tables among other details.

### Example
```javascript
var OpenPartyApi = require('open_party_api');

var apiInstance = new OpenPartyApi.VenueApi();

var id = 3.4; // Number | Id for selected venue.

var _date = new Date("2013-10-20"); // Date | Date given for retrieve tables.


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.venuesIdTablepricingGet(id, _date, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Number**| Id for selected venue. | 
 **_date** | **Date**| Date given for retrieve tables. | 

### Return type

[**[Event]**](Event.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

