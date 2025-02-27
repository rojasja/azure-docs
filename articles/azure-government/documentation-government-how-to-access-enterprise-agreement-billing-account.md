---
title: Access your EA billing account in the Azure Government portal | Microsoft Docs
description: This article describes how to Access your EA billing account in the Azure Government portal.
services: azure-government
cloud: gov
documentationcenter: ''
ms.service: azure-government
author: bandersmsft
ms.author: banders
ms.reviewer: prsaini
ms.topic: article
ms.tgt_pltfrm: na
ms.workload: azure-government
ms.date: 05/08/2023
---

# Access your EA billing account in the Azure Government portal

As an Azure Government Enterprise Agreement (EA) customer, you can now manage your EA billing account directly from [Azure Government portal](https://portal.azure.us/). This article helps you to get started with your billing account on the Azure Government portal.

> [!NOTE]
> The Azure Enterprise (EA) portal is getting retired. We recommend that both direct and indirect EA Azure Government customers use Cost Management + Billing in the Azure Government portal to manage their enrollment and billing instead of using the EA portal.

## Access the Azure Government portal

You can manage your Enterprise Agreement (EA) billing account using the [Azure Government portal](https://portal.azure.us/). To access the portal, sign in using your Azure Government credentials.

If you don't have Azure Government credentials, contact the User Administrator or Global Administrator of your Azure Government Active Directory (Azure AD) tenant. Ask them to add you as a new user in Azure Government Active directory.

A User Administrator or Global Administrator uses the following steps to add a new user:

1. Sign in to the [Azure Government portal](https://portal.azure.us/) in the User Administrator or Global Administrator role.
1. Navigate to **Azure Active Directory** > **Users**.
1. Select **New user** > **Create new user** from the menu.  
    :::image type="content" source="./media/documentation-government-how-to-access-enterprise-agreement-billing-account-01.png" alt-text="Screenshot showing the New user option." lightbox="./media/documentation-government-how-to-access-enterprise-agreement-billing-account-01.png" :::
1. On the **New User** page, provide the new user's information like user name, display name, role etc.
1. Copy the autogenerated password provided in the **Password** box. Share it with the new user to sign in for the first time.
1. Select **Create**.

Once you have the credentials, sign into the [Azure Government Portal](https://portal.azure.us/) and you should see **Microsoft Azure Government** in the upper left section of the main navigation bar.

:::image type="content" source="./media/documentation-government-how-to-access-enterprise-agreement-billing-account-02.png" alt-text="Screenshot showing the Microsoft Azure Government environment." lightbox="./media/documentation-government-how-to-access-enterprise-agreement-billing-account-02.png" :::

To access your Enterprise Agreement (EA) billing account or enrollment, assign the appropriate permissions to the newly created Azure Government user account. Reach out to an existing Enterprise Administrator and they should be able to assign one of the following roles:

- Enterprise Administrator
- Enterprise Administrator (read only)
- Department Administrator
- Department Administrator (read only)
- Account Owner

Each role has a varying degree of user limits and permissions. For more information, see [Organization structure and permissions by role](../cost-management-billing/manage/understand-ea-roles.md#organization-structure-and-permissions-by-role).

## Access your EA billing account

Billing administration on the Azure Government portal happens in the context of a billing account scope (or enrollment scope). To access your EA billing account, use the following steps:

1. Sign in to the [Azure Government Portal](https://portal.azure.us/)
1. Search for **Cost Management + Billing**  and select it.  
      :::image type="content" source="./media/documentation-government-how-to-access-enterprise-agreement-billing-account-03.png" alt-text="Screenshot showing search for Cost Management + Billing." lightbox="./media/documentation-government-how-to-access-enterprise-agreement-billing-account-03.png" :::
1. If you have access to more than one billing account, select **Billing scopes** from the navigation menu. Then, select the billing account that you want to work with.  
    :::image type="content" source="./media/documentation-government-how-to-access-enterprise-agreement-billing-account-04.png" alt-text="Screenshot showing Billing scopes." lightbox="./media/documentation-government-how-to-access-enterprise-agreement-billing-account-04.png" :::

## Next steps

Once you have access to your enrollment on the Azure Government portal, refer to the following articles.

- For more information about managing your enrollment, creating a department or subscription, adding administrators and account owners, and other administrative tasks, see [Azure EA billing administration](../cost-management-billing/manage/direct-ea-administration.md).
- To view a usage summary, price sheet, and download reports, see [Review usage charges](../cost-management-billing/manage/direct-ea-azure-usage-charges-invoices.md#review-usage-charges).
- To learn more about EA billing roles, read [Understand Azure Enterprise Agreement administrative roles in Azure](../cost-management-billing/manage/understand-ea-roles.md)
- For information on which REST APIs to use with your Azure enterprise enrollment and an explanation for how to resolve common issues with REST APIs, see [Azure Enterprise REST APIs](../cost-management-billing/manage/enterprise-rest-apis.md).