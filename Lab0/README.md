# DevOps Lab 0 - Setup

Complete the steps below to setup the lab environment.

## Access the IBM Cloud via CLI

1. Login to your web terminal. Lab instructors should provide the access information.

	> Note: if you are doing the lab in a non-workshop environment, you may perform the steps in a command window or terminal. Pre-requisite CLIs are required to be installed locally.

1. Login to your IBM Cloud account. Enter your IBM Cloud account username and password when prompted.

    ```console
    $ ibmcloud login -r us-south -g Default
    ```

1.  Set CF API endpoint, Org and Space. If there are multiple choices, you'll be prompted.

	```console
	$ ibmcloud target --cf
	```

## Fork the Guestbook App in Github

Optionally, fork the Guestbook App in Github.

1. Login to https://github.com. You would need a GitHub account.

1. Go to https://github.com/IBM/guestbook in the same browser.

1. Fork the repo by clicking on the `Fork` button at the top-right of your screen.

1. Make a note of your new Git repo link. You may use the link to your personal fork in the Lab.s

## Unique Name of IBM Cloud Services

For most of services, you need a name globally unique in the IBM Cloud. IBM Cloud may generate a default name including a timestamp part. 

In the lab, you can keep and re-use the generated timestamp, or you can create a new timestamp from bash commandline with `$ date +%s`,

	```console
	$ date +%s

	1571778717
	```