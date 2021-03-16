

This github app is used to run up a quick test from openshift.

It was created as a HELLO WORLD app to deploy a litte tangible proof 
for OpenShift clusters built using YAKKO (https://ozchamo.github.io/YAKKO).
YAKKO offers a simple call to build the app automatically with the
appropriate OpenShift route to complete the demonstration.

From the OpenShift Menus, you would do all this to make it work:
- Create a new Project
- Create a new app: Add -> From Git
- Git Repo URL: https://github.com/ozchamo/yakko-test-app
- Builder Image: Httpd  (Which is Apache)
- Resources: Deployment
- CREATE
- Add route... etc etc

From the OC command line:
- oc new-app httpd:latest~https://github.com/ozchamo/yakko-test-app.git

From YAKKO - after creating a cluster, simply run
- yakko ops yakkotest

This last call brings together the following, along with the appropriate 
warning that you must first deploy a registry using "yakko ops addlocalregistry"
- oc new-project yakkotest
- oc new-app httpd:latest~https://github.com/ozchamo/yakko-test.git --name=yakko
- oc expose service yakko --hostname=yakkotest.apps.${CLUSTERFQDN}
