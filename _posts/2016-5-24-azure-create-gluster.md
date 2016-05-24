---
layout: post
title: Bin ich online ?
---

```
$ azure login
info:    Executing command login
|info:    To sign in, use a web browser to open the page https://aka.ms/devicelogin. Enter the code CG4GDNGNW to authenticate.
-info:    Added subscription Nutzungsbasierte Bezahlung
+
info:    login command OK
$ azure config mode arm
info:    Executing command config mode
info:    New mode is arm
info:    config mode command OK
$ azure group create -n osev3-group -l westeurope
info:    Executing command group create
+ Getting resource group osev3-group                                           
+ Creating resource group osev3-group                                          
info:    Created resource group osev3-group
data:    Id:                  /subscriptions/4bdffgg-0f6c-4827-a8de-a989767868659c/resourceGroups/osev3-group
data:    Name:                osev3-group
data:    Location:            westeurope
data:    Provisioning State:  Succeeded
data:    Tags: null
data:    
info:    group create command OK
$ azure group template validate -f azure
azuredeploy.json             azuredeploy.parameters.json  azuregfs.sh                  
$ azure group template validate -f azure
azuredeploy.json             azuredeploy.parameters.json  azuregfs.sh                  
$ azure group template validate -f azuredeploy.json -p azuredeploy.parameters.json -g osev3-group
info:    Executing command group template validate
error:   Unexpected token a
info:    Error information has been recorded to /home/robert/.azure/azure.err
error:   group template validate command failed

$ azure group template validate -f azuredeploy.json -e azuredeploy.parameters.json -g osev3-group
info:    Executing command group template validate
+ Initializing template configurations and parameters                          
+ Validating the template                                                      
info:    group template validate command OK
$ azure group deployment create --debug-setting All -f azuredeploy.json -e azuredeploy.parameters.json -g osev3-group -n osev3-storage
info:    Executing command group deployment create
+ Initializing template configurations and parameters                          
+ Creating a deployment                                                        
info:    Created template deployment "osev3-storage"
+ Waiting for deployment to complete                                           
error:   Deployment provisioning state was not successful
error:   uniqueStorageAccount1 is not a valid storage account name. Storage account name must be between 3 and 24 characters in length and use numbers and lower-case letters only.
error:   uniqueStorageAccount0 is not a valid storage account name. Storage account name must be between 3 and 24 characters in length and use numbers and lower-case letters only.
data:    DeploymentName     : osev3-storage
data:    ResourceGroupName  : osev3-group
data:    ProvisioningState  : Failed
data:    Timestamp          :
data:    Mode               : Incremental
data:    CorrelationId      : 5916619e-933f-41bd-8eb6-10854cb0de2b
data:    DeploymentParameters :
data:    Name                          Type          Value                                                                                                    
data:    ----------------------------  ------------  ---------------------------------------------------------------------------------------------------------
data:    hostOs                        String        Centos                                                                                                   
data:    storageAccountName            String        uniqueStorageAccount                                                                                     
data:    scaleNumber                   Int           2                                                                                                        
data:    virtualNetworkName            String        testVnet                                                                                                 
data:    adminUsername                 String        username                                                                                                 
data:    adminPassword                 SecureString  undefined                                                                                                
data:    vmSize                        String        Standard_A1                                                                                              
data:    vmNamePrefix                  String        testVM                                                                                                   
data:    vmIPPrefix                    String        10.0.0.1                                                                                                 
data:    vnetAddressPrefix             String        10.0.0.0/16                                                                                              
data:    gfsSubnetName                 String        Subnet-1                                                                                                 
data:    gfsSubnetPrefix               String        10.0.0.0/24                                                                                              
data:    customScriptFilePath          String        https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/gluster-file-system/azuregfs.sh
data:    customScriptCommandToExecute  String        bash azuregfs.sh                                                                                         
data:    volumeName                    String        gfsvol                                                                                                   
data:    DebugSetting       : RequestContent, ResponseContent
info:    group deployment create command OK
``` 


