Overview
========

This repo contains a "getting started" sample for MongoDB with Node.js on VMWare's CloudFoundry platform.

The sample is broken up in to steps based on the last digit of the file name. So `app.js.1` is the first step, `app.js.2` is the second step and so on.

Step 1
------

Gets a basic "Hello World" functioning on Cloud Foundry.

Step 2
------

Add parsing and printing of MongoDB environment variables.

The output of this function should allow you to connect to the server from the command line.

Step 3
------

Includes the `node-mongodb-native` driver. Performs a simple insert of IP and Timestamp whenever the page is visited.

Step 4
------

Extend step 3 with a /history option that will print the 10 most recent visits.
