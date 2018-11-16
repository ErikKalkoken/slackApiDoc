# slackApiDoc
An unofficial documentation of "undocumented" Slack API methods.

## Purpose
Slack has a great web API which is documented [here](https://api.slack.com/web). In addition there are a couple of so called "undocumented" methods. These methods provide some additional and very useful functionality that is not available with the official set of API methods. The purpose of this document is to provide an up-to-date documentation to anyone who wants to use these methods.

## Disclaimer
Please note that Slack explicitely states in its [API Terms of Service](https://slack.com/terms-of-service/api) that all undocumented methods "may change at any time, you should not rely on these behaviors.". So use them at your own risk.

## Scope of this repo
This repo contains a documentation of so called "undocumented" API methods for Slack. These methods are not documented in the official API documentation and usually require a [legacy token](https://api.slack.com/custom-integrations/legacy-tokens) to be used.

API methods that are only available via the web UI and require a runtime token are **out of scope** of this repo.

## How to use undocumented API methods
- **Token type**: In general all undocumented API methods require the `post` scopes and therefore needs to be called with a [legacy token](https://api.slack.com/custom-integrations/legacy-tokens).
- **Slack apps**: Since the `post` scope is not available through the standard Oauth process they can not be directly used in a normal Slack app. In order to use them in a Slack app a legacy token for the respective workspace needs to always be manually create and added.
- **Request types**: In general these API methods support GET and standard POST requests only. Standard POST requests use bodies encoded as `application/x-www-form-urlencoded`. The more modern JSON encoded bodies are not supported.

## Licence
This documentation is provided as public domain. Any help in keeping this document up-to-date and as complete and accurate as possible is very welcome. 

Slack and the Slack API is owned by [Slack Technologies, Inc.](https://slack.com/) All rights reserved by Slack.


