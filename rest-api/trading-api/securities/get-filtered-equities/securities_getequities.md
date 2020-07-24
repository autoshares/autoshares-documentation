# Syntax

## Get equities

```text
GET /v{version}/equities
```

### Description

This API endpoint enables you to retrieve a collection of equities filtered by a specific query.

### Parameters

| Type | Name | Description | Schema | Default |
| :--- | :--- | :--- | :--- | :--- |
| **Header** | **Authorization**   _required_ | This is the authorization token that you retrieved from the first endpoint \(/token\). | string |  |
| **Header** | **Et-App-Key**   _required_ | This is your app’s unique key that can be retrieved from the BO Companies widget in Autoshares Trader. | string |  |
| **Path** | **version**   _required_ | This is the version of the API. Unless you have multiple versions of Autoshares Trader’s API deployed in your environment, leave it at 1.0. | string | `"1"` |
| **Query** | **desc**   _required_ | This is a boolean field that indicates if the returned equities should be sorted in the descending \(true\) or ascending \(false\) order. | boolean |  |
| **Query** | **filter**   _optional_ | This is a filter query used to retrieve only those equities that satisfy the conditions of the query. | string \(String\) |  |
| **Query** | **pageNumber**   _required_ | This is the page number \(all equities are split into pages\). | integer \(int32\) |  |
| **Query** | **pageSize**   _required_ | This is the number of equities that should be retrieved from the specified page. | integer \(int32\) |  |
| **Query** | **sortField**   _required_ | This is the field by which all equities should be sorted. For example, if you specify Type, first you'll receive stocks, then ETFs, etc. | string |  |

### Responses

| HTTP Code | Description | Schema |
| :--- | :--- | :--- |
| **200** | Successful request, JSON data containing the collection of filtered equities is returned. | &lt; [EquityResource](securities_getequities.md#equityresource) &gt; array |
| **401** | The access level of the provided authorization token is not sufficient to perform this operation. | No Content |
| **403** | The provided Et-App-Key is incorrect. | No Content |
| **422** | A validation error occurred while processing the request. | No Content |
| **500** | Internal server error | No Content |

### Produces

* `application/json`
* `text/json`

