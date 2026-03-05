# ErrorResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Description** | **string** | A human readable message that describes the error. | 
**ErrorCode** | **string** | A constant string that can be used to identify this error class programmatically.  If additional information is available for an errorCode, it will be provided as key-value pairs with the parameter **details**. The keys available for a specific errorCode are documented directly with the errorCode. Unless stated otherwise, the values are of type string.  As an example, the following errorCode provides one key-value pair in the **details**. The key is called **message**. * &#x60;GENERAL_UNAUTHENTICATED&#x60; - Invalid or missing authentication credentials.   * &#x60;message&#x60; - An additional error message.  Note that additional errorCodes as well as the **details** of existing errorCodes may be added at any time. Furthermore, the **description** may change at any time.  **HTTP status code: 400** * &#x60;GENERAL_VALIDATION_ERROR&#x60; - The validation of the request failed. Details can be found in **causes**. * &#x60;GENERAL_PARSING_ERROR&#x60; - The JSON syntax is invalid. * &#x60;ROUTING_ERROR&#x60; - The calculation failed. Details can be found in **causes**.  **HTTP status code: 401** * &#x60;GENERAL_UNAUTHENTICATED&#x60; - Invalid or missing authentication credentials.   * &#x60;message&#x60; - An additional error message.  **HTTP status code: 403** * &#x60;GENERAL_FORBIDDEN&#x60; - Insufficient access rights. * &#x60;GENERAL_QUOTA_EXCEEDED&#x60; - The transaction limit is exceeded.   * &#x60;message&#x60; - An additional error message. * &#x60;ROUTING_RESTRICTION_EXCEEDED&#x60; - A product-specific restriction is exceeded.  **HTTP status code: 404** * &#x60;GENERAL_RESOURCE_NOT_FOUND&#x60; - A requested resource does not exist.   * &#x60;message&#x60; - An additional error message.  **HTTP status code: 410** * &#x60;GENERAL_GONE&#x60; - A requested resource is not longer available.   * &#x60;message&#x60; - An additional error message.   * &#x60;hint&#x60; - A hint how to solve the problem.  **HTTP status code: 429** * &#x60;GENERAL_RATE_LIMIT_EXCEEDED&#x60; - The rate limit is exceeded.  **HTTP status code: 500** * &#x60;GENERAL_INTERNAL_SERVER_ERROR&#x60; - The request could not be processed due to an internal error.   * &#x60;message&#x60; - An additional error message.   * &#x60;hint&#x60; - A hint how to solve the problem.  **HTTP status code: 503** * &#x60;GENERAL_SERVICE_UNAVAILABLE&#x60; - The service is temporarily unavailable.  **HTTP status code: 4xx-5xx** * &#x60;GENERAL_INTERNAL_GATEWAY_ERROR&#x60; - The request could not be processed due to an internal gateway error.   * &#x60;hint&#x60; - A hint how to solve the problem. | 
**TraceId** | **string** | A unique identifier of the corresponding trace forest. It can be used to trace errors by the support. | 
**ErrorId** | Pointer to **string** | A unique identifier specific to this error instance. It can be used to trace errors by the support. | [optional] 
**Causes** | Pointer to [**[]CausingError**](CausingError.md) | A list of affected parameters and/or properties that caused this error. | [optional] 
**Details** | Pointer to **map[string]interface{}** | Additional properties specific to this error class. | [optional] 

## Methods

### NewErrorResponse

`func NewErrorResponse(description string, errorCode string, traceId string, ) *ErrorResponse`

NewErrorResponse instantiates a new ErrorResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewErrorResponseWithDefaults

`func NewErrorResponseWithDefaults() *ErrorResponse`

NewErrorResponseWithDefaults instantiates a new ErrorResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDescription

`func (o *ErrorResponse) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *ErrorResponse) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *ErrorResponse) SetDescription(v string)`

SetDescription sets Description field to given value.


### GetErrorCode

`func (o *ErrorResponse) GetErrorCode() string`

GetErrorCode returns the ErrorCode field if non-nil, zero value otherwise.

### GetErrorCodeOk

`func (o *ErrorResponse) GetErrorCodeOk() (*string, bool)`

GetErrorCodeOk returns a tuple with the ErrorCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetErrorCode

`func (o *ErrorResponse) SetErrorCode(v string)`

SetErrorCode sets ErrorCode field to given value.


### GetTraceId

`func (o *ErrorResponse) GetTraceId() string`

GetTraceId returns the TraceId field if non-nil, zero value otherwise.

### GetTraceIdOk

`func (o *ErrorResponse) GetTraceIdOk() (*string, bool)`

GetTraceIdOk returns a tuple with the TraceId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTraceId

`func (o *ErrorResponse) SetTraceId(v string)`

SetTraceId sets TraceId field to given value.


### GetErrorId

`func (o *ErrorResponse) GetErrorId() string`

GetErrorId returns the ErrorId field if non-nil, zero value otherwise.

### GetErrorIdOk

`func (o *ErrorResponse) GetErrorIdOk() (*string, bool)`

GetErrorIdOk returns a tuple with the ErrorId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetErrorId

`func (o *ErrorResponse) SetErrorId(v string)`

SetErrorId sets ErrorId field to given value.

### HasErrorId

`func (o *ErrorResponse) HasErrorId() bool`

HasErrorId returns a boolean if a field has been set.

### GetCauses

`func (o *ErrorResponse) GetCauses() []CausingError`

GetCauses returns the Causes field if non-nil, zero value otherwise.

### GetCausesOk

`func (o *ErrorResponse) GetCausesOk() (*[]CausingError, bool)`

GetCausesOk returns a tuple with the Causes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCauses

`func (o *ErrorResponse) SetCauses(v []CausingError)`

SetCauses sets Causes field to given value.

### HasCauses

`func (o *ErrorResponse) HasCauses() bool`

HasCauses returns a boolean if a field has been set.

### GetDetails

`func (o *ErrorResponse) GetDetails() map[string]interface{}`

GetDetails returns the Details field if non-nil, zero value otherwise.

### GetDetailsOk

`func (o *ErrorResponse) GetDetailsOk() (*map[string]interface{}, bool)`

GetDetailsOk returns a tuple with the Details field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDetails

`func (o *ErrorResponse) SetDetails(v map[string]interface{})`

SetDetails sets Details field to given value.

### HasDetails

`func (o *ErrorResponse) HasDetails() bool`

HasDetails returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


