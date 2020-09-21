---
title: Hvordan kan jeg tilpasse forretningsprocesforløbet Projektfaser?
description: En oversigt over, hvordan jeg kan tilpasse forretningsprocesforløbet Projektfaser.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750500"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Hvordan kan jeg tilpasse forretningsprocesforløbet Projektfaser?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Der er et kendt begrænsning i tidligere versioner af programmet Project Service – navnene på faserne i forretningsprocesforløbet Projektfaser skal nøjagtigt stemme overens med de forventede engelske navne (**Quote**, **Plan**, **Close**). I modsat fald fungerer forretningslogikken, der er afhængig af de engelske fasenavne, ikke korrekt. Det er derfor, at velkendte handlinger, f.eks. **Skift process** eller **Rediger proces**, ikke ser ud til at være tilgængelige i projektformularen, og tilpasning af forretningsprocesforløbet tilrådes ikke. 

Denne begrænsning er blevet ændret i version 2.4.5.48 og nyere versioner. Denne artikel indeholder foreslåede løsninger, hvis du har brug for at tilpasse standardforretningsprocesforløbet til tidligere versioner.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Forretningslogik kræver fuld overensstemmelse med engelske fasenavne

Forretningsprocesforløbet Projektfaser indeholder forretningslogik, der understøtter følgende funktionsmåder i appen:
- Når projektet knyttes til et tilbud, indstiller koden forretningsprocesforløbet til fasen **Quote**.
- Når projektet knyttes til en kontrakt, indstiller koden forretningsprocesforløbet til fasen **Plan**.
- Når forretningsprocessen er rykket frem til fasen **Close**, deaktiveres projektposten. Når projektet er deaktiveret, indstilles projektformularen og arbejdsopgavehierarkiet (WBS) til skrivebeskyttet, de navngivne ressourcereservationer udgives, og eventuelle tilknyttede prislister deaktiveres.

Denne forretningslogik er baseret på de engelske navne for projektfaserne. Denne afhængighed af engelske fasenavne er den vigtigste årsag til, at vi ikke tilråder tilpasning af forretningsprocesforløbet Projektfaser, og til, at du ikke kan se de almindelige handlinger i forretningsprocesforløbet f.eks. **Skift proces** eller **Rediger proces** i projektobjektet.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Hvad sker der, hvis fasenavnene ikke stemmer overens med de engelske navne?

I Project Service-appen version 1.x på 8.2-platformen, når fasenavnene i forretningsprocesforløbet ikke stemmer nøjagtigt overens med de engelske fasenavne, ignoreres den forretningslogik, der angiver den relevante fase for tilbud eller kontrakter, eller som lukker projektet. Der vises ingen fejlmeddelelser. Derfor ser det ud, som om du kan tilpasse forretningsprocesforløbet Projektfaser. Du kan imidlertid ikke se nogen af de automatiske processer, der bruges til tilbud, kontrakter og lukning af projekter.

I Project Service-appen version 2.4.4.30 eller tidligere på 9.0 platformen opstod der en betydelig arkitektonisk ændring af forretningsprocesser, som krævede omarbejdelse af forretningslogikken for forretningsprocesforløbet. Det betyder, hvis procesfasenavnene ikke stemmer overens med de forventede engelske navne, modtager du en fejlmeddelelse. 

Derfor, hvis du vil tilpasse forretningsprocesforløbet Projektfaser for projektobjektet, kan du kun tilføje helt nye faser i standardforretningsprocesforløbet for projektobjektet, mens du bevarer **Quote**, **Plan** og **Close**-faserne, som de er. Denne begrænsning sikrer, at du ikke får fejlmeddelelser fra den forretningslogik, der forventer de engelske fasenavne i forretningsprocesforløbet.

I version 2.4.5.48 eller nyere versioner fjernes den forretningslogik, der er beskrevet i denne artikel, fra standardforretningsprocesforløbet for projektobjektet. Hvis du opgraderer til den pågældende version eller nyere, kan du tilpasse eller erstatte standardforretningsprocesforløbet med et af dine egne forløb. 

## <a name="workarounds-for-earlier-versions"></a>Løsninger til tidligere versioner

Hvis du ikke vil opgradere, kan du tilpasse forretningsprocesforløbet Projektfaser for projektobjektet på en af følgende to måder:

1. Føj flere faser til standardkonfigurationen, samtidig med at du bevarer de engelske fasenavne for **Quote**, **Plan** og **Close**.

   > [!div class="mx-imgBorder"] 
   > ![Skærmbillede af tilføjelse af faser til standardkonfiguration](media/FAQ-Customize-BPF-1.png)
 
2. Opret dit eget forretningsprocesforløb, og gør det til det primære forretningsprocesforløb for projektobjektet, hvor du kan bruge de ønskede fasenavne. Men hvis du vil bruge de samme standardprojektfaser **Quote**, **Plan** og **Close**, skal du udføre nogle tilpasninger, der er baseret på dine brugerdefinerede fasenavne. Den mere komplekse logik er i den afsluttende del af projektet, som du kan stadig udløse ved blot at deaktivere projektposten.

   > [!div class="mx-imgBorder"] 
   > ![Skærmbillede af BPF-tilpasning](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Yderligere info om appen Project Service version 2.4.4.30 eller tidligere på platform 9.0

I Project Service 2.4.4.30 eller ældre på platform 9.0, med et brugerdefineret forretningsprocesforløb opdateres feltet **Fasenavn** i det projektobjekt, der bruges i diagrammet **Projekt efter fase** og projektets listevisninger, ikke, fordi det er kombineret med standardforretningsprocesforløbet Projektfaser. Du kan løse dette problem ved at udføre følgende trin:

- Tilføj et brugerdefineret felt for at få adgang til den aktuelle fase i forretningsprocesforløbet, som opdateres, efterhånden som brugeren går frem i det brugerdefinerede forretningsprocesforløb.

- Rediger diagrammet **Projekt efter fase**, så du kan arbejde med det brugerdefinerede felt i stedet for standardkonfiguration.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Trin til at oprette dit eget forretningsprocesforløb for projektobjektet

Du kan oprette dit eget forretningsprocesforløb for projektobjektet ved at gøre følgende:

1. Gå til **Indstillinger** > **Procescenter**. Undlad at kopiere forretningsprocesforløbet Projektfaser, fordi det også kopierer virksomhedslogikken i Project Service.

   > [!div class="mx-imgBorder"] 
   > ![Skærmbillede af BPF-tilpasning](media/FAQ-Customize-BPF-3.png)

2. Brug procesdesigneren til at oprette de ønskede fasenavne. Hvis du vil bruge de samme funktioner som til standardfaserne for **Quote**, **Plan** og **Close**, skal du oprette dem baseret på fasenavnene i dit brugerdefinerede forretningsprocesforløb.

   > [!div class="mx-imgBorder"] 
   > ![Skærmbillede af procesdesigner, der bruges til at tilpasse BPF](media/FAQ-Customize-BPF-4.png) 

3. I procesdesigneren skal du klikke på **Ordreprocesforløb** for at gøre forretningsprocesforløbet til det primære forretningsprocesforløb for projektobjektet ved at flytte det op øverst på listen over forretningsprocesforløbet Projektfaser.

   > [!div class="mx-imgBorder"] 
   > ![Skærmbillede af Ordreprocesforløb](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Følgende trin gælder for Project Service-appen 2.4.4.30 eller tidligere på 9.0-platformen

4. Føj et nyt brugerdefineret felt til projektobjektet for at hente de brugerdefinerede faser i dit brugerdefinerede forretningsprocesforløb. Du skal tilføje forretningslogik (plug-in/arbejdsproces) for at opdatere dette felt, når fasen i det brugerdefinerede forretningsprocesforløb opdateres.

   > [!div class="mx-imgBorder"] 
   > ![Skærmbillede af tilpasning af projektobjektet](media/FAQ-Customize-BPF-6-720.png)

5. Rediger diagrammet **Projekt efter fase** for at bruge det nye brugerdefinerede felt for faser.

   > [!div class="mx-imgBorder"] 
   > ![Skærmbillede af brug af diagrammet Projekt efter fase](media/FAQ-Customize-BPF-7-720.png)

6. Rediger visninger for projektobjekt, så de medtager det nye brugerdefinerede felt for faser.

   > [!div class="mx-imgBorder"] 
   > ![Skærmbillede af ændring af visninger i projektobjektet](media/FAQ-Customize-BPF-8-720.png)

