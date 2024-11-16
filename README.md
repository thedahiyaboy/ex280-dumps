
# 🎩 EX280 practice dump questions

## Question-1:  Configure an identity provider 
Configure your OpenShift cluster to use an HTPasswd identity provider with the following 
- The name of the identity provider is: `ex280-htpasswd`
- The name of the secret is: `ex280-idp-secret` 
- The user account `Armstrong` is present and can log in with password `indionce`.
- The user account `collins` is present and can log in with password `veraster`. 
- The user account `aldrin` is present and can log in with password `roonkere`. 
- The user account `jobs` is present and can log in with password `sestiver`. 
- The user account `Wozniak` is present and can log in with password `glegunge`. 

## Question-2: Configure cluster permissions 
Configure your OpenShift cluster to meet the following requirements: 
- The user account `jobs` can perform cluster administration tasks.
- The user account `wozniak` can create projects. 
- The user account `wozniak` cannot perform cluster administration tasks. 
- The user account `armstrong` cannot create projects. 
- The user account `kubeadmin` is not present 

## Question-3:  configure project permissions
Configure your OpenShift cluster to meet the following requirements: 
- The following projects exist: 
  * `apollo` 
  * `manhattan` 
  * `gemini`
  * `bluebook` 
  * `titan` 
- The user account `armstrong` is an administrator for project `apollo` and project `gemini` 
- The user account `wozniak` can view project `titan` but not administer or delete it 

## Question-4: Configure groups
Configure your OpenShift cluster to meet the following requirements:
- The user account `armstrong` is a member of the `commander` group
- The user account `collins` is a member of the `pilot` group
- The user account `aldrin` is a member of the `pilot` group
- Members of the `commander` group have edit permission in the `apollo` project 
- Members of the `pilot` group have view permission in the `apollo` project

## Question-5: Configure quotas
Configure your OpenShift cluster to use quotas in the manhattan project with the following require
The name of the quota is: `ex280-quota`
- The amount of memory consumed across all containers may not exceed 160Mi.
- The total amount of CPU consumed across all containers may not exceed 2 full cores.
- The maximum number of replication controllers does not exceed 3.
- The maximum number of pods does not exceed 3.
- The maximum number of services does not exceed 6.

## Question-6: Scale an application manually
- Ensure that there are exactly 5 replicas of the `minion` application in the `guru` project.


## Question-7: Scale an application automatically
Automatically scale the `hydra` deployment in the `lerna` project with the follow
- Minimum number of pods: 2
- Maximum number of pods: 9
- Target average CPU utilization per pod: 60 percent
- The pods require 25m CPU time to operate
- The pods must not consume more than 180 CPU time

## Question-8: Configure a secure route
Configure the oxcart application in the `area51` project with the following requirements:
- The application uses a secure route called `oxcart`
- Traffic between the client and the router is encrypted
- Traffic between the router and the service is unencrypted
- The route uses a CA signed certificate with the following subject fields: `/C=US/ST=NV/L=Hiko/O=CIA/OU=USAF/CN=classified.apps.domain20.example.co`
- The application is reachable only at the following address: `https://classified.apps.domain28.example.com` The application produces output


## Question-9:
Configure application data
Deploy an application using the `openshift/hello-openshift` image that meets the following requirements:
- The application is part of a project named: `acid`
The application is named: `phosphoric`
The application uses a key named `RESPONSE` in a configuration map named `sedicen`
The application is running and available at `http://phosphoric acid.apps.domain20.example.com` and display 
 `Soda pop won't stop can't stop`


## Question-10: Deploy an application with helm
- Deploy the chart named `redhat-movie` in the project `ascii-movie` from the repository `http://helm.domain20.example.com/chart/`
- You may use the telnet or ne commands to validate the deployment.


## Queston-11: Configure a secret
Configure a secret in the math project with the following requirements:
- The name of the secret is: `magic`
- The secret defines a key with name: `decoder_ring`
- The secret defines the key with value: `XpWy9KdcP3T`


## Question-12: Configure an application to use a secret
Configure the application called `qed` in the `math` project with the following requirements:
- The application uses the secret previously created called: `magic` The secret defines an environment variable with name: `DECODER_RING`
- The application output no longer displays: `Sorry, application is not configured correctly.`


## Queston-13: Configure a service account
Configure a service account in the `apples` project to meet the following requirements:
- The name of the service account is `ex280sa`
- The service account allows pods to be run as any available user


## Question-14: Deploy an application
Deploy the application called `oranges` in the `apples` project so that the following condition
- No configuration components have been added or removed
- The application produces output
- The application uses the `ex280sa` service account


## Question-15: Debug an application
Deploy the application called `atlas` in the `mercury` project so that the following condition
- No configuration components have been added or removed
- The application produces any error in output

## Question-16: Configure a network policy
Configure a network policy using the `database` and `checker` projects with the following requirements:
- The `database` project has network policy with the name `db-allow-sysql-conn` based on pod selector label `network.openshift.io/policy-group`
- Connections to the `database` project are restricted to deployments from the `checker` project.
- The network policy is filtered by project selector using the team devsecops label and pod selector using the `deploymentb-sysql` label
- The application can establish a connection to port `3306/TCP`
- You can check your work by examining the logs in the `checker` project.
