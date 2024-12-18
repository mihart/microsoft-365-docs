---
title: Configure Microsoft Syntex for pay-as-you-go billing
ms.author: chucked
author: chuckedmonson
ms.reviewer: kkamath
ms.date: 06/12/2024
manager: jtremper
audience: admin
ms.topic: conceptual
ms.service: microsoft-syntex
ms.collection: 
    - essentials-get-started
    - m365initiative-syntex
    - Tier1
search.appverid: MET150
ms.localizationpriority: medium
description: Learn about how to set up pay-as-you-go Azure billing for Microsoft Syntex and how to monitor your usage.
---

# Configure Microsoft Syntex for pay-as-you-go billing

Microsoft Syntex services are billed on a pay-as-you-go basis. These services use an Azure subscription for billing and track usage and cost with a Syntex meter. Read the [Microsoft Syntex pay-as-you-go terms of service](/legal/microsoft-365/microsoft-syntex-pay-as-you-go-terms) before you configure pay-as-you-go.

For a list of Microsoft Syntex services that use pay-as-you-go, see [Licensing for Microsoft Syntex](syntex-licensing.md).

## Prerequisites

To use Microsoft Syntex pay-as-you go, you need:

- An Azure subscription in the same tenant as Microsoft Syntex
- An Azure resource group in that subscription

If you already have these resources for other purposes, you can also use them with Microsoft Syntex.

For information about how to create an Azure subscription, see [Create your initial Azure subscriptions](/azure/cloud-adoption-framework/ready/azure-best-practices/initial-subscriptions).

For information about how to create an Azure resource group, see [Manage Azure resource groups by using the Azure portal](/azure/azure-resource-manager/management/manage-resource-groups-portal).

## Connect Syntex to an Azure subscription for billing

When you set up Microsoft Syntex billing in Azure, events will be sent to the Azure meter in your account, and you'll be able to view the pages processed for unstructured and prebuilt document processing models.

The following permissions are required to set up Microsoft Syntex billing:

- You must be a [SharePoint Administrator](/entra/identity/role-based-access-control/permissions-reference#sharepoint-administrator) or [Global Administrator](/entra/identity/role-based-access-control/permissions-reference#global-administrator) to be able to access the Microsoft 365 admin center and set up Syntex.

   [!INCLUDE [global-administrator-note](../includes/global-administrator-note.md)]

- You must have owner or contributor rights to the Azure subscription that you want to use for Microsoft Syntex billing.

To configure Microsoft Syntex billing, follow these steps:

1. In the Microsoft 365 admin center, select <a href="https://go.microsoft.com/fwlink/p/?linkid=2171997" target="_blank">**Setup**</a>, and then view the **Files and content** section.

2. In the **Files and content** section, select **Automate content processes with Syntex**.

3. On the **Automate content processes with Syntex** page, select **Go to Syntex settings**.

4. On the **Microsoft Syntex** page, select **Manage pay-as-you-go billing** to walk through the setup process.

5. On the **Manage billing** panel, follow the steps to set up your Azure subscription, resource group, and region. (The region determines where your tenant ID and usage information such as site names will be stored.)

6. Read and accept the [Microsoft Syntex pay-as-you-go terms of service](/legal/microsoft-365/microsoft-syntex-pay-as-you-go-terms).

7. Select **Save**.

If you need to change or disconnect your Azure subscription, you can do so from the  **Manage pay-as-you-go billing** panel.

## Monitor your Microsoft Syntex pay-as-you-go usage

You can monitor your Microsoft Syntex pay-as-you-go usage in Microsoft Cost Management for Azure. You must have at least *read* access to the resource group that you specified for Microsoft Syntex. Note that usage information might take up to 24 hours to appear in Cost Management.

To see the charges applied to the Syntex meters, follow these steps:

1. Sign in to [Microsoft Cost Management for Azure](https://portal.azure.com/#view/Microsoft_Azure_CostManagement/Menu/~/overview).

2. Under **Cost Management**, select **Cost analysis**.

3. Select **Add filter**, choose **Product** from the list, and then choose the product (listed below) that you want to filter on.

4. Select **Add filter**, choose **Tag** from the list, and then choose the tag (listed below) that you want to filter on.

The following Microsoft Syntex products are currently available:

- Prebuilt document processing
- Structured and freeform document processing
- Unstructured document processing
- Autofill columns
- Content assembly
- Image tagging
- Taxonomy tagging
- Document translation
- Syntex eSignature
- Optical character recognition
- Microsoft 365 Archive
- Microsoft 365 Backup

The following tags are available:
- Site

For more information about filter options in Cost Management, see [Group and filter options in Cost analysis](/azure/cost-management-billing/costs/group-filter).

## Related articles

[Overview of Microsoft Syntex](syntex-overview.md)

[Licensing for Microsoft Syntex](syntex-licensing.md)
