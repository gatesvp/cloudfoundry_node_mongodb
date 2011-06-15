Overview
========

This repo contains a "getting started" sample for MongoDB with Node.js on VMWare's CloudFoundry platform.

The sample is broken up in to steps based on the last digit of the file name. So `app.js.1` is the first step, `app.js.2` is the second step and so on.

Step 1
------

Gets a basic "Hello World" functioning on Cloud Foundry.

To test visit `my_app_name.cloudfoundry.com`.

Step 2
------

Add parsing and printing of MongoDB environment variables. See the `generate_mongo_url` function. The output of this function is a "connection string" to the local MongoDB instance. Note the relatively naive implementation.

Step 3
------

Includes the `node-mongodb-native` driver. Performs a simple insert of IP and Timestamp whenever the URL is visited. There's no routing, just a simple increment.

See the `record_visit` function for implementation details.

Step 4
------

Extend step 3 with a /history option that will print the 10 most recent visits.

To test visit `my_app_name.cloudfoundry.com/history`.

See the `print_visits` function for implementation details.

Step 5
------

For building a better a UI, take a look at the `express` framework. (expressjs.org)
