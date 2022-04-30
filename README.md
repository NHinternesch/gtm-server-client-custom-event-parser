# Custom Event Parser

This client template for Google Tag Manager Server-Side takes an incoming GET or POST request, extracts information from the query string, headers, IP, request body, and cookies and returns the data to the server container as an event object. It is vendor agnostic and can handle any tracking request.

For an example request like `https://myServerContainer.com/measure?property1=value1&property2=value2&property3=value3` with a request body like `{
    "bodyProperty1": "bodyValue1",
    "bodyProperty2": "bodyValue2"
}`, the **event data mapping** for the object returned would look like this:

Event Object Key | Source
--- | ---
property1 | Query String 
property2 | Query String
property3 | Query String
fullQueryString | Query String
requestPath | Path
bodyProperty1 | Request Body
bodyProperty2 | Request Body
page_location | Request Header: referer
user_agent | Request Header: user-agent
ip_override | Request IP
timestamp | Request Timestamp
*CookieName* | Request Header: cookie (*CookieName* as specified in the template input field)

Full blog post with instructions available [here](https://nhinternesch.medium.com/google-tag-manager-server-side-parsing-event-data-from-any-custom-vendor-request-4d2ea7f25991). 

Please feel free to get in touch for feedback and suggestions. 
