# TokenRequest


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_id** | **str** | The client ID you received when you first created the application | 
**client_secret** | **str** | The client secret. Since there can be multiple &#x60;client_secret&#x60;s (to allow for rotation of secrets without downtime to your customers), any current &#x60;client_secret&#x60; is valid  Please email me after signup and I will set both your client secret and redirect_uri (required) when you reach out.  | 
**code** | **str** | This is the code you received in the query string | 
**redirect_uri** | **str** | Indicates the URI to return the user to after authorization is complete, which is the endpoint on your server to receive the authorization_code.  Must be identical to the redirect URI provided in the original link.  Please email me after signup and I will set both your client secret and redirect_uri (required) when you reach out.  | 
**grant_type** | **str** | This is a hardcoded value required by the OAuth 2.1 spec | defaults to "authorization_code"

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


