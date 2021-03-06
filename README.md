# node-hipchatbot
A very basic bot for creating custom slash commands on Hipchat using node.js. 

#### Install dependencies
After cloning the files, Open up a command window in the directory and type the following:

`npm install`

This will install all the required node modules needed to get this basic app running.

This step is not needed when using Heroku as that picks up the dependencies in the Packages.json file and installs on that platform.

#### Running the app locally

Once you have the dependencies installed locally, use the `npm start` command to run the app. Using [Postman](https://www.getpostman.com/ "Postman") or your favorite REST client you can then POST a request to the local endpoint.

POST Request:
`localhost:3000/hipchatbot`

JSON Body:
`{ "item": { "message": { "message": "Test Sentence" } } }`

Endpoint Response:
`{ "message": "You entered the following text: Test Sentence" }`

#### Deploying the app to Heroku

This integration can be deployed using Heroku. The Procfile in the repository is all that you will need to start the server.

Here is a guide for deploying a node app to Heroku: https://devcenter.heroku.com/articles/deploying-nodejs

Once this bot is deployed using either Heroku, AWS or any other platform, you can link it up to Hipchat and start using it to do...well, anything you tell it to do.

These custom slash command bots can be added to Hipchat by following the details contained in this Hipchat blog post.

https://blog.hipchat.com/2015/02/11/build-your-own-integration-with-hipchat/


