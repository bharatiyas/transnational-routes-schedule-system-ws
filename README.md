# transnational-routes-schedule-system-ws


## Introduction
This is an implementation for *Transnational Routes And Schedule System API* which provides the capability to query location routes and the departure schedule from Transnational. It calls Transnational's Routes and Schedule APIs, and then transforms their result in FirstBooking's Canonical Routes and Schedule Data models.

## API Details
More about *Transnational Routes And Schedule System API* can be found at https://anypoint.mulesoft.com/exchange/portals/scrollwell/4c4287b2-7066-4b83-864f-60985a79247e/transnational-routes-and-schedule-system-api/

## Some Implementation Details
1. Currently there are no secutiry requirements for this API hence its not secured
2. Schedules API has not been implemented yet. Hence, it will return HTTP status code 501 upon invocation.
3. Currently it calls the SOAP-UI mocks. But this is easily configurable and changeable to call actual APIs. For that, you may preferably want to create another config yaml file

## Running and Testing the project
To run the application from Anypoint Studio perform the following steps:

1. Fetch the project from Github
2. Extract the SOAP-UI Mocks from *src/test/resources/soapui-mocks* directory
3. Import the files in SOAP-UI and run the mock. There is only one mock for Routes API because Schedules API has not been implemented.
4. Edit Run Configurations to provide an environment variables: env = dev
5. Run the configuration
6. Extract the Postman collection and environment files from *src/test/resources/postman*
7. Import the Postman collection and environment files in Postman
8. Select *firstbooking-dev* and invoke the requests
