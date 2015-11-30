# pg_studio_1.2_cf
PostgreSQL Studio 1.2 for Cloud Foundry

This is a slightly modified version of [pgStudio] (https://bitbucket.org/openscg/pgstudio).  My [fork] (https://bitbucket.org/john_k_ge/pgstudio) is publicly-available as well.  I increased the width of the username and password fields to accomodate the large strings used in Predix Cloud.  I also modified ConnectionInfo.java to remove the incorrect DatabaseConnectionExceptions due to the HA_Proxy load-balancing.

To use this application, simply clone this repo and modify the manifest.yml to give it a unique name.  Afterwards, you can push this to your space and logon using the form.  There is no need to bind your deployed instance to this and restage; you can just enter the host, port, DB name and credentials found in any app's environment variables.
