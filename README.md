# Installing rocket-chat into minishift
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
oc new-project rocket-chat
```
