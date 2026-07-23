# PenaltyOptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ByRoadCategory** | Pointer to **[]int32** | Penalty values per road category [8 elements]. The first element represents motorways, the last one pedestrian and cycle paths. See [here](../data-api/concepts/road-categories) for more information on road categories. Cannot be used together with **options[avoid]&#x3D;HIGHWAYS** or **options[routingMode]&#x3D;SHORTEST**.  Example: &#x60;[0,0,15,35,100,255,1000,1000]&#x60; | [optional] 
**DeliveryOnly** | Pointer to **int32** | Penalty for roads that are restricted to delivery vehicles only. The value 2501 is currently not supported. | [optional] 
**ResidentsOnly** | Pointer to **int32** | Penalty for roads that are restricted to residents only. | [optional] 
**Toll** | Pointer to **int32** | Penalty for toll roads. Cannot be used together with **options[avoid]&#x3D;TOLL**. | [optional] 
**Ferries** | Pointer to **int32** | Penalty for ferries. Cannot be used together with **options[avoid]&#x3D;FERRIES**. | [optional] 
**RailShuttles** | Pointer to **int32** | Penalty for rail shuttles. Cannot be used together with **options[avoid]&#x3D;RAIL_SHUTTLES**. | [optional] 

## Methods

### NewPenaltyOptions

`func NewPenaltyOptions() *PenaltyOptions`

NewPenaltyOptions instantiates a new PenaltyOptions object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPenaltyOptionsWithDefaults

`func NewPenaltyOptionsWithDefaults() *PenaltyOptions`

NewPenaltyOptionsWithDefaults instantiates a new PenaltyOptions object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetByRoadCategory

`func (o *PenaltyOptions) GetByRoadCategory() []int32`

GetByRoadCategory returns the ByRoadCategory field if non-nil, zero value otherwise.

### GetByRoadCategoryOk

`func (o *PenaltyOptions) GetByRoadCategoryOk() (*[]int32, bool)`

GetByRoadCategoryOk returns a tuple with the ByRoadCategory field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetByRoadCategory

`func (o *PenaltyOptions) SetByRoadCategory(v []int32)`

SetByRoadCategory sets ByRoadCategory field to given value.

### HasByRoadCategory

`func (o *PenaltyOptions) HasByRoadCategory() bool`

HasByRoadCategory returns a boolean if a field has been set.

### GetDeliveryOnly

`func (o *PenaltyOptions) GetDeliveryOnly() int32`

GetDeliveryOnly returns the DeliveryOnly field if non-nil, zero value otherwise.

### GetDeliveryOnlyOk

`func (o *PenaltyOptions) GetDeliveryOnlyOk() (*int32, bool)`

GetDeliveryOnlyOk returns a tuple with the DeliveryOnly field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDeliveryOnly

`func (o *PenaltyOptions) SetDeliveryOnly(v int32)`

SetDeliveryOnly sets DeliveryOnly field to given value.

### HasDeliveryOnly

`func (o *PenaltyOptions) HasDeliveryOnly() bool`

HasDeliveryOnly returns a boolean if a field has been set.

### GetResidentsOnly

`func (o *PenaltyOptions) GetResidentsOnly() int32`

GetResidentsOnly returns the ResidentsOnly field if non-nil, zero value otherwise.

### GetResidentsOnlyOk

`func (o *PenaltyOptions) GetResidentsOnlyOk() (*int32, bool)`

GetResidentsOnlyOk returns a tuple with the ResidentsOnly field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResidentsOnly

`func (o *PenaltyOptions) SetResidentsOnly(v int32)`

SetResidentsOnly sets ResidentsOnly field to given value.

### HasResidentsOnly

`func (o *PenaltyOptions) HasResidentsOnly() bool`

HasResidentsOnly returns a boolean if a field has been set.

### GetToll

`func (o *PenaltyOptions) GetToll() int32`

GetToll returns the Toll field if non-nil, zero value otherwise.

### GetTollOk

`func (o *PenaltyOptions) GetTollOk() (*int32, bool)`

GetTollOk returns a tuple with the Toll field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToll

`func (o *PenaltyOptions) SetToll(v int32)`

SetToll sets Toll field to given value.

### HasToll

`func (o *PenaltyOptions) HasToll() bool`

HasToll returns a boolean if a field has been set.

### GetFerries

`func (o *PenaltyOptions) GetFerries() int32`

GetFerries returns the Ferries field if non-nil, zero value otherwise.

### GetFerriesOk

`func (o *PenaltyOptions) GetFerriesOk() (*int32, bool)`

GetFerriesOk returns a tuple with the Ferries field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFerries

`func (o *PenaltyOptions) SetFerries(v int32)`

SetFerries sets Ferries field to given value.

### HasFerries

`func (o *PenaltyOptions) HasFerries() bool`

HasFerries returns a boolean if a field has been set.

### GetRailShuttles

`func (o *PenaltyOptions) GetRailShuttles() int32`

GetRailShuttles returns the RailShuttles field if non-nil, zero value otherwise.

### GetRailShuttlesOk

`func (o *PenaltyOptions) GetRailShuttlesOk() (*int32, bool)`

GetRailShuttlesOk returns a tuple with the RailShuttles field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRailShuttles

`func (o *PenaltyOptions) SetRailShuttles(v int32)`

SetRailShuttles sets RailShuttles field to given value.

### HasRailShuttles

`func (o *PenaltyOptions) HasRailShuttles() bool`

HasRailShuttles returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


