
**CORS Bypass** is a NodeJS proxy which adds CORS headers to the proxied request.

The url to proxy is literally taken from the path, validated and proxied. The protocol
part of the proxied URI is optional, and defaults to "http". If port 443 is specified,
the protocol defaults to "https".

This package does not put any restrictions on the http methods or headers, except for
cookies. Requesting [user credentials](http://www.w3.org/TR/cors/#user-credentials) is disallowed.
The app can be configured to require a header for proxying a request, for example to avoid
a direct visit from the browser.

## Documentation

### Client

To use the API, just prefix the URL with the API URL:

https://ezlife-cors.herokuapp.com/ + API_URL 

Example using Angular HTTP.        
        return this.http
            .post(this.corsBypassURL + this.endpointURL, body, { headers: headers });

