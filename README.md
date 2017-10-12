# Installing rocket-chat into minishift
Here I'am telling how to intall rocketchat into minishift with persistent volumes.


## Create user and set policies and create project
Log into minishift as system administrater
```
oc login -u system:admin
```

```
oc adm policy add-role-to-user system:deployer rc
```
Create a new user
```
oc create user rc
```
Log as the new user
```
oc login -u rc
```
Create a new project
```
oc new-project rocketchat
```
## Import the YAML file to project
* Namespace : openshift
* Database Service Name : mongodb
* MongoDB User : admin
* MongoDB Password : admin
* MongoDB Database Name : rocketchat
* MongoDB Admin Password : admin

## Finally
Scale rocketchat to 0 pod.

Scale mongodb to 0 pod.

Scale rocketchat to 1 pod.

Scale mongodb to 1 pod.
