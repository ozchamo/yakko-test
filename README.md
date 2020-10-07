

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
oc new-app httpd:24~https://github.com/ozchamo/yakko-test-app.git







-------------------------------------------------------------------------------------------


And this is a reminder of the buttons to press with GITHUB :)




Quick setup — if you’ve done this kind of thing before
or	
https://github.com/ozchamo/yakko-test-app.git
Get started by creating a new file or uploading an existing file. We recommend every repository include a README, LICENSE, and .gitignore.

…or create a new repository on the command line
echo "# yakko-test-app" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/ozchamo/yakko-test-app.git
git push -u origin main
                
…or push an existing repository from the command line
git remote add origin https://github.com/ozchamo/yakko-test-app.git
git branch -M main
git push -u origin main
…or import code from another repository
You can initialize this repository with code from a Subversion, Mercurial, or TFS project.


