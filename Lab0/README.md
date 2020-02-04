# DevOps Lab 0 - Setup

Complete the steps below to setup the lab environment.

## Access the IBM Cloud via CLI

1. Login to your web terminal. Lab instructors should provide the access information.

	> Note: if you are doing the lab in a non-workshop environment, you may perform the steps in a command window or terminal. Pre-requisite CLIs are required to be installed locally.

1. Login to your IBM Cloud account. Enter your IBM Cloud account username and password when prompted.

    ```console
    $ ibmcloud logins
    ```

1.  Set `CF API endpoint`, `Org` and `Space`. If there are multiple choices, you'll be prompted.

	```console
	$ ibmcloud target --cf 
	```

1. Set `Region` and `Resource Group`.

    ```
    $ ibmcloud target -r us-east -g Feb2020Workshop
    ```

1. Configure your Kubernetes client using this command. This will also configure your Kubernetes client for future login sessions by adding the command into your .bash_profile. Your cluster name should be provided by the instructors.

    ```sh
    $ eval $(ibmcloud ks cluster-config --cluster <k8s-cluster-name> --export | tee -a ~/.bash_profile) 
    ```

    > Note: If the command has a syntax error in your terminal (e.g. windows cmd shell), you may instead run the command `ibmcloud ks cluster-config --cluster <k8s-cluster-name>`. Then, copy the output and execute it in the same terminal.

6. You should be able to use kubectl to list kubernetes resources. Try getting the list of pods (there should be none yet)

    ```sh
    $ kubectl get pods

    No resources found.
    ```

7. Login to the registry service

    ```sh
    $ ibmcloud cr login
    ```

8. Add a new `name space` in registry to store your docker image

	```
	$ ibmcloud  cr  namespace-add  clink_[your initial]

	$ export CRNAMESPACE=clink_[your initial]
	```

> Note: the new name space clink_[your initial] must be unique in the entire registry. If the new name space is not unique, change it slightly and try again.

> Note: Make a note of your new name space. Its name will be used later.


## Fork the Guestbook App in Github

Optionally, fork the Guestbook App in Github.

1. Login to https://github.com. You would need a GitHub account.

1. Go to https://github.com/IBM/guestbook in the same browser.

1. Fork the repo by clicking on the `Fork` button at the top-right of your screen.

1. Make a note of your new Git repo link. You may use the link to your personal fork in the Lab.s

## Unique Name of IBM Cloud Services

For most of services, you need a name globally unique in the IBM Cloud. IBM Cloud may generate a default name including a timestamp part. 

In the lab, you can keep and re-use the generated timestamp, or optiopnally you can create a new timestamp from bash commandline with `$ date +%s`,

	```console
	$ date +%s

	1571778717
	```