# Dropbox API testing with postman 

## Introduction 

This repository was created for API test automation of the Dropbox cloud-based online storage platform.
The platform chosen to implement this automated testing is [Postman](https://www.postman.com/) and uses JavaScript as the underlying implementation language. The below section gives a brief overview of how Postman is used in this testing.

## Setup

- clone this repository
- install all dependencies for this project with `npm install` or separately => 
- `npm install newman`
- `npm i newman-reporter-htmlextra`

## Refresh Token

Since we are working with static collection which was exported in certain period and by the Dropbox policies access token is only valid for 4 hours, before running the test new access token should be generated:

- open the terminal
- add to this line of code values from assets/data.js and run updated command `curl https://api.dropbox.com/oauth2/token -d grant_type=refresh_token -d refresh_token=<ADD REFRESH TOKEN HERE FROM assets/data.js> -u <ADD base64 code HERE from assets/data.js>`
- from the response copy value of the access token
- open the postman_environment.json file find the key `BEARERTOKEN` and paste copied access token to its value
- in case of any issues, download and watch video instruction from the assets folder

## Running test

- navigate to the project directory 
- open terminal
- to run the test: `npm run test`
- to run the test, generate a report: `npm run report` 
- to open the report navigate to the newly created newman folder(same directory) and open the HTML file in your browser