# Sample Page

\[\[\_get\_token\]\] ==== Get token .... POST /token ....

===== Description Authentication method that provides token to access API.

===== Parameters

\[options="header", cols=".^2,.^3,.^9,.^4,.^2"\] \|=== \|Type\|Name\|Description\|Schema\|Default \|**Header**\|**Authorization** + **optional**\|Authorization token, required on every step except first\|string\|`""` \|**Header**\|**Et-App-Key** + **required**\|Application key\|string\| \|**Header**\|**Password** + **optional**\|User password, required\|string\|`"testpassword"` \|**Header**\|**PinCode** + **optional**\|User pin code, on demand\|string\|`""` \|**Header**\|**Username** + **optional**\|User login, required\|string\|`"testusername"` \|**Header**\|**VerificationCode** + **optional**\|User verification code, on demand\|string\|`""` \|===

===== Responses

\[options="header", cols=".^2,.^14,.^4"\] \|=== \|HTTP Code\|Description\|Schema \|**200**\|Authentication complete and token is ready to use.\|No Content \|**202**\|Several authentication steps are passed, but server is expecting additional parameters. Use a token from response and provide correct additional data to complete authentication procedure.\|No Content \|**401**\|Authentication parameters determined as incorrect.\|No Content \|===

===== Produces

* `State`
* `Step`
* `Reason`
* `Token`

===== Example HTTP response

====== Response 200

## \[source,json\]

{ "State" : "Succeeded", "Token" : "VGhpcyBpcyBleGFtcGxlIHRva2Vu..."

## }

====== Response 202

## \[source,json\]

{ "Step" : "SecutityPin", "Reason" : "Invalid pin", "State" : "Expecting", "Token" : "VGhpcyBpcyBleGFtcGxlIHRva2Vu...."

## }

====== Response 401

## \[source,json\]

{ "State" : "Failed", "Step" : "SecutityPin", "Reason" : "Invalid pin"

## }

