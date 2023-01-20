---
title: "Embedding the app"
chapter: false
weight: 30
---

## Publishing your app

The app is now ready to be used within Genesys Cloud. There are several ways to use it:

### Using localhost

This is what you have been doing so far. You can keep the app running locally and use it to your Genesys Cloud organization however **it will only work from your own computer**.

### Using your own domain

You can copy the source code in your own web server(s). Make sure the app can be reached via a publicly accessible URL (e.g. `https://mydomain.com/gdpr-requests`).

### Github pages

You can host this static web site using Github Pages if you have a Github Account. This is practical because it will give you a free `https` URL The credentials in `static/js/genesyscloud.js` are not critical as it requires anyone who uses it to also enter their username and password to authenticate.

A sample page is available [here](https://github.com/purecloudgdprrequests/purecloudgdprrequests.github.io). In this case, the `Authorized redirect URI` is `https://purecloudgdprrequests.github.io/index.html`

## Embed the app in your organization

To embed your web site directly inside PureCloud, you need to create a new `Integration`

- Go to `Admin/Integrations` and click on `+Integrations` on the top right to add a new client application
- In the `Details` tab:
  - Enter a name for the new client application
- In the `Configuration` tab, enter the following:
  - Application URL: The full path to your site home page (e.g. [https://purecloudgdprrequests.github.io](https://purecloudgdprrequests.github.io))
  - Application Type: widget
  - Application Category: (leave empty)
  - Iframe Sandbox Options: allow-scripts,allow-same-origin,allow-forms,allow-modals (default value)
  - Group Filtering: Select a group of users who can access this client application. You might have to create a new group first in `Admin/Groups`
  - Click on `Save`
- Go back to the `Details` tab and click on `Active` to activate this application

You might need to logout and log back in to view the app inside the `Apps` section on the left side.

![Embedded app](../images/app_icons.jpg)

Jump to the [Conclusion](../090-Conclution/_index.html) section to read what you have achieved.
