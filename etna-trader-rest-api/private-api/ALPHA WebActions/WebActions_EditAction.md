
<a name="webactions_editaction"></a>
#### Modify specified web action
```
PUT /v{version}/webactions/{actionId}
```


##### Description
Provides specified web action by action ID


##### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Header**|**Authorization**  <br>*required*|This is the authorization token that you retrieved from the first endpoint (/token).|string||
|**Header**|**Et-App-Key**  <br>*required*|This is your app’s unique key that can be retrieved from the BO Companies widget in Autoshares Trader.|string||
|**Path**|**actionId**  <br>*required*|Action ID|integer (int32)||
|**Path**|**version**  <br>*required*|This is the version of the API. Unless you have multiple versions of Autoshares Trader’s API deployed in your environment, leave it at 1.0.|string|`"1"`|
|**Body**|**body**  <br>*required*|Action model|[WebActionModifyModel](#webactionmodifymodel)||


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Action was successfully modified|[WebActionMapModel](#webactionmapmodel)|
|**401**|The access level of the provided authorization token is not sufficient to perform this operation.|No Content|
|**403**|The provided Et-App-Key is incorrect.|No Content|
|**422**|A validation error occurred while processing the request.|No Content|
|**500**|Internal server error|No Content|


##### Consumes

* `application/json`
* `text/json`


##### Produces

* `application/json`
* `text/json`



