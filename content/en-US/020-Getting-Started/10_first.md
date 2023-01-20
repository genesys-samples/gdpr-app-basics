---
title: "First Steps"
chapter: false
weight: 10
---

## Requirements

- [Visual Studio Code](https://code.visualstudio.com/)
- Git
- Genesys Cloud organization

## Create an OAuth Client

The website will use Genesys Cloud OAuth to authenticate users so you first need to create a new OAuth `implicit grant` client id/secret in your Genesys Cloud organization.

- Open Genesys Cloud, go to `Admin` and click on `OAuth` (under `Integrations`)
- Click on `Add Client`
- Give your app a name (e.g. `GDPR Requests`). Description is optional.
- Select `Token Implicit Grant (Browser)`
- Enter `http://localhost:3000` as the `Redirect URI`
- In the `Scope` section, select `gdpr` and `gdpr:readonly`
- Click `Save` and note the `Client ID` string value

## Download the source code

- Run `git clone https://github.com/PierrickI3/genesyscloud-gdpr-requests` to get the latest code
- Use vscode to open the files:
  - `cd genesyscloud-gdpr-requests`
  - `code .`

Next, go to [Update code and Launch the app](20_second.html) to launch the app locally.
