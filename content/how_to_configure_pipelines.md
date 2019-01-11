# How to configure pipelines

### Basic Configuration

* <a href=#1>1. Configuring Version Control Providers</a>

* <a href=#2>2. Configuring Pipeline Stages and Steps</a>

* <a href=#3>3. Running the Pipeline</a>

* <a href=#4>4. Configuring Persistent Data for Pipeline Components</a>

###  <a href=#5>Advanced Configuration</a>





## <a name="1">1. Configuring Version Control Providers</a>

Here we use github. And you have a repository for example:https://github.com/lizhi123456/magento2

* Github

first: Authenticate the rancher pipeline to use github.

login in github ->settings -> developers settings 

and further opreate for example put in the Homepage URL,Authorization callback URL

and then you will get a Client ID,Client Secret.



* Rancher 

From GitHub, copy the Client ID and Client Secret. Paste them into Rancher.

we have add a cluster,its name magento2 and it have two namespace one default, other system. 

click cluster tab "magento2"-> Default -> Pipelines -> Cobfigure Repositories -> Authorize&Fetch Your Own Repositories

-> Configure now -> github ->Client ID: 5a172db14621202121    Client Secret:e1a4e276b03fc5482f5bcf0eb99
 
 -> Authenticate
 
 If the Client ID and  Client Secret is right , you will get the list of the github repositories, and then you can select the 
	
 lizhi123456/magento2  to enable.

Now back to the pipleline, you will see the  lizhi123456/magento2 showing.

## <a name="2">2. Configuring Pipeline Stages and Steps</a>

You can use web UI or yml files to configure pipeline stages and steps. Here we use yml to configure.

Step types available include:

* Clone

The first stage is preserved to be a cloning step that checks out source code from your repo. Rancher handles the cloning of the 

git repository. This action is equivalent to git clone <repository_link> <workspace_dir>.

This stage is automate runing that you dont need to configure.


* Run Script

The Run Script step executes arbitrary commands in the workspace inside a specified container. You can use it to build, test and do

more, given whatever utilities the base image provides. For your convenience you can use variables to refer to metadata of a pipeline

execution. Please go to the Pipeline Variable Reference for the list of available variables.


* Build and Publish Images

The Build and Publish Image step builds and publishes a Docker image. This process requires a Dockerfile in your source code’s

repository to complete successfully.



* Deploy YAML

This step deploys arbitrary Kubernetes resources to the project. This deployment requires a Kubernetes manifest file to be present in

the source code repository. Pipeline variable substitution is supported in the manifest file. You can view an example file at GitHub.

For available variables, refer to Pipeline Variable Reference.



## <a name="3">3. Running the Pipeline</a>

## <a name="4">4. Configuring Persistent Data for Pipeline Components</a>

## <a name="5">Advanced Configuration</a>
