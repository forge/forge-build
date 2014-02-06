forge-build
===========

Used to release Furnace and Forge projects

To release Furnace and Forge together:

````
    git submodule update --remote && git commit -m "Updated submodules"
    mvn clean release:prepare release:perform -DdevelopmentVersion=DEV_VERSION -Dtag=REL_VERSION -DreleaseVersion=REL_VERSION

````


To release only Furnace:

````
    git submodule update --remote && git commit -m "Updated submodules"
    mvn clean release:prepare release:perform -Pfurnace -DdevelopmentVersion=DEV_VERSION -Dtag=REL_VERSION -DreleaseVersion=REL_VERSION 

````

To release only Forge:

````
    git submodule update --remote && git commit -m "Updated submodules"
    mvn clean release:prepare release:perform -Pforge -DdevelopmentVersion=DEV_VERSION -Dtag=REL_VERSION -DreleaseVersion=REL_VERSION

````

Where:
- *DEV_VERSION* should be replaced by the next development version. Eg: 2.1.0-SNAPSHOT
- *REL_VERSION* should be replaced by the released version. Eg: 2.0.0.Final


w
