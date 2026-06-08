# Event

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Latitude** | **float64** | The latitude of the position where the event takes place in degrees (WGS84/EPSG:4326) from south to north. | 
**Longitude** | **float64** | The longitude of the position where the event takes place in degrees (WGS84/EPSG:4326) from west to east. | 
**StartsAt** | Pointer to **time.Time** | The time at which the event starts formatted according to [RFC 3339](https://tools.ietf.org/html/rfc3339). Will not be present for **trafficMode** _AVERAGE_ or _CONSTANT_ when neither **startTime** nor **arrivalTime** is specified. | [optional] 
**DistanceFromStart** | **int32** | The distance from the start to this event [m]. | 
**TravelTimeFromStart** | **int32** | The travel time from the start to this event [s]. | 
**CountryCode** | **string** | Countries are represented according to their [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) or [ISO 3166-2](https://en.wikipedia.org/wiki/ISO_3166-2) if referring to a subdivision. | 
**UtcOffset** | **int32** | The offset to UTC [min]. Will not contain daylight-saving time for **trafficMode** _AVERAGE_ or _CONSTANT_ when neither **startTime** nor **arrivalTime** is specified. | 
**Toll** | Pointer to [**TollEvent**](TollEvent.md) |  | [optional] 
**Maneuver** | Pointer to [**ManeuverEvent**](ManeuverEvent.md) |  | [optional] 
**Border** | Pointer to [**BorderEvent**](BorderEvent.md) |  | [optional] 
**Violation** | Pointer to [**ViolationEvent**](ViolationEvent.md) |  | [optional] 
**Waypoint** | Pointer to [**WaypointEvent**](WaypointEvent.md) |  | [optional] 
**UtcOffsetChange** | Pointer to [**UTCOffsetChangeEvent**](UTCOffsetChangeEvent.md) |  | [optional] 
**Schedule** | Pointer to [**ScheduleEvent**](ScheduleEvent.md) |  | [optional] 
**CombinedTransport** | Pointer to [**CombinedTransportEvent**](CombinedTransportEvent.md) |  | [optional] 
**Traffic** | Pointer to [**TrafficEvent**](TrafficEvent.md) |  | [optional] 
**LowEmissionZone** | Pointer to [**LowEmissionZoneEvent**](LowEmissionZoneEvent.md) |  | [optional] 
**DeliveryOnly** | Pointer to [**DeliveryOnlyEvent**](DeliveryOnlyEvent.md) |  | [optional] 
**EvStatus** | Pointer to [**EvStatusEvent**](EvStatusEvent.md) |  | [optional] 
**Charge** | Pointer to [**ChargeEvent**](ChargeEvent.md) |  | [optional] 

## Methods

### NewEvent

`func NewEvent(latitude float64, longitude float64, distanceFromStart int32, travelTimeFromStart int32, countryCode string, utcOffset int32, ) *Event`

NewEvent instantiates a new Event object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewEventWithDefaults

`func NewEventWithDefaults() *Event`

NewEventWithDefaults instantiates a new Event object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetLatitude

`func (o *Event) GetLatitude() float64`

GetLatitude returns the Latitude field if non-nil, zero value otherwise.

### GetLatitudeOk

`func (o *Event) GetLatitudeOk() (*float64, bool)`

GetLatitudeOk returns a tuple with the Latitude field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLatitude

`func (o *Event) SetLatitude(v float64)`

SetLatitude sets Latitude field to given value.


### GetLongitude

`func (o *Event) GetLongitude() float64`

GetLongitude returns the Longitude field if non-nil, zero value otherwise.

### GetLongitudeOk

`func (o *Event) GetLongitudeOk() (*float64, bool)`

GetLongitudeOk returns a tuple with the Longitude field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLongitude

`func (o *Event) SetLongitude(v float64)`

SetLongitude sets Longitude field to given value.


### GetStartsAt

`func (o *Event) GetStartsAt() time.Time`

GetStartsAt returns the StartsAt field if non-nil, zero value otherwise.

### GetStartsAtOk

`func (o *Event) GetStartsAtOk() (*time.Time, bool)`

GetStartsAtOk returns a tuple with the StartsAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStartsAt

`func (o *Event) SetStartsAt(v time.Time)`

SetStartsAt sets StartsAt field to given value.

### HasStartsAt

`func (o *Event) HasStartsAt() bool`

HasStartsAt returns a boolean if a field has been set.

### GetDistanceFromStart

`func (o *Event) GetDistanceFromStart() int32`

GetDistanceFromStart returns the DistanceFromStart field if non-nil, zero value otherwise.

### GetDistanceFromStartOk

`func (o *Event) GetDistanceFromStartOk() (*int32, bool)`

GetDistanceFromStartOk returns a tuple with the DistanceFromStart field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDistanceFromStart

`func (o *Event) SetDistanceFromStart(v int32)`

SetDistanceFromStart sets DistanceFromStart field to given value.


### GetTravelTimeFromStart

`func (o *Event) GetTravelTimeFromStart() int32`

GetTravelTimeFromStart returns the TravelTimeFromStart field if non-nil, zero value otherwise.

### GetTravelTimeFromStartOk

`func (o *Event) GetTravelTimeFromStartOk() (*int32, bool)`

GetTravelTimeFromStartOk returns a tuple with the TravelTimeFromStart field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTravelTimeFromStart

`func (o *Event) SetTravelTimeFromStart(v int32)`

SetTravelTimeFromStart sets TravelTimeFromStart field to given value.


### GetCountryCode

`func (o *Event) GetCountryCode() string`

GetCountryCode returns the CountryCode field if non-nil, zero value otherwise.

### GetCountryCodeOk

`func (o *Event) GetCountryCodeOk() (*string, bool)`

GetCountryCodeOk returns a tuple with the CountryCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCountryCode

`func (o *Event) SetCountryCode(v string)`

SetCountryCode sets CountryCode field to given value.


### GetUtcOffset

`func (o *Event) GetUtcOffset() int32`

GetUtcOffset returns the UtcOffset field if non-nil, zero value otherwise.

### GetUtcOffsetOk

`func (o *Event) GetUtcOffsetOk() (*int32, bool)`

GetUtcOffsetOk returns a tuple with the UtcOffset field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUtcOffset

`func (o *Event) SetUtcOffset(v int32)`

SetUtcOffset sets UtcOffset field to given value.


### GetToll

`func (o *Event) GetToll() TollEvent`

GetToll returns the Toll field if non-nil, zero value otherwise.

### GetTollOk

`func (o *Event) GetTollOk() (*TollEvent, bool)`

GetTollOk returns a tuple with the Toll field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToll

`func (o *Event) SetToll(v TollEvent)`

SetToll sets Toll field to given value.

### HasToll

`func (o *Event) HasToll() bool`

HasToll returns a boolean if a field has been set.

### GetManeuver

`func (o *Event) GetManeuver() ManeuverEvent`

GetManeuver returns the Maneuver field if non-nil, zero value otherwise.

### GetManeuverOk

`func (o *Event) GetManeuverOk() (*ManeuverEvent, bool)`

GetManeuverOk returns a tuple with the Maneuver field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetManeuver

`func (o *Event) SetManeuver(v ManeuverEvent)`

SetManeuver sets Maneuver field to given value.

### HasManeuver

`func (o *Event) HasManeuver() bool`

HasManeuver returns a boolean if a field has been set.

### GetBorder

`func (o *Event) GetBorder() BorderEvent`

GetBorder returns the Border field if non-nil, zero value otherwise.

### GetBorderOk

`func (o *Event) GetBorderOk() (*BorderEvent, bool)`

GetBorderOk returns a tuple with the Border field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBorder

`func (o *Event) SetBorder(v BorderEvent)`

SetBorder sets Border field to given value.

### HasBorder

`func (o *Event) HasBorder() bool`

HasBorder returns a boolean if a field has been set.

### GetViolation

`func (o *Event) GetViolation() ViolationEvent`

GetViolation returns the Violation field if non-nil, zero value otherwise.

### GetViolationOk

`func (o *Event) GetViolationOk() (*ViolationEvent, bool)`

GetViolationOk returns a tuple with the Violation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetViolation

`func (o *Event) SetViolation(v ViolationEvent)`

SetViolation sets Violation field to given value.

### HasViolation

`func (o *Event) HasViolation() bool`

HasViolation returns a boolean if a field has been set.

### GetWaypoint

`func (o *Event) GetWaypoint() WaypointEvent`

GetWaypoint returns the Waypoint field if non-nil, zero value otherwise.

### GetWaypointOk

`func (o *Event) GetWaypointOk() (*WaypointEvent, bool)`

GetWaypointOk returns a tuple with the Waypoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetWaypoint

`func (o *Event) SetWaypoint(v WaypointEvent)`

SetWaypoint sets Waypoint field to given value.

### HasWaypoint

`func (o *Event) HasWaypoint() bool`

HasWaypoint returns a boolean if a field has been set.

### GetUtcOffsetChange

`func (o *Event) GetUtcOffsetChange() UTCOffsetChangeEvent`

GetUtcOffsetChange returns the UtcOffsetChange field if non-nil, zero value otherwise.

### GetUtcOffsetChangeOk

`func (o *Event) GetUtcOffsetChangeOk() (*UTCOffsetChangeEvent, bool)`

GetUtcOffsetChangeOk returns a tuple with the UtcOffsetChange field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUtcOffsetChange

`func (o *Event) SetUtcOffsetChange(v UTCOffsetChangeEvent)`

SetUtcOffsetChange sets UtcOffsetChange field to given value.

### HasUtcOffsetChange

`func (o *Event) HasUtcOffsetChange() bool`

HasUtcOffsetChange returns a boolean if a field has been set.

### GetSchedule

`func (o *Event) GetSchedule() ScheduleEvent`

GetSchedule returns the Schedule field if non-nil, zero value otherwise.

### GetScheduleOk

`func (o *Event) GetScheduleOk() (*ScheduleEvent, bool)`

GetScheduleOk returns a tuple with the Schedule field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSchedule

`func (o *Event) SetSchedule(v ScheduleEvent)`

SetSchedule sets Schedule field to given value.

### HasSchedule

`func (o *Event) HasSchedule() bool`

HasSchedule returns a boolean if a field has been set.

### GetCombinedTransport

`func (o *Event) GetCombinedTransport() CombinedTransportEvent`

GetCombinedTransport returns the CombinedTransport field if non-nil, zero value otherwise.

### GetCombinedTransportOk

`func (o *Event) GetCombinedTransportOk() (*CombinedTransportEvent, bool)`

GetCombinedTransportOk returns a tuple with the CombinedTransport field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCombinedTransport

`func (o *Event) SetCombinedTransport(v CombinedTransportEvent)`

SetCombinedTransport sets CombinedTransport field to given value.

### HasCombinedTransport

`func (o *Event) HasCombinedTransport() bool`

HasCombinedTransport returns a boolean if a field has been set.

### GetTraffic

`func (o *Event) GetTraffic() TrafficEvent`

GetTraffic returns the Traffic field if non-nil, zero value otherwise.

### GetTrafficOk

`func (o *Event) GetTrafficOk() (*TrafficEvent, bool)`

GetTrafficOk returns a tuple with the Traffic field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTraffic

`func (o *Event) SetTraffic(v TrafficEvent)`

SetTraffic sets Traffic field to given value.

### HasTraffic

`func (o *Event) HasTraffic() bool`

HasTraffic returns a boolean if a field has been set.

### GetLowEmissionZone

`func (o *Event) GetLowEmissionZone() LowEmissionZoneEvent`

GetLowEmissionZone returns the LowEmissionZone field if non-nil, zero value otherwise.

### GetLowEmissionZoneOk

`func (o *Event) GetLowEmissionZoneOk() (*LowEmissionZoneEvent, bool)`

GetLowEmissionZoneOk returns a tuple with the LowEmissionZone field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLowEmissionZone

`func (o *Event) SetLowEmissionZone(v LowEmissionZoneEvent)`

SetLowEmissionZone sets LowEmissionZone field to given value.

### HasLowEmissionZone

`func (o *Event) HasLowEmissionZone() bool`

HasLowEmissionZone returns a boolean if a field has been set.

### GetDeliveryOnly

`func (o *Event) GetDeliveryOnly() DeliveryOnlyEvent`

GetDeliveryOnly returns the DeliveryOnly field if non-nil, zero value otherwise.

### GetDeliveryOnlyOk

`func (o *Event) GetDeliveryOnlyOk() (*DeliveryOnlyEvent, bool)`

GetDeliveryOnlyOk returns a tuple with the DeliveryOnly field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDeliveryOnly

`func (o *Event) SetDeliveryOnly(v DeliveryOnlyEvent)`

SetDeliveryOnly sets DeliveryOnly field to given value.

### HasDeliveryOnly

`func (o *Event) HasDeliveryOnly() bool`

HasDeliveryOnly returns a boolean if a field has been set.

### GetEvStatus

`func (o *Event) GetEvStatus() EvStatusEvent`

GetEvStatus returns the EvStatus field if non-nil, zero value otherwise.

### GetEvStatusOk

`func (o *Event) GetEvStatusOk() (*EvStatusEvent, bool)`

GetEvStatusOk returns a tuple with the EvStatus field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEvStatus

`func (o *Event) SetEvStatus(v EvStatusEvent)`

SetEvStatus sets EvStatus field to given value.

### HasEvStatus

`func (o *Event) HasEvStatus() bool`

HasEvStatus returns a boolean if a field has been set.

### GetCharge

`func (o *Event) GetCharge() ChargeEvent`

GetCharge returns the Charge field if non-nil, zero value otherwise.

### GetChargeOk

`func (o *Event) GetChargeOk() (*ChargeEvent, bool)`

GetChargeOk returns a tuple with the Charge field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCharge

`func (o *Event) SetCharge(v ChargeEvent)`

SetCharge sets Charge field to given value.

### HasCharge

`func (o *Event) HasCharge() bool`

HasCharge returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


