# Vehicle

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EngineType** | Pointer to [**EngineType**](EngineType.md) |  | [optional] 
**FuelType** | Pointer to [**FuelType**](FuelType.md) |  | [optional] 
**ElectricityType** | Pointer to [**ElectricityType**](ElectricityType.md) |  | [optional] 
**AverageFuelConsumption** | Pointer to **float64** | The average fuel consumption of the vehicle. Depending on the **fuelType** [l/100km] for liquid fuel types or [kg/100km] for gaseous fuel types.  Supported for **engineType** _COMBUSTION_  or _HYBRID_. Relevant for &#x60;emissions&#x60;.  | [optional] 
**AverageElectricityConsumption** | Pointer to **float64** | The average electricity consumption of the vehicle [kWh/100km].  Supported for **engineType** _ELECTRIC_ or _HYBRID_. Relevant for &#x60;emissions&#x60;.  | [optional] 
**BioFuelRatio** | Pointer to **int32** | The ratio of biofuel to conventional fuel [%], i.e. 10 for E10 with 10% biofuel.  Supported for **engineType** _COMBUSTION_ or _HYBRID_ and only for the fuel types _GASOLINE_, _DIESEL_, _CNG_GASOLINE_ and _LNG_GASOLINE_. Relevant for &#x60;emissions&#x60;.  | [optional] 
**HybridRatio** | Pointer to **int32** | Electric energy usage ratio from the total amount of energy consumed by the vehicle.  Supported for **engineType** _HYBRID_. Relevant for &#x60;emissions&#x60;.  | [optional] 
**DualFuelRatio** | Pointer to **int32** | Ratio of CNG or LPG usage from the total amount of fuel consumption.  Supported for **engineType** _COMBUSTION_ with **fuelType**  _CNG_GASOLINE_ or _LPG_GASOLINE_. Relevant for &#x60;emissions&#x60;.  | [optional] 
**CylinderCapacity** | Pointer to **int32** | The cylinder capacity of the vehicle [cm&amp;#x00B3;]. This value is present for compatibility reasons and does not influence any of the results.  Supported for **engineType** _COMBUSTION_ or _HYBRID_.  | [optional] 
**EmissionStandard** | Pointer to [**EmissionStandard**](EmissionStandard.md) |  | [optional] 
**Co2EmissionClass** | Pointer to **int32** | The CO&amp;#8322; emission class valid in the European Union. See also the  [Directive 1999/62/EC](https://eur-lex.europa.eu/eli/dir/1999/62/2022-03-24) of the European Parliament and  of the Council on the charging of heavy goods vehicles for the use of certain infrastructures, Article 7ga.  Must be 1 for combustion and hybrid vehicles with any **emissionStandard**, 2-4 for combustion and hybrid vehicles with **emissionStandard** of at least _EURO_6_, and 5 for electric vehicles.   Relevant for &#x60;toll&#x60;.  | [optional] 
**LowEmissionZoneTypes** | Pointer to **string** | Comma-separated list of the low-emission zone types of the vehicle. This parameter is deprecated and superseded by **lowEmissionZoneApprovals**. When still being used, only low-emission zones in Germany are affected, zones in other countries which need an environmental badge or vehicle registration can be entered without restriction. It is not possible to specify both parameters.  Available values are provided by type &#x60;LowEmissionZoneTypes&#x60;:  \&quot;DE_GREEN\&quot; \&quot;DE_YELLOW\&quot; \&quot;DE_RED\&quot; \&quot;DE_NONE\&quot;  Relevant for &#x60;routing&#x60;.  | [optional] 
**LowEmissionZoneApprovals** | Pointer to **string** | Comma-separated list of approvals to enter low-emission zones. Usually, such approvals are environmental badges to be placed on the windscreen, but that can also be any other kind of approval or vehicle registration allowing it to enter a low-emission zone.  Low-emission zones which do not need any kind of approval but depend only on the **emissionStandard** are not affected by this parameter. Instead they can be entered if the **emissionStandard**  is sufficient. Electric vehicles can always enter these zones.  The default of the selected predefined profile allows entering all low-emission zones the vehicle can get an approval for. So, if you do not want to care about that and your  vehicle operates in a region where it has all necessary approvals, leave this parameter empty.  In order to consider low-emission zones depending on the actually available approvals, i.e. on  the environmental badges on the windscreen and other vehicle registrations, specify all of them here. The vehicle can then enter only those zones for which a proper approval is present. Low-emission zones in countries for which no value is specified cannot be entered.  Available values are provided by type &#x60;LowEmissionZoneApprovals&#x60;. \&quot;NONE\&quot; \&quot;AT_EURO_1\&quot; \&quot;AT_EURO_2\&quot; \&quot;AT_EURO_3\&quot; \&quot;AT_EURO_4\&quot; \&quot;AT_EURO_5\&quot; \&quot;AT_EURO_6\&quot; \&quot;DE_GREEN\&quot; \&quot;DE_YELLOW\&quot; \&quot;DE_RED\&quot; \&quot;DK_AUTHORIZED\&quot; \&quot;ES_CAT_B\&quot; \&quot;ES_CAT_C\&quot; \&quot;ES_CAT_ECO\&quot; \&quot;ES_CAT_ZERO\&quot; \&quot;FR_CRITAIR_0\&quot; \&quot;FR_CRITAIR_1\&quot; \&quot;FR_CRITAIR_2\&quot; \&quot;FR_CRITAIR_3\&quot; \&quot;FR_CRITAIR_4\&quot; \&quot;FR_CRITAIR_5\&quot;  Only one value per country can be specified. Relevant for &#x60;routing&#x60;. See [here](./concepts/low-emission-zones) for more information.  | [optional] 
**LowEmissionZoneExemptions** | Pointer to **string** | Comma-separated list of exemptions to enter low-emission zones.  Available values are provided by type &#x60;LowEmissionZoneExemptions&#x60;: \&quot;BE_LAGE_EMISSIEZONE_ANTWERPEN\&quot; \&quot;BE_LAGE_EMISSIEZONE_GENT\&quot; \&quot;BE_ZONE_BASSE_EMISSION_BRUXELLES\&quot; \&quot;DK_AALBORG_MILJOZONE\&quot; \&quot;DK_ARHUS_MILJOZONE\&quot; \&quot;DK_FREDERIKSBERG_MILJOZONE\&quot; \&quot;DK_KOBENHAVN_MILJOZONE\&quot; \&quot;DK_ODENSE_MILJOZONE\&quot; \&quot;ES_ZBEDEP_MADRID_PLAZA_ELIPTICA\&quot; \&quot;ES_ZBE_ALCOBENDAS\&quot; \&quot;ES_ZBE_ALMERIA\&quot; \&quot;ES_ZBE_BILBAO\&quot; \&quot;ES_ZBE_BOADILLA_DEL_MONTE\&quot; \&quot;ES_ZBE_CERDANYOLA_DEL_VALLES\&quot; \&quot;ES_ZBE_CHICLANA_DE_LA_FRONTERA\&quot; \&quot;ES_ZBE_CORDOBA\&quot; \&quot;ES_ZBE_CUENCA\&quot; \&quot;ES_ZBE_EL_PRAT_DE_LLOBREGAT\&quot; \&quot;ES_ZBE_ESTEPONA\&quot; \&quot;ES_ZBE_FUENLABRADA\&quot; \&quot;ES_ZBE_GETAFE\&quot; \&quot;ES_ZBE_GRANOLLERS\&quot; \&quot;ES_ZBE_LLEIDA\&quot; \&quot;ES_ZBE_MOLLET_DEL_VALLES\&quot; \&quot;ES_ZBE_MOSTOLES\&quot; \&quot;ES_ZBE_MOTRIL\&quot; \&quot;ES_ZBE_PALMA\&quot; \&quot;ES_ZBE_PARLA\&quot; \&quot;ES_ZBE_RIVAS_CEIP_COLEGIO_LUYFE\&quot; \&quot;ES_ZBE_RIVAS_CEIP_DULCE_CHACON\&quot; \&quot;ES_ZBE_RIVAS_CEIP_HANS_CHRISTIAN_ANDERSEN\&quot; \&quot;ES_ZBE_RIVAS_CEIP_JARAMA\&quot; \&quot;ES_ZBE_RIVAS_CEIP_JOSE_HIERRO\&quot; \&quot;ES_ZBE_RIVAS_CEIP_JOSE_ITURZAETA\&quot; \&quot;ES_ZBE_RIVAS_CEIP_LAS_CIGUENAS\&quot; \&quot;ES_ZBE_RIVAS_CEIP_VICTORIA_KENT\&quot; \&quot;ES_ZBE_RIVAS_COLEGIO_SANTA_MONICA\&quot; \&quot;ES_ZBE_SABADELL\&quot; \&quot;ES_ZBE_SAN_SEBASTIAN\&quot; \&quot;ES_ZBE_SEGOVIA\&quot; \&quot;ES_ZBE_TERRASSA\&quot; \&quot;ES_ZBE_TORREJON_DE_ARDOZ\&quot; \&quot;ES_ZBE_TORRELAVEGA\&quot; \&quot;ES_ZBE_TORREMOLINOS\&quot; \&quot;ES_ZBE_VALLADOLID\&quot; \&quot;FR_ANGERS_ZFE\&quot; \&quot;FR_STRASBOURG_ZFE\&quot; \&quot;GB_ABERDEEN_LEZ\&quot; \&quot;GB_BATH_CAZ\&quot; \&quot;GB_BIRMINGHAM_CAZ\&quot; \&quot;GB_BRADFORD_CAZ\&quot; \&quot;GB_BRISTOL_CAZ\&quot; \&quot;GB_DUNDEE_LEZ\&quot; \&quot;GB_EDINBURGH_LEZ\&quot; \&quot;GB_GLASGOW_LEZ\&quot; \&quot;GB_LONDON_ULTRA_LOW_EMISSION_ZONE\&quot; \&quot;GB_NEWCASTLE_CAZ\&quot; \&quot;GB_PORTSMOUTH_CAZ\&quot; \&quot;GB_SHEFFIELD_CAZ\&quot; \&quot;IT_MILANO_AREA_C\&quot; \&quot;IT_PALERMO_ZTL\&quot; \&quot;NL_AMSTERDAM_MILIEUZONE\&quot; \&quot;NL_AMSTERDAM_ZERO_EMISSIEZONE\&quot; \&quot;NL_ARNHEM_MILIEUZONE\&quot; \&quot;NL_ASSEN_ZERO_EMISSIEZONE\&quot; \&quot;NL_BREDA_MILIEUZONE\&quot; \&quot;NL_DELFT_HAAG_ZERO_EMISSIEZONE\&quot; \&quot;NL_DELFT_MILIEUZONE\&quot; \&quot;NL_DEN_HAAG_MILIEUZONE\&quot; \&quot;NL_DEN_HAAG_ZERO_EMISSIEZONE\&quot; \&quot;NL_EINDHOVEN_MILIEUZONE\&quot; \&quot;NL_EINDHOVEN_ZERO_EMISSIEZONE\&quot; \&quot;NL_GOUDA_ZERO_EMISSIEZONE\&quot; \&quot;NL_HAARLEM_MILIEUZONE\&quot; \&quot;NL_LEIDEN_MILIEUZONE\&quot; \&quot;NL_LEIDEN_ZERO_EMISSIEZONE\&quot; \&quot;NL_MAASTRICHT_MILIEUZONE\&quot; \&quot;NL_MAASTRICHT_ZERO_EMISSIEZONE\&quot; \&quot;NL_MAASVLAKTE_ROTTERDAM_MILIEUZONE\&quot; \&quot;NL_NIJMEGEN_ZERO_EMISSIEZONE\&quot; \&quot;NL_RIJSWIJK_MILIEUZONE\&quot; \&quot;NL_ROTTERDAM_MILIEUZONE\&quot; \&quot;NL_ROTTERDAM_ZERO_EMISSIEZONE\&quot; \&quot;NL_S_GRAVENDIJKWAL_MILIEUZONE\&quot; \&quot;NL_S_HERTOGENBOSCH_MILIEUZONE\&quot; \&quot;NL_TILBURG_MILIEUZONE\&quot; \&quot;NL_TILBURG_ZERO_EMISSIEZONE\&quot; \&quot;NL_UTRECHT_MILIEUZONE\&quot; \&quot;NL_UTRECHT_ZERO_EMISSIEZONE\&quot; \&quot;NL_ZWOLLE_ZERO_EMISSIEZONE\&quot;             Relevant for &#x60;routing&#x60;. See [here](./concepts/low-emission-zones) for more information.  | [optional] 
**ParticleReductionClass** | Pointer to [**ParticleReductionClass**](ParticleReductionClass.md) |  | [optional] 
**EmptyWeight** | Pointer to **int32** | The empty weight of the vehicle [kg].  Relevant for &#x60;routing&#x60;, &#x60;emissions&#x60;, &#x60;range calculation&#x60;.  | [optional] 
**LoadWeight** | Pointer to **int32** | The weight of the vehicle&#39;s load [kg].  Relevant for &#x60;routing&#x60;, &#x60;emissions&#x60;, &#x60;range calculation&#x60;.  | [optional] 
**TotalPermittedWeight** | Pointer to **int32** | The total permitted weight of the vehicle and its load [kg]. This is the weight the vehicle is usually registered with. If this value is not specified but **totalTechnicallyPermittedWeight** is specified then that value is used  for both **totalPermittedWeight** and **totalTechnicallyPermittedWeight**.  Relevant for &#x60;routing&#x60;, &#x60;toll&#x60;, &#x60;emissions&#x60;.  | [optional] 
**TotalTechnicallyPermittedWeight** | Pointer to **int32** | The total technically permitted weight of the vehicle and its load [kg].  Sometimes vehicles are registered with a smaller **totalPermittedWeight** than technically possible. For  such cases the possibly larger total technically permitted weight is specified here, it is relevant for  toll calculation in some European countries. If this value is not specified but **totalPermittedWeight** is specified then that value is used  for both **totalPermittedWeight** and **totalTechnicallyPermittedWeight**.  Relevant for &#x60;toll&#x60;.  | [optional] 
**AxleWeight** | Pointer to **int32** | The maximum distributed weight that may be supported by an axle of the vehicle [kg].  Relevant for &#x60;routing&#x60;, &#x60;toll&#x60;.  | [optional] 
**NumberOfAxles** | Pointer to **int32** | The total number of axles of the vehicle including the trailers.  Relevant for &#x60;toll&#x60;.  | [optional] 
**NumberOfTires** | Pointer to **int32** | The total number of tires of the vehicle including the trailers.  Relevant for &#x60;toll&#x60;.  | [optional] 
**Height** | Pointer to **int32** | The height of the vehicle [cm].  Relevant for &#x60;routing&#x60;, &#x60;toll&#x60;.  | [optional] 
**HeightAboveFrontAxle** | Pointer to **int32** | The height above the front axle [cm].  Relevant for &#x60;toll&#x60;.  | [optional] 
**Length** | Pointer to **int32** | The length of the vehicle [cm].  Relevant for &#x60;routing&#x60;, &#x60;toll&#x60;.  | [optional] 
**Width** | Pointer to **int32** | The width of the vehicle [cm].  Relevant for &#x60;routing&#x60;, &#x60;toll&#x60;.  | [optional] 
**HazardousMaterials** | Pointer to **string** | Comma-separated list of hazardous materials the vehicle has loaded. If none of the specific values applies, specify _OTHER_ to mark the vehicle carrying unspecific hazardous materials. If _NONE_ is specified along with other hazardous materials it is ignored. Depending on the load the route will avoid roads prohibited for and/or prefer roads prescribed for specific hazardous materials.  Available values are provided by type &#x60;HazardousMaterials&#x60;:  \&quot;HAZARDOUS_TO_WATER\&quot; \&quot;EXPLOSIVE\&quot; \&quot;FLAMMABLE\&quot; \&quot;RADIOACTIVE\&quot; \&quot;INHALATION_HAZARD\&quot; \&quot;MEDICAL_WASTE\&quot; \&quot;OTHER\&quot; \&quot;NONE\&quot;  Relevant for &#x60;routing&#x60;.  | [optional] 
**TunnelRestrictionCode** | Pointer to [**TunnelRestrictionCode**](TunnelRestrictionCode.md) |  | [optional] 
**TruckRoutes** | Pointer to **string** | Comma-separated list of truck routes the vehicle has to follow.  Available values are provided by type &#x60;TruckRoutes&#x60;:  * &#x60;DE_LKWUEBERLSTVAUSNV&#x60;  Preferred routes for long trucks in Germany, also known as Lang-LKW.  * &#x60;NL_LZV&#x60;  Preferred routes for long trucks in the Netherlands, also known as LZV (Langere en Zwaardere Vrachtautocombinatie).  * &#x60;NZ_HPMV&#x60;  The network for High Productivity Motor Vehicles (HPMV) carrying the maximum loads available under a permit (New Zealand Transport Agency).  * &#x60;SE_BK_1&#x60;  Public roads and bridges that support up to 64 t total permitted weight (Swedish Transport Administration).  * &#x60;SE_BK_2&#x60;  Public roads and bridges that support up to 51.4 t total permitted weight.  Actual limit depends on wheelbase and axle weight (Swedish Transport Administration).  * &#x60;SE_BK_3&#x60;  Public roads and bridges that support up to 37.5 t total permitted weight.  Actual limit depends on wheelbase and axle weight (Swedish Transport Administration).  * &#x60;SE_BK_4&#x60;  Public roads and bridges that support up to 74 t total permitted weight (draft summer 2018, Swedish Transport Administration).  * &#x60;US_STAA&#x60;  Routes that belong to the highway network as defined by the Surface Transportation Assistance Act in the US.  * &#x60;US_TD&#x60;  Part of a state-designated highway network for trucks in the US.  * &#x60;AU_B_DOUBLE&#x60;  B-Double routes as defined in Australia.  * &#x60;AU_B_DOUBLE_HML&#x60;  Routes for B-Double vehicle combinations operating at Higher Mass Limits (HML) (Australian Transport Administration).  * &#x60;AU_B_TRIPLE&#x60;  B-Triple routes as defined in Australia.  * &#x60;AU_B_TRIPLE_HML&#x60;  Routes for B-Triple vehicle combinations operating at Higher Mass Limits (HML) (Australian Transport Administration).  * &#x60;AU_AB_TRIPLE&#x60;  Routes for AB-Triple vehicle combinations operating (Australian Transport Administration).  * &#x60;AU_AB_TRIPLE_HML&#x60;  Routes for AB-Triple vehicle combinations operating at Higher Mass Limits (HML) (Australian Transport Administration).  * &#x60;GENERAL_TRUCK_ROUTES&#x60;  General routes designated for trucks, for example to prevent trucks routing through city centres when they are on transit.  * &#x60;NONE&#x60;  Overrides the profile settings to specify not to follow any truck routes.   If _NONE_ is specified along with other truck routes it is ignored.  This parameter will be ignored for non-truck profiles, e.g. _EUR_CAR_, _EUR_VAN_, _USA_1_PICKUP_ or _AUS_LCV_LIGHT_COMMERCIAL_ and for routing modes other than _FAST_. Relevant for &#x60;routing&#x60;.  | [optional] 
**Commercial** | Pointer to **bool** | Specifies if the vehicle usage is commercial.  Relevant for &#x60;toll&#x60;.  | [optional] 
**EtcSubscriptions** | Pointer to **string** | Comma-separated list of ETC Subscriptions. See [here](./concepts/electronic-toll-collection) for more information on available subscriptions.  Available values are provided by type &#x60;EtcSubscriptionTypes&#x60;:  \&quot;AT_GOBOX\&quot; \&quot;BE_TELETOL\&quot; \&quot;BE_VIAPASS\&quot; \&quot;CH_LSVA\&quot; \&quot;DE_QUICKBOX\&quot; \&quot;DE_TOLLCOLLECT\&quot; \&quot;DE_WARNOWTUNNEL_RFID\&quot; \&quot;DK_BROPAS_BUSINESS\&quot; \&quot;IT_TELEPASS\&quot; \&quot;NL_TELECARD\&quot; \&quot;NL_TTAG\&quot; \&quot;NO_AUTOPASS\&quot; \&quot;PT_VIA_VERDE\&quot; \&quot;US_APASS\&quot; \&quot;US_BREEZEBY\&quot; \&quot;US_DOWNBEACH_EXPRESSPASS\&quot; \&quot;US_EPASS\&quot; \&quot;US_EXPRESSACCOUNT\&quot; \&quot;US_EXPRESSCARD\&quot; \&quot;US_EXPRESSPASS\&quot; \&quot;US_EXPRESSTOLL\&quot; \&quot;US_EZPASS\&quot; \&quot;US_EZTAG\&quot; \&quot;US_FASTRAK\&quot; \&quot;US_GEAUXPASS\&quot; \&quot;US_GOODTOGO\&quot; \&quot;US_GOPASS\&quot; \&quot;US_IPASS\&quot; \&quot;US_KTAG\&quot; \&quot;US_LEEWAY\&quot; \&quot;US_MACKINACBRIDGE_MACPASS\&quot; \&quot;US_MARYLAND_EZPASS\&quot; \&quot;US_MASSACHUSETTS_EZPASS\&quot; \&quot;US_NC_QUICKPASS\&quot; \&quot;US_NEWHAMPSHIRE_EZPASS\&quot; \&quot;US_NEWJERSEY_EZPASS\&quot; \&quot;US_NEWYORK_EZPASS\&quot; \&quot;US_NEXPRESS\&quot; \&quot;US_OHIO_EZPASS\&quot; \&quot;US_PALPASS\&quot; \&quot;US_PIKEPASS\&quot; \&quot;US_RIVERLINK\&quot; \&quot;US_RIVERLINK_NOTRANSPONDER\&quot; \&quot;US_SEAWAYTRANSITCARD\&quot; \&quot;US_SUNPASS\&quot; \&quot;US_TOLLTAG\&quot; \&quot;US_TXTAG\&quot; \&quot;US_VIRGINIA_EZPASS\&quot; \&quot;US_WESTVIRGINIA_EZPASS\&quot; \&quot;US_PEACHPASS\&quot; \&quot;US_NEXUS\&quot; \&quot;US_DELAWARE_EZPASS\&quot; \&quot;US_GROSSEILETOLLBRIDGE_PASSTAG\&quot; \&quot;US_EZPASS_PAYBYPLATE\&quot;  Relevant for &#x60;toll&#x60;.  | [optional] 

## Methods

### NewVehicle

`func NewVehicle() *Vehicle`

NewVehicle instantiates a new Vehicle object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewVehicleWithDefaults

`func NewVehicleWithDefaults() *Vehicle`

NewVehicleWithDefaults instantiates a new Vehicle object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetEngineType

`func (o *Vehicle) GetEngineType() EngineType`

GetEngineType returns the EngineType field if non-nil, zero value otherwise.

### GetEngineTypeOk

`func (o *Vehicle) GetEngineTypeOk() (*EngineType, bool)`

GetEngineTypeOk returns a tuple with the EngineType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEngineType

`func (o *Vehicle) SetEngineType(v EngineType)`

SetEngineType sets EngineType field to given value.

### HasEngineType

`func (o *Vehicle) HasEngineType() bool`

HasEngineType returns a boolean if a field has been set.

### GetFuelType

`func (o *Vehicle) GetFuelType() FuelType`

GetFuelType returns the FuelType field if non-nil, zero value otherwise.

### GetFuelTypeOk

`func (o *Vehicle) GetFuelTypeOk() (*FuelType, bool)`

GetFuelTypeOk returns a tuple with the FuelType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFuelType

`func (o *Vehicle) SetFuelType(v FuelType)`

SetFuelType sets FuelType field to given value.

### HasFuelType

`func (o *Vehicle) HasFuelType() bool`

HasFuelType returns a boolean if a field has been set.

### GetElectricityType

`func (o *Vehicle) GetElectricityType() ElectricityType`

GetElectricityType returns the ElectricityType field if non-nil, zero value otherwise.

### GetElectricityTypeOk

`func (o *Vehicle) GetElectricityTypeOk() (*ElectricityType, bool)`

GetElectricityTypeOk returns a tuple with the ElectricityType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetElectricityType

`func (o *Vehicle) SetElectricityType(v ElectricityType)`

SetElectricityType sets ElectricityType field to given value.

### HasElectricityType

`func (o *Vehicle) HasElectricityType() bool`

HasElectricityType returns a boolean if a field has been set.

### GetAverageFuelConsumption

`func (o *Vehicle) GetAverageFuelConsumption() float64`

GetAverageFuelConsumption returns the AverageFuelConsumption field if non-nil, zero value otherwise.

### GetAverageFuelConsumptionOk

`func (o *Vehicle) GetAverageFuelConsumptionOk() (*float64, bool)`

GetAverageFuelConsumptionOk returns a tuple with the AverageFuelConsumption field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAverageFuelConsumption

`func (o *Vehicle) SetAverageFuelConsumption(v float64)`

SetAverageFuelConsumption sets AverageFuelConsumption field to given value.

### HasAverageFuelConsumption

`func (o *Vehicle) HasAverageFuelConsumption() bool`

HasAverageFuelConsumption returns a boolean if a field has been set.

### GetAverageElectricityConsumption

`func (o *Vehicle) GetAverageElectricityConsumption() float64`

GetAverageElectricityConsumption returns the AverageElectricityConsumption field if non-nil, zero value otherwise.

### GetAverageElectricityConsumptionOk

`func (o *Vehicle) GetAverageElectricityConsumptionOk() (*float64, bool)`

GetAverageElectricityConsumptionOk returns a tuple with the AverageElectricityConsumption field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAverageElectricityConsumption

`func (o *Vehicle) SetAverageElectricityConsumption(v float64)`

SetAverageElectricityConsumption sets AverageElectricityConsumption field to given value.

### HasAverageElectricityConsumption

`func (o *Vehicle) HasAverageElectricityConsumption() bool`

HasAverageElectricityConsumption returns a boolean if a field has been set.

### GetBioFuelRatio

`func (o *Vehicle) GetBioFuelRatio() int32`

GetBioFuelRatio returns the BioFuelRatio field if non-nil, zero value otherwise.

### GetBioFuelRatioOk

`func (o *Vehicle) GetBioFuelRatioOk() (*int32, bool)`

GetBioFuelRatioOk returns a tuple with the BioFuelRatio field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBioFuelRatio

`func (o *Vehicle) SetBioFuelRatio(v int32)`

SetBioFuelRatio sets BioFuelRatio field to given value.

### HasBioFuelRatio

`func (o *Vehicle) HasBioFuelRatio() bool`

HasBioFuelRatio returns a boolean if a field has been set.

### GetHybridRatio

`func (o *Vehicle) GetHybridRatio() int32`

GetHybridRatio returns the HybridRatio field if non-nil, zero value otherwise.

### GetHybridRatioOk

`func (o *Vehicle) GetHybridRatioOk() (*int32, bool)`

GetHybridRatioOk returns a tuple with the HybridRatio field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHybridRatio

`func (o *Vehicle) SetHybridRatio(v int32)`

SetHybridRatio sets HybridRatio field to given value.

### HasHybridRatio

`func (o *Vehicle) HasHybridRatio() bool`

HasHybridRatio returns a boolean if a field has been set.

### GetDualFuelRatio

`func (o *Vehicle) GetDualFuelRatio() int32`

GetDualFuelRatio returns the DualFuelRatio field if non-nil, zero value otherwise.

### GetDualFuelRatioOk

`func (o *Vehicle) GetDualFuelRatioOk() (*int32, bool)`

GetDualFuelRatioOk returns a tuple with the DualFuelRatio field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDualFuelRatio

`func (o *Vehicle) SetDualFuelRatio(v int32)`

SetDualFuelRatio sets DualFuelRatio field to given value.

### HasDualFuelRatio

`func (o *Vehicle) HasDualFuelRatio() bool`

HasDualFuelRatio returns a boolean if a field has been set.

### GetCylinderCapacity

`func (o *Vehicle) GetCylinderCapacity() int32`

GetCylinderCapacity returns the CylinderCapacity field if non-nil, zero value otherwise.

### GetCylinderCapacityOk

`func (o *Vehicle) GetCylinderCapacityOk() (*int32, bool)`

GetCylinderCapacityOk returns a tuple with the CylinderCapacity field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCylinderCapacity

`func (o *Vehicle) SetCylinderCapacity(v int32)`

SetCylinderCapacity sets CylinderCapacity field to given value.

### HasCylinderCapacity

`func (o *Vehicle) HasCylinderCapacity() bool`

HasCylinderCapacity returns a boolean if a field has been set.

### GetEmissionStandard

`func (o *Vehicle) GetEmissionStandard() EmissionStandard`

GetEmissionStandard returns the EmissionStandard field if non-nil, zero value otherwise.

### GetEmissionStandardOk

`func (o *Vehicle) GetEmissionStandardOk() (*EmissionStandard, bool)`

GetEmissionStandardOk returns a tuple with the EmissionStandard field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEmissionStandard

`func (o *Vehicle) SetEmissionStandard(v EmissionStandard)`

SetEmissionStandard sets EmissionStandard field to given value.

### HasEmissionStandard

`func (o *Vehicle) HasEmissionStandard() bool`

HasEmissionStandard returns a boolean if a field has been set.

### GetCo2EmissionClass

`func (o *Vehicle) GetCo2EmissionClass() int32`

GetCo2EmissionClass returns the Co2EmissionClass field if non-nil, zero value otherwise.

### GetCo2EmissionClassOk

`func (o *Vehicle) GetCo2EmissionClassOk() (*int32, bool)`

GetCo2EmissionClassOk returns a tuple with the Co2EmissionClass field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCo2EmissionClass

`func (o *Vehicle) SetCo2EmissionClass(v int32)`

SetCo2EmissionClass sets Co2EmissionClass field to given value.

### HasCo2EmissionClass

`func (o *Vehicle) HasCo2EmissionClass() bool`

HasCo2EmissionClass returns a boolean if a field has been set.

### GetLowEmissionZoneTypes

`func (o *Vehicle) GetLowEmissionZoneTypes() string`

GetLowEmissionZoneTypes returns the LowEmissionZoneTypes field if non-nil, zero value otherwise.

### GetLowEmissionZoneTypesOk

`func (o *Vehicle) GetLowEmissionZoneTypesOk() (*string, bool)`

GetLowEmissionZoneTypesOk returns a tuple with the LowEmissionZoneTypes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLowEmissionZoneTypes

`func (o *Vehicle) SetLowEmissionZoneTypes(v string)`

SetLowEmissionZoneTypes sets LowEmissionZoneTypes field to given value.

### HasLowEmissionZoneTypes

`func (o *Vehicle) HasLowEmissionZoneTypes() bool`

HasLowEmissionZoneTypes returns a boolean if a field has been set.

### GetLowEmissionZoneApprovals

`func (o *Vehicle) GetLowEmissionZoneApprovals() string`

GetLowEmissionZoneApprovals returns the LowEmissionZoneApprovals field if non-nil, zero value otherwise.

### GetLowEmissionZoneApprovalsOk

`func (o *Vehicle) GetLowEmissionZoneApprovalsOk() (*string, bool)`

GetLowEmissionZoneApprovalsOk returns a tuple with the LowEmissionZoneApprovals field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLowEmissionZoneApprovals

`func (o *Vehicle) SetLowEmissionZoneApprovals(v string)`

SetLowEmissionZoneApprovals sets LowEmissionZoneApprovals field to given value.

### HasLowEmissionZoneApprovals

`func (o *Vehicle) HasLowEmissionZoneApprovals() bool`

HasLowEmissionZoneApprovals returns a boolean if a field has been set.

### GetLowEmissionZoneExemptions

`func (o *Vehicle) GetLowEmissionZoneExemptions() string`

GetLowEmissionZoneExemptions returns the LowEmissionZoneExemptions field if non-nil, zero value otherwise.

### GetLowEmissionZoneExemptionsOk

`func (o *Vehicle) GetLowEmissionZoneExemptionsOk() (*string, bool)`

GetLowEmissionZoneExemptionsOk returns a tuple with the LowEmissionZoneExemptions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLowEmissionZoneExemptions

`func (o *Vehicle) SetLowEmissionZoneExemptions(v string)`

SetLowEmissionZoneExemptions sets LowEmissionZoneExemptions field to given value.

### HasLowEmissionZoneExemptions

`func (o *Vehicle) HasLowEmissionZoneExemptions() bool`

HasLowEmissionZoneExemptions returns a boolean if a field has been set.

### GetParticleReductionClass

`func (o *Vehicle) GetParticleReductionClass() ParticleReductionClass`

GetParticleReductionClass returns the ParticleReductionClass field if non-nil, zero value otherwise.

### GetParticleReductionClassOk

`func (o *Vehicle) GetParticleReductionClassOk() (*ParticleReductionClass, bool)`

GetParticleReductionClassOk returns a tuple with the ParticleReductionClass field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParticleReductionClass

`func (o *Vehicle) SetParticleReductionClass(v ParticleReductionClass)`

SetParticleReductionClass sets ParticleReductionClass field to given value.

### HasParticleReductionClass

`func (o *Vehicle) HasParticleReductionClass() bool`

HasParticleReductionClass returns a boolean if a field has been set.

### GetEmptyWeight

`func (o *Vehicle) GetEmptyWeight() int32`

GetEmptyWeight returns the EmptyWeight field if non-nil, zero value otherwise.

### GetEmptyWeightOk

`func (o *Vehicle) GetEmptyWeightOk() (*int32, bool)`

GetEmptyWeightOk returns a tuple with the EmptyWeight field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEmptyWeight

`func (o *Vehicle) SetEmptyWeight(v int32)`

SetEmptyWeight sets EmptyWeight field to given value.

### HasEmptyWeight

`func (o *Vehicle) HasEmptyWeight() bool`

HasEmptyWeight returns a boolean if a field has been set.

### GetLoadWeight

`func (o *Vehicle) GetLoadWeight() int32`

GetLoadWeight returns the LoadWeight field if non-nil, zero value otherwise.

### GetLoadWeightOk

`func (o *Vehicle) GetLoadWeightOk() (*int32, bool)`

GetLoadWeightOk returns a tuple with the LoadWeight field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLoadWeight

`func (o *Vehicle) SetLoadWeight(v int32)`

SetLoadWeight sets LoadWeight field to given value.

### HasLoadWeight

`func (o *Vehicle) HasLoadWeight() bool`

HasLoadWeight returns a boolean if a field has been set.

### GetTotalPermittedWeight

`func (o *Vehicle) GetTotalPermittedWeight() int32`

GetTotalPermittedWeight returns the TotalPermittedWeight field if non-nil, zero value otherwise.

### GetTotalPermittedWeightOk

`func (o *Vehicle) GetTotalPermittedWeightOk() (*int32, bool)`

GetTotalPermittedWeightOk returns a tuple with the TotalPermittedWeight field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTotalPermittedWeight

`func (o *Vehicle) SetTotalPermittedWeight(v int32)`

SetTotalPermittedWeight sets TotalPermittedWeight field to given value.

### HasTotalPermittedWeight

`func (o *Vehicle) HasTotalPermittedWeight() bool`

HasTotalPermittedWeight returns a boolean if a field has been set.

### GetTotalTechnicallyPermittedWeight

`func (o *Vehicle) GetTotalTechnicallyPermittedWeight() int32`

GetTotalTechnicallyPermittedWeight returns the TotalTechnicallyPermittedWeight field if non-nil, zero value otherwise.

### GetTotalTechnicallyPermittedWeightOk

`func (o *Vehicle) GetTotalTechnicallyPermittedWeightOk() (*int32, bool)`

GetTotalTechnicallyPermittedWeightOk returns a tuple with the TotalTechnicallyPermittedWeight field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTotalTechnicallyPermittedWeight

`func (o *Vehicle) SetTotalTechnicallyPermittedWeight(v int32)`

SetTotalTechnicallyPermittedWeight sets TotalTechnicallyPermittedWeight field to given value.

### HasTotalTechnicallyPermittedWeight

`func (o *Vehicle) HasTotalTechnicallyPermittedWeight() bool`

HasTotalTechnicallyPermittedWeight returns a boolean if a field has been set.

### GetAxleWeight

`func (o *Vehicle) GetAxleWeight() int32`

GetAxleWeight returns the AxleWeight field if non-nil, zero value otherwise.

### GetAxleWeightOk

`func (o *Vehicle) GetAxleWeightOk() (*int32, bool)`

GetAxleWeightOk returns a tuple with the AxleWeight field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAxleWeight

`func (o *Vehicle) SetAxleWeight(v int32)`

SetAxleWeight sets AxleWeight field to given value.

### HasAxleWeight

`func (o *Vehicle) HasAxleWeight() bool`

HasAxleWeight returns a boolean if a field has been set.

### GetNumberOfAxles

`func (o *Vehicle) GetNumberOfAxles() int32`

GetNumberOfAxles returns the NumberOfAxles field if non-nil, zero value otherwise.

### GetNumberOfAxlesOk

`func (o *Vehicle) GetNumberOfAxlesOk() (*int32, bool)`

GetNumberOfAxlesOk returns a tuple with the NumberOfAxles field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNumberOfAxles

`func (o *Vehicle) SetNumberOfAxles(v int32)`

SetNumberOfAxles sets NumberOfAxles field to given value.

### HasNumberOfAxles

`func (o *Vehicle) HasNumberOfAxles() bool`

HasNumberOfAxles returns a boolean if a field has been set.

### GetNumberOfTires

`func (o *Vehicle) GetNumberOfTires() int32`

GetNumberOfTires returns the NumberOfTires field if non-nil, zero value otherwise.

### GetNumberOfTiresOk

`func (o *Vehicle) GetNumberOfTiresOk() (*int32, bool)`

GetNumberOfTiresOk returns a tuple with the NumberOfTires field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNumberOfTires

`func (o *Vehicle) SetNumberOfTires(v int32)`

SetNumberOfTires sets NumberOfTires field to given value.

### HasNumberOfTires

`func (o *Vehicle) HasNumberOfTires() bool`

HasNumberOfTires returns a boolean if a field has been set.

### GetHeight

`func (o *Vehicle) GetHeight() int32`

GetHeight returns the Height field if non-nil, zero value otherwise.

### GetHeightOk

`func (o *Vehicle) GetHeightOk() (*int32, bool)`

GetHeightOk returns a tuple with the Height field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHeight

`func (o *Vehicle) SetHeight(v int32)`

SetHeight sets Height field to given value.

### HasHeight

`func (o *Vehicle) HasHeight() bool`

HasHeight returns a boolean if a field has been set.

### GetHeightAboveFrontAxle

`func (o *Vehicle) GetHeightAboveFrontAxle() int32`

GetHeightAboveFrontAxle returns the HeightAboveFrontAxle field if non-nil, zero value otherwise.

### GetHeightAboveFrontAxleOk

`func (o *Vehicle) GetHeightAboveFrontAxleOk() (*int32, bool)`

GetHeightAboveFrontAxleOk returns a tuple with the HeightAboveFrontAxle field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHeightAboveFrontAxle

`func (o *Vehicle) SetHeightAboveFrontAxle(v int32)`

SetHeightAboveFrontAxle sets HeightAboveFrontAxle field to given value.

### HasHeightAboveFrontAxle

`func (o *Vehicle) HasHeightAboveFrontAxle() bool`

HasHeightAboveFrontAxle returns a boolean if a field has been set.

### GetLength

`func (o *Vehicle) GetLength() int32`

GetLength returns the Length field if non-nil, zero value otherwise.

### GetLengthOk

`func (o *Vehicle) GetLengthOk() (*int32, bool)`

GetLengthOk returns a tuple with the Length field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLength

`func (o *Vehicle) SetLength(v int32)`

SetLength sets Length field to given value.

### HasLength

`func (o *Vehicle) HasLength() bool`

HasLength returns a boolean if a field has been set.

### GetWidth

`func (o *Vehicle) GetWidth() int32`

GetWidth returns the Width field if non-nil, zero value otherwise.

### GetWidthOk

`func (o *Vehicle) GetWidthOk() (*int32, bool)`

GetWidthOk returns a tuple with the Width field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetWidth

`func (o *Vehicle) SetWidth(v int32)`

SetWidth sets Width field to given value.

### HasWidth

`func (o *Vehicle) HasWidth() bool`

HasWidth returns a boolean if a field has been set.

### GetHazardousMaterials

`func (o *Vehicle) GetHazardousMaterials() string`

GetHazardousMaterials returns the HazardousMaterials field if non-nil, zero value otherwise.

### GetHazardousMaterialsOk

`func (o *Vehicle) GetHazardousMaterialsOk() (*string, bool)`

GetHazardousMaterialsOk returns a tuple with the HazardousMaterials field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHazardousMaterials

`func (o *Vehicle) SetHazardousMaterials(v string)`

SetHazardousMaterials sets HazardousMaterials field to given value.

### HasHazardousMaterials

`func (o *Vehicle) HasHazardousMaterials() bool`

HasHazardousMaterials returns a boolean if a field has been set.

### GetTunnelRestrictionCode

`func (o *Vehicle) GetTunnelRestrictionCode() TunnelRestrictionCode`

GetTunnelRestrictionCode returns the TunnelRestrictionCode field if non-nil, zero value otherwise.

### GetTunnelRestrictionCodeOk

`func (o *Vehicle) GetTunnelRestrictionCodeOk() (*TunnelRestrictionCode, bool)`

GetTunnelRestrictionCodeOk returns a tuple with the TunnelRestrictionCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTunnelRestrictionCode

`func (o *Vehicle) SetTunnelRestrictionCode(v TunnelRestrictionCode)`

SetTunnelRestrictionCode sets TunnelRestrictionCode field to given value.

### HasTunnelRestrictionCode

`func (o *Vehicle) HasTunnelRestrictionCode() bool`

HasTunnelRestrictionCode returns a boolean if a field has been set.

### GetTruckRoutes

`func (o *Vehicle) GetTruckRoutes() string`

GetTruckRoutes returns the TruckRoutes field if non-nil, zero value otherwise.

### GetTruckRoutesOk

`func (o *Vehicle) GetTruckRoutesOk() (*string, bool)`

GetTruckRoutesOk returns a tuple with the TruckRoutes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTruckRoutes

`func (o *Vehicle) SetTruckRoutes(v string)`

SetTruckRoutes sets TruckRoutes field to given value.

### HasTruckRoutes

`func (o *Vehicle) HasTruckRoutes() bool`

HasTruckRoutes returns a boolean if a field has been set.

### GetCommercial

`func (o *Vehicle) GetCommercial() bool`

GetCommercial returns the Commercial field if non-nil, zero value otherwise.

### GetCommercialOk

`func (o *Vehicle) GetCommercialOk() (*bool, bool)`

GetCommercialOk returns a tuple with the Commercial field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCommercial

`func (o *Vehicle) SetCommercial(v bool)`

SetCommercial sets Commercial field to given value.

### HasCommercial

`func (o *Vehicle) HasCommercial() bool`

HasCommercial returns a boolean if a field has been set.

### GetEtcSubscriptions

`func (o *Vehicle) GetEtcSubscriptions() string`

GetEtcSubscriptions returns the EtcSubscriptions field if non-nil, zero value otherwise.

### GetEtcSubscriptionsOk

`func (o *Vehicle) GetEtcSubscriptionsOk() (*string, bool)`

GetEtcSubscriptionsOk returns a tuple with the EtcSubscriptions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEtcSubscriptions

`func (o *Vehicle) SetEtcSubscriptions(v string)`

SetEtcSubscriptions sets EtcSubscriptions field to given value.

### HasEtcSubscriptions

`func (o *Vehicle) HasEtcSubscriptions() bool`

HasEtcSubscriptions returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


