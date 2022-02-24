---
title: Fastlægge projektets omkostnings- og omsætningsestimater
description: Sådan fastlægger du projektets omkostnings- og omsætningsestimater i Project Service
author: ruhercul
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a91e988632d2b2cdebfe7fd17516c5d6886728fc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148816"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Fastlægge projektets omkostnings- og omsætningsestimater 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projektestimater giver en økonomisk visning af det arbejde, der er estimeret og planlagt i projektets arbejdsopgavehierarki. Visningen med estimater viser virkningen af omkostninger og indtægter på det planlagte arbejde. Visningen med estimater fungerer som et værktøj til at få vist oplysninger om et antal foruddefinerede dimensioner, der bedst muligt skal informere dig om den økonomiske indvirkning på projektet.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Omkostninger og salgsværdi af projektet  
Prislister for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] definerer omkostnings- og faktureringssatser for roller, som bruges i projektet. Baseret på de roller, der er knyttet til opgaverne i projektets arbejdsopgavehierarki, kan du angive indvirkningen af omkostninger og indtægter på det arbejde, der er involveret.  
  
## <a name="cost-price-defaulting"></a>Kostprisstandard  
Alle projekter hører til en organisation (angivet i **Enhed, der ejer** i projektet). Prislisten tilknyttet den ejende afdeling bestemmer kostpris pr. enhed. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] bestemmer kostpriser for roller ved at søge efter kombinationen af roller, enhed og afdeling på kostprislisten for at få den korrekte kostpris til ikrafttrædelsesdatoen på estimatlinjer.  
  
Hvis kombinationen af rolle, enhed og afdeling ikke resulterer ikke i en kostpris fra den ejende enhed prisliste, tilsidesættes enheden til fordel for kombinationen af rolle og afdeling. Hvis der er en kostpris, konverteres prisen til enheden, du har valgt på estimatlinjen.  
  
Hvis en kombination af rolle og afdeling ikke resulterer i en kostpris, tilsidesættes afdelingen til fordel for kombinationen af rolle og enhed, og prisen angives som standard efter anvendelse af en konvertering, hvis det er nødvendigt.  
  
 Hvis der ikke er en pris for rollen, bliver kostprisen som standard 0,00 på estimatlinjen.  
  
 Alle kostbeløb på projektets linjer med omkostningsestimater er i samme valuta som den ejende afdeling.  
  
## <a name="sales-price-defaulting"></a>Salgsprisstandard  
Salgsprislisten er baseret på det salgsobjekt, projektet er tilknyttet. Den salgsprisliste, der er tilknyttet tilbuddet eller kontrakten, bestemmer salgspris pr. enhed. Hvis der er en brugerdefineret prisliste til tilbuddet eller kontrakten, vil denne være standardsalgsprislisten for projektestimater. Hvis der ikke er nogen tilknytning til salgsobjekter, vil den standardsalgsprisliste, der er konfigureret i parameterindstillingerne, være standardsalgsprislisten for projektet. Hver estimatlinje har en ressourceafdeling, der er tilknyttet for at angive den afdeling, hvorfra der bestilles ressourcer til at udføre opgaven. Salgsprisen for de tilknyttede roller bestemmes ved at søge efter kombinationen af rolle, enhed og ressourceafdeling på salgsprislisten for at få den korrekte salgspris til ikrafttrædelsesdatoen på estimatlinjer.  
  
Hvis kombinationen af rolle, enhed og ressourceafdeling ikke resulterer i en salgspris på salgsprislisten, ser systemet bort fra enheden og søger efter kombinationen af rolle og ressourceafdeling. Hvis der findes en salgspris, konverteres denne til den enhed, du har valgt på salgsestimatlinjen.  
  
Hvis systemet ikke finder en pris for rollen, skal salgsprisen som standard være 0,00 på estimatlinjen.  
  
Estimatvisningen har en gittervisning, der viser et fladt gitter af estimatlinjer med enhedspris og samlet kost- og salgspris.  
  
## <a name="time-phased-view-of-project-estimates"></a>Visning med tidsfaser af projektestimater  
I visningen med tidsfaser for projektestimater er estimatdataene fra gittervisningen som standard pivoteret efter rolle og viser en spredning af estimatdata hen over tidslinjen i den valgte tidsskala.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Fordeling af indsatsestimat baseret på opgavetilstand  
I visningen med tidsfaser er den samlede estimerede indsats for opgaven distribueret ved at fordele et bestemt antal indsatstimer pr. enhedstidsperiode for den valgte tidsskala. I Project Service bestemmer opgavetilstanden, hvordan indsatsen fordeles hen over opgavens varighed. De to former for fordeling er ligelig fordeling og arbejdstidsbaseret fordeling. 
  
## <a name="work-hours-based-allocation"></a>Arbejdstidsbaseret fordeling  
Opgavetilstanden til automatisk planlægning for en opgave bestemmer, at for antallet af ressourcer, der er beregnet for opgaven, er de beregnet til at blive udnyttet alle arbejdstimer pr. dag. Dette gælder også ved fordeling af indsats ved at opdele den hen over varigheden af opgaver i visningen med tidsfaser. For tidsskalaen en "Dag" for en opgave, der er estimeret til at blive udført af én ressource, vil den indsats, der er allokeret pr. dag, f.eks. ikke overstige arbejdstimer pr. dag defineret i projektets kalender. Indsatsfordelingen sikrer derfor altid, at ressourcerne estimeres til at blive udnyttet hele dagen.  
  
## <a name="even-distribution"></a>Ligelig distribution  
Opgavetilstanden til manuelt planlagte opgaver imødekommer ikke arbejdstimer, projektkalender eller antal ressourcer, der er defineret for opgaven. Opgaveplanlægningen er baseret på input fra brugeren. For sådanne opgaver har indsatsfordelingen pr. tidsenhedsperiode i den valgte tidsskala ikke nogen begrænsende faktorer. Den samlede indsats på opgaven er ligeledes opdelt og fordelt for hver enhedstidsperiode på den valgte tidsskala.  
  
På denne måde bestemmer tilstanden opgave, der er defineret for opgaven, indsatsdistributionen eller allokeringen pr. enhedstidsperiode i tidsfaseinddelte estimater.  
  
## <a name="grouping-and-time-phasing-options"></a>Indstillinger for gruppering og tidsfaser  
Denne visning giver dig indsigt i fordelingen af indsats, omkostninger og salgsestimater på en pr. dag, uge, måned eller år. Indstillingen Gruppér efter kan pivotere estimatdataene på to dimensioner: kategori og ressource. Du kan vælge de felter, der skal vises i både gittervisning og visning med tidsfaser. Totaler for hver af tidsblokkene vises nederst med angivelse af samlet, anslået indsats, omkostninger og salg for dagen, ugen, måneden eller året.  
  
Standarden for kostpris og salgspris er ikrafttrædelsesdatoen. Når satserne for rollerne ændres, bliver det mere synligt i visningen med tidsfaser i forbindelse med visningen af estimatdata, der er pivoterede omkring "Ressource" og opdelt i tidsfaser på ugebasis.  
  
## <a name="expense-estimates"></a>Udgiftsestimater  
Enhver udgift, der skal afholdes i projektet, og som ikke er direkte relateret til arbejdskraft, der skal bruges, kan registreres i projektestimater i gittervisning. Du kan opnå dette ved hjælp af indstillingen **Tilføj udgiftsestimat** i gittervisningen. Udgiftsestimaterne for en bestemt opgave eller for hele projektet kan registreres. Du kan vælge udgiftskategorier på disse linjer og vælge en foreløbig dato for, hvor udgiften forventes at blive afholdt. Hvis de tilknyttede omkostnings- og salgsprislinjer har standardpriser eller markeringsprocentsatser defineret for udgiftskategorier, vil det være standardangivet på estimatlinjen ved tilknytning.  
  
### <a name="see-also"></a>Se også  
 [Vejledning til projektledere](../psa/project-manager-guide.md)
