# Currencies

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **string** | The date of the exchange rates formatted according to [RFC 3339](https://tools.ietf.org/html/rfc3339). The rate may be older if there is no newer rate available. | 
**Provider** | **string** | The provider of the exchange rates. | 
**BaseCurrency** | **string** | The [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) currency code as provided in the request. | 
**ExchangeRates** | [**[]ExchangeRate**](ExchangeRate.md) | The exchange rates that were used to determine the converted prices. | 

## Methods

### NewCurrencies

`func NewCurrencies(date string, provider string, baseCurrency string, exchangeRates []ExchangeRate, ) *Currencies`

NewCurrencies instantiates a new Currencies object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCurrenciesWithDefaults

`func NewCurrenciesWithDefaults() *Currencies`

NewCurrenciesWithDefaults instantiates a new Currencies object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDate

`func (o *Currencies) GetDate() string`

GetDate returns the Date field if non-nil, zero value otherwise.

### GetDateOk

`func (o *Currencies) GetDateOk() (*string, bool)`

GetDateOk returns a tuple with the Date field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDate

`func (o *Currencies) SetDate(v string)`

SetDate sets Date field to given value.


### GetProvider

`func (o *Currencies) GetProvider() string`

GetProvider returns the Provider field if non-nil, zero value otherwise.

### GetProviderOk

`func (o *Currencies) GetProviderOk() (*string, bool)`

GetProviderOk returns a tuple with the Provider field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProvider

`func (o *Currencies) SetProvider(v string)`

SetProvider sets Provider field to given value.


### GetBaseCurrency

`func (o *Currencies) GetBaseCurrency() string`

GetBaseCurrency returns the BaseCurrency field if non-nil, zero value otherwise.

### GetBaseCurrencyOk

`func (o *Currencies) GetBaseCurrencyOk() (*string, bool)`

GetBaseCurrencyOk returns a tuple with the BaseCurrency field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBaseCurrency

`func (o *Currencies) SetBaseCurrency(v string)`

SetBaseCurrency sets BaseCurrency field to given value.


### GetExchangeRates

`func (o *Currencies) GetExchangeRates() []ExchangeRate`

GetExchangeRates returns the ExchangeRates field if non-nil, zero value otherwise.

### GetExchangeRatesOk

`func (o *Currencies) GetExchangeRatesOk() (*[]ExchangeRate, bool)`

GetExchangeRatesOk returns a tuple with the ExchangeRates field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExchangeRates

`func (o *Currencies) SetExchangeRates(v []ExchangeRate)`

SetExchangeRates sets ExchangeRates field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


