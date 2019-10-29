# Mongo Cookbook :man_cook:

This is a cookbook with mongodb!

## Assignment 1

### Summary
We need to create a reusable chef cookbook for installing and managing mongodb servers.

### Tasks
- Create a new cookbook called mongo
- Create a ChefSpec suite that tests for the following:
   - Sources list is updated
   - mongodb-org is added to the sources list ( there is a matcher for this )
   - MongoDB will be installed
- And InSpec tests for the following:
  - MongoDB is installed
  - MongoDB is version 3.*
- Create a recipe that installs and configures this cookbook correctly to pass all these tests.

## Assignment 2

### Summary
Our Mongo cookbook currently only install mongodb but it is not configured or started. Let's used templates and attributes to configure the cookbook

### Tasks
- Add new ChefSpec tests for the following:
  - Create a mongod.conf file in /etc/mongod.conf
  - Create a mongod.service file in /etc/systemd/system/mongod.service
  - MongoDB service should be enabled
  - MongoDB service should be started
- And InSpec tests for the following:
  - MongoDB is running
  - MongoDB is enabled
  - MongoDB is listening on 27017 by default
  - MongoDB is listening on 0.0.0.0 by default
- Create a recipe that installs and configures this cookbook correctly to pass all these tests.
- Use attributes to allow the port number and ip to be configurable.
