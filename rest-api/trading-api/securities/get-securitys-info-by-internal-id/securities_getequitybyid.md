# Syntax

## Get equity by id

```text
GET /v{version}/equities/{id}
```

### Description

This API endpoint enables you to retrieve detailed information about a specific equity by providing its internal identifier in Autoshares Trader.

### Parameters

| Type | Name | Description | Schema | Default |
| :--- | :--- | :--- | :--- | :--- |
| **Header** | **Authorization**   _required_ | This is the authorization token that you retrieved from the first endpoint \(/token\). | string |  |
| **Header** | **Et-App-Key**   _required_ | This is your app’s unique key that can be retrieved from the BO Companies widget in Autoshares Trader. | string |  |
| **Path** | **id**   _required_ | This is the internal identifier of the enquired equity in Autoshares Trader. | integer \(int32\) |  |
| **Path** | **version**   _required_ | This is the version of the API. Unless you have multiple versions of Autoshares Trader’s API deployed in your environment, leave it at 1.0. | string | `"1"` |

### Responses

| HTTP Code | Description | Schema |
| :--- | :--- | :--- |
| **200** | Successful request, JSON data containing detailed information about the enquired security is returned. | [EquityResource](securities_getequitybyid.md#equityresource) |
| **401** | The access level of the provided authorization token is not sufficient to perform this operation. | No Content |
| **403** | The provided Et-App-Key is incorrect. | No Content |
| **404** | Enquired security is non-existent in Autoshares Trader. | No Content |
| **422** | A validation error occurred while processing the request. | No Content |
| **500** | Internal server error | No Content |

### Produces

* `application/json`
* `text/json`

