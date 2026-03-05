# SpeedByRoadCategory

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MinimumSpeed** | **int32** | The minimum speed of the vehicle [km/h] for roads of this road category. Must be less or equal to the maximum speed. | 
**MaximumSpeed** | **int32** | The maximum speed of the vehicle [km/h] for roads of this road category. Must be greater or equal to the minimum speed. | 

## Methods

### NewSpeedByRoadCategory

`func NewSpeedByRoadCategory(minimumSpeed int32, maximumSpeed int32, ) *SpeedByRoadCategory`

NewSpeedByRoadCategory instantiates a new SpeedByRoadCategory object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSpeedByRoadCategoryWithDefaults

`func NewSpeedByRoadCategoryWithDefaults() *SpeedByRoadCategory`

NewSpeedByRoadCategoryWithDefaults instantiates a new SpeedByRoadCategory object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMinimumSpeed

`func (o *SpeedByRoadCategory) GetMinimumSpeed() int32`

GetMinimumSpeed returns the MinimumSpeed field if non-nil, zero value otherwise.

### GetMinimumSpeedOk

`func (o *SpeedByRoadCategory) GetMinimumSpeedOk() (*int32, bool)`

GetMinimumSpeedOk returns a tuple with the MinimumSpeed field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMinimumSpeed

`func (o *SpeedByRoadCategory) SetMinimumSpeed(v int32)`

SetMinimumSpeed sets MinimumSpeed field to given value.


### GetMaximumSpeed

`func (o *SpeedByRoadCategory) GetMaximumSpeed() int32`

GetMaximumSpeed returns the MaximumSpeed field if non-nil, zero value otherwise.

### GetMaximumSpeedOk

`func (o *SpeedByRoadCategory) GetMaximumSpeedOk() (*int32, bool)`

GetMaximumSpeedOk returns a tuple with the MaximumSpeed field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMaximumSpeed

`func (o *SpeedByRoadCategory) SetMaximumSpeed(v int32)`

SetMaximumSpeed sets MaximumSpeed field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


