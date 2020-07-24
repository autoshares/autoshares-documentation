# Syntax

## Create batch allocation request

```text
POST /v{version}/allocations/simple
```

### Description

Executes several trade allocations requests

### Parameters

| Type | Name | Description | Schema | Default |
| :--- | :--- | :--- | :--- | :--- |
| **Header** | **Authorization**   _required_ | Bearer type token string | string |  |
| **Header** | **Et-App-Key**   _required_ | Application key | string |  |
| **Path** | **version**   _required_ | The requested API version | string | `"1.0"` |
| **Body** | **body**   _required_ | Allocation request models collection | &lt; [SimpleAllocationRequest](../../definitions.md#simpleallocationrequest) &gt; array |  |

### Responses

| HTTP Code | Description | Schema |
| :--- | :--- | :--- |
| **200** | Succeeded allocation request result | &lt; [AllocationResultInfo\[SimpleAllocationRequest\]](../../definitions.md#allocationresultinfo-simpleallocationrequest) &gt; array |
| **401** | Authorization has been denied for this request. | No Content |
| **403** | Application key is not defined or does not exist | No Content |
| **409** | Failed allocation request result | &lt; [AllocationResultInfo\[SimpleAllocationRequest\]](../../definitions.md#allocationresultinfo-simpleallocationrequest) &gt; array |
| **422** | Validation error occurred while processing entity | No Content |
| **500** | Internal server error | No Content |

### Consumes

* `application/json`
* `text/json`

### Produces

* `application/json`
* `text/json`

