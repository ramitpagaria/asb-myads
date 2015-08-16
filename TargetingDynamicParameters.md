# Targeting By Dynamic Parameters #

You can pass any custom parameters from our ad tag to the ad server and target by their values.
To do that first take a look at the ad tag. Find the line:
```
var asb_custom_parameters = "";
```
You can see that the default value is empty string. You can set this JavaScript variable to any value in the format:
```
parameter1=value1&parameter2=value2&parametersN=valueN
```
Obviously you are going to do that using the server scripting technology you are using on your site. Eg.: jsp, asp, php, perl, etc.

Next you need to add parameters with their values to the targeting in Banner->Targeting->Dynamic Parameters.

You can use [patterns](http://code.google.com/p/asb-myads/wiki/patterns) or regular expressions to set parameter value.

## Example ##

You want to target males aged 20-29. If your site has registration with those data you can pass them to the ad server for targeting:
```
var asb_custom_parameters = "sex=male&age=29";
```
On the server side with jsp technology this could be expressed as:
```
var asb_custom_parameters = "<%=request.getParameter("asb_custom_parameters")%>";
```
The sex and age of the user as custom parameters would probably be set to the request somewhere in a servlet:
```
request.setParameter("asb_custom_parameters","sex="+currentUser.getSex()+"&age="+currentUser.getAge());
```

Now you can target males aged 20-29 by adding the following parameters to a banner's targeting:
| **Parameter name** | **Pattern** | **Type** |
|:-------------------|:------------|:---------|
| sex                | male        | pattern  |
| age                | `2[0-9]{1`} | regexp   |


## Caveat ##
Like with other targeting options dynamic parameters are using exclusive logic. Meaning: if targeting by dynamic parameters is used the ad server is trying to find them in the request and if not found the banner is not displayed and other banners are considered.