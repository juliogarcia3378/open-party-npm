# OpenPartyApi.EventApi

All URIs are relative to *https://api.openparty.co/v0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**eventsGet**](EventApi.md#eventsGet) | **GET** /events | Retrieve Events By Venue and Date


<a name="eventsGet"></a>
# **eventsGet**
> [Event] eventsGet(_date, opts)

Retrieve Events By Venue and Date

The Venues endpoint returns information about a venue by given id. The response includes the display name and other details about the venue.

### Example
```javascript
var OpenPartyApi = require('open_party_api');

var apiInstance = new OpenPartyApi.EventApi();

var _date = new Date("2013-10-20"); // Date | Date for event.

var opts = { 
  'venue': "venue_example" // String | Id for the venue.
};

var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
};
apiInstance.eventsGet(_date, opts, callback);
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **_date** | **Date**| Date for event. | 
 **venue** | **String**| Id for the venue. | [optional] 

### Return type

[**[Event]**](Event.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

