# TokenResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_token** | **str** | The issued access_token | [readonly] 
**mode** | [**ModeResponse**](ModeResponse.md) |  | 
**provider** | [**ProviderResponse**](ProviderResponse.md) |  | 
**scopes** | [**[ScopesResponse]**](ScopesResponse.md) | One or more scope values indicating which parts of the user&#39;s account you wish to access.  Note, slight deviation from the OAuth 2.1 spec in that the param is scopes (plural) is used vs scope (singular)  | [readonly] 
**token_type** | **str** | The token type to pass in the &#x60;Authorization&#x60; header | [readonly] defaults to "Bearer"

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


