# PayslipResponse


## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The Affix-assigned id of the payslip | 
**remote_id** | **str** | the remote system-assigned id of the payrun | 
**employee_id** | **str** |  | 
**payrun_id** | **str** |  | 
**currency** | **str** |  | 
**gross_pay** | **float** | if USD/EUR/GBP, in cent | 
**net_pay** | **float** | if USD/EUR/GBP, in cent | 
**start_date** | **date** |  | 
**end_date** | **date** |  | 
**payment_date** | **date** |  | 
**earnings** | [**[PayslipResponseEarnings]**](PayslipResponseEarnings.md) |  | 
**contributions** | [**[PayslipResponseContributions], none_type**](PayslipResponseContributions.md) | Items paid by the employer that are not included in gross pay, such as employer-paid portion of private health insurance  | 
**deductions** | [**[PayslipResponseDeductions]**](PayslipResponseDeductions.md) |  | 
**taxes** | [**[PayslipResponseTaxes]**](PayslipResponseTaxes.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


