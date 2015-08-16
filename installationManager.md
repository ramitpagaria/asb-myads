# Installation Manager #

## IM provides the following functionality: ##
  * setting the number of instances
  * setting custom MySQL username/password

## IM **does not** allow any of the following: ##
  * removing or clearing any of the database intances

So IM is pretty safe. Only incremental database updates are possible.

## For IM to appear the following conditions should be met: ##
  * app server should be started/restarted for the installation manager to check db state (it happens only once during the initialization of the application)
  * open browser at /myads/index.html - the location of the Flex client application
  * software update or first install that requires db schema update or creation. Software update occurs during the deployment of a new version. OR
  * db.update.required is set to 'true' in `<UserHome>/.dbProperties` file created by ASB MyAds

## About `<UserHome>/.dbProperties` File ##

This file is created by IM to store custom db username and password and also db.update.required variable used to trigger IM on app server restart.

## Requirements: ##
  * database server (MySQL) should contain a user that has permissions to create databases. You can create such user using the following SQL:
> > `grant all privileges on *.* to 'banner'@localhost identified by 'banner123';`
  * MySQL 5.1.`*` + (with support for stored procedures and triggers)
  * database server should be running on localhost (127.0.0.1) port 3306 (default) - we currently do not have this setting in the installer