# Syntax

## Verify replacing order

```text
PUT /v{version}/accounts/{accountId}/preview/orders/{orderId}
```

### Description

This API endpoint enables you to validate updated information about an order that needs to be modified.

### Parameters

| Type | Name | Description | Schema | Default |
| :--- | :--- | :--- | :--- | :--- |
| **Header** | **Authorization**   _required_ | This is the authorization token that you retrieved from the first endpoint \(/token\). | string |  |
| **Header** | **Et-App-Key**   _required_ | This is your app’s unique key that can be retrieved from the BO Companies widget in ETNA Trader. | string |  |
| **Path** | **accountId**   _required_ | This is the unique identifier of the trading account on which a new order is to be modified. | integer \(int32\) |  |
| **Path** | **orderId**   _required_ | This is the ID of the order that needs to be modified. | integer \(int32\) |  |
| **Path** | **version**   _required_ | This is the version of the API. Unless you have multiple versions of ETNA Trader’s API deployed in your environment, leave it at 1.0. | string | `"1"` |
| **Body** | **body**   _required_ | This is JSON data that contains updated information about the order. | [ModifyOrderResource](orders_previewmodifyorder.md#modifyorderresource) |  |

### Responses

| HTTP Code | Description | Schema |
| :--- | :--- | :--- |
| **200** | JSON data with the updated order information is returned, indicating if the order modification JSON is properly constructed \(examine the isSuccessful parameter in the JSON file\). | [VerifyOrderModel](orders_previewmodifyorder.md#verifyordermodel) |
| **401** | The access level of the provided authorization token is not sufficient to perform this operation. | No Content |
| **403** | The provided Et-App-Key is incorrect. | No Content |
| **422** | A validation error occurred while processing the request. | No Content |
| **500** | Internal server error | No Content |

### Consumes

* `application/json`
* `text/json`

### Produces

* `application/json`
* `text/json`

