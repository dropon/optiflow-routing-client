# CausingError

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Description** | **string** | A human readable message that describes the error. | 
**ErrorCode** | **string** | A constant string that can be used to identify this error class programmatically.  If additional information is available for an errorCode, it will be provided as key-value pairs with the parameter **details**. The keys available for a specific errorCode are documented directly with the errorCode. Unless stated otherwise, the values are of type string.  As an example, the following errorCode provides one key-value pair in the **details**. The key is called **value**. * &#x60;GENERAL_INVALID_VALUE&#x60; - A parameter is set to an invalid value.   * &#x60;value&#x60; - The invalid value.  Note that additional errorCodes as well as the **details** of existing errorCodes may be added at any time. Furthermore, the **description** may change at any time.  **Error codes for** &#x60;GENERAL_VALIDATION_ERROR&#x60;  * &#x60;GENERAL_UNRECOGNIZED_PARAMETER&#x60; - A parameter is unknown. * &#x60;GENERAL_MISSING_PARAMETER&#x60; - A required parameter is missing. * &#x60;GENERAL_TYPE_VIOLATED&#x60; - The value of a parameter has an invalid type.   * &#x60;type&#x60; - The type. * &#x60;GENERAL_FORMAT_VIOLATED&#x60; - The value of a parameter has an invalid format.   * &#x60;format&#x60; - The format. * &#x60;GENERAL_PATTERN_VIOLATED&#x60; - The value of a string parameter does not satisfy the required pattern.   * &#x60;pattern&#x60; - The pattern. * &#x60;GENERAL_MINIMUM_LENGTH_VIOLATED&#x60; - The minimum length of a string is violated.   * &#x60;minimumLength&#x60; - The minimum length (integer). * &#x60;GENERAL_MAXIMUM_LENGTH_VIOLATED&#x60; - The maximum length of a string is violated.   * &#x60;maximumLength&#x60; - The maximum length (integer). * &#x60;GENERAL_MINIMUM_ITEMS_VIOLATED&#x60; - The minimum number of items of an array is violated.   * &#x60;minimumItems&#x60; - The minimum number of items (integer). * &#x60;GENERAL_MAXIMUM_ITEMS_VIOLATED&#x60; - The maximum number of items of an array is violated.   * &#x60;maximumItems&#x60; - The maximum number of items (integer). * &#x60;GENERAL_MINIMUM_VALUE_VIOLATED&#x60; - The minimum value of a parameter is violated.   * &#x60;minimumValue&#x60; - The minimum value (integer or double). * &#x60;GENERAL_MAXIMUM_VALUE_VIOLATED&#x60; - The maximum value of a parameter is violated.   * &#x60;maximumValue&#x60; - The maximum value (integer or double). * &#x60;GENERAL_ENUM_VIOLATED&#x60; - The value of a parameter is not one of the specified enum values.   * &#x60;enum&#x60; - The allowed enum values. * &#x60;GENERAL_INVALID_VALUE&#x60; - A parameter is set to an invalid value.   * &#x60;value&#x60; - The invalid value. * &#x60;GENERAL_DUPLICATE_PARAMETER&#x60; - A parameter is duplicated. * &#x60;GENERAL_INVALID_LIST&#x60; - A list has an invalid format such as duplicate commas.   * &#x60;value&#x60; - The invalid list. * &#x60;GENERAL_INVALID_INTERVAL&#x60; - A time interval is invalid, i.e. start is greater than end. * &#x60;ROUTING_INVALID_WAYPOINT_ATTRIBUTE&#x60; - A waypoint attribute is set to an invalid value.   * &#x60;attribute&#x60; - The invalid waypoint attribute. * &#x60;ROUTING_UNRECOGNIZED_WAYPOINT_ATTRIBUTE&#x60; - A waypoint attribute is unknown.   * &#x60;attribute&#x60; - The invalid waypoint key. * &#x60;ROUTING_DUPLICATE_WAYPOINT_ATTRIBUTE&#x60; - A waypoint attribute is duplicated.   * &#x60;attribute&#x60; - The duplicated waypoint key. * &#x60;ROUTING_WAYPOINT_ATTRIBUTE_CONFLICT&#x60; - Two waypoint attributes are in conflict with each other.   * &#x60;attribute&#x60; - The first conflicting attribute.   * &#x60;conflictingAttribute&#x60; - The second conflicting attribute. * &#x60;ROUTING_INVALID_MANIPULATION_WAYPOINT_ORDER&#x60; - The manipulation waypoint is not valid for start or destination. * &#x60;ROUTING_INVALID_COMBINED_TRANSPORT_WAYPOINT_ORDER&#x60; - The combinedTransport waypoint is not valid for start or destination. * &#x60;ROUTING_INVALID_WAYPOINT_LIST_FOR_ALTERNATIVE_ROUTES&#x60; - Alternative routes are supported only for two on-road or off-road waypoints. * &#x60;ROUTING_INVALID_WAYPOINT&#x60; - A waypoint contains multiple types or none of them, but exactly one must be specified. * &#x60;ROUTING_MUST_HAVE_WAYPOINTS_OR_ROUTE_ID&#x60; - The request must have either at least two **waypoints** or a **routeId**. * &#x60;ROUTING_EMISSIONS_MUTUALLY_EXCLUSIVE&#x60; - All emissions _EN16258_2012_ results and _ISO14083_2022_ or _ISO14083_2023_ results are mutually exclusive.   * &#x60;attribute&#x60; - The first conflicting emissions standard.   * &#x60;conflictingAttributes&#x60; - The list of other conflicting emissions standards. * &#x60;ROUTING_START_AND_ARRIVAL_TIME_MUTUALLY_EXCLUSIVE&#x60; - **options[startTime]** and **options[arrivalTime]** are mutually exclusive. - _The **parameter** remains empty._ * &#x60;ROUTING_ESTIMATED_DISTANCE_TOO_LONG&#x60; - The distance of the route (estimated by air-line) for the selected vehicle is too long. - _The **parameter** remains empty._   * &#x60;distance&#x60; - The estimated distance (integer).   * &#x60;limit&#x60; - The maximum allowable distance (integer). * &#x60;ROUTING_PARAMETER_CONFLICT&#x60; - Two parameters are in conflict with each other.   * &#x60;conflictingParameter&#x60; - The conflicting parameter.   * &#x60;message&#x60; - The error message. * &#x60;ROUTING_NO_VALID_COUNTRY_ALLOWED&#x60; - The list of allowed countries does not contain any of the available countries so that the effective list of countries allowed for routing is empty.   * &#x60;allowedCountries&#x60; - The list of allowed countries. * &#x60;ROUTING_ALL_VALID_COUNTRIES_PROHIBITED&#x60; - The list of prohibited countries contains all available countries so that the effective list of countries allowed for routing is empty.   * &#x60;prohibitedCountries&#x60; - The list of prohibited countries. * &#x60;ROUTING_MAXIMUM_HORIZON_VALUE_VIOLATED&#x60; - The maximum value of horizon is violated.   * &#x60;limit&#x60; - The maximum allowable horizon (integer). * &#x60;ROUTING_MUST_HAVE_ONE_WAYPOINT_OR_ROUTE_ID&#x60; - The request must have either a **waypoint** or a **routeId**. * &#x60;ROUTING_HORIZONS_EQUAL_OR_NOT_ASCENDING&#x60; - The horizons have equal values or are not ascending.   * &#x60;value&#x60; - The invalid horizon. * &#x60;ROUTING_ROUTE_TOO_LONG_FOR_REACHABILITY&#x60; - The route is too long to be used with reachable areas or locations.   * &#x60;length&#x60; - The actual route length (integer).   * &#x60;limit&#x60; - The maximum allowable route length (integer). * &#x60;ROUTING_ALLOWED_AND_PROHIBITED_COUNTRIES_IN_CONFLICT_WITH_ROUTE_ID&#x60; - The lists of allowed and prohibited countries are in conflict with the **routeId** which passes an effectively prohibited country.   * &#x60;value&#x60; - The value in conflict. * &#x60;ROUTING_ROUTE_ID_NOT_FOUND&#x60; - The **routeId** cannot be found.   * &#x60;value&#x60; - The routeId. * &#x60;ROUTING_ROUTE_ID_CANNOT_BE_USED&#x60; - The **routeId** cannot be used for this operation as it was created by a service other than routing and lacks a routing context.   * &#x60;value&#x60; - The routeId. * &#x60;ROUTING_PROFILE_NOT_FOUND&#x60; - The requested **profile** could not be found.   * &#x60;value&#x60; - The profile name. * &#x60;ROUTING_UNSUPPORTED_CURRENCY&#x60; - The specified currency is not supported.   * &#x60;currency&#x60; - The unsupported currency. * &#x60;ROUTING_PARAMETER_ONLY_SUPPORTED_BY_POST&#x60; - The requested parameter is not supported by this GET operation, it is only supported by the corresponding POST operation.   * &#x60;value&#x60; - The invalid parameter value. * &#x60;ROUTING_PARAMETER_NOT_SUPPORTED_BY_GET_ROUTE_BY_ROUTE_ID&#x60; - The requested parameter is not supported by this **getRouteByRouteId** operation.   * &#x60;value&#x60; - The invalid parameter value. * &#x60;ROUTING_OPENING_INTERVALS_REQUIRE_TIME&#x60; - When using waypoints with opening intervals or a **routeId** containing such waypoints, a start time has to be specified when **options[trafficMode]** is _AVERAGE_. * &#x60;ROUTING_ARRIVAL_TIME_WITH_SCHEDULE&#x60; - **options[arrivalTime]** cannot be used with the **results** _SCHEDULE_REPORT_ and _SCHEDULE_EVENT_ nor when **openingIntervals**, **serviceTime** or **workingHoursPreset** are specified.   * &#x60;value&#x60; - The invalid parameter value. * &#x60;ROUTING_INVALID_NUMBER_OF_COORDINATES&#x60; - The polyline cannot be parsed because the number of coordinates is not even or less than 4.   * &#x60;value&#x60; - The invalid parameter value.   * &#x60;polylineIndex&#x60; - The index denoting the polyline in which the error was found (integer). * &#x60;ROUTING_INVALID_COORDINATE&#x60; - The provided coordinate is not in the valid range or cannot be parsed.   * &#x60;value&#x60; - The invalid parameter value.   * &#x60;polylineIndex&#x60; - The index denoting the polyline in which the error was found (integer).   * &#x60;coordinateIndex&#x60; - The index denoting the erroneous coordinate within the polyline (integer). * &#x60;ROUTING_FEATURE_NOT_SUPPORTED_WITH_MONETARY_COSTS&#x60; - The requested feature is not supported when **options[routingMode]** is _MONETARY_.   * &#x60;value&#x60; - The invalid parameter value. * &#x60;ROUTING_MUST_HAVE_MONETARY_COST_VALUE&#x60; - Both values **monetaryCostOptions[costPerKilometer]** and **monetaryCostOptions[workingCostPerHour]** are zero. Use a value greater zero for at least one of this **monetaryCostOptions** parameters. * &#x60;ROUTING_CUSTOM_ROAD_ATTRIBUTE_SCENARIO_NOT_FOUND&#x60; - At least one of the requested **options[customRoadAttributeScenarios]** could not be found.   * &#x60;scenarios&#x60; - The scenarios which could not be found (comma-separated list). * &#x60;ROUTING_CUSTOM_ROAD_ATTRIBUTE_SCENARIOS_TOO_LARGE&#x60; - The scenarios given in **options[customRoadAttributeScenarios]** are too large and can not all be considered at the same time. * &#x60;ROUTING_POSITION_AND_WAYPOINT_MUTUALLY_EXCLUSIVE&#x60; - **position** and **waypoint** are mutually exclusive. - _The **parameter** remains empty._ * &#x60;ROUTING_VEHICLE_POSITION_MISSING&#x60; - The position of the vehicle must be specified by either **position** or **waypoint**. - _The **parameter** remains empty._ * &#x60;ROUTING_UNSUPPORTED_WAYPOINT_TYPE_FOR_ETA_CALCULATION&#x60; - The ETA calculation does not support route-manipulation waypoints, combined-transport waypoints or vehicle parameters at waypoints.   * &#x60;waypointIndex&#x60; - The index of the waypoint (integer). * &#x60;ROUTING_MISSING_WAYPOINT_NAME&#x60; - The requested route for the **routeId** contains a waypoint which does not have a name.   * &#x60;waypointIndex&#x60; - The index of the waypoint (integer). * &#x60;ROUTING_DUPLICATE_WAYPOINT_NAME&#x60; - The requested route for the **routeId** contains waypoints with a duplicate name.   * &#x60;waypointIndexes&#x60; - The indexes of the waypoints with the duplicated name (comma-separated list).   * &#x60;name&#x60; - The duplicate waypoint name. * &#x60;ROUTING_WAYPOINT_NAME_NOT_FOUND&#x60; - The waypoint name could not be found in the requested route for the **routeId**.   * &#x60;name&#x60; - The invalid waypoint name. * &#x60;ROUTING_VEHICLE_POSITION_BEFORE_FIRST_WAYPOINT&#x60; - The position of the vehicle cannot be before the first waypoint. * &#x60;ROUTING_ROUTE_ID_REQUIRES_WORKLOGBOOK&#x60; - The route associated with the given **routeId** has been calculated with a **driver** and requires the **workLogbook** to be specified in the ETA request. * &#x60;ROUTING_ROUTE_ID_DOES_NOT_SUPPORT_WORKLOGBOOK&#x60; - The route associated with the given **routeId** has been calculated without a **driver** and does not support the **workLogbook** specified in the ETA request. * &#x60;ROUTING_CONFLICTING_LOW_EMISSION_ZONE_TYPES&#x60; - Some requested low-emission zone types are in conflict with each other, specify only one of them. * &#x60;ROUTING_SERVICE_CANNOT_BE_SCHEDULED&#x60; - The **serviceTime** at a waypoint cannot be scheduled as it exceeds the maximum time between breaks permitted by the selected **workingHoursPreset**. - _The **parameter** remains empty._  **Error codes for** &#x60;ROUTING_ERROR&#x60;  * &#x60;ROUTING_WAYPOINT_CANNOT_BE_MATCHED&#x60; - The waypoint cannot be matched to the nearest possible road. * &#x60;ROUTING_ROUTE_NOT_FOUND&#x60; - A route between at least two waypoints could not be found for the current configuration and profile. The **parameter** contains the waypoint where the problematic part that could not be routed starts, i.e., the problematic part of the route is between this waypoint and the next one. Note that only the first problematic part that was encountered is reported. * &#x60;ROUTING_TIMEOUT&#x60; - The route calculation has timed out. * &#x60;ROUTING_UTC_OFFSET_CANNOT_BE_DETERMINED&#x60; - The UTC offset of the start waypoint cannot be determined. * &#x60;ROUTING_BLOCK_INTERSECTING_ROADS_TOO_MANY_SEGMENTS&#x60; - The maximum number of road segments intersecting one polyline must not exceed 5000.  **Error codes for** &#x60;ROUTING_RESTRICTION_EXCEEDED&#x60;  * &#x60;ROUTING_TOO_MANY_WAYPOINTS&#x60; - The request contains too many waypoints.   * &#x60;limit&#x60;- The maximum allowed number of waypoints for a single request (integer).  **Error codes for** &#x60;GENERAL_RESOURCE_NOT_FOUND&#x60;  * &#x60;GENERAL_INVALID_ID&#x60; - No resource exists for the provided ID.   * &#x60;value&#x60; - The ID for which no resource exists. | 
**Parameter** | Pointer to **string** | The name of the affected query or path parameter or a JSONPath to the affected property of the request. | [optional] 
**Details** | Pointer to **map[string]interface{}** | Additional properties specific to this error class. | [optional] 

## Methods

### NewCausingError

`func NewCausingError(description string, errorCode string, ) *CausingError`

NewCausingError instantiates a new CausingError object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCausingErrorWithDefaults

`func NewCausingErrorWithDefaults() *CausingError`

NewCausingErrorWithDefaults instantiates a new CausingError object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDescription

`func (o *CausingError) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *CausingError) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *CausingError) SetDescription(v string)`

SetDescription sets Description field to given value.


### GetErrorCode

`func (o *CausingError) GetErrorCode() string`

GetErrorCode returns the ErrorCode field if non-nil, zero value otherwise.

### GetErrorCodeOk

`func (o *CausingError) GetErrorCodeOk() (*string, bool)`

GetErrorCodeOk returns a tuple with the ErrorCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetErrorCode

`func (o *CausingError) SetErrorCode(v string)`

SetErrorCode sets ErrorCode field to given value.


### GetParameter

`func (o *CausingError) GetParameter() string`

GetParameter returns the Parameter field if non-nil, zero value otherwise.

### GetParameterOk

`func (o *CausingError) GetParameterOk() (*string, bool)`

GetParameterOk returns a tuple with the Parameter field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParameter

`func (o *CausingError) SetParameter(v string)`

SetParameter sets Parameter field to given value.

### HasParameter

`func (o *CausingError) HasParameter() bool`

HasParameter returns a boolean if a field has been set.

### GetDetails

`func (o *CausingError) GetDetails() map[string]interface{}`

GetDetails returns the Details field if non-nil, zero value otherwise.

### GetDetailsOk

`func (o *CausingError) GetDetailsOk() (*map[string]interface{}, bool)`

GetDetailsOk returns a tuple with the Details field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDetails

`func (o *CausingError) SetDetails(v map[string]interface{})`

SetDetails sets Details field to given value.

### HasDetails

`func (o *CausingError) HasDetails() bool`

HasDetails returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


