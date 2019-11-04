# Lab0 - Setup

Make sure you have set the following environment variables, as defined in the setup of the workshop:

	```console
	$ IBM_RG=<your-workshop-id> IBM_USERID=<your-ibm-id> IBM_PASSWORD='<your-ibm-password>' IBM_CFAPI=https://api.ng.bluemix.net IBM_ORG=<your-ibm-org> CLUSTER_NAME=<your-iks-cluster-name> ES_SVC_NAME=<your-eventstreams-service-name> REGION=us-south ZONE=dal10 ACCOUNTID=<your-account-id>
	```

	for us-east, use 
	https://api.us-east.cf.cloud.ibm.com
	wdc04

## Access the IBM Cloud and IKS from your Client

1. Login to your IBM Cloud account,

    ```console
    $ ibmcloud login -u $IBM_USERID -p $IBM_PASSWORD -r $REGION -g $IBM_RG -c $ACCOUNTID

	API endpoint: https://cloud.ibm.com
	Authenticating...
	OK

	Targeted account USER ONE's Account (1ab2c3de456789fg01h23i4j5k6l78mn) <-> 1234567

	Targeted resource group your-resourcegroup

	Targeted region us-east

                        
    API endpoint:      https://cloud.ibm.com   
    Region:            us-east   
    User:              userone@email.com   
    Account:           USER ONE's Account (1ab2c3de456789fg01h23i4j5k6l78mn) <-> 1234567   
    Resource group:    your-resourcegroups'   
    CF API endpoint:      
    Org:                  
    Space:          
    ```

2.  Assign the CF API endpoint,

    * If you don't have a custom resource group, then use the `default`,

    ```console
    $ ibmcloud target --cf-api $IBM_CFAPI
	Targeted Cloud Foundry (https://api.ng.bluemix.net)

	Targeted org 1234567

	Targeted space dev
					
	API endpoint:      https://cloud.ibm.com   
    Region:            us-east   
    User:              userone@email.com   
    Account:           USER ONE's Account (1ab2c3de456789fg01h23i4j5k6l78mn) <-> 1234567   
    Resource group:    your-resourcegroups'  
	CF API endpoint:   https://api.us-east.cf.cloud.ibm.com (API version: 2.128.0)   
	Org:                  
	Space:                        
    ```

2.  Or assign the default CF API endpoint,

	```console
	$ ibmcloud target --cf
	```

# Create a Fork in Github of the Guestbook App

* Go to https://github.com/IBM/guestbook
* Create a Fork to your personal Github account
* You will need the link to this personal fork in the Labs
