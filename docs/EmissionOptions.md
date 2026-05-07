# EmissionOptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CalculationMethods** | **string** | Comma-separated list of the calculation method to be returned.  Available values are provided by type &#x60;EmissionCalculationMethod&#x60;:  * &#x60;EN16258_2012&#x60;     Emissions according to EN16258 from 2012 (a.k.a. CEN).  * &#x60;ISO14083_2023&#x60;     Emissions according to ISO 14083:2023 (a.k.a. ISO).      Only supported for [European and American profiles](../data-api/concepts/profiles).     If **defaultConsumption** is true, only supported for [European profiles](../data-api/concepts/profiles).  * &#x60;FRENCH_CO2E_DECREE_2017_639&#x60;     Emissions according to the French CO2E decree from 2017. | 
**DefaultConsumption** | Pointer to **bool** | If true, the fuel or electricity consumption is automatically calculated through HBEFA 4.2.  Otherwise, the **averageFuelConsumption** or **averageElectricityConsumption** specified calculating the route represented by **routeId** will be considered. This requires elevations, which are unavailable for some regions beyond −60° and +60° latitude. If elevations are unavailable for any part of a route, a _ROUTING_ELEVATIONS_UNAVAILABLE_ warning will be returned. This parameter will be ignored for calculation method _FRENCH_CO2E_DECREE_2017_639_. | [optional] [default to false]
**Iso14083EmissionFactorsVersion** | Pointer to [**Iso14083EmissionFactorsVersion**](Iso14083EmissionFactorsVersion.md) |  | [optional] [default to INITIAL]

## Methods

### NewEmissionOptions

`func NewEmissionOptions(calculationMethods string, ) *EmissionOptions`

NewEmissionOptions instantiates a new EmissionOptions object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewEmissionOptionsWithDefaults

`func NewEmissionOptionsWithDefaults() *EmissionOptions`

NewEmissionOptionsWithDefaults instantiates a new EmissionOptions object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCalculationMethods

`func (o *EmissionOptions) GetCalculationMethods() string`

GetCalculationMethods returns the CalculationMethods field if non-nil, zero value otherwise.

### GetCalculationMethodsOk

`func (o *EmissionOptions) GetCalculationMethodsOk() (*string, bool)`

GetCalculationMethodsOk returns a tuple with the CalculationMethods field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCalculationMethods

`func (o *EmissionOptions) SetCalculationMethods(v string)`

SetCalculationMethods sets CalculationMethods field to given value.


### GetDefaultConsumption

`func (o *EmissionOptions) GetDefaultConsumption() bool`

GetDefaultConsumption returns the DefaultConsumption field if non-nil, zero value otherwise.

### GetDefaultConsumptionOk

`func (o *EmissionOptions) GetDefaultConsumptionOk() (*bool, bool)`

GetDefaultConsumptionOk returns a tuple with the DefaultConsumption field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDefaultConsumption

`func (o *EmissionOptions) SetDefaultConsumption(v bool)`

SetDefaultConsumption sets DefaultConsumption field to given value.

### HasDefaultConsumption

`func (o *EmissionOptions) HasDefaultConsumption() bool`

HasDefaultConsumption returns a boolean if a field has been set.

### GetIso14083EmissionFactorsVersion

`func (o *EmissionOptions) GetIso14083EmissionFactorsVersion() Iso14083EmissionFactorsVersion`

GetIso14083EmissionFactorsVersion returns the Iso14083EmissionFactorsVersion field if non-nil, zero value otherwise.

### GetIso14083EmissionFactorsVersionOk

`func (o *EmissionOptions) GetIso14083EmissionFactorsVersionOk() (*Iso14083EmissionFactorsVersion, bool)`

GetIso14083EmissionFactorsVersionOk returns a tuple with the Iso14083EmissionFactorsVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIso14083EmissionFactorsVersion

`func (o *EmissionOptions) SetIso14083EmissionFactorsVersion(v Iso14083EmissionFactorsVersion)`

SetIso14083EmissionFactorsVersion sets Iso14083EmissionFactorsVersion field to given value.

### HasIso14083EmissionFactorsVersion

`func (o *EmissionOptions) HasIso14083EmissionFactorsVersion() bool`

HasIso14083EmissionFactorsVersion returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


