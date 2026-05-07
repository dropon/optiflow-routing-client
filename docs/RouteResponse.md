# RouteResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Distance** | **int32** | The distance of the route [m]. | 
**TravelTime** | **int32** | The travel time for the route [s]. | 
**TrafficDelay** | Pointer to **int32** | The total delay due to live traffic on the route [s].  This value contains the sum of all traffic events on the route and will be non-zero only if **options[trafficMode]&#x3D;REALISTIC**. See [here](./concepts/traffic-modes) for more information. | [optional] 
**Violated** | **bool** | If there is no valid route but the resulting route can be calculated by using actually prohibited roads, the route is marked as violated. When requesting _VIOLATION_EVENTS_ there is a corresponding violation event containing the position, time and the vehicle property in question. See [here](./concepts/violations) for more information. | 
**RouteId** | Pointer to **string** | The ID of the calculated route. It is valid for 12 hours. | [optional] 
**Legs** | Pointer to [**[]Leg**](Leg.md) | The legs of the route. | [optional] 
**Toll** | Pointer to [**Toll**](Toll.md) |  | [optional] 
**Polyline** | Pointer to **string** | The polyline of the route in the format specified by **options[polylineFormat]**. | [optional] 
**Events** | Pointer to [**[]Event**](Event.md) | Detailed information on maneuvers, border crossings and other events along the route in chronological order. | [optional] 
**Emissions** | Pointer to [**Emissions**](Emissions.md) |  | [optional] 
**AlternativeRoutes** | Pointer to [**[]AlternativeRoute**](AlternativeRoute.md) | Detailed information on alternative routes. Requires _ALTERNATIVE_ROUTES_ to be requested. The array may be empty when no alternative routes are found. | [optional] 
**ScheduleReport** | Pointer to [**ScheduleReport**](ScheduleReport.md) |  | [optional] 
**EvReport** | Pointer to [**EvReport**](EvReport.md) |  | [optional] 
**GuidedNavigation** | Pointer to **string** | A base64 encoded representation of the route that can be used for the [PTV Navigator](https://www.myptv.com/en/logistics-software/ptv-navigator). The base64 binary has to be decoded and saved as a text file with the extension .bcr. Requires _GUIDED_NAVIGATION_ to be requested. | [optional] 
**MonetaryCosts** | Pointer to [**MonetaryCosts**](MonetaryCosts.md) |  | [optional] 
**ElevationReport** | Pointer to [**ElevationReport**](ElevationReport.md) |  | [optional] 
**Warnings** | Pointer to [**[]Warning**](Warning.md) | A list of warnings concerning the validity of the result. | [optional] 

## Methods

### NewRouteResponse

`func NewRouteResponse(distance int32, travelTime int32, violated bool, ) *RouteResponse`

NewRouteResponse instantiates a new RouteResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRouteResponseWithDefaults

`func NewRouteResponseWithDefaults() *RouteResponse`

NewRouteResponseWithDefaults instantiates a new RouteResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDistance

`func (o *RouteResponse) GetDistance() int32`

GetDistance returns the Distance field if non-nil, zero value otherwise.

### GetDistanceOk

`func (o *RouteResponse) GetDistanceOk() (*int32, bool)`

GetDistanceOk returns a tuple with the Distance field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDistance

`func (o *RouteResponse) SetDistance(v int32)`

SetDistance sets Distance field to given value.


### GetTravelTime

`func (o *RouteResponse) GetTravelTime() int32`

GetTravelTime returns the TravelTime field if non-nil, zero value otherwise.

### GetTravelTimeOk

`func (o *RouteResponse) GetTravelTimeOk() (*int32, bool)`

GetTravelTimeOk returns a tuple with the TravelTime field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTravelTime

`func (o *RouteResponse) SetTravelTime(v int32)`

SetTravelTime sets TravelTime field to given value.


### GetTrafficDelay

`func (o *RouteResponse) GetTrafficDelay() int32`

GetTrafficDelay returns the TrafficDelay field if non-nil, zero value otherwise.

### GetTrafficDelayOk

`func (o *RouteResponse) GetTrafficDelayOk() (*int32, bool)`

GetTrafficDelayOk returns a tuple with the TrafficDelay field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTrafficDelay

`func (o *RouteResponse) SetTrafficDelay(v int32)`

SetTrafficDelay sets TrafficDelay field to given value.

### HasTrafficDelay

`func (o *RouteResponse) HasTrafficDelay() bool`

HasTrafficDelay returns a boolean if a field has been set.

### GetViolated

`func (o *RouteResponse) GetViolated() bool`

GetViolated returns the Violated field if non-nil, zero value otherwise.

### GetViolatedOk

`func (o *RouteResponse) GetViolatedOk() (*bool, bool)`

GetViolatedOk returns a tuple with the Violated field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetViolated

`func (o *RouteResponse) SetViolated(v bool)`

SetViolated sets Violated field to given value.


### GetRouteId

`func (o *RouteResponse) GetRouteId() string`

GetRouteId returns the RouteId field if non-nil, zero value otherwise.

### GetRouteIdOk

`func (o *RouteResponse) GetRouteIdOk() (*string, bool)`

GetRouteIdOk returns a tuple with the RouteId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRouteId

`func (o *RouteResponse) SetRouteId(v string)`

SetRouteId sets RouteId field to given value.

### HasRouteId

`func (o *RouteResponse) HasRouteId() bool`

HasRouteId returns a boolean if a field has been set.

### GetLegs

`func (o *RouteResponse) GetLegs() []Leg`

GetLegs returns the Legs field if non-nil, zero value otherwise.

### GetLegsOk

`func (o *RouteResponse) GetLegsOk() (*[]Leg, bool)`

GetLegsOk returns a tuple with the Legs field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLegs

`func (o *RouteResponse) SetLegs(v []Leg)`

SetLegs sets Legs field to given value.

### HasLegs

`func (o *RouteResponse) HasLegs() bool`

HasLegs returns a boolean if a field has been set.

### GetToll

`func (o *RouteResponse) GetToll() Toll`

GetToll returns the Toll field if non-nil, zero value otherwise.

### GetTollOk

`func (o *RouteResponse) GetTollOk() (*Toll, bool)`

GetTollOk returns a tuple with the Toll field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToll

`func (o *RouteResponse) SetToll(v Toll)`

SetToll sets Toll field to given value.

### HasToll

`func (o *RouteResponse) HasToll() bool`

HasToll returns a boolean if a field has been set.

### GetPolyline

`func (o *RouteResponse) GetPolyline() string`

GetPolyline returns the Polyline field if non-nil, zero value otherwise.

### GetPolylineOk

`func (o *RouteResponse) GetPolylineOk() (*string, bool)`

GetPolylineOk returns a tuple with the Polyline field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPolyline

`func (o *RouteResponse) SetPolyline(v string)`

SetPolyline sets Polyline field to given value.

### HasPolyline

`func (o *RouteResponse) HasPolyline() bool`

HasPolyline returns a boolean if a field has been set.

### GetEvents

`func (o *RouteResponse) GetEvents() []Event`

GetEvents returns the Events field if non-nil, zero value otherwise.

### GetEventsOk

`func (o *RouteResponse) GetEventsOk() (*[]Event, bool)`

GetEventsOk returns a tuple with the Events field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEvents

`func (o *RouteResponse) SetEvents(v []Event)`

SetEvents sets Events field to given value.

### HasEvents

`func (o *RouteResponse) HasEvents() bool`

HasEvents returns a boolean if a field has been set.

### GetEmissions

`func (o *RouteResponse) GetEmissions() Emissions`

GetEmissions returns the Emissions field if non-nil, zero value otherwise.

### GetEmissionsOk

`func (o *RouteResponse) GetEmissionsOk() (*Emissions, bool)`

GetEmissionsOk returns a tuple with the Emissions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEmissions

`func (o *RouteResponse) SetEmissions(v Emissions)`

SetEmissions sets Emissions field to given value.

### HasEmissions

`func (o *RouteResponse) HasEmissions() bool`

HasEmissions returns a boolean if a field has been set.

### GetAlternativeRoutes

`func (o *RouteResponse) GetAlternativeRoutes() []AlternativeRoute`

GetAlternativeRoutes returns the AlternativeRoutes field if non-nil, zero value otherwise.

### GetAlternativeRoutesOk

`func (o *RouteResponse) GetAlternativeRoutesOk() (*[]AlternativeRoute, bool)`

GetAlternativeRoutesOk returns a tuple with the AlternativeRoutes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAlternativeRoutes

`func (o *RouteResponse) SetAlternativeRoutes(v []AlternativeRoute)`

SetAlternativeRoutes sets AlternativeRoutes field to given value.

### HasAlternativeRoutes

`func (o *RouteResponse) HasAlternativeRoutes() bool`

HasAlternativeRoutes returns a boolean if a field has been set.

### GetScheduleReport

`func (o *RouteResponse) GetScheduleReport() ScheduleReport`

GetScheduleReport returns the ScheduleReport field if non-nil, zero value otherwise.

### GetScheduleReportOk

`func (o *RouteResponse) GetScheduleReportOk() (*ScheduleReport, bool)`

GetScheduleReportOk returns a tuple with the ScheduleReport field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScheduleReport

`func (o *RouteResponse) SetScheduleReport(v ScheduleReport)`

SetScheduleReport sets ScheduleReport field to given value.

### HasScheduleReport

`func (o *RouteResponse) HasScheduleReport() bool`

HasScheduleReport returns a boolean if a field has been set.

### GetEvReport

`func (o *RouteResponse) GetEvReport() EvReport`

GetEvReport returns the EvReport field if non-nil, zero value otherwise.

### GetEvReportOk

`func (o *RouteResponse) GetEvReportOk() (*EvReport, bool)`

GetEvReportOk returns a tuple with the EvReport field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEvReport

`func (o *RouteResponse) SetEvReport(v EvReport)`

SetEvReport sets EvReport field to given value.

### HasEvReport

`func (o *RouteResponse) HasEvReport() bool`

HasEvReport returns a boolean if a field has been set.

### GetGuidedNavigation

`func (o *RouteResponse) GetGuidedNavigation() string`

GetGuidedNavigation returns the GuidedNavigation field if non-nil, zero value otherwise.

### GetGuidedNavigationOk

`func (o *RouteResponse) GetGuidedNavigationOk() (*string, bool)`

GetGuidedNavigationOk returns a tuple with the GuidedNavigation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGuidedNavigation

`func (o *RouteResponse) SetGuidedNavigation(v string)`

SetGuidedNavigation sets GuidedNavigation field to given value.

### HasGuidedNavigation

`func (o *RouteResponse) HasGuidedNavigation() bool`

HasGuidedNavigation returns a boolean if a field has been set.

### GetMonetaryCosts

`func (o *RouteResponse) GetMonetaryCosts() MonetaryCosts`

GetMonetaryCosts returns the MonetaryCosts field if non-nil, zero value otherwise.

### GetMonetaryCostsOk

`func (o *RouteResponse) GetMonetaryCostsOk() (*MonetaryCosts, bool)`

GetMonetaryCostsOk returns a tuple with the MonetaryCosts field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMonetaryCosts

`func (o *RouteResponse) SetMonetaryCosts(v MonetaryCosts)`

SetMonetaryCosts sets MonetaryCosts field to given value.

### HasMonetaryCosts

`func (o *RouteResponse) HasMonetaryCosts() bool`

HasMonetaryCosts returns a boolean if a field has been set.

### GetElevationReport

`func (o *RouteResponse) GetElevationReport() ElevationReport`

GetElevationReport returns the ElevationReport field if non-nil, zero value otherwise.

### GetElevationReportOk

`func (o *RouteResponse) GetElevationReportOk() (*ElevationReport, bool)`

GetElevationReportOk returns a tuple with the ElevationReport field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetElevationReport

`func (o *RouteResponse) SetElevationReport(v ElevationReport)`

SetElevationReport sets ElevationReport field to given value.

### HasElevationReport

`func (o *RouteResponse) HasElevationReport() bool`

HasElevationReport returns a boolean if a field has been set.

### GetWarnings

`func (o *RouteResponse) GetWarnings() []Warning`

GetWarnings returns the Warnings field if non-nil, zero value otherwise.

### GetWarningsOk

`func (o *RouteResponse) GetWarningsOk() (*[]Warning, bool)`

GetWarningsOk returns a tuple with the Warnings field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetWarnings

`func (o *RouteResponse) SetWarnings(v []Warning)`

SetWarnings sets Warnings field to given value.

### HasWarnings

`func (o *RouteResponse) HasWarnings() bool`

HasWarnings returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


