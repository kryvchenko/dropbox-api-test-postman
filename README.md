# Dropbox API testing with postman 

## Introduction 

This repository was created for API test automation of the Dropbox cloud-based online storage platform.
The platform chosen to implement this automated testing is [Postman](https://www.postman.com/) and uses JavaScript as the underlying implementation language. The below section gives a brief overview of how Postman is used in this testing.

## Setup

- clone this repository
- install all dependencies for this project with `npm install` or separately => 
- `npm install newman`
- `npm install newman-reporter-htmlextra`

## Running test

- navigate to the project directory 
- open terminal
- to run the test: `npm run test`
- to generate a report: `npm run report` 
- to open the report navigate to the newman folder and open the HTML file in your browser