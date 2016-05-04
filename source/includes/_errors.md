# Status codes

The Nutanix intentful API uses the following error codes:


Status Code	| Definition
------------|-----------
200 | The API request was successful and received a response.
201 | The API request was successful and created an object.

Status Code	| Definition
------------|-----------
400 | The API request was malformed and could not be processed.
401 | You have no access and/or are not authorized.
403 | You are authorized but do not have the privileges for this API.
404 | The URL was not found.
405 | The called method is not allowed or is not supported.
408 | The request timed out (20 seconds maximum).

Status Code	| Definition
------------|-----------
500 | The API request was received but there was a server error.
503 | Service unavailable at this time or too early to process.
505 | HTTP other than 1.1 not supported.