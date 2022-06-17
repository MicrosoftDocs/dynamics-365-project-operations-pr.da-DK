---
title: Tilføje nye brugerdefinerede objektformularer (Project Service Automation 2.x)
description: Denne artikel indeholder oplysninger om, hvordan du kan tilføje brugerdefinerede objektformularer for salgsmuligheder, tilbud, ordrer eller fakturaer i Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: b7e5cbefd9d9705e0bafcb2551e1ce56457a187e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922721"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Tilføje nye brugerdefinerede objektformularer (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Feltet Type 

Dynamics 365 Project Service Automation bruger feltet **Type** (**msdyn\_ordertype**) i objekterne Salgsmulighed, Tilbud, Ordre og Faktura til at skelne mellem **arbejdsbaserede** versioner af disse objekter og **varebaserede** og **servicebaserede** versioner. Arbejdsbaserede versioner af disse objekter håndteres af PSA. masser af forretningslogik på klientsiden og serversiden af løsningen afhænger af feltet **Type**. Det er derfor vigtigt, at feltet initialiseres med en korrekt værdi, når objekterne oprettes. En forkert værdi kan medføre forkerte funktionsmåder, og nogen forretningslogik kører muligvis ikke korrekt.

## <a name="automatic-form-switching"></a>Automatisk skift af formularer

For at undgå potentielle beskadigelser af data og uventede funktionsmåder, der skyldes forkert initialisering og redigering af salgsobjektposterne, inkluderer PSA nu logik til automatisk skift af formularer i standardformularer. Denne logik fører brugerne til den korrekte formular for arbejde med den arbejdsbaserede version eller en anden type salgsmuligheds-, tilbuds-, ordre- eller fakturaobjekt. Når en bruger åbner den arbejdsbaserede version af et salgsmuligheds-, tilbuds-, ordre- eller fakturaobjekt, skifter formularen til **Projektoplysninger**.

Den automatiske formularskiftningslogik benytter tilknytningen mellem **formId**-værdien og feltet **msdyn\_ordertype**. Alle indbyggede formularer er føjet til den pågældende tilknytning. Men brugerdefinerede formularer skal tilføjes manuelt for at angive, hvilken version af objektet de skal håndtere. Dette er baseret på feltet **msdyn\_ordertype**. Hvis formularskiftet mangler i tilknytningen, skifter logikken til den indbyggede formular baseret på den værdi, der er gemt i feltet **msdyn\_ordertype** for objektet.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Tilføje brugerdefinerede formularer og aktivere logikken for formularskift

I følgende eksempel kan du se, hvordan du kan tilføje en brugerdefineret formular, **Mine projektoplysninger**, så de fungerer som arbejdsbaserede salgsmuligheder. Den samme proces bruges til at tilføje brugerdefinerede formularer, så de kan arbejde med tilbud, ordrer og fakturaer.

Benyt følgende fremgangsmåde for at oprette en brugerdefineret version af formularen **Projektoplysninger**.

1. Åbn formularen **Projektoplysninger** i objektet Salgsmulighed, og gem en kopi under navnet **Mine projektoplysninger**.
2. Åbn den nye formular, og kontrollér derefter, at scripts til formularinitialisering fra formularen **Projektoplysninger** findes i egenskaberne. 

    > [!IMPORTANT]
    > Du må ikke fjerne scripts. I modsat fald kan nogle data blive initialiseret forkert.

3. Kontrollér, at feltet **Type** (**msdyn\_ordertype**) findes i formularen. 

    > [!IMPORTANT]
    > Du må ikke fjerne dette felt. Hvis du gør det, kan initialiseringsscripts ikke udføres.

4. Find **formId**-værdien for den nye formular. Det kan du gøre på to forskellige måder:

    - Eksportér formularen **Mine projektoplysninger** som en del af en ikke-administreret løsning, og slå derefter værdien af **formId** op i filen customization.xml for den eksporterede løsning.
    - Åbn formularen **Mine projektoplysninger** i formulareditoren, og søg derefter efter GUID (Globally Unique Identifier) ud for parameteren **fromId** i URL-adressen, som vist i følgende illustration.

    ![Værdien af formId for den nye formular i URL-adressen..](media/how-to-add-custom-forms-in-v2.0.png)

5. Opret en **msdyn\_ordertype**-tilknytning for værdien **formId** ved at redigere webressourcen msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Fjern koden fra ressourcen, og erstat den med følgende kode.

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

6. Gem og publicer derefter tilpasningerne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
