ARM templates: 
---
* Follows a structure.
  
Has 5 components:
--
* schema: Has URL and defines the ARM template structure & contentVersion: Defines template version(Mandatory)
* parameters: Has static data.
* variables: Has dynamic data that keeps on changing for deployment to deployment.
* resources: Actual resource that you create. It's an array. Has resource provider.
* outputs:

Mandatory files for ARM templates:
--
* .json file
* parameters.json: Same like variables.tf file in terraform.


Template Link: https://github.com/Azure/azure-quickstart-templates.git
--

How many ways you can create resources using ARM templates: Using "templates" resource in azure, powershell, AzureDevops.
--
