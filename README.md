# Easy-Integration
Servicenow Application Easy to Install --> easy to configure --> easy to use --> enjoy!

![EasyIntegration-now](https://user-images.githubusercontent.com/37014061/143721864-69b8c3f8-e302-4887-ad21-9a43c3d86f93.png)

Description:
------------
Servicenow integration setup utility, configure it once and use it everywhere simple is that :)
+ You can track all integrations usability from which entity as well as what are the params / payloads and target tables in the background.
+ No need to create rest api messages anymore! for the same endpoint.
+ Use specific resolver (graphQl system) in order to customize your own response.
+ Support midserver option.
+ Open to be adjusted and configured based on your needs requirements.

![main page](https://user-images.githubusercontent.com/37014061/143722028-91d61d6c-24e9-43c0-a61b-7bd3be0334b5.JPG)

How to use:
-----------
Link: https://www.youtube.com/watch?v=spNPUn9uKmk

Script usage:
-------------

var response = repo.XXXXX(PathExt, Method, Params, Payload, SourceGlideRecord, LevelSource);

+ XXXXX: this integration setup name.
+ PathExt: Optional to be add to the url.
+ Method: get/post/put/patch/delete.
+ Params: Json or valid url path format, e.g: '?sysparm_limit=1' or {"sysparm_limit":"1"}
+ Payload: Json format or Valid Object.
+ SourceGlideRecord: source that use this integration spoke.
+ LevelSource: level message as string value, for debuging and reporting purposes, e.g: "testing","business logic" ...etc.

Output:
-------
Response = {data /*Response data*/, status /*Api call status*/, req /*Request Object*/}
+ req:{reqBody, reqQueryParam, url}
+ Important: data can be transformed using a valid/active resolver.
