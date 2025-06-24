# **Portofolio - Maria Michailidi**

**IP Stack**
https://ipstack.com/ provides a public HTTP API for software developers to search the geolocation of IP addresses. It uses a database of IP addresses that are associated to cities along with other relevant information like time zone, latitude and longitude.

**URL**:

**Prerequisites**
IPStack API key


**IPStack API key **
The key can be obtained from the [Ipstack](https://ipstack.com/dashboard) website. The free plan allows to have 100 queries per month.
 Please note, that the registration, even for free plan, requires credit card details.

JSON

**Input**
https://api.ipstack.com/xx.xx.xxx.xxx
It required one parameter to run. It has to be a public IP address

**Output**
The output of the program consist of two float numbers. They represent the:

 - latitude
 - longitude

**Error Handling**

- 404	404_not_found	The requested resource does not exist.
- 101	missing_access_key	No API Key was specified.
 - 101	invalid_access_key	No API Key was specified or an invalid API Key was specified.
 - 102	inactive_user	The current user account is not active. User will be prompted to get in touch with Customer Support.
 - 103	invalid_api_function	The requested API endpoint does not exist.
 - 104	usage_limit_reached	The maximum allowed amount of monthly API requests has been reached.
 - 301	invalid_fields	One or more invalid fields were specified using the fields parameter.
 - 302	too_many_ips	Too many IPs have been specified for the Bulk Lookup Endpoint. (max. 50)
 - 303	batch_not_supported_on_plan	The Bulk Lookup Endpoint is not supported on the current subscription plan
 - 400 Bad Request: malformed request (e.g., invalid IP)


**Parameters Summary**
| Parameter |	Endpoint | Type | Description |
|---|---|---|---|
|access_key|	All	|   required	|        Authentication key|
|hostname|	Standard, Bulk	|     flag	   |     Include DNS hostname|
|security	Standard | Bulk	|     flag	    |    Enable security data|
|language |	All	   |         string	       |Language code (2-letter)|
|fields	|	All    |             string	 |      Comma-separated list to |limit |response|
|output	|	All        |         string	   |      xml for XML output|
