# EventHubRESTAPItests
API REST testing with Postman

Eventhub is a demo website is an events platform where people can buy tickets.
Website: https://eventhub.rahulshettyacademy.com/login
Swagger\contract is available here: https://api.eventhub.rahulshettyacademy.com/api/docs/
API REST Tests
Prerequisites: Node.js installed on your PC
Environment: Prod environmente is READY to be tested. Dev Env is !--work in progress--! but the base url has been provided



E2E flows are automated:
Token can be retrieved from the response of the login request (no OAuth2.0, it's a bearer token)
Collection variables are "get" and "set" in pre and post script.
Tests can be found, as always, in the post-script of the requests:
Status code validation
Success message is in the responses, I used it as validation
EventBooked as an Event ID validation, to be sure that the event is present in the booked events personal page





NEWMAN
you can install Newman library globally from terminal:
npm.cmd install -g newman
And the html report:
npm install -g newman-reporter-htmlextra
you can run the collection with the following cmd:
newman run exported_collection.json -e exported_environment.json -d dataset.csv -r htmlextra



CI\CD
Test Run can be launched on Jenkins (but it needs local files). Git Actions incoming..

