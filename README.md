# Welcome to WHYNOGROUP API!
Here is a js wrapper allowing a simplified use of your Rest API server hosted by whynogroup.

```js

/**
* First, include this script to your application.
*/
<script src="wrapper-js.wng"></script>
<script>

/**
* Instanciate an WNG Client.
* You can generate new credentials with full access to your account on
* the token creation page -> [https://api.whyno.group/?new]
*/
var wng = new wngApi(
  'api-eu.whyno.group',    // Endpoint of API WNG (List of available endpoints) 
                           // -> http://api.whyno.group/?documentation&endpointList
  'xxxxxxxxxx'             // Consumer Key
);

/**
* This API allows you to update your personal information, you can 
* also use any API in the same way.
* @return null
*/
var result = wng.post("/me", [
  "FIRSTNAME"               : "Patrick",
  "LASTNAME"                : "Slown", 
]);

/**
* Return "null" if the request has been fulfilled
*/
console.log(result);

/**
* Another example. You have created an API "/test/time" in order to
* obtain the unix time from the server. As you wish to obtain 
* information the method will necessarily be of GET type, example 
* of use:
* @return int
*/
var result = wng.get("/test/time");


/**
* Returns "1576536041" if the request has been made correctly
*/
console.log(result);
</script>
```

Are you ready?
----------
It's really simple, I explain to you, [ask for a consumer key](https://api.whyno.group/?new), then authenticate you (api.whyno.group/?cas-auth) 
entering your nichandle and your password, press 'login' and then your consumer key is now ready to be used!

What to do next?
----------
Then download this wrapper, and insert in your project folder. Once the client is ready, [explore the list of our API!](https://api.whyno.group/?console)

Pratical Link
----------
* Documentation: https://api.whyno.group/?docs
* Console: https://api.whyno.group/?console
* Create application credentials: https://cas.whyno.group/?new
* Active your consumer key: https://api.whyno.group/?auth
* Check if your consumer key work perfectly: https://cas.whyno.group/?check

