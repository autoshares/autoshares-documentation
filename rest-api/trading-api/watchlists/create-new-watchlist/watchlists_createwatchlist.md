# Syntax

## Create watchlist

```text
POST /v{version}/users/{userId}/watchlists
```

### Description

This API endpoint enables you to create a new watchlist.

### Parameters

| Type | Name | Description | Schema | Default |
| :--- | :--- | :--- | :--- | :--- |
| **Header** | **Authorization**   _required_ | This is the authorization token that you retrieved from the first endpoint \(/token\). | string |  |
| **Header** | **Et-App-Key**   _required_ | This is your app’s unique key that can be retrieved from the BO Companies widget in Autoshares Trader. | string |  |
| **Path** | **userId**   _required_ | This is the internal identifier of the user for whom a new watchlist needs to be created. | integer \(int32\) |  |
| **Path** | **version**   _required_ | This is the version of the API. Unless you have multiple versions of Autoshares Trader’s API deployed in your environment, leave it at 1.0. | string | `"1"` |
| **Query** | **resultIncludeSecurities**   _required_ | This boolean parameter indicates if the list of securities in the watchlist should be returned in the request response. | boolean |  |
| **Body** | **body**   _required_ | This is JSON data that contains information about the new watchlist as well as the list of securities the watchlist should contain. | [CreateWatchlistModel](watchlists_createwatchlist.md#createwatchlistmodel) |  |

### Responses

| HTTP Code | Description | Schema |
| :--- | :--- | :--- |
| **200** | Successful request, JSON data containing the information about the new watchlist is returned \(along with its securities if the resultIncludeSecurities parameter was set to true\). | [WatchlistModel](watchlists_createwatchlist.md#watchlistmodel) |
| **401** | The access level of the provided authorization token is not sufficient to perform this operation. | No Content |
| **403** | The provided Et-App-Key is incorrect. | No Content |
| **409** | The watchlist couldn’t be created because another watchlist with the same name already exists or the specified securities couldn’t be added. | [WatchlistModel](watchlists_createwatchlist.md#watchlistmodel) |
| **422** | A validation error occurred while processing the request. | No Content |
| **500** | Internal server error | No Content |

### Consumes

* `application/json`
* `text/json`

### Produces

* `application/json`
* `text/json`

