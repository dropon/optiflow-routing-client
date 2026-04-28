# \ReachableLocationsAPI

All URIs are relative to *https://api.myptv.com/routing/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DeleteReachableLocations**](ReachableLocationsAPI.md#DeleteReachableLocations) | **Delete** /reachable-locations/{id} | 
[**GetReachableLocations**](ReachableLocationsAPI.md#GetReachableLocations) | **Get** /reachable-locations/{id} | 
[**StartAndCreateReachableLocations**](ReachableLocationsAPI.md#StartAndCreateReachableLocations) | **Post** /reachable-locations | 



## DeleteReachableLocations

> DeleteReachableLocations(ctx, id).Execute()





### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/GIT_USER_ID/GIT_REPO_ID"
)

func main() {
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | The ID of the calculated reachable locations.

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.ReachableLocationsAPI.DeleteReachableLocations(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ReachableLocationsAPI.DeleteReachableLocations``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | The ID of the calculated reachable locations. | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteReachableLocationsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

 (empty response body)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetReachableLocations

> ReachableLocationsResponse GetReachableLocations(ctx, id).MaximumPollingPeriod(maximumPollingPeriod).Execute()





### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/GIT_USER_ID/GIT_REPO_ID"
)

func main() {
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | The ID of the calculated reachable locations.
	maximumPollingPeriod := int32(56) // int32 | If the calculation is still running, this operation will be blocked and will not return before this period [ms] expires. If the calculation is completed, it will return immediately.  The default of 0 ms will cause the operation to return immediately in any case. Use a value > 0 to implement long polling to reduce the number of requests. See the [tutorial](https://developer.myptv.com/en/resources/tutorials/general/how-use-asynchronous-requests-ptv-developer-apis) on asynchronous requests for details.  (optional) (default to 0)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ReachableLocationsAPI.GetReachableLocations(context.Background(), id).MaximumPollingPeriod(maximumPollingPeriod).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ReachableLocationsAPI.GetReachableLocations``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetReachableLocations`: ReachableLocationsResponse
	fmt.Fprintf(os.Stdout, "Response from `ReachableLocationsAPI.GetReachableLocations`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | The ID of the calculated reachable locations. | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetReachableLocationsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **maximumPollingPeriod** | **int32** | If the calculation is still running, this operation will be blocked and will not return before this period [ms] expires. If the calculation is completed, it will return immediately.  The default of 0 ms will cause the operation to return immediately in any case. Use a value &gt; 0 to implement long polling to reduce the number of requests. See the [tutorial](https://developer.myptv.com/en/resources/tutorials/general/how-use-asynchronous-requests-ptv-developer-apis) on asynchronous requests for details.  | [default to 0]

### Return type

[**ReachableLocationsResponse**](ReachableLocationsResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## StartAndCreateReachableLocations

> ReachableLocationsId StartAndCreateReachableLocations(ctx).Horizon(horizon).Locations(locations).Waypoint(waypoint).RouteId(routeId).Profile(profile).HorizonType(horizonType).Options(options).Execute()





### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/GIT_USER_ID/GIT_REPO_ID"
)

func main() {
	horizon := int32(100) // int32 | The distance [m] or travel time [s] of the horizons, depending of the **horizonType** (limited to 200 km or 2 hours from a waypoint, 50 km or 45 minutes from a route).
	locations := *openapiclient.NewLocations([]openapiclient.Location{*openapiclient.NewLocation(float64(49.480301), float64(6.110667))}) // Locations | 
	waypoint := "waypoint_example" // string | The start or destination waypoint. The format of the waypoint is `<lat>,<lon>[;<attribute>;<attribute>;...]` representing a point with the latitude value in degrees from south to north and the longitude value in degrees (WGS84/EPSG:4326) from west to east. This point will be matched to the nearest possible road. By default the air-line connection between given and matched coordinates is not included in the distance or duration. We will refer to this type of waypoint as an _on-road waypoint_.  The behaviour of a waypoint can be changed by appending the following attributes:   * `includeLastMeters` to include the air-line connection between given and matched coordinates in the distance or duration.   We will refer to this type of waypoint as an _off-road waypoint_.   * `roadAccess=<lat>,<lon>`, to use these coordinates for matching to the nearest road. Implies **includeLastMeters**, i.e.   the air-line connection between the waypoint coordinates and the matched coordinates   is included in the distance or duration. This is useful if the waypoint should not be matched to the nearest possible road but to some road further away,   e.g. garage exit at a different road.  See [here](./concepts/waypoints) for more information. (optional)
	routeId := "3a58b824-fa8b-47eb-a5b8-73d6b753e1b4" // string | Instead of the waypoint mentioned above, a **routeId** from a previously calculated route or a matched track can be entered. More information and applying restrictions can be found [here](./concepts/route-ids). (optional)
	profile := "profile_example" // string | A profile defines a vehicle by a set of attributes, matching typical transport situations. It must be the name of one of the [predefined profiles](../data-api/concepts/profiles) such as _EUR_TRAILER_TRUCK_.  If this parameter is not specified and the first waypoint or the routeId is located in the Americas, _USA_8_SEMITRAILER_5AXLE_ is used as the default instead of _EUR_TRAILER_TRUCK_.  If the first waypoint or the routeId is located in the Americas but a non-American profile is specified or vice-versa, a warning is returned (routing only). Always use a profile which matches the region of the waypoints to obtain best results.  If the attributes of the profile do not fit to your vehicle, the values can be changed by the corresponding attributes in the **vehicle** parameter (routing only).  The values of the predefined profiles may be adapted to reflect current vehicle standards. To obtain the same results when values change, it is recommended to  always send with the request the **vehicle** parameters that are important for your use case. (optional) (default to "EUR_TRAILER_TRUCK")
	horizonType := openapiclient.HorizonType("DISTANCE") // HorizonType |  (optional) (default to "TRAVEL_TIME")
	options := *openapiclient.NewReachableOptions() // ReachableOptions | Routing-relevant options like driving direction or the use of additional data. Use array notation like `options[trafficMode]=AVERAGE` to set options. (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ReachableLocationsAPI.StartAndCreateReachableLocations(context.Background()).Horizon(horizon).Locations(locations).Waypoint(waypoint).RouteId(routeId).Profile(profile).HorizonType(horizonType).Options(options).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ReachableLocationsAPI.StartAndCreateReachableLocations``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `StartAndCreateReachableLocations`: ReachableLocationsId
	fmt.Fprintf(os.Stdout, "Response from `ReachableLocationsAPI.StartAndCreateReachableLocations`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiStartAndCreateReachableLocationsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **horizon** | **int32** | The distance [m] or travel time [s] of the horizons, depending of the **horizonType** (limited to 200 km or 2 hours from a waypoint, 50 km or 45 minutes from a route). | 
 **locations** | [**Locations**](Locations.md) |  | 
 **waypoint** | **string** | The start or destination waypoint. The format of the waypoint is &#x60;&lt;lat&gt;,&lt;lon&gt;[;&lt;attribute&gt;;&lt;attribute&gt;;...]&#x60; representing a point with the latitude value in degrees from south to north and the longitude value in degrees (WGS84/EPSG:4326) from west to east. This point will be matched to the nearest possible road. By default the air-line connection between given and matched coordinates is not included in the distance or duration. We will refer to this type of waypoint as an _on-road waypoint_.  The behaviour of a waypoint can be changed by appending the following attributes:   * &#x60;includeLastMeters&#x60; to include the air-line connection between given and matched coordinates in the distance or duration.   We will refer to this type of waypoint as an _off-road waypoint_.   * &#x60;roadAccess&#x3D;&lt;lat&gt;,&lt;lon&gt;&#x60;, to use these coordinates for matching to the nearest road. Implies **includeLastMeters**, i.e.   the air-line connection between the waypoint coordinates and the matched coordinates   is included in the distance or duration. This is useful if the waypoint should not be matched to the nearest possible road but to some road further away,   e.g. garage exit at a different road.  See [here](./concepts/waypoints) for more information. | 
 **routeId** | **string** | Instead of the waypoint mentioned above, a **routeId** from a previously calculated route or a matched track can be entered. More information and applying restrictions can be found [here](./concepts/route-ids). | 
 **profile** | **string** | A profile defines a vehicle by a set of attributes, matching typical transport situations. It must be the name of one of the [predefined profiles](../data-api/concepts/profiles) such as _EUR_TRAILER_TRUCK_.  If this parameter is not specified and the first waypoint or the routeId is located in the Americas, _USA_8_SEMITRAILER_5AXLE_ is used as the default instead of _EUR_TRAILER_TRUCK_.  If the first waypoint or the routeId is located in the Americas but a non-American profile is specified or vice-versa, a warning is returned (routing only). Always use a profile which matches the region of the waypoints to obtain best results.  If the attributes of the profile do not fit to your vehicle, the values can be changed by the corresponding attributes in the **vehicle** parameter (routing only).  The values of the predefined profiles may be adapted to reflect current vehicle standards. To obtain the same results when values change, it is recommended to  always send with the request the **vehicle** parameters that are important for your use case. | [default to &quot;EUR_TRAILER_TRUCK&quot;]
 **horizonType** | [**HorizonType**](HorizonType.md) |  | [default to &quot;TRAVEL_TIME&quot;]
 **options** | [**ReachableOptions**](ReachableOptions.md) | Routing-relevant options like driving direction or the use of additional data. Use array notation like &#x60;options[trafficMode]&#x3D;AVERAGE&#x60; to set options. | 

### Return type

[**ReachableLocationsId**](ReachableLocationsId.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

