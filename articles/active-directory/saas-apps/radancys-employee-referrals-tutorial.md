---
title: Azure AD SSO integration with Radancy's Employee Referrals
description: Learn how to configure single sign-on between Azure Active Directory and Radancy's Employee Referrals.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 01/19/2023
ms.author: jeedes

---

# Azure AD SSO integration with Radancy's Employee Referrals

In this tutorial, you'll learn how to integrate Radancy's Employee Referrals with Azure Active Directory (Azure AD). When you integrate Radancy's Employee Referrals with Azure AD, you can:

* Control in Azure AD who has access to Radancy's Employee Referrals.
* Enable your users to be automatically signed-in to Radancy's Employee Referrals with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Radancy's Employee Referrals single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* Radancy's Employee Referrals supports **SP and IDP** initiated SSO.
* Radancy's Employee Referrals supports **Just In Time** user provisioning.

## Add Radancy's Employee Referrals from the gallery

To configure the integration of Radancy's Employee Referrals into Azure AD, you need to add Radancy's Employee Referrals from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **Radancy's Employee Referrals** in the search box.
1. Select **Radancy's Employee Referrals** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, and walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

## Configure and test Azure AD SSO for Radancy's Employee Referrals

Configure and test Azure AD SSO with Radancy's Employee Referrals using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in Radancy's Employee Referrals.

To configure and test Azure AD SSO with Radancy's Employee Referrals, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure Radancy's Employee Referrals SSO](#configure-radancys-employee-referrals-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Radancy's Employee Referrals test user](#create-radancys-employee-referrals-test-user)** - to have a counterpart of B.Simon in Radancy's Employee Referrals that are linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **Radancy's Employee Referrals** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows how to edit Basic SAML Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://<company-domain>.auth.1brd.com/saml/sp`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<company-domain>.auth.1brd.com/saml/callback`

1. Perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<company-domain>.1brd.com/login`

	> [!NOTE]
	> These values are not real. Update these values with the actual Identifier, Reply URL and Sign-on URL. Contact [Radancy's Employee Referrals Client support team](mailto:support@firstbird.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

1. Radancy's Employee Referrals application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows the list of default attributes.

	![Screenshot shows the image of token attributes configuration.](common/edit-attribute.png "Image")

1. In addition to above, Radancy's Employee Referrals application expects few more attributes to be passed back in SAML response, which are shown below. These attributes are also pre populated but you can review them as per your requirement.

	| Name | Source Attribute|
	| ---------------| --------- |
	| first_name | user.givenname |
	| last_name | user.surname |
    | email | user.mail |

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section, find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

	![Screenshot shows the Certificate download link.](common/metadataxml.png "Certificate")

1. On the **Set up Radancy's Employee Referrals** section, copy the appropriate URL(s) based on your requirement.

	![Screenshot shows how to copy configuration URL.](common/copy-configuration-urls.png "Metadata")

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B.Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B.Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to Radancy's Employee Referrals.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **Radancy's Employee Referrals**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you're expecting any role value in the SAML assertion, in the **Select Role** dialog, select the appropriate role for the user from the list and then click the **Select** button at the bottom of the screen.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Radancy's Employee Referrals SSO

1. Log in to the Radancy's Employee Referrals website as an administrator.

1. Navigate to **Account Preferences** > **Authentication** > **Single Sign-On**.

1. In the **SAML IdP Metadata Configuration** section, perform the following steps:
    
    ![Screenshot shows how to upload the Federation Metadata.](media/radancys-employee-referrals-tutorial/certificate.png "Federation")

    1. In the **Entity ID** textbox, paste the **Azure AD Identifier** value, which you've copied from the Azure portal.

    1. In the **SSO-service URL** textbox, paste the **Login URL** value, which you've copied from the Azure portal.

    1. In the **Signing certificate** textbox, paste the **Federation Metadata XML** file, which you've downloaded from the Azure portal.

    1. **Save configuration** and verify the setup.

    > [!NOTE]
    > You need to have the SSO option included in your contract.

### Create Radancy's Employee Referrals test user

In this section, a user called B.Simon is created in Radancy's Employee Referrals. Radancy's Employee Referrals supports just-in-time user provisioning, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in Radancy's Employee Referrals, a new one is created after authentication.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to Radancy's Employee Referrals Sign-on URL where you can initiate the login flow.  

* Go to Radancy's Employee Referrals Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the Radancy's Employee Referrals for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the Radancy's Employee Referrals tile in the My Apps, if configured in SP mode you would be redirected to the application sign-on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Radancy's Employee Referrals for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](../user-help/my-apps-portal-end-user-access.md).

## Next steps

Once you configure Radancy's Employee Referrals you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).