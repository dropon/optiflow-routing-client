# ElevationReport

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ascent** | **int32** | Total ascent of the route or leg [m], estimated from sampled elevation data along the route. | 
**Descent** | **int32** | Total descent of the route or leg [m], estimated from sampled elevation data along the route. | 

## Methods

### NewElevationReport

`func NewElevationReport(ascent int32, descent int32, ) *ElevationReport`

NewElevationReport instantiates a new ElevationReport object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewElevationReportWithDefaults

`func NewElevationReportWithDefaults() *ElevationReport`

NewElevationReportWithDefaults instantiates a new ElevationReport object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAscent

`func (o *ElevationReport) GetAscent() int32`

GetAscent returns the Ascent field if non-nil, zero value otherwise.

### GetAscentOk

`func (o *ElevationReport) GetAscentOk() (*int32, bool)`

GetAscentOk returns a tuple with the Ascent field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAscent

`func (o *ElevationReport) SetAscent(v int32)`

SetAscent sets Ascent field to given value.


### GetDescent

`func (o *ElevationReport) GetDescent() int32`

GetDescent returns the Descent field if non-nil, zero value otherwise.

### GetDescentOk

`func (o *ElevationReport) GetDescentOk() (*int32, bool)`

GetDescentOk returns a tuple with the Descent field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescent

`func (o *ElevationReport) SetDescent(v int32)`

SetDescent sets Descent field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


