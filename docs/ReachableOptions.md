# ReachableOptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DrivingDirection** | Pointer to [**DrivingDirection**](DrivingDirection.md) |  | [optional] [default to OUTBOUND]
**ReferenceTime** | Pointer to **time.Time** | Defines the start time for **drivingDirection** _OUTBOUND_ or the arrival time for **drivingDirection** _INBOUND_ formatted according to [RFC 3339](https://tools.ietf.org/html/rfc3339). If none of them is specified the current time will be used.  If the date-time string does not include an explicit offset to UTC, the time will be interpreted as the local time of the waypoint. The date must not be before 1970-01-01T00:00:00+00:00 nor after 2037-12-31T23:59:59+00:00. The response will contain the offset to UTC specified in the request or that of the waypoint. For best results it should not be more than one month in the past nor more than six months in the future. See [here](./concepts/date-and-time) for more information on the relevance of date and time. | [optional] 
**TrafficMode** | Pointer to [**ReachableTrafficMode**](ReachableTrafficMode.md) |  | [optional] [default to AVERAGE]
**AllowedCountries** | Pointer to **string** | Comma-separated list of countries the route is allowed to pass. By default, all countries are allowed. If this parameter is present, only these countries are allowed to be passed, i.e. drive only in these countries. Countries are represented according to their [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) or [ISO 3166-2](https://en.wikipedia.org/wiki/ISO_3166-2) if referring to a subdivision. This parameter is mutually exclusive with **prohibitedCountries** and will be ignored, if a **routeId** is specified. | [optional] 
**ProhibitedCountries** | Pointer to **string** | Comma-separated list of countries the route must not pass. By default, all countries are allowed. If this parameter is present, all but the given countries are allowed to be passed, i.e. do not drive in these countries.  Countries are represented according to their [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) or [ISO 3166-2](https://en.wikipedia.org/wiki/ISO_3166-2) if referring to a subdivision. This parameter is mutually exclusive with **allowedCountries** and will be ignored, if a **routeId** is specified. | [optional] 
**BlockIntersectingRoads** | Pointer to **string** | Pipe-separated list of polylines.   Roads and combined transports that intersect the given polylines will be considered as prohibited and will not be used in the route calculation. Each list element is a polyline. Each point is a coordinate of latitude and longitude. Coordinates and points are separated by a comma. Format: &#x60;&lt;poly1_lat1&gt;,&lt;poly1_lon1&gt;,...,&lt;poly1_latN&gt;,&lt;poly1_lonN&gt;|&lt;poly2_lat1&gt;,&lt;poly2_lon1&gt;,...,&lt;poly2_latN&gt;,&lt;poly2_lonN&gt;|...&#x60;   Notes: * Be aware of the URL length restrictions. * If there is no other route connecting two waypoints the will be reported as violated and correspondingly violation events with type **BLOCKED_ROAD_BY_INTERSECTION** will be reported if violation events are requested. * Requests will be rejected if at least one provided polyline   * does not consist of an even number of coordinates,   * consists of less than two points,   * contains invalid coordinates or   * intersects more than 5000 road segments.  This parameter will be ignored, if a **routeId** is specified.  | [optional] 

## Methods

### NewReachableOptions

`func NewReachableOptions() *ReachableOptions`

NewReachableOptions instantiates a new ReachableOptions object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewReachableOptionsWithDefaults

`func NewReachableOptionsWithDefaults() *ReachableOptions`

NewReachableOptionsWithDefaults instantiates a new ReachableOptions object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDrivingDirection

`func (o *ReachableOptions) GetDrivingDirection() DrivingDirection`

GetDrivingDirection returns the DrivingDirection field if non-nil, zero value otherwise.

### GetDrivingDirectionOk

`func (o *ReachableOptions) GetDrivingDirectionOk() (*DrivingDirection, bool)`

GetDrivingDirectionOk returns a tuple with the DrivingDirection field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDrivingDirection

`func (o *ReachableOptions) SetDrivingDirection(v DrivingDirection)`

SetDrivingDirection sets DrivingDirection field to given value.

### HasDrivingDirection

`func (o *ReachableOptions) HasDrivingDirection() bool`

HasDrivingDirection returns a boolean if a field has been set.

### GetReferenceTime

`func (o *ReachableOptions) GetReferenceTime() time.Time`

GetReferenceTime returns the ReferenceTime field if non-nil, zero value otherwise.

### GetReferenceTimeOk

`func (o *ReachableOptions) GetReferenceTimeOk() (*time.Time, bool)`

GetReferenceTimeOk returns a tuple with the ReferenceTime field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReferenceTime

`func (o *ReachableOptions) SetReferenceTime(v time.Time)`

SetReferenceTime sets ReferenceTime field to given value.

### HasReferenceTime

`func (o *ReachableOptions) HasReferenceTime() bool`

HasReferenceTime returns a boolean if a field has been set.

### GetTrafficMode

`func (o *ReachableOptions) GetTrafficMode() ReachableTrafficMode`

GetTrafficMode returns the TrafficMode field if non-nil, zero value otherwise.

### GetTrafficModeOk

`func (o *ReachableOptions) GetTrafficModeOk() (*ReachableTrafficMode, bool)`

GetTrafficModeOk returns a tuple with the TrafficMode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTrafficMode

`func (o *ReachableOptions) SetTrafficMode(v ReachableTrafficMode)`

SetTrafficMode sets TrafficMode field to given value.

### HasTrafficMode

`func (o *ReachableOptions) HasTrafficMode() bool`

HasTrafficMode returns a boolean if a field has been set.

### GetAllowedCountries

`func (o *ReachableOptions) GetAllowedCountries() string`

GetAllowedCountries returns the AllowedCountries field if non-nil, zero value otherwise.

### GetAllowedCountriesOk

`func (o *ReachableOptions) GetAllowedCountriesOk() (*string, bool)`

GetAllowedCountriesOk returns a tuple with the AllowedCountries field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAllowedCountries

`func (o *ReachableOptions) SetAllowedCountries(v string)`

SetAllowedCountries sets AllowedCountries field to given value.

### HasAllowedCountries

`func (o *ReachableOptions) HasAllowedCountries() bool`

HasAllowedCountries returns a boolean if a field has been set.

### GetProhibitedCountries

`func (o *ReachableOptions) GetProhibitedCountries() string`

GetProhibitedCountries returns the ProhibitedCountries field if non-nil, zero value otherwise.

### GetProhibitedCountriesOk

`func (o *ReachableOptions) GetProhibitedCountriesOk() (*string, bool)`

GetProhibitedCountriesOk returns a tuple with the ProhibitedCountries field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProhibitedCountries

`func (o *ReachableOptions) SetProhibitedCountries(v string)`

SetProhibitedCountries sets ProhibitedCountries field to given value.

### HasProhibitedCountries

`func (o *ReachableOptions) HasProhibitedCountries() bool`

HasProhibitedCountries returns a boolean if a field has been set.

### GetBlockIntersectingRoads

`func (o *ReachableOptions) GetBlockIntersectingRoads() string`

GetBlockIntersectingRoads returns the BlockIntersectingRoads field if non-nil, zero value otherwise.

### GetBlockIntersectingRoadsOk

`func (o *ReachableOptions) GetBlockIntersectingRoadsOk() (*string, bool)`

GetBlockIntersectingRoadsOk returns a tuple with the BlockIntersectingRoads field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBlockIntersectingRoads

`func (o *ReachableOptions) SetBlockIntersectingRoads(v string)`

SetBlockIntersectingRoads sets BlockIntersectingRoads field to given value.

### HasBlockIntersectingRoads

`func (o *ReachableOptions) HasBlockIntersectingRoads() bool`

HasBlockIntersectingRoads returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


