# ClientRequest


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_secret** | **[str]** | The client secret(s). It is an array datatype to allow for rotation of secrets without downtime for your customers  | 
**redirect_uris** | **[str]** | Indicates the URI to return the user to after authorization is complete, which is the endpoint on your server to receive the authorization_code.  Must be identical to the redirect URI provided in the original link.  Please email me after signup and I will set both your client secret and redirect_uri (required) when you reach out.  | 
**name** | **str** | Name of your app that shows up in the Affix Connect application  | 
**webhook_uri** | **str, none_type** | If enabled, webhooks will be sent to this endpoint  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


