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

## <a name="3">3. Running the Pipeline</a>

## <a name="4">4. Configuring Persistent Data for Pipeline Components</a>

## <a name="5">Advanced Configuration</a>
