# Custom Event Parser

This client template for Google Tag Manager Server-Side extracts information from the query string, headers, IP, and cookies and returns the data to the server container as an event object. It is vendor agnostic and can handle any tracking request.

For an example request like `https://myDomain.com/measure?property1=value1&property2=value2&property3=value3…`, the **event data mapping** would look like this:

Event Object Key | Source
--- | ---
property1 | Query String 
property2 | Query String

