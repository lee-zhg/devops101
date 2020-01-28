# Lab0 - Setup


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

* Create a Fork to your personal Github account
* You will need the link to this personal fork in the Labs
