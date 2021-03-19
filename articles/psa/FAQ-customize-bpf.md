---
title: Hvordan kan jeg tilpasse forretningsprocesforløbet Projektfaser?
description: En oversigt over, hvordan jeg kan tilpasse forretningsprocesforløbet Projektfaser.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f95677c56b745bf7900ad503596c93f1e722281
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286151"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="e5902-103">Hvordan kan jeg tilpasse forretningsprocesforløbet Projektfaser?</span><span class="sxs-lookup"><span data-stu-id="e5902-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="e5902-104">Der er et kendt begrænsning i tidligere versioner af programmet Project Service – navnene på faserne i forretningsprocesforløbet Projektfaser skal nøjagtigt stemme overens med de forventede engelske navne (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="e5902-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="e5902-105">I modsat fald fungerer forretningslogikken, der er afhængig af de engelske fasenavne, ikke korrekt.</span><span class="sxs-lookup"><span data-stu-id="e5902-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="e5902-106">Det er derfor, at velkendte handlinger, f.eks. **Skift process** eller **Rediger proces**, ikke ser ud til at være tilgængelige i projektformularen, og tilpasning af forretningsprocesforløbet tilrådes ikke.</span><span class="sxs-lookup"><span data-stu-id="e5902-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="e5902-107">Denne begrænsning er blevet ændret i version 2.4.5.48 og nyere versioner.</span><span class="sxs-lookup"><span data-stu-id="e5902-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="e5902-108">Denne artikel indeholder foreslåede løsninger, hvis du har brug for at tilpasse standardforretningsprocesforløbet til tidligere versioner.</span><span class="sxs-lookup"><span data-stu-id="e5902-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="e5902-109">Forretningslogik kræver fuld overensstemmelse med engelske fasenavne</span><span class="sxs-lookup"><span data-stu-id="e5902-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="e5902-110">Forretningsprocesforløbet Projektfaser indeholder forretningslogik, der understøtter følgende funktionsmåder i appen:</span><span class="sxs-lookup"><span data-stu-id="e5902-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="e5902-111">Når projektet knyttes til et tilbud, indstiller koden forretningsprocesforløbet til fasen **Quote**.</span><span class="sxs-lookup"><span data-stu-id="e5902-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="e5902-112">Når projektet knyttes til en kontrakt, indstiller koden forretningsprocesforløbet til fasen **Plan**.</span><span class="sxs-lookup"><span data-stu-id="e5902-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="e5902-113">Når forretningsprocessen er rykket frem til fasen **Close**, deaktiveres projektposten.</span><span class="sxs-lookup"><span data-stu-id="e5902-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="e5902-114">Når projektet er deaktiveret, indstilles projektformularen og arbejdsopgavehierarkiet (WBS) til skrivebeskyttet, de navngivne ressourcereservationer udgives, og eventuelle tilknyttede prislister deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="e5902-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="e5902-115">Denne forretningslogik er baseret på de engelske navne for projektfaserne.</span><span class="sxs-lookup"><span data-stu-id="e5902-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="e5902-116">Denne afhængighed af engelske fasenavne er den vigtigste årsag til, at vi ikke tilråder tilpasning af forretningsprocesforløbet Projektfaser, og til, at du ikke kan se de almindelige handlinger i forretningsprocesforløbet f.eks. **Skift proces** eller **Rediger proces** i projektobjektet.</span><span class="sxs-lookup"><span data-stu-id="e5902-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="e5902-117">Hvad sker der, hvis fasenavnene ikke stemmer overens med de engelske navne?</span><span class="sxs-lookup"><span data-stu-id="e5902-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="e5902-118">I Project Service-appen version 1.x på 8.2-platformen, når fasenavnene i forretningsprocesforløbet ikke stemmer nøjagtigt overens med de engelske fasenavne, ignoreres den forretningslogik, der angiver den relevante fase for tilbud eller kontrakter, eller som lukker projektet.</span><span class="sxs-lookup"><span data-stu-id="e5902-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="e5902-119">Der vises ingen fejlmeddelelser.</span><span class="sxs-lookup"><span data-stu-id="e5902-119">No error messages are displayed.</span></span> <span data-ttu-id="e5902-120">Derfor ser det ud, som om du kan tilpasse forretningsprocesforløbet Projektfaser.</span><span class="sxs-lookup"><span data-stu-id="e5902-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="e5902-121">Du kan imidlertid ikke se nogen af de automatiske processer, der bruges til tilbud, kontrakter og lukning af projekter.</span><span class="sxs-lookup"><span data-stu-id="e5902-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="e5902-122">I Project Service-appen version 2.4.4.30 eller tidligere på 9.0 platformen opstod der en betydelig arkitektonisk ændring af forretningsprocesser, som krævede omarbejdelse af forretningslogikken for forretningsprocesforløbet.</span><span class="sxs-lookup"><span data-stu-id="e5902-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="e5902-123">Det betyder, hvis procesfasenavnene ikke stemmer overens med de forventede engelske navne, modtager du en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="e5902-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="e5902-124">Derfor, hvis du vil tilpasse forretningsprocesforløbet Projektfaser for projektobjektet, kan du kun tilføje helt nye faser i standardforretningsprocesforløbet for projektobjektet, mens du bevarer **Quote**, **Plan** og **Close**-faserne, som de er.</span><span class="sxs-lookup"><span data-stu-id="e5902-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="e5902-125">Denne begrænsning sikrer, at du ikke får fejlmeddelelser fra den forretningslogik, der forventer de engelske fasenavne i forretningsprocesforløbet.</span><span class="sxs-lookup"><span data-stu-id="e5902-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="e5902-126">I version 2.4.5.48 eller nyere versioner fjernes den forretningslogik, der er beskrevet i denne artikel, fra standardforretningsprocesforløbet for projektobjektet.</span><span class="sxs-lookup"><span data-stu-id="e5902-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="e5902-127">Hvis du opgraderer til den pågældende version eller nyere, kan du tilpasse eller erstatte standardforretningsprocesforløbet med et af dine egne forløb.</span><span class="sxs-lookup"><span data-stu-id="e5902-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="e5902-128">Løsninger til tidligere versioner</span><span class="sxs-lookup"><span data-stu-id="e5902-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="e5902-129">Hvis du ikke vil opgradere, kan du tilpasse forretningsprocesforløbet Projektfaser for projektobjektet på en af følgende to måder:</span><span class="sxs-lookup"><span data-stu-id="e5902-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="e5902-130">Føj flere faser til standardkonfigurationen, samtidig med at du bevarer de engelske fasenavne for **Quote**, **Plan** og **Close**.</span><span class="sxs-lookup"><span data-stu-id="e5902-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Skærmbillede af tilføjelse af faser til standardkonfiguration](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="e5902-132">Opret dit eget forretningsprocesforløb, og gør det til det primære forretningsprocesforløb for projektobjektet, hvor du kan bruge de ønskede fasenavne.</span><span class="sxs-lookup"><span data-stu-id="e5902-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="e5902-133">Men hvis du vil bruge de samme standardprojektfaser **Quote**, **Plan** og **Close**, skal du udføre nogle tilpasninger, der er baseret på dine brugerdefinerede fasenavne.</span><span class="sxs-lookup"><span data-stu-id="e5902-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="e5902-134">Den mere komplekse logik er i den afsluttende del af projektet, som du kan stadig udløse ved blot at deaktivere projektposten.</span><span class="sxs-lookup"><span data-stu-id="e5902-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF-tilpasning](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="e5902-136">Yderligere info om appen Project Service version 2.4.4.30 eller tidligere på platform 9.0</span><span class="sxs-lookup"><span data-stu-id="e5902-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="e5902-137">I Project Service 2.4.4.30 eller ældre på platform 9.0, med et brugerdefineret forretningsprocesforløb opdateres feltet **Fasenavn** i det projektobjekt, der bruges i diagrammet **Projekt efter fase** og projektets listevisninger, ikke, fordi det er kombineret med standardforretningsprocesforløbet Projektfaser.</span><span class="sxs-lookup"><span data-stu-id="e5902-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="e5902-138">Du kan løse dette problem ved at udføre følgende trin:</span><span class="sxs-lookup"><span data-stu-id="e5902-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="e5902-139">Tilføj et brugerdefineret felt for at få adgang til den aktuelle fase i forretningsprocesforløbet, som opdateres, efterhånden som brugeren går frem i det brugerdefinerede forretningsprocesforløb.</span><span class="sxs-lookup"><span data-stu-id="e5902-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="e5902-140">Rediger diagrammet **Projekt efter fase**, så du kan arbejde med det brugerdefinerede felt i stedet for standardkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e5902-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="e5902-141">Trin til at oprette dit eget forretningsprocesforløb for projektobjektet</span><span class="sxs-lookup"><span data-stu-id="e5902-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="e5902-142">Du kan oprette dit eget forretningsprocesforløb for projektobjektet ved at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="e5902-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="e5902-143">Gå til **Indstillinger** > **Procescenter**.</span><span class="sxs-lookup"><span data-stu-id="e5902-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="e5902-144">Undlad at kopiere forretningsprocesforløbet Projektfaser, fordi det også kopierer virksomhedslogikken i Project Service.</span><span class="sxs-lookup"><span data-stu-id="e5902-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Opret proces](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="e5902-146">Brug procesdesigneren til at oprette de ønskede fasenavne.</span><span class="sxs-lookup"><span data-stu-id="e5902-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="e5902-147">Hvis du vil bruge de samme funktioner som til standardfaserne for **Quote**, **Plan** og **Close**, skal du oprette dem baseret på fasenavnene i dit brugerdefinerede forretningsprocesforløb.</span><span class="sxs-lookup"><span data-stu-id="e5902-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Skærmbillede af procesdesigner, der bruges til at tilpasse BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="e5902-149">I procesdesigneren skal du klikke på **Ordreprocesforløb** for at gøre forretningsprocesforløbet til det primære forretningsprocesforløb for projektobjektet ved at flytte det op øverst på listen over forretningsprocesforløbet Projektfaser.</span><span class="sxs-lookup"><span data-stu-id="e5902-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="e5902-150">Skærmbillede af Ordreprocesforløb</span><span class="sxs-lookup"><span data-stu-id="e5902-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="e5902-151">Følgende trin gælder for Project Service-appen 2.4.4.30 eller tidligere på 9.0-platformen</span><span class="sxs-lookup"><span data-stu-id="e5902-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="e5902-152">Føj et nyt brugerdefineret felt til projektobjektet for at hente de brugerdefinerede faser i dit brugerdefinerede forretningsprocesforløb.</span><span class="sxs-lookup"><span data-stu-id="e5902-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="e5902-153">Du skal tilføje forretningslogik (plug-in/arbejdsproces) for at opdatere dette felt, når fasen i det brugerdefinerede forretningsprocesforløb opdateres.</span><span class="sxs-lookup"><span data-stu-id="e5902-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Skærmbillede af tilpasning af projektobjektet](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="e5902-155">Rediger diagrammet **Projekt efter fase** for at bruge det nye brugerdefinerede felt for faser.</span><span class="sxs-lookup"><span data-stu-id="e5902-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Skærmbillede af brug af diagrammet Projekt efter fase](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="e5902-157">Rediger visninger for projektobjekt, så de medtager det nye brugerdefinerede felt for faser.</span><span class="sxs-lookup"><span data-stu-id="e5902-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Skærmbillede af ændring af visninger i projektobjektet](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]