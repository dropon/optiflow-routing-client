# RouteOptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MaximumSpeed** | Pointer to **int32** | The maximum speed of the vehicle [km/h]. The speeds for calculating the driving times on all roads will be limited to this value. See [here](./concepts/speeds) for more information. Do not specify **options[maximumSpeed]**, if this parameter is given. | [optional] 
**SpeedsByRoadCategory** | Pointer to [**[]SpeedByRoadCategory**](SpeedByRoadCategory.md) | The speeds used to calculate the driving times by road category. For each road category a minimum and a maximum speed have to be specified. The first array element represents motorways, the last one pedestrian and cycle paths, see [here](../data-api/concepts/road-categories) for more information on road categories.  The speed actually used for a road segment depends on its road category and a speed category defined in the map data and is calculated by linear interpolation between the minimum and maximum speed.  This parameter can be specified only, if **options[trafficMode]** is _CONSTANT_, or if _AVERAGE_ and neither **options[startTime]**  nor **options[arrivalTime]** is specified. Otherwise, an error will be returned.  See [here](./concepts/speeds) for more information, in particular on the influence of further speed-related parameters such as **options[maximumSpeed]**, **options[speedFactor]** and relative speeds applied by custom road attribute scenarios. | [optional] 
**Penalties** | Pointer to [**PenaltyOptions**](PenaltyOptions.md) |  | [optional] 
**AllowDeliveryOnlyGates** | Pointer to **bool** | If set to true, gates that restrict access to delivery-only zones are allowed to pass during route calculation. A delivery-only gate is located at a specific point of the road network where passing through is normally prohibited unless the vehicle is authorized for delivery.  This parameter will be ignored, if a **routeId** is specified.  It will also be ignored for non-motorized profiles such as _BICYCLE_ or _PEDESTRIAN_. | [optional] 
**TimePreferenceOverDistance** | Pointer to **int32** | Specifies the weighting between travel time and travel distance when calculating a route. The value defines the preference for minimizing travel time over minimizing travel distance. - 0: Route is optimized purely for shortest distance. - 100: Route is optimized purely for shortest travel time. - 1-99: A weighted combination of travel time and distance is applied, with higher values     giving more importance to travel time.  For motorized profiles, values between 80 and 90 typically provide the most realistic and efficient routing behavior whereas values below 30 often produce routes that are not realistically driveable. Such low values are mainly useful for determining theoretical lower bounds on distance rather than for practical route planning.  This parameter will be ignored, if a **routeId** is specified. | [optional] 

## Methods

### NewRouteOptions

`func NewRouteOptions() *RouteOptions`

NewRouteOptions instantiates a new RouteOptions object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRouteOptionsWithDefaults

`func NewRouteOptionsWithDefaults() *RouteOptions`

NewRouteOptionsWithDefaults instantiates a new RouteOptions object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMaximumSpeed

`func (o *RouteOptions) GetMaximumSpeed() int32`

GetMaximumSpeed returns the MaximumSpeed field if non-nil, zero value otherwise.

### GetMaximumSpeedOk

`func (o *RouteOptions) GetMaximumSpeedOk() (*int32, bool)`

GetMaximumSpeedOk returns a tuple with the MaximumSpeed field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMaximumSpeed

`func (o *RouteOptions) SetMaximumSpeed(v int32)`

SetMaximumSpeed sets MaximumSpeed field to given value.

### HasMaximumSpeed

`func (o *RouteOptions) HasMaximumSpeed() bool`

HasMaximumSpeed returns a boolean if a field has been set.

### GetSpeedsByRoadCategory

`func (o *RouteOptions) GetSpeedsByRoadCategory() []SpeedByRoadCategory`

GetSpeedsByRoadCategory returns the SpeedsByRoadCategory field if non-nil, zero value otherwise.

### GetSpeedsByRoadCategoryOk

`func (o *RouteOptions) GetSpeedsByRoadCategoryOk() (*[]SpeedByRoadCategory, bool)`

GetSpeedsByRoadCategoryOk returns a tuple with the SpeedsByRoadCategory field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSpeedsByRoadCategory

`func (o *RouteOptions) SetSpeedsByRoadCategory(v []SpeedByRoadCategory)`

SetSpeedsByRoadCategory sets SpeedsByRoadCategory field to given value.

### HasSpeedsByRoadCategory

`func (o *RouteOptions) HasSpeedsByRoadCategory() bool`

HasSpeedsByRoadCategory returns a boolean if a field has been set.

### GetPenalties

`func (o *RouteOptions) GetPenalties() PenaltyOptions`

GetPenalties returns the Penalties field if non-nil, zero value otherwise.

### GetPenaltiesOk

`func (o *RouteOptions) GetPenaltiesOk() (*PenaltyOptions, bool)`

GetPenaltiesOk returns a tuple with the Penalties field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPenalties

`func (o *RouteOptions) SetPenalties(v PenaltyOptions)`

SetPenalties sets Penalties field to given value.

### HasPenalties

`func (o *RouteOptions) HasPenalties() bool`

HasPenalties returns a boolean if a field has been set.

### GetAllowDeliveryOnlyGates

`func (o *RouteOptions) GetAllowDeliveryOnlyGates() bool`

GetAllowDeliveryOnlyGates returns the AllowDeliveryOnlyGates field if non-nil, zero value otherwise.

### GetAllowDeliveryOnlyGatesOk

`func (o *RouteOptions) GetAllowDeliveryOnlyGatesOk() (*bool, bool)`

GetAllowDeliveryOnlyGatesOk returns a tuple with the AllowDeliveryOnlyGates field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAllowDeliveryOnlyGates

`func (o *RouteOptions) SetAllowDeliveryOnlyGates(v bool)`

SetAllowDeliveryOnlyGates sets AllowDeliveryOnlyGates field to given value.

### HasAllowDeliveryOnlyGates

`func (o *RouteOptions) HasAllowDeliveryOnlyGates() bool`

HasAllowDeliveryOnlyGates returns a boolean if a field has been set.

### GetTimePreferenceOverDistance

`func (o *RouteOptions) GetTimePreferenceOverDistance() int32`

GetTimePreferenceOverDistance returns the TimePreferenceOverDistance field if non-nil, zero value otherwise.

### GetTimePreferenceOverDistanceOk

`func (o *RouteOptions) GetTimePreferenceOverDistanceOk() (*int32, bool)`

GetTimePreferenceOverDistanceOk returns a tuple with the TimePreferenceOverDistance field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTimePreferenceOverDistance

`func (o *RouteOptions) SetTimePreferenceOverDistance(v int32)`

SetTimePreferenceOverDistance sets TimePreferenceOverDistance field to given value.

### HasTimePreferenceOverDistance

`func (o *RouteOptions) HasTimePreferenceOverDistance() bool`

HasTimePreferenceOverDistance returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


