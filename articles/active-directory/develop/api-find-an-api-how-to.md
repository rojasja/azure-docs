---
title: Find an API for a custom-developed app
description: How to configure the permissions you need to access a particular API in your custom developed Azure AD application
services: active-directory
author: rwike77
manager: CelesteDG

ms.service: active-directory
ms.subservice: develop
ms.workload: identity
ms.topic: conceptual
ms.date: 09/27/2021
ms.author: ryanwi
ROBOTS: NOINDEX
---

# How to find a specific API needed for a custom-developed application

Access to APIs require configuration of access scopes and roles. If you want to expose your resource application web APIs to client applications, configure access scopes and roles for the API. If you want a client application to access a web API, configure permissions to access the API in the app registration.

## Configuring a resource application to expose web APIs

When you expose your web API, the API be displayed in the **Select an API** list when adding permissions to an app registration. To add access scopes, follow the steps outlined in [Configure an application to expose web APIs](quickstart-configure-app-expose-web-apis.md).

## Configuring a client application to access web APIs

When you add permissions to your app registration, you can **add API access** to exposed web APIs. To access web APIs, follow the steps outlined in [Configure a client application to access web APIs](quickstart-configure-app-access-web-apis.md).

## Next steps

- [Understanding the Azure Active Directory application manifest](./reference-app-manifest.md)
