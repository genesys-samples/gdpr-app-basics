---
title: "Update code and Launch the app"
chapter: false
weight: 20
---

## Update the app configuration

- Open the `/static/js/genesyscloud.js` file
- Set the `clientId`, `redirectUrl` and `environment` constants to the values you got from Genesys Cloud earlier, e.g.:

```js
const clientId = "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx";
const redirectUrl = "http://localhost";
const environment = "mypurecloud.ie"; // Your Genesys Cloud environment (e.g. mypurecloud.com, mypurecloud.de)
```

Find your environment [here](https://developer.genesys.cloud/platform/api/)

## Launch the app

- Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in Visual Studio Code
- Make sure the `index.html` file is open in the editor
- Click on `Go Live` to start a local web server

You should be able to see the following page:

![First launch](../images/app_first_launch.jpg)

## How to use the app

### Starting a new request

- Click on the `New Request` button
- Select the request type
  - `Delete` will anonymize a user's [PII](https://en.wikipedia.org/wiki/Personal_data)
  - `Export` will export a user's activities within Genesys Cloud. The exported file is a set of CSV and JSON files.
  - `Update` will update a user's details throughout Genesys Cloud.
- Enter a name, an address, a phone number or an email address. Only one of these fields is required but you can enter as many as you like to find the right person.
- Click on `Search`
- Click on `Select and Submit` after you have identified the correct person

![Search Subject](../images/app_search_subject.jpg)

- If the request succeeds, you should now see the following:

![Searching](../images/app_searching.jpg)

- Requests typically take between 24h and 48h to be processed. You can check the status of your request by refreshing the page.

Next, go to [Embedding the app](30_third.html) to embed this app in your own Genesys Cloud organization.
