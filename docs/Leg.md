# Leg

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Distance** | **int32** | The distance of the leg [m]. | 
**TravelTime** | **int32** | The travel time for the leg [s]. | 
**TrafficDelay** | Pointer to **int32** | The total delay due to live traffic on this leg [s].  This value contains the sum of all traffic events on this leg and will be non-zero only if **options[trafficMode]&#x3D;REALISTIC**. See [here](./concepts/traffic-modes) for more information. | [optional] 
**Violated** | **bool** | If there is no valid connection between the waypoints of this leg but the resulting leg can be calculated by using actually prohibited roads, the route is marked as violated. | 
**TollCosts** | Pointer to [**TollCosts**](TollCosts.md) |  | [optional] 
**Polyline** | Pointer to **string** | The polyline of the leg in the format specified by **options[polylineFormat]**. | [optional] 
**EvReport** | Pointer to [**EvReportLeg**](EvReportLeg.md) |  | [optional] 
**ElevationReport** | Pointer to [**ElevationReport**](ElevationReport.md) |  | [optional] 

## Methods

### NewLeg

`func NewLeg(distance int32, travelTime int32, violated bool, ) *Leg`

NewLeg instantiates a new Leg object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLegWithDefaults

`func NewLegWithDefaults() *Leg`

NewLegWithDefaults instantiates a new Leg object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDistance

`func (o *Leg) GetDistance() int32`

GetDistance returns the Distance field if non-nil, zero value otherwise.

### GetDistanceOk

`func (o *Leg) GetDistanceOk() (*int32, bool)`

GetDistanceOk returns a tuple with the Distance field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDistance

`func (o *Leg) SetDistance(v int32)`

SetDistance sets Distance field to given value.


### GetTravelTime

`func (o *Leg) GetTravelTime() int32`

GetTravelTime returns the TravelTime field if non-nil, zero value otherwise.

### GetTravelTimeOk

`func (o *Leg) GetTravelTimeOk() (*int32, bool)`

GetTravelTimeOk returns a tuple with the TravelTime field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTravelTime

`func (o *Leg) SetTravelTime(v int32)`

SetTravelTime sets TravelTime field to given value.


### GetTrafficDelay

`func (o *Leg) GetTrafficDelay() int32`

GetTrafficDelay returns the TrafficDelay field if non-nil, zero value otherwise.

### GetTrafficDelayOk

`func (o *Leg) GetTrafficDelayOk() (*int32, bool)`

GetTrafficDelayOk returns a tuple with the TrafficDelay field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTrafficDelay

`func (o *Leg) SetTrafficDelay(v int32)`

SetTrafficDelay sets TrafficDelay field to given value.

### HasTrafficDelay

`func (o *Leg) HasTrafficDelay() bool`

HasTrafficDelay returns a boolean if a field has been set.

### GetViolated

`func (o *Leg) GetViolated() bool`

GetViolated returns the Violated field if non-nil, zero value otherwise.

### GetViolatedOk

`func (o *Leg) GetViolatedOk() (*bool, bool)`

GetViolatedOk returns a tuple with the Violated field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetViolated

`func (o *Leg) SetViolated(v bool)`

SetViolated sets Violated field to given value.


### GetTollCosts

`func (o *Leg) GetTollCosts() TollCosts`

GetTollCosts returns the TollCosts field if non-nil, zero value otherwise.

### GetTollCostsOk

`func (o *Leg) GetTollCostsOk() (*TollCosts, bool)`

GetTollCostsOk returns a tuple with the TollCosts field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTollCosts

`func (o *Leg) SetTollCosts(v TollCosts)`

SetTollCosts sets TollCosts field to given value.

### HasTollCosts

`func (o *Leg) HasTollCosts() bool`

HasTollCosts returns a boolean if a field has been set.

### GetPolyline

`func (o *Leg) GetPolyline() string`

GetPolyline returns the Polyline field if non-nil, zero value otherwise.

### GetPolylineOk

`func (o *Leg) GetPolylineOk() (*string, bool)`

GetPolylineOk returns a tuple with the Polyline field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPolyline

`func (o *Leg) SetPolyline(v string)`

SetPolyline sets Polyline field to given value.

### HasPolyline

`func (o *Leg) HasPolyline() bool`

HasPolyline returns a boolean if a field has been set.

### GetEvReport

`func (o *Leg) GetEvReport() EvReportLeg`

GetEvReport returns the EvReport field if non-nil, zero value otherwise.

### GetEvReportOk

`func (o *Leg) GetEvReportOk() (*EvReportLeg, bool)`

GetEvReportOk returns a tuple with the EvReport field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEvReport

`func (o *Leg) SetEvReport(v EvReportLeg)`

SetEvReport sets EvReport field to given value.

### HasEvReport

`func (o *Leg) HasEvReport() bool`

HasEvReport returns a boolean if a field has been set.

### GetElevationReport

`func (o *Leg) GetElevationReport() ElevationReport`

GetElevationReport returns the ElevationReport field if non-nil, zero value otherwise.

### GetElevationReportOk

`func (o *Leg) GetElevationReportOk() (*ElevationReport, bool)`

GetElevationReportOk returns a tuple with the ElevationReport field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetElevationReport

`func (o *Leg) SetElevationReport(v ElevationReport)`

SetElevationReport sets ElevationReport field to given value.

### HasElevationReport

`func (o *Leg) HasElevationReport() bool`

HasElevationReport returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


