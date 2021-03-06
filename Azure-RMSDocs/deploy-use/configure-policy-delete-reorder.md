---
# required metadata

title: Delete or reorder an Azure Information Protection label
description: You can delete or re-order the labels that users see on the Information Protection bar by configuring this in the Azure Information Protection policy.
author: cabailey
ms.author: cabailey
manager: mbaldwin
ms.date: 09/26/2017
ms.topic: article
ms.prod:
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: ae0f603f-a632-4ac5-a3f7-6358d4255eff

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: eymanor
#ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# How to delete or reorder a label for Azure Information Protection

>*Applies to: Azure Information Protection*

You can delete or re-order the labels that users see on the Information Protection bar by selecting these actions in the Azure Information Protection policy.

![Delete or reorder labels in the Azure Information Protection policy](../media/info-protect-contextmenu.png)

When you delete a label that has been applied to documents and emails, and then publish the Azure Information Protection policy, that label will be automatically removed from these documents or emails when they are next opened by the Azure Information Protection client.

However, if the label applied protection, that protection is not removed. The protection settings from the label remain and display in the **Protection templates**. This template can now be converted to a new label or linked to a label. While this template remains, you cannot create a new label with the same name as the label that you deleted. If you want to do that, you have the following options:

- Convert the template to a label. 
    
    This action is recommended because if required, you can then change the name of the template and modify the protection settings.

- Use PowerShell to rename the template or delete it.
    
    Before you do these action, consider whether other admins or services are using the template and identify it by its current name. Delete a template only if you don't need to open documents or emails that were protected by the template.

For more information about managing protection templates, see [Configuring and managing templates for Azure Information Protection](configure-policy-templates.md).

Before you delete a label, consider whether to disable it, instead. When you disable a label that has been applied to documents and emails, the applied label will not be removed from these documents and emails but it no longer displays as a label that users can select on the Information Protection bar. Disabling a label also lets you keep the original configuration for when you might want users to select the label at a later time, when you simply re-enable it.

Order the labels so that users see them in a logical progression in the Information Protection bar. For example, order the labels in increasing sensitivity so that users see the least sensitive label first and the most sensitive label last. The [default policy](configure-policy-default.md) uses this configuration and reflects the increasing sensitivity in the label names.

> [!IMPORTANT]
>If you configure [conditions](configure-policy-classification.md) for your labels that might apply to more than one label, you must order the labels from least sensitive to most sensitive. This ordering ensures that the most sensitive label is applied when the conditions are evaluated.


Use the following instructions to make these changes.

1. If you haven't already done so, open a new browser window and sign in to the [Azure portal](https://portal.azure.com) as a security admin or global admin. Then navigate to the **Azure Information Protection** blade. 
    
    For example, on the hub menu, click **More services** and start typing **Information** in the Filter box. Select **Azure Information Protection**.

2. If the label that you want to configure will apply to all users, stay on the **Azure Information Protection - Global policy** blade.
    
    If the label that you want to configure is in a [scoped policy](configure-policy-scope.md) so that it applies to selected users only, from the **POLICIES** menu selection, select **Scoped policies**. Then select your scoped policy from the **Azure Information Protection - Scoped polices** blade.

3. From the **Azure Information Protection - Global policy** blade, or the **Policy:\<name>** blade, do one or more of the following actions. 

    - To delete a label: Right-click or select the context menu (**...**) for the label that you want to delete, click **Delete this label**, and click **Yes** to confirm. Then click **Save**. 

    - To disable a label: Select the label that you want to disable. On the **Label** blade, for **Enabled**, click **Off**, and then click **Save**.

    - To re-order a label: Right-click or select the context menu (**...**) for the label that you want to re-order, click **Move up** or **Move down** until the label is in the order that you want. Then click **Save**. 

4. To make your changes available to users, on the **Azure Information Protection** blade, click **Publish**.

## Next steps

For more information about configuring your Azure Information Protection policy, use the links in the [Configuring your organization's policy](configure-policy.md#configuring-your-organizations-policy) section.  

[!INCLUDE[Commenting house rules](../includes/houserules.md)]

