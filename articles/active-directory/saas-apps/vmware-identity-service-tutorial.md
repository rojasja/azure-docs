---
title: Azure Active Directory SSO integration with VMware Identity Service
description: Learn how to configure single sign-on between Azure Active Directory and VMware Identity Service.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: how-to
ms.date: 12/09/2022
ms.author: jeedes

---

# Azure Active Directory SSO integration with VMware Identity Service

In this article, you'll learn how to integrate VMware Identity Service with Azure Active Directory (Azure AD). VMware Identity Service provides integration with Azure AD for VMware products. It uses the SCIM protocol for user and group provisioning and SAML for authentication. When you integrate VMware Identity Service with Azure AD, you can:

* Control in Azure AD who has access to VMware Identity Service.
* Enable your users to be automatically signed-in to VMware Identity Service with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

You'll configure and test Azure AD single sign-on for VMware Identity Service in a test environment. VMware Identity Service supports both **SP** and **IDP** initiated single sign-on and **Just In Time** user provisioning.

## Prerequisites

To integrate Azure Active Directory with VMware Identity Service, you need:

* An Azure AD user account. If you don't already have one, you can [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* One of the following roles: Global Administrator, Cloud Application Administrator, Application Administrator, or owner of the service principal.
* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* VMware Identity Service single sign-on (SSO) enabled subscription.

## Add application and assign a test user

Before you begin the process of configuring single sign-on, you need to add the VMware Identity Service application from the Azure AD gallery. You need a test user account to assign to the application and test the single sign-on configuration.

### Add VMware Identity Service from the Azure AD gallery

Add VMware Identity Service from the Azure AD application gallery to configure single sign-on with VMware Identity Service. For more information on how to add application from the gallery, see the [Quickstart: Add application from the gallery](../manage-apps/add-application-portal.md).

### Create and assign Azure AD test user

Follow the guidelines in the [create and assign a user account](../manage-apps/add-application-portal-assign-users.md) article to create a test user account in the Azure portal called B.Simon.

Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, and assign roles. The wizard also provides a link to the single sign-on configuration pane in the Azure portal. [Learn more about Microsoft 365 wizards](/microsoft-365/admin/misc/azure-ad-setup-guides). 

## Configure Azure AD SSO

Complete the following steps to enable Azure AD single sign-on in the Azure portal.

1. In the Azure portal, on the **VMware Identity Service** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows how to edit Basic SAML Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier** textbox, type a URL using one of the following patterns:

    | **Identifier** |
    |-----------|
    | `https://<CustomerName>.vmwareidentity.com/SAAS/API/1.0/GET/metadata/sp.xml` |
    | `https://<CustomerName>.workspaceoneaccess.com/SAAS/API/1.0/GET/metadata/sp.xml` |
    | `https://<CustomerName>.vmwareidentity.asia/SAAS/API/1.0/GET/metadata/sp.xml` |
    | `https://<CustomerName>.vmwareidentity.eu/SAAS/API/1.0/GET/metadata/sp.xml` |
    | `https://<CustomerName>.vmwareidentity.co.uk/SAAS/API/1.0/GET/metadata/sp.xml` |
    | `https://<CustomerName>.vmwareidentity.de/SAAS/API/1.0/GET/metadata/sp.xml` |
    | `https://<CustomerName>.vmwareidentity.ca/SAAS/API/1.0/GET/metadata/sp.xml` |
    | `https://<CustomerName>.vmwareidentity.com.au/SAAS/API/1.0/GET/metadata/sp.xml` |
    | `https://<CustomerName>.vidmpreview.com/SAAS/API/1.0/GET/metadata/sp.xml` |

    b. In the **Reply URL** textbox, type a URL using one of the following patterns:

    | **Reply URL** |
    |-------------|
    | `https://<CustomerName>.vmwareidentity.com/SAAS/auth/saml/response` |
    | `https://<CustomerName>.workspaceoneaccess.com/SAAS/auth/saml/response` |
    | `https://<CustomerName>.vmwareidentity.asia/SAAS/auth/saml/response` |
    | `https://<CustomerName>.vmwareidentity.eu/SAAS/auth/saml/response` |
    | ` https://<CustomerName>.vmwareidentity.co.uk/SAAS/auth/saml/response` |
    | `https://<CustomerName>.vmwareidentity.de/SAAS/auth/saml/response` |
    | `https://<CustomerName>.vmwareidentity.ca/SAAS/auth/saml/response` |
    | `https://<CustomerName>.vmwareidentity.com.au/SAAS/auth/saml/response` |
    | `https://<CustomerName>.vidmpreview.com/SAAS/auth/saml/response` |

1. If you want to configure **SP** initiated SSO, then perform the following step:  

    In the **Sign on URL** textbox, type a URL using one of the following patterns:

    | **Sign on URL** |
    |-------------|
    | `https://<CustomerName>.vmwareidentity.com` |
    | `https://<CustomerName>.workspaceoneaccess.com` |
    | `https://<CustomerName>.vmwareidentity.asia` |
    | `https://<CustomerName>.vmwareidentity.eu` |
    | `https://<CustomerName>.vmwareidentity.co.uk` |
    | `https://<CustomerName>.vmwareidentity.de` |
    | `https://<CustomerName>.vmwareidentity.ca` |
    | `https://<CustomerName>.vmwareidentity.com.au` |
    | `https://<CustomerName>.vidmpreview.com` |

    > [!Note]
    > These values are not the real. Update these values with the actual Identifier, Reply URL and Sign on URL. Contact [VMware Identity Service Client support team](mailto:support@vmware.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

1. VMware Identity Service application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

    ![Screenshot shows the image of token attributes.](common/default-attributes.png "Image")

1. In addition to above, VMware Identity Service application expects few more attributes to be passed back in SAML response, which are shown below. These attributes are also pre populated but you can review them as per your requirements.

    | Name | Source Attribute|
    | ------------ | --------- |
    | firstName | user.givenname |
    | lastName | user.surname |
    | userName | user.userprincipalname |
    | externalId | user.objectid |
    | email | user.mail |

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section, click copy button to copy **App Federation Metadata Url** and save it on your computer.

    ![Screenshot shows the Certificate download link.](common/copy-metadataurl.png "Certificate")

## Configure VMware Identity Service SSO

To configure single sign-on on **VMware Identity Service SSO** side, you need to send the **App Federation Metadata Url** to [VMware Identity Service SSO support team](mailto:support@vmware.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create VMware Identity Service test user

In this section, a user called B.Simon is created in VMware Identity Service. VMware Identity Service supports just-in-time user provisioning, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in VMware Identity Service, a new one is created after authentication.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to VMware Identity Service Sign on URL where you can initiate the login flow.  

* Go to VMware Identity Service Sign on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the VMware Identity Service for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the VMware Identity Service tile in the My Apps, if configured in SP mode you would be redirected to the application sign-on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the VMware Identity Service for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](../user-help/my-apps-portal-end-user-access.md).

## Additional resources

* [What is single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)
* [Plan a single sign-on deployment](../manage-apps/plan-sso-deployment.md).

## Next steps

Once you configure VMware Identity Service you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).