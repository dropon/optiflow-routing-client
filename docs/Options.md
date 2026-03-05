# Options

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StartTime** | Pointer to **time.Time** | Defines the start time of the route formatted according to [RFC 3339](https://tools.ietf.org/html/rfc3339). If none of them is specified the current time will be used as the start time for **trafficMode** _REALISTIC_.  If the date-time string does not include an explicit offset to UTC, the time will be interpreted as the local time of the start waypoint. The date must not be before 1970-01-01T00:00:00+00:00 nor after 2037-12-31T23:59:59+00:00.  The response will contain the offset to UTC specified in the request or that of the start waypoint. For best results it should not be more than one month in the past nor more than six months in the future.   This parameter is mutually exclusive with **arrivalTime** and **tollTime**. See [here](./concepts/date-and-time) for more information on the relevance of date and time. | [optional] 
**ArrivalTime** | Pointer to **time.Time** | Defines the arrival time of the route formatted according to [RFC 3339](https://tools.ietf.org/html/rfc3339).  If the date-time string does not include an explicit offset to UTC, the time will be interpreted as the local time of the destination waypoint. The date must not be before 1970-01-01T00:00:00+00:00 nor after 2037-12-31T23:59:59+00:00.  The response will contain the offset to UTC specified in the request or that of the destination waypoint. For best results it should not be more than one month in the past nor more than six months in the future.   This parameter is mutually exclusive with **startTime** and **tollTime** and cannot be used with the **results** _SCHEDULE_REPORT_ and _SCHEDULE_EVENT_ nor when **openingIntervals**, **serviceTime** or **workingHoursPreset** are specified. See [here](./concepts/date-and-time) for more information on the relevance of date and time. | [optional] 
**TollTime** | Pointer to **time.Time** | Defines the date and time at which to calculate toll prices formatted according to [RFC 3339](https://tools.ietf.org/html/rfc3339).  If the date-time string does not include an explicit offset to UTC, the time will be interpreted as the local time of the start waypoint. The date must not be before 1970-01-01T00:00:00+00:00 nor after 2037-12-31T23:59:59+00:00.   This parameter only has an influence if toll related results are requested. It can only be used in combination with **trafficMode** _AVERAGE_  and is mutually exclusive with both **startTime** and **arrivalTime**. It will be ignored for non-motorized profiles such as _BICYCLE_ or _PEDESTRIAN_. See [here](./concepts/date-and-time) for more information on the relevance of date and time. | [optional] 
**TrafficMode** | Pointer to [**TrafficMode**](TrafficMode.md) |  | [optional] [default to REALISTIC]
**Language** | Pointer to **string** | The language of texts such as the descriptions of _MANEUVER_EVENTS_ and _TRAFFIC_EVENTS_. Languages have to be specified according to their [ISO-639-1](https://www.loc.gov/standards/iso639-2/php/code_list.php) code or as a combination of language code and sub-tag according to [BCP47](https://tools.ietf.org/rfc/bcp/bcp47.txt).   The **warningCode** _ROUTING_MANEUVERS_IN_DIFFERENT_LANGUAGE_ is returned if the language is not supported for maneuvers. | [optional] [default to "en"]
**PolylineFormat** | Pointer to [**PolylineFormat**](PolylineFormat.md) |  | [optional] [default to GEO_JSON]
**PolylineMapType** | Pointer to [**PolylineMapType**](PolylineMapType.md) |  | [optional] [default to RASTER]
**AllowedCountries** | Pointer to **string** | Comma-separated list of countries the route is allowed to pass. By default, all countries are allowed. If this parameter is present, only these countries are allowed to be passed, i.e. drive only in these countries. Countries are represented according to their [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) or [ISO 3166-2](https://en.wikipedia.org/wiki/ISO_3166-2) if referring to a subdivision. This parameter is mutually exclusive with **prohibitedCountries** and will be ignored, if a **routeId** is specified. | [optional] 
**ProhibitedCountries** | Pointer to **string** | Comma-separated list of countries the route must not pass. By default, all countries are allowed. If this parameter is present, all but the given countries are allowed to be passed, i.e. do not drive in these countries.  Countries are represented according to their [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) or [ISO 3166-2](https://en.wikipedia.org/wiki/ISO_3166-2) if referring to a subdivision. This parameter is mutually exclusive with **allowedCountries** and will be ignored, if a **routeId** is specified. | [optional] 
**Currency** | Pointer to **string** | The currency code according to [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217).   If it is not specified, the currency is taken from the **profile**.   It is used for the costs in the monetary cost report if _MONETARY_COSTS_ are requested in the **results** and for  toll price conversion if _TOLL_COSTS_ or _TOLL_SECTIONS_ are requested in the **results**. Furthermore, it is used  when setting **options[routingMode]&#x3D;MONETARY**. | [optional] 
**PreferTurnsOnPassengerSide** | Pointer to **bool** | Specifies that the route is constructed such that turns to the passenger side are preferred.  This parameter will be ignored, if **options[routingMode]&#x3D;MONETARY**, **vehicle[truckRoutes]** or a **routeId** is specified. It will also be ignored for non-motorized profiles such as _BICYCLE_ or _PEDESTRIAN_.  | [optional] [default to false]
**Avoid** | Pointer to **string** | Comma-separated list of features which should be avoided on the route. Avoided features could be included in a route if there is no possibility to reach the target otherwise.  Available values are provided by type &#x60;AvoidFeature&#x60;: * &#x60;TOLL&#x60; - Avoid roads with toll. * &#x60;FERRIES&#x60; - Avoid ferries. Ferries which cannot be avoided can be requested with _COMBINED_TRANSPORT_EVENTS_ and will appear with the type _BOAT_. * &#x60;RAIL_SHUTTLES&#x60; - Avoid rail shuttles. Rail shuttles which cannot be avoided can be requested with _COMBINED_TRANSPORT_EVENTS_ and will appear with the type _RAIL_. * &#x60;HIGHWAYS&#x60; - Avoid highways and motorways. Waypoints will not be matched to highways, they will be matched to the nearest road which is not a highway.  This parameter will be ignored, if **options[routingMode]&#x3D;MONETARY** or a **routeId** is specified. See [here](./concepts/avoid) for more information.  | [optional] 
**BlockIntersectingRoads** | Pointer to **string** | Pipe-separated list of polylines.   Roads and combined transports that intersect the given polylines will be considered as prohibited and will not be used in the route calculation. Each list element is a polyline. Each point is a coordinate of latitude and longitude. Coordinates and points are separated by a comma. Format: &#x60;&lt;poly1_lat1&gt;,&lt;poly1_lon1&gt;,...,&lt;poly1_latN&gt;,&lt;poly1_lonN&gt;|&lt;poly2_lat1&gt;,&lt;poly2_lon1&gt;,...,&lt;poly2_latN&gt;,&lt;poly2_lonN&gt;|...&#x60;   Notes: * Be aware of the URL length restrictions. * If there is no other route connecting two waypoints the will be reported as violated and correspondingly violation events with type **BLOCKED_ROAD_BY_INTERSECTION** will be reported if violation events are requested. * Requests will be rejected if at least one provided polyline   * does not consist of an even number of coordinates,   * consists of less than two points,   * contains invalid coordinates or   * intersects more than 5000 road segments.  This parameter will be ignored, if a **routeId** is specified.  | [optional] 
**CustomRoadAttributeScenarios** | Pointer to **string** | Comma-separated list of [custom road attribute scenarios](../data-api/concepts/custom-road-attributes) to be considered in the route calculation.  Each scenario can be specified by its name or its ID. A shared scenario can only be specified by its ID.  The size limitations that apply to each scenario, also apply to the collection of scenarios, i.e. the limit  on the number of roads in one scenario can not be circumvented by splitting it in multiple scenarios. If the request contains a **routeId**, specifying custom road attribute scenarios may lead to violated routes in case one of the requested scenarios prohibits roads on the route represented by the **routeId**. | [optional] 
**RoutingMode** | Pointer to [**RoutingMode**](RoutingMode.md) |  | [optional] [default to FAST]
**MaximumSpeed** | Pointer to **int32** | The maximum speed of the vehicle [km/h]. The speeds for calculating the driving times on all roads will be limited to this value.  See [here](./concepts/speeds) for more information. | [optional] 
**SpeedFactor** | Pointer to **float64** | An additional factor to apply to the speed of the vehicle. This modified speed is used to modify the driving times after the route has been calculated. That means in particular that the route itself will not be modified by applying a speed factor. When lower than one, the driving time of the vehicle will increase, when greater than one, the driving time of the vehicle will decrease. Note that the factor is only applied on the parts of the route where the vehicle is driving. Therefore, a speed factor of 1.1 does not necessarily mean that the **travelTime** of the resulting route will be 10% faster. The speed is not capped by the maximum speed of the  vehicle or of the road.  See [here](./concepts/speeds) for more information. | [optional] [default to 1]

## Methods

### NewOptions

`func NewOptions() *Options`

NewOptions instantiates a new Options object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOptionsWithDefaults

`func NewOptionsWithDefaults() *Options`

NewOptionsWithDefaults instantiates a new Options object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetStartTime

`func (o *Options) GetStartTime() time.Time`

GetStartTime returns the StartTime field if non-nil, zero value otherwise.

### GetStartTimeOk

`func (o *Options) GetStartTimeOk() (*time.Time, bool)`

GetStartTimeOk returns a tuple with the StartTime field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStartTime

`func (o *Options) SetStartTime(v time.Time)`

SetStartTime sets StartTime field to given value.

### HasStartTime

`func (o *Options) HasStartTime() bool`

HasStartTime returns a boolean if a field has been set.

### GetArrivalTime

`func (o *Options) GetArrivalTime() time.Time`

GetArrivalTime returns the ArrivalTime field if non-nil, zero value otherwise.

### GetArrivalTimeOk

`func (o *Options) GetArrivalTimeOk() (*time.Time, bool)`

GetArrivalTimeOk returns a tuple with the ArrivalTime field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetArrivalTime

`func (o *Options) SetArrivalTime(v time.Time)`

SetArrivalTime sets ArrivalTime field to given value.

### HasArrivalTime

`func (o *Options) HasArrivalTime() bool`

HasArrivalTime returns a boolean if a field has been set.

### GetTollTime

`func (o *Options) GetTollTime() time.Time`

GetTollTime returns the TollTime field if non-nil, zero value otherwise.

### GetTollTimeOk

`func (o *Options) GetTollTimeOk() (*time.Time, bool)`

GetTollTimeOk returns a tuple with the TollTime field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTollTime

`func (o *Options) SetTollTime(v time.Time)`

SetTollTime sets TollTime field to given value.

### HasTollTime

`func (o *Options) HasTollTime() bool`

HasTollTime returns a boolean if a field has been set.

### GetTrafficMode

`func (o *Options) GetTrafficMode() TrafficMode`

GetTrafficMode returns the TrafficMode field if non-nil, zero value otherwise.

### GetTrafficModeOk

`func (o *Options) GetTrafficModeOk() (*TrafficMode, bool)`

GetTrafficModeOk returns a tuple with the TrafficMode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTrafficMode

`func (o *Options) SetTrafficMode(v TrafficMode)`

SetTrafficMode sets TrafficMode field to given value.

### HasTrafficMode

`func (o *Options) HasTrafficMode() bool`

HasTrafficMode returns a boolean if a field has been set.

### GetLanguage

`func (o *Options) GetLanguage() string`

GetLanguage returns the Language field if non-nil, zero value otherwise.

### GetLanguageOk

`func (o *Options) GetLanguageOk() (*string, bool)`

GetLanguageOk returns a tuple with the Language field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLanguage

`func (o *Options) SetLanguage(v string)`

SetLanguage sets Language field to given value.

### HasLanguage

`func (o *Options) HasLanguage() bool`

HasLanguage returns a boolean if a field has been set.

### GetPolylineFormat

`func (o *Options) GetPolylineFormat() PolylineFormat`

GetPolylineFormat returns the PolylineFormat field if non-nil, zero value otherwise.

### GetPolylineFormatOk

`func (o *Options) GetPolylineFormatOk() (*PolylineFormat, bool)`

GetPolylineFormatOk returns a tuple with the PolylineFormat field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPolylineFormat

`func (o *Options) SetPolylineFormat(v PolylineFormat)`

SetPolylineFormat sets PolylineFormat field to given value.

### HasPolylineFormat

`func (o *Options) HasPolylineFormat() bool`

HasPolylineFormat returns a boolean if a field has been set.

### GetPolylineMapType

`func (o *Options) GetPolylineMapType() PolylineMapType`

GetPolylineMapType returns the PolylineMapType field if non-nil, zero value otherwise.

### GetPolylineMapTypeOk

`func (o *Options) GetPolylineMapTypeOk() (*PolylineMapType, bool)`

GetPolylineMapTypeOk returns a tuple with the PolylineMapType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPolylineMapType

`func (o *Options) SetPolylineMapType(v PolylineMapType)`

SetPolylineMapType sets PolylineMapType field to given value.

### HasPolylineMapType

`func (o *Options) HasPolylineMapType() bool`

HasPolylineMapType returns a boolean if a field has been set.

### GetAllowedCountries

`func (o *Options) GetAllowedCountries() string`

GetAllowedCountries returns the AllowedCountries field if non-nil, zero value otherwise.

### GetAllowedCountriesOk

`func (o *Options) GetAllowedCountriesOk() (*string, bool)`

GetAllowedCountriesOk returns a tuple with the AllowedCountries field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAllowedCountries

`func (o *Options) SetAllowedCountries(v string)`

SetAllowedCountries sets AllowedCountries field to given value.

### HasAllowedCountries

`func (o *Options) HasAllowedCountries() bool`

HasAllowedCountries returns a boolean if a field has been set.

### GetProhibitedCountries

`func (o *Options) GetProhibitedCountries() string`

GetProhibitedCountries returns the ProhibitedCountries field if non-nil, zero value otherwise.

### GetProhibitedCountriesOk

`func (o *Options) GetProhibitedCountriesOk() (*string, bool)`

GetProhibitedCountriesOk returns a tuple with the ProhibitedCountries field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProhibitedCountries

`func (o *Options) SetProhibitedCountries(v string)`

SetProhibitedCountries sets ProhibitedCountries field to given value.

### HasProhibitedCountries

`func (o *Options) HasProhibitedCountries() bool`

HasProhibitedCountries returns a boolean if a field has been set.

### GetCurrency

`func (o *Options) GetCurrency() string`

GetCurrency returns the Currency field if non-nil, zero value otherwise.

### GetCurrencyOk

`func (o *Options) GetCurrencyOk() (*string, bool)`

GetCurrencyOk returns a tuple with the Currency field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCurrency

`func (o *Options) SetCurrency(v string)`

SetCurrency sets Currency field to given value.

### HasCurrency

`func (o *Options) HasCurrency() bool`

HasCurrency returns a boolean if a field has been set.

### GetPreferTurnsOnPassengerSide

`func (o *Options) GetPreferTurnsOnPassengerSide() bool`

GetPreferTurnsOnPassengerSide returns the PreferTurnsOnPassengerSide field if non-nil, zero value otherwise.

### GetPreferTurnsOnPassengerSideOk

`func (o *Options) GetPreferTurnsOnPassengerSideOk() (*bool, bool)`

GetPreferTurnsOnPassengerSideOk returns a tuple with the PreferTurnsOnPassengerSide field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPreferTurnsOnPassengerSide

`func (o *Options) SetPreferTurnsOnPassengerSide(v bool)`

SetPreferTurnsOnPassengerSide sets PreferTurnsOnPassengerSide field to given value.

### HasPreferTurnsOnPassengerSide

`func (o *Options) HasPreferTurnsOnPassengerSide() bool`

HasPreferTurnsOnPassengerSide returns a boolean if a field has been set.

### GetAvoid

`func (o *Options) GetAvoid() string`

GetAvoid returns the Avoid field if non-nil, zero value otherwise.

### GetAvoidOk

`func (o *Options) GetAvoidOk() (*string, bool)`

GetAvoidOk returns a tuple with the Avoid field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAvoid

`func (o *Options) SetAvoid(v string)`

SetAvoid sets Avoid field to given value.

### HasAvoid

`func (o *Options) HasAvoid() bool`

HasAvoid returns a boolean if a field has been set.

### GetBlockIntersectingRoads

`func (o *Options) GetBlockIntersectingRoads() string`

GetBlockIntersectingRoads returns the BlockIntersectingRoads field if non-nil, zero value otherwise.

### GetBlockIntersectingRoadsOk

`func (o *Options) GetBlockIntersectingRoadsOk() (*string, bool)`

GetBlockIntersectingRoadsOk returns a tuple with the BlockIntersectingRoads field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBlockIntersectingRoads

`func (o *Options) SetBlockIntersectingRoads(v string)`

SetBlockIntersectingRoads sets BlockIntersectingRoads field to given value.

### HasBlockIntersectingRoads

`func (o *Options) HasBlockIntersectingRoads() bool`

HasBlockIntersectingRoads returns a boolean if a field has been set.

### GetCustomRoadAttributeScenarios

`func (o *Options) GetCustomRoadAttributeScenarios() string`

GetCustomRoadAttributeScenarios returns the CustomRoadAttributeScenarios field if non-nil, zero value otherwise.

### GetCustomRoadAttributeScenariosOk

`func (o *Options) GetCustomRoadAttributeScenariosOk() (*string, bool)`

GetCustomRoadAttributeScenariosOk returns a tuple with the CustomRoadAttributeScenarios field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCustomRoadAttributeScenarios

`func (o *Options) SetCustomRoadAttributeScenarios(v string)`

SetCustomRoadAttributeScenarios sets CustomRoadAttributeScenarios field to given value.

### HasCustomRoadAttributeScenarios

`func (o *Options) HasCustomRoadAttributeScenarios() bool`

HasCustomRoadAttributeScenarios returns a boolean if a field has been set.

### GetRoutingMode

`func (o *Options) GetRoutingMode() RoutingMode`

GetRoutingMode returns the RoutingMode field if non-nil, zero value otherwise.

### GetRoutingModeOk

`func (o *Options) GetRoutingModeOk() (*RoutingMode, bool)`

GetRoutingModeOk returns a tuple with the RoutingMode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRoutingMode

`func (o *Options) SetRoutingMode(v RoutingMode)`

SetRoutingMode sets RoutingMode field to given value.

### HasRoutingMode

`func (o *Options) HasRoutingMode() bool`

HasRoutingMode returns a boolean if a field has been set.

### GetMaximumSpeed

`func (o *Options) GetMaximumSpeed() int32`

GetMaximumSpeed returns the MaximumSpeed field if non-nil, zero value otherwise.

### GetMaximumSpeedOk

`func (o *Options) GetMaximumSpeedOk() (*int32, bool)`

GetMaximumSpeedOk returns a tuple with the MaximumSpeed field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMaximumSpeed

`func (o *Options) SetMaximumSpeed(v int32)`

SetMaximumSpeed sets MaximumSpeed field to given value.

### HasMaximumSpeed

`func (o *Options) HasMaximumSpeed() bool`

HasMaximumSpeed returns a boolean if a field has been set.

### GetSpeedFactor

`func (o *Options) GetSpeedFactor() float64`

GetSpeedFactor returns the SpeedFactor field if non-nil, zero value otherwise.

### GetSpeedFactorOk

`func (o *Options) GetSpeedFactorOk() (*float64, bool)`

GetSpeedFactorOk returns a tuple with the SpeedFactor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSpeedFactor

`func (o *Options) SetSpeedFactor(v float64)`

SetSpeedFactor sets SpeedFactor field to given value.

### HasSpeedFactor

`func (o *Options) HasSpeedFactor() bool`

HasSpeedFactor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


