Context-Aware Configuration Training: AEM
=========================================

This training projects targets the following training modules:
* [PVTRAIN-167 wcm.io Context-Aware Configuration](https://confluence.pvtool.org/x/wIWmE)


Requirements
------------

* AEM 6.2 author instance running on port 4502


Deploy sample project
---------------------

You can use this script for a full deployment (application, sample content, configuration) into a local AEM instance running at http://localhost:4502:

```
clean_install_deploy_package.sh
```

This script also cleans and builds all maven projects and generates eclipse project files.

For the exercise you will work in the `bundles/base` and `bundles/editorial` bundles. Example to redeploy only one of these bundles:

```
cd bundles/editorial
mvn cq:install
```


Configure File System Resource Provider
---------------------------------------

You can mount the files system of your eclipse project to directly see changes in Sightly HTML, JSON oder other files in your running AEM application without having to redeploy the OSGi bundles. Deploying the OSGi bundle is only required if you change Java code.

To setup the files ystem synchronization go to the folder of the bundle project below `bundles/` and execute on it:

```
mvn sling:fsmount
```


Exercises
---------

See [PVTRAIN-168-02 AEM Context-Aware Configuration](https://confluence.pvtool.org/x/oIamE)