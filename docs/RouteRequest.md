# RouteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Waypoints** | Pointer to [**[]Waypoint**](Waypoint.md) | The list of waypoints the route will be calculated for. At least two waypoints are necessary, a maximum number may apply according to your subscription. The first waypoint is the start and the last is the destination of the route. Additional intermediate waypoints are possible.  Each waypoint must either have latitude and longitude or one of the representations combinedTransport, address or place. | [optional] 
**RouteId** | Pointer to **string** | Instead of the list of waypoints, a **routeId** from a previously calculated route or a matched track can be entered. See [here](./concepts/route-ids) for more information. | [optional] 
**Driver** | Pointer to [**DriverBody**](DriverBody.md) |  | [optional] 
**RouteOptions** | Pointer to [**RouteOptions**](RouteOptions.md) |  | [optional] 

## Methods

### NewRouteRequest

`func NewRouteRequest() *RouteRequest`

NewRouteRequest instantiates a new RouteRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRouteRequestWithDefaults

`func NewRouteRequestWithDefaults() *RouteRequest`

NewRouteRequestWithDefaults instantiates a new RouteRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetWaypoints

`func (o *RouteRequest) GetWaypoints() []Waypoint`

GetWaypoints returns the Waypoints field if non-nil, zero value otherwise.

### GetWaypointsOk

`func (o *RouteRequest) GetWaypointsOk() (*[]Waypoint, bool)`

GetWaypointsOk returns a tuple with the Waypoints field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetWaypoints

`func (o *RouteRequest) SetWaypoints(v []Waypoint)`

SetWaypoints sets Waypoints field to given value.

### HasWaypoints

`func (o *RouteRequest) HasWaypoints() bool`

HasWaypoints returns a boolean if a field has been set.

### GetRouteId

`func (o *RouteRequest) GetRouteId() string`

GetRouteId returns the RouteId field if non-nil, zero value otherwise.

### GetRouteIdOk

`func (o *RouteRequest) GetRouteIdOk() (*string, bool)`

GetRouteIdOk returns a tuple with the RouteId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRouteId

`func (o *RouteRequest) SetRouteId(v string)`

SetRouteId sets RouteId field to given value.

### HasRouteId

`func (o *RouteRequest) HasRouteId() bool`

HasRouteId returns a boolean if a field has been set.

### GetDriver

`func (o *RouteRequest) GetDriver() DriverBody`

GetDriver returns the Driver field if non-nil, zero value otherwise.

### GetDriverOk

`func (o *RouteRequest) GetDriverOk() (*DriverBody, bool)`

GetDriverOk returns a tuple with the Driver field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDriver

`func (o *RouteRequest) SetDriver(v DriverBody)`

SetDriver sets Driver field to given value.

### HasDriver

`func (o *RouteRequest) HasDriver() bool`

HasDriver returns a boolean if a field has been set.

### GetRouteOptions

`func (o *RouteRequest) GetRouteOptions() RouteOptions`

GetRouteOptions returns the RouteOptions field if non-nil, zero value otherwise.

### GetRouteOptionsOk

`func (o *RouteRequest) GetRouteOptionsOk() (*RouteOptions, bool)`

GetRouteOptionsOk returns a tuple with the RouteOptions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRouteOptions

`func (o *RouteRequest) SetRouteOptions(v RouteOptions)`

SetRouteOptions sets RouteOptions field to given value.

### HasRouteOptions

`func (o *RouteRequest) HasRouteOptions() bool`

HasRouteOptions returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


