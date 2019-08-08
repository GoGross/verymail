![FinCharts](https://raw.githubusercontent.com/GoGross/exactip/master/exactip.png)

---
## VeryMail

Verymail, email address validation REST API engine, an thorough aggregated email verification api and mailing list authenticator service.

## :cloud: Installation

```sh
# Using npm
npm install --save verymail

```

## Getting started

[![FinCharts](https://raw.githubusercontent.com/GoGross/fincharts/master/free-key.jpg)](https://exactip.gogross.com)

Verymail offers for developers a method to connect their applications via our interactive, always live api inorder to keep control of their email comminication.

## API

Verymail exposes its data via an Application Programming Interface (API), so developers can interact in a programmatic way with the Verymail Service. This document is the official reference for that functionality.

## Authentication

#### Auth: API Key
All Verymail API endpoints require an access token generated from your dashboard as an API key.

## Cross-Origin Resource Sharing (CORS) 

Verymail is CORS enabled and allows Access-Control Headers. This will enable you to use our API via Cross-Origin HTTP Requests in application/json, application/x-www-form-urlencoded, multipart/form-data, text/plain. You don't need to specify any headers to make a CORS request as they are enabled by default.

## :clipboard: Example

### NodeJS
```
curl -X GET \
  -H "Content-Type: application/json" \
  -d '{"mailingList":[]}' \
  https://api.gogross.com/verymail?key=get_free_api_key
```
 

```js
const VeryMail     = require ( './index' );
const VERYMAIL_KEY   = process.env.VERYMAIL_KEY;  // API Key

const mail = {
	options: {
		saveList : false, // dedicated plans only
	},
	mailingList: ["zealmurapa@gmail.com"] // array, limit 100
};

const veryMail     = new VeryMail ( mail, VERYMAIL_KEY  );
veryMail.verify ( )
	.then ( ( results ) => {
		
		console.log ( results );
		
	} )
	.catch ( ( error ) => {
		
		console.trace ( error );
		
	} );

```

Except as otherwise noted, the content of this page is licensed under the Creative Commons Attribution 3.0 License, and code samples are licensed under the Apache 2.0 License. For details, see our Site Policies. Java is a registered trademark of Oracle and/or its affiliates.





