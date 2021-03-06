---
# required metadata

title: Quick start tutorial step 1 - AIP
description: Step 1 of an introduction tutorial to quickly try out Azure Information Protection - Activate the protection service.
author: cabailey
ms.author: cabailey
manager: mbaldwin
ms.date: 11/17/2017
ms.topic: article
ms.prod:
ms.service: information-protection
ms.technology: techgroup-identity
ms.assetid: f6dbb143-96f7-4a9c-8208-be9280d69de9

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
#ms.reviewer: eymanor
#ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Step 1: Activate protection
 
>*Applies to: Azure Information Protection*

> [!NOTE]
>Even if you have already activated the Azure Rights Management service for your tenant, complete this step to confirm the activation status. The instructions include signing in to the Azure portal and creating the Azure Information Protection blade, so that you are ready for step 2. 

When the Azure Rights Management service is activated, you can protect your organization's most sensitive documents and emails, and track how protected documents are used when you share them with others. There are different ways that you can activate protection, which include using Windows PowerShell, and using the admin portals.

For this tutorial, we'll use the Azure portal, which is where you also configure labels for users. 

## To activate the Azure Rights Management service

1. Sign in to the [Azure portal](https://portal.azure.com) as a global admin or security admin for your tenant.

2. On the hub menu, click **New**, and then, from the **MARKETPLACE** list, select **Security + Identity**. 
    
3.  On the **Security + Identify** blade, from the **FEATURED APPS** list, select **Azure Information Protection**. Then, on the **Azure Information Protection** blade, click **Create**.
    
    This action creates the **Azure Information Protection** blade so that the next time you sign in to the portal, you can select the service from the hub **More services** list. 
    
    > [!TIP] 
    > Select **Pin to dashboard** to create an **Azure Information Protection** tile on your dashboard, so that you can skip browsing to the service the next time you sign in to the portal.

4. Note the information on the **Quick start** page that automatically opens the first time you connect to the service. You can come back to this later. For this tutorial, select **Protection activation**. 

5. You now see whether the Azure Rights Management service is activated for your tenant. 
    
    - If the service is activated, you see the following confirmation:
        
        ![Azure Information Protection status for Azure RMS](../media/info-protect-azurerms-activated.png)
        
    - If the service is not activated, you see this reflected in the status information, and the option to activate:
        
        ![Azure Information Protection status for Azure RMS](../media/info-protect-azurerms-deactivated.png)

6. If the service isn't activated, select **Activate**. 

    When activation is complete, the information bar displays **Activation finished successfully**.

That's all you need to do for this first step to complete this tutorial. You're ready to go to step 2.

|If you want more information|Additional information|
|--------------------------------|--------------------------|
|About activating Rights Management|[Activating Azure Rights Management](../deploy-use/activate-service.md)|


>[!div class="step-by-step"]
[&#171; Introduction](infoprotect-quick-start-tutorial.md)
[Step 2 &#187;](infoprotect-tutorial-step2.md)

[!INCLUDE[Commenting house rules](../includes/houserules.md)]
