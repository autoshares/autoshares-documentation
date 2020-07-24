
<a name="allocations_allocatebatch"></a>
#### Create batch multileg allocation request
```
POST /v{version}/allocations/multileg
```


##### Description
This POST endpoint enables you to create and send multiple allocation requests for multi-leg orders.


##### Parameters

|Type|Name|Description|Schema|Default|
|---|---|---|---|---|
|**Header**|**Authorization**  <br>*required*|This is the authorization token that you retrieved from the first endpoint (/token).|string||
|**Header**|**Et-App-Key**  <br>*required*|This is your app’s unique key that can be retrieved from the BO Companies widget in Autoshares Trader.|string||
|**Path**|**version**  <br>*required*|This is the version of the API. Unless you have multiple versions of Autoshares Trader’s API deployed in your environment, leave it at 1.0.|string|`"1"`|
|**Body**|**body**  <br>*required*|This is a JSON dictionary that contains information about the new multi-leg allocations.|< [MultilegAllocationRequest](#multilegallocationrequest) > array||


##### Responses

|HTTP Code|Description|Schema|
|---|---|---|
|**200**|Successful request, JSON data is returned, containing an array of multi-leg allocation requests’ details along with one extra parameter — IsSucceed — which indicates if the allocations have been successfully carried out.|< [AllocationResultInfo[MultilegAllocationRequest]](#allocationresultinfo-multilegallocationrequest) > array|
|**401**|The access level of the provided authorization token is not sufficient to perform this operation.|No Content|
|**403**|The provided Et-App-Key is incorrect.|No Content|
|**409**|Failed allocation request result|< [AllocationResultInfo[MultilegAllocationRequest]](#allocationresultinfo-multilegallocationrequest) > array|
|**422**|A validation error occurred while processing the request.|No Content|
|**500**|Internal server error|No Content|


##### Consumes

* `application/json`
* `text/json`


##### Produces

* `application/json`
* `text/json`



