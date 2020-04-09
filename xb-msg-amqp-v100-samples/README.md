# Sample application for Messaging Client Node.js

## Description
Sample application (plain Node.js) of how to use the _Enterprise Messaging Client_ to send and receive messages via _SAP Cloud Platform Enterprise Messaging_.

## How To run
This section includes the _Prerequisite_, describe _how to install_ and _how to configure_ this basic sample.

  1. Prerequisite: Enable Enterprise Messaging on _SAP CP_ 
      1. Create required _Enterprise Messaging_ service via e.g. `cf cs enterprise-messaging default enterprise-messaging-service-instance-name -c config/descriptor.json'`
      1. Create service key via e.g. `cf csk enterprise-messaging-service-instance-name key-name -c config/descriptor.json'`
      1. Get key via e.g. `cf service-key enterprise-messaging-service-instance-name key-name`
      1. Update the `config/cf-sample-config.js` with information of the _service key_
      1. More info regarding enterprise messaging serviceinstance creation is available [here](https://help.sap.com/viewer/bf82e6b26456494cbdd197057c09979f/Cloud/en-US/d0483a9e38434f23a4579d6fcc72654b.html)
 
  1. Install required dependencies via `npm install` 
  1. Run sample application
      1. Start producer via `npm run-script producer` (default) or via `node src/producer.js ../config/cf-sample-config.js` (with given config file)
      1. Start consumer via `npm run-script consumer` (default) or via `node src/consumer.js ../config/cf-sample-config.js` (with given config file)

## Support
This project is _'as-is'_ with no support, no changes being made.  
You are welcome to make changes to improve it but we are not available for questions or support of any kind.

## License
Copyright (c) 2017 SAP SE or an SAP affiliate company. All rights reserved.  
This file is licensed under the _SAP SAMPLE CODE LICENSE AGREEMENT, v1.0-071618_ except as noted otherwise in the [LICENSE file](../LICENSE.txt).
