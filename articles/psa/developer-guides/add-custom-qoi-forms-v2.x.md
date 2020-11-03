---
title: Tilføje nye brugerdefinerede objektformularer (Project Service Automation 2.x)
description: Denne emne indeholder oplysninger om, hvordan du kan tilføje brugerdefinerede objektformularer for salgsmuligheder, tilbud, ordrer eller fakturaer i Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074366"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="a8801-103">Tilføje nye brugerdefinerede objektformularer (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="a8801-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="a8801-104">Feltet Type</span><span class="sxs-lookup"><span data-stu-id="a8801-104">Type field</span></span> 

<span data-ttu-id="a8801-105">Dynamics 365 Project Service Automation bruger feltet **Type** ( **msdyn\_ordertype** ) i objekterne Salgsmulighed, Tilbud, Ordre og Faktura til at skelne mellem **arbejdsbaserede** versioner af disse objekter og **varebaserede** og **servicebaserede** versioner.</span><span class="sxs-lookup"><span data-stu-id="a8801-105">Dynamics 365 Project Service Automation relies on the **Type** ( **msdyn\_ordertype** ) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="a8801-106">Arbejdsbaserede versioner af disse objekter håndteres af PSA.</span><span class="sxs-lookup"><span data-stu-id="a8801-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="a8801-107">masser af forretningslogik på klientsiden og serversiden af løsningen afhænger af feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="a8801-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="a8801-108">Det er derfor vigtigt, at feltet initialiseres med en korrekt værdi, når objekterne oprettes.</span><span class="sxs-lookup"><span data-stu-id="a8801-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="a8801-109">En forkert værdi kan medføre forkerte funktionsmåder, og nogen forretningslogik kører muligvis ikke korrekt.</span><span class="sxs-lookup"><span data-stu-id="a8801-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="a8801-110">Automatisk skift af formularer</span><span class="sxs-lookup"><span data-stu-id="a8801-110">Automatic form switching</span></span>

<span data-ttu-id="a8801-111">For at undgå potentielle beskadigelser af data og uventede funktionsmåder, der skyldes forkert initialisering og redigering af salgsobjektposterne, inkluderer PSA nu logik til automatisk skift af formularer i standardformularer.</span><span class="sxs-lookup"><span data-stu-id="a8801-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="a8801-112">Denne logik fører brugerne til den korrekte formular for arbejde med den arbejdsbaserede version eller en anden type salgsmuligheds-, tilbuds-, ordre- eller fakturaobjekt.</span><span class="sxs-lookup"><span data-stu-id="a8801-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="a8801-113">Når en bruger åbner den arbejdsbaserede version af et salgsmuligheds-, tilbuds-, ordre- eller fakturaobjekt, skifter formularen til **Projektoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="a8801-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="a8801-114">Den automatiske formularskiftningslogik benytter tilknytningen mellem **formId** -værdien og feltet **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="a8801-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="a8801-115">Alle indbyggede formularer er føjet til den pågældende tilknytning.</span><span class="sxs-lookup"><span data-stu-id="a8801-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="a8801-116">Men brugerdefinerede formularer skal tilføjes manuelt for at angive, hvilken version af objektet de skal håndtere.</span><span class="sxs-lookup"><span data-stu-id="a8801-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="a8801-117">Dette er baseret på feltet **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="a8801-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="a8801-118">Hvis formularskiftet mangler i tilknytningen, skifter logikken til den indbyggede formular baseret på den værdi, der er gemt i feltet **msdyn\_ordertype** for objektet.</span><span class="sxs-lookup"><span data-stu-id="a8801-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="a8801-119">Tilføje brugerdefinerede formularer og aktivere logikken for formularskift</span><span class="sxs-lookup"><span data-stu-id="a8801-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="a8801-120">I følgende eksempel kan du se, hvordan du kan tilføje en brugerdefineret formular, **Mine projektoplysninger** , så de fungerer som arbejdsbaserede salgsmuligheder.</span><span class="sxs-lookup"><span data-stu-id="a8801-120">The following example shows how to add a custom form, **My Project Information** , so that it works with work-based opportunities.</span></span> <span data-ttu-id="a8801-121">Den samme proces bruges til at tilføje brugerdefinerede formularer, så de kan arbejde med tilbud, ordrer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="a8801-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="a8801-122">Benyt følgende fremgangsmåde for at oprette en brugerdefineret version af formularen **Projektoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="a8801-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="a8801-123">Åbn formularen **Projektoplysninger** i objektet Salgsmulighed, og gem en kopi under navnet **Mine projektoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="a8801-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="a8801-124">Åbn den nye formular, og kontrollér derefter, at scripts til formularinitialisering fra formularen **Projektoplysninger** findes i egenskaberne.</span><span class="sxs-lookup"><span data-stu-id="a8801-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="a8801-125">Du må ikke fjerne scripts.</span><span class="sxs-lookup"><span data-stu-id="a8801-125">Don't remove the scripts.</span></span> <span data-ttu-id="a8801-126">I modsat fald kan nogle data blive initialiseret forkert.</span><span class="sxs-lookup"><span data-stu-id="a8801-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="a8801-127">Kontrollér, at feltet **Type** ( **msdyn\_ordertype** ) findes i formularen.</span><span class="sxs-lookup"><span data-stu-id="a8801-127">Verify that the **Type** ( **msdyn\_ordertype** ) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="a8801-128">Du må ikke fjerne dette felt.</span><span class="sxs-lookup"><span data-stu-id="a8801-128">Don't remove this field.</span></span> <span data-ttu-id="a8801-129">Hvis du gør det, kan initialiseringsscripts ikke udføres.</span><span class="sxs-lookup"><span data-stu-id="a8801-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="a8801-130">Find **formId** -værdien for den nye formular.</span><span class="sxs-lookup"><span data-stu-id="a8801-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="a8801-131">Det kan du gøre på to forskellige måder:</span><span class="sxs-lookup"><span data-stu-id="a8801-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="a8801-132">Eksportér formularen **Mine projektoplysninger** som en del af en ikke-administreret løsning, og slå derefter værdien af **formId** op i filen customization.xml for den eksporterede løsning.</span><span class="sxs-lookup"><span data-stu-id="a8801-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="a8801-133">Åbn formularen **Mine projektoplysninger** i formulareditoren, og søg derefter efter GUID (Globally Unique Identifier) ud for parameteren **fromId** i URL-adressen, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="a8801-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Værdien af formId for den nye formular i URL-adressen.](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="a8801-135">Opret en **msdyn\_ordertype** -tilknytning for værdien **formId** ved at redigere webressourcen msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="a8801-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="a8801-136">Fjern koden fra ressourcen, og erstat den med følgende kode.</span><span class="sxs-lookup"><span data-stu-id="a8801-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="a8801-137">Gem og publicer derefter tilpasningerne.</span><span class="sxs-lookup"><span data-stu-id="a8801-137">Save and then publish the customizations.</span></span>
