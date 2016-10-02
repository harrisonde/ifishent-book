#API Response Structure

Ah, ya! I've hit the point that I'm going to return the first response from my API. Before doing so, I'd like to setup a [strict status code/ response system](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html) which dictates the structure of all API response.

### Status Code
The following defines the headers attached to a given API response:

* 200	OK
* 201	Created
* 202	Accepted
* 304	Not Modified
* 400	Bad Request
* 401	Not Authorized
* 403	Forbidden
* 404	Not Found
* 405	Method Not Allowed
* 500	Internal Server Error


### Error Code
This list defines system level response codes and is loosely related RFC 2616:

#### Generic 
* 400	Validation

#### Identification
* 401   Undefined
* 402   Unknown


### Response

1. No generic error messages
2. All responses must be descriptive
3. Error response is an object and contains the code, message, and description.  

```javascript
error : {
    code : 100
    description: 'A user id is required to complete this action.'
    message : 'Undefined user id.'
    
}
```

