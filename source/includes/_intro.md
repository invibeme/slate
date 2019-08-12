# Introduction

Welcome to the CheKin API! 

The first you need to use CheKin API is to signup to create an account and get a token.

You can use our API to access the following services:

- Legal compliance For Guest registration: Police & Statistics

- Documentation management service

- MRZ / OCR Scanner

- Biometric Match Service

- Check-in Online


The CheKin API is organized around REST. Our API has predictable, resource-oriented URLs, and uses HTTP response codes to indicate API errors. We use built-in HTTP features, like HTTP authentication and HTTP verbs, which are understood by off-the-shelf HTTP clients. 
We support cross-origin resource sharing, allowing you to interact securely with our API from a client-side web application. 

CheKin API accepts data as JSON or also as multipart/form-data. JSON is returned by all API responses, including errors.

The base url for CheKin API endpoints is `https://api.chekin.io/api/v1/`

For the police api the last version is v1.1, then the base url is `https://api.chekin.io/api/v1.1/`

# Security
All the API runs over HTTPS, so data transmission in encrypted. Also, the guests data and signature are stored encrypted into our database.


