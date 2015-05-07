# service-adapter plugin

Javascript plug in that acts as a wrapper for making AJAX calls. 

## Code Example

```js
        var sa = new serviceAdapter();
        sa.settings.url = 'api/service';
        sa.qsParameters.add('foo', 1);
        sa.settings.contentType = 'application/json';
        sa.callbacks.customSuccessCallback = function(e){ 
        console.log('my custom callback');};
        sa.get();
```

## Motivation

I wanted a lightweight proficient way to make AJAX calls without relying on JQUERY. This
Plugin for the most part replicates what JQUERY's AJAX methods do, but I gives you a more,
complete experience.

## Installation

Simply reference the JS file accordingly in your html.

## API Reference

###Properties

```
-responseData
type: object
description: The raw response object.
```

```
-responseXml
type: xml
description: The response object's xml.
```

```
-responseText
type: text
description: The response object's text.
```

```
-responseJson
type: json
description: The response object's json.
```
      
```
-data
type: object
description: The request payload.
```
            
```
-enctype
type: string
description: This should reflect the encoding type of the request data.
see: http://www.w3schools.com/tags/att_form_enctype.asp.
```

```
-contentType
type: string
description: The content-type of the request being generated. (i.e. application/json)
see: http://www.w3.org/Protocols/rfc1341/4_Content-Type.html
```

```
-method
type: string
description: This is method signature of the xmlHttpRequest (i.e. post, get, etc.) 
see: http://www.w3schools.com/tags/att_form_method.asp.
```

```
-url
type: string
description: The endpoint that your request is being sent to.
```

```
-isAsync
type: bool
description: The method call behavior synchronous vs asynchronous. 
see: http://www.w3schools.com/tags/att_script_async.asp.
default: true
```

```
-isJson
type: bool
description: The expected response data type. 
```

```
-enableLogging
type: bool
description: Allows for console logging of the request to occur.  Logs during the various
state changes of the request. Also returns an overall transaction time.
default: true
```

###Methods

```
-send function()
type: method
description: Generic Ajax call. Nothing is defined all setting must be provided by the
programmer.
```

```
-get function()
type: method
description: Get Ajax call. The method is defaulted to 'GET'. Additional settings are 
provided by the programmer.
```

```
-getJson function()
type: method
description: Get Ajax call. The method is defaulted to 'GET', isJson is set true. 
Additional settings are provided by the programmer.
```

```
-getXml function()
type: method
description: Get Ajax call. The method is defaulted to 'GET', isJson is set false. 
Additional settings are provided by the programmer.
```

```
-post function()
type: method
description: Post Ajax call. The method is defaulted to 'POST'. Additional settings are 
provided by the programmer.
```

```
-postJson function()
type: method
description: Post Ajax call. The method is defaulted to 'POST', ContentType is set to
application/json. Additional settings are provided by the programmer.
```

```
-postXml function()
type: method
description: Post Ajax call. The method is defaulted to 'POST', ContentType is set to
application/xml. Additional settings are provided by the programmer.
```

```
qsParameters.:
-add function(id, value)
type: method
description: Adds values to the query string of your request.
parameters: id - querystring parameter name; value - querystring parameter value
```

```
headers.:
-add function(id, value)
type: method
description: Adds values to the request header.
parameters: id - header type; value - value
```


## Tests

To properly test the javascript you will need an html file, a js file, and an endpoint 
you can post to. I'd recommend you download the ServiceWrapper.zip. It's a .net based
web api project. If you don't want to use it you can still pull the JS/HTML out of the 
project and wire it up to your own test harness.

## License

MIT
