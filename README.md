# service-adapter plugin

Javascript plug in that acts as a wrapper for making AJAX calls. 

## Code Example

```js
formDataHelper.module.settings.target = 'formDataUpload';
formDataHelper.module.settings.action = '/IFrameTestHandler.ashx';
formDataHelper.module.createFormData(parameters, files, false);
formDataHelper.module.createIframe('formDataUpload', null);
formDataHelper.module.submitFormData();
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
-enctype
type: string
description: This should reflect the encoding type of the request data, 
see: http://www.w3schools.com/tags/att_form_enctype.asp.
default: multipart/form-data.
```

```
-method
type: string
description: This should reflect the method signature your action will perform. 
see: http://www.w3schools.com/tags/att_form_method.asp.
default: post
```


###Methods

```
-send function()
type: method
description: 
parameters:
```

```
-get function()
type: method
description: 
parameters:
```

```
-getJson function()
type: method
description: 
parameters:
```

```
-getXml function()
type: method
description: 
parameters:
```

```
-post function()
type: method
description: 
parameters:
```

```
-postjson function()
type: method
description: 
parameters:
```

```
-postXml function()
type: method
description: 
parameters:
```

```
qsParameters
-add function()
type: method
description: 
parameters:
```

```
headers
-add function()
type: method
description: 
parameters:
```


## Tests

To properly test the javascript you will need an html file, a js file, and an endpoint 
you can post to. I'd recommend you download the ServiceWrapper.zip. It's a .net based
web api project. If you don't want to use it you can still pull the JS/HTML out of the 
project and wire it up to your own test harness.

## License

MIT
