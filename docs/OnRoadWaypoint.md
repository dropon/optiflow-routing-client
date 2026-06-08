# OnRoadWaypoint

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Latitude** | **float64** | The latitude value in degrees (WGS84/EPSG:4326) from south to north. | 
**Longitude** | **float64** | The longitude value in degrees (WGS84/EPSG:4326) from west to east. | 
**MatchSideOfStreet** | Pointer to **bool** | Specifies that this waypoint will be reached at the side of street on which it is located. This is useful to prevent the driver from crossing the street to actually reach the location represented by this waypoint. | [optional] [default to false]
**ServiceTime** | Pointer to **int32** | The service time [s] that is required at this waypoint, e.g. for pickup or delivery. | [optional] [default to 0]
**UseServiceTimeForRecreation** | Pointer to **bool** | If true, the service time can be used for a break or rest. This parameter will be ignored, if **serviceTime** is 0 or if no **driver** is specified. | [optional] [default to false]
**OpeningIntervals** | Pointer to [**[]TimeInterval**](TimeInterval.md) | The opening intervals at this waypoint, each specified by two points in time - the beginning and the end of the interval. Leaving this parameter empty means that the waypoint is always open. Service can only start within one of the opening intervals. If the vehicle does not arrive at a waypoint within an opening interval, a waiting time will be scheduled.  When using a multi-day **workingHoursPreset** this waiting time will usually be used for daily rests instead, in order to continue the route with a rested driver. Requires **options[startTime]** to be specified, or **options[trafficMode]** _REALISTIC_ with no time being specified. | [optional] 
**VehicleParameters** | Pointer to [**VehicleParametersAtWaypoint**](VehicleParametersAtWaypoint.md) |  | [optional] 
**EvParameters** | Pointer to [**EvParametersAtWaypoint**](EvParametersAtWaypoint.md) |  | [optional] 

## Methods

### NewOnRoadWaypoint

`func NewOnRoadWaypoint(latitude float64, longitude float64, ) *OnRoadWaypoint`

NewOnRoadWaypoint instantiates a new OnRoadWaypoint object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOnRoadWaypointWithDefaults

`func NewOnRoadWaypointWithDefaults() *OnRoadWaypoint`

NewOnRoadWaypointWithDefaults instantiates a new OnRoadWaypoint object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetLatitude

`func (o *OnRoadWaypoint) GetLatitude() float64`

GetLatitude returns the Latitude field if non-nil, zero value otherwise.

### GetLatitudeOk

`func (o *OnRoadWaypoint) GetLatitudeOk() (*float64, bool)`

GetLatitudeOk returns a tuple with the Latitude field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLatitude

`func (o *OnRoadWaypoint) SetLatitude(v float64)`

SetLatitude sets Latitude field to given value.


### GetLongitude

`func (o *OnRoadWaypoint) GetLongitude() float64`

GetLongitude returns the Longitude field if non-nil, zero value otherwise.

### GetLongitudeOk

`func (o *OnRoadWaypoint) GetLongitudeOk() (*float64, bool)`

GetLongitudeOk returns a tuple with the Longitude field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLongitude

`func (o *OnRoadWaypoint) SetLongitude(v float64)`

SetLongitude sets Longitude field to given value.


### GetMatchSideOfStreet

`func (o *OnRoadWaypoint) GetMatchSideOfStreet() bool`

GetMatchSideOfStreet returns the MatchSideOfStreet field if non-nil, zero value otherwise.

### GetMatchSideOfStreetOk

`func (o *OnRoadWaypoint) GetMatchSideOfStreetOk() (*bool, bool)`

GetMatchSideOfStreetOk returns a tuple with the MatchSideOfStreet field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMatchSideOfStreet

`func (o *OnRoadWaypoint) SetMatchSideOfStreet(v bool)`

SetMatchSideOfStreet sets MatchSideOfStreet field to given value.

### HasMatchSideOfStreet

`func (o *OnRoadWaypoint) HasMatchSideOfStreet() bool`

HasMatchSideOfStreet returns a boolean if a field has been set.

### GetServiceTime

`func (o *OnRoadWaypoint) GetServiceTime() int32`

GetServiceTime returns the ServiceTime field if non-nil, zero value otherwise.

### GetServiceTimeOk

`func (o *OnRoadWaypoint) GetServiceTimeOk() (*int32, bool)`

GetServiceTimeOk returns a tuple with the ServiceTime field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetServiceTime

`func (o *OnRoadWaypoint) SetServiceTime(v int32)`

SetServiceTime sets ServiceTime field to given value.

### HasServiceTime

`func (o *OnRoadWaypoint) HasServiceTime() bool`

HasServiceTime returns a boolean if a field has been set.

### GetUseServiceTimeForRecreation

`func (o *OnRoadWaypoint) GetUseServiceTimeForRecreation() bool`

GetUseServiceTimeForRecreation returns the UseServiceTimeForRecreation field if non-nil, zero value otherwise.

### GetUseServiceTimeForRecreationOk

`func (o *OnRoadWaypoint) GetUseServiceTimeForRecreationOk() (*bool, bool)`

GetUseServiceTimeForRecreationOk returns a tuple with the UseServiceTimeForRecreation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUseServiceTimeForRecreation

`func (o *OnRoadWaypoint) SetUseServiceTimeForRecreation(v bool)`

SetUseServiceTimeForRecreation sets UseServiceTimeForRecreation field to given value.

### HasUseServiceTimeForRecreation

`func (o *OnRoadWaypoint) HasUseServiceTimeForRecreation() bool`

HasUseServiceTimeForRecreation returns a boolean if a field has been set.

### GetOpeningIntervals

`func (o *OnRoadWaypoint) GetOpeningIntervals() []TimeInterval`

GetOpeningIntervals returns the OpeningIntervals field if non-nil, zero value otherwise.

### GetOpeningIntervalsOk

`func (o *OnRoadWaypoint) GetOpeningIntervalsOk() (*[]TimeInterval, bool)`

GetOpeningIntervalsOk returns a tuple with the OpeningIntervals field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOpeningIntervals

`func (o *OnRoadWaypoint) SetOpeningIntervals(v []TimeInterval)`

SetOpeningIntervals sets OpeningIntervals field to given value.

### HasOpeningIntervals

`func (o *OnRoadWaypoint) HasOpeningIntervals() bool`

HasOpeningIntervals returns a boolean if a field has been set.

### GetVehicleParameters

`func (o *OnRoadWaypoint) GetVehicleParameters() VehicleParametersAtWaypoint`

GetVehicleParameters returns the VehicleParameters field if non-nil, zero value otherwise.

### GetVehicleParametersOk

`func (o *OnRoadWaypoint) GetVehicleParametersOk() (*VehicleParametersAtWaypoint, bool)`

GetVehicleParametersOk returns a tuple with the VehicleParameters field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVehicleParameters

`func (o *OnRoadWaypoint) SetVehicleParameters(v VehicleParametersAtWaypoint)`

SetVehicleParameters sets VehicleParameters field to given value.

### HasVehicleParameters

`func (o *OnRoadWaypoint) HasVehicleParameters() bool`

HasVehicleParameters returns a boolean if a field has been set.

### GetEvParameters

`func (o *OnRoadWaypoint) GetEvParameters() EvParametersAtWaypoint`

GetEvParameters returns the EvParameters field if non-nil, zero value otherwise.

### GetEvParametersOk

`func (o *OnRoadWaypoint) GetEvParametersOk() (*EvParametersAtWaypoint, bool)`

GetEvParametersOk returns a tuple with the EvParameters field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEvParameters

`func (o *OnRoadWaypoint) SetEvParameters(v EvParametersAtWaypoint)`

SetEvParameters sets EvParameters field to given value.

### HasEvParameters

`func (o *OnRoadWaypoint) HasEvParameters() bool`

HasEvParameters returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


