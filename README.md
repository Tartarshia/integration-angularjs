see the original repo  
tealium_angular modified:  
add local service url:  
"http://" + $location.host() + ":" + $location.port() + "/{{}}api/resources/tealium/properties"  
service will provide environment, account and profile  
Then it will get utag.js from:  
"//tags.tiqcdn.com/utag/"+param.TEALIUM_PROPERTY_ACCOUNT+"/"+param.TEALIUM_PROPERTY_PROFILE+"/"+param.TEALIUM_PROPERTY_ENVIRONMENT+"/utag.js"  
  
This modify is necessary due to our PRE and PRO(include shadow) are using the same package that generated in Local-Pre, so we cannot use env properties in Maven to tell how to build.
