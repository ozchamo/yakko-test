

This app is a github based test to be able to run up an app quickly off openshift.
My little Hello World for OpenShift, from command line or menu.

From the OpenShift Menus, you would do all this to make it work:
- Create a new Project
- Create a new app: Add -> From Git
- Git Repo URL: https://github.com/ozchamo/yakko-test-app
- Builder Image: Httpd  (Which is Apache)
- Resources: Deployment
- CREATE

From the OC command line:
oc new-app httpd:latest~https://github.com/ozchamo/yakko-test-app.git

