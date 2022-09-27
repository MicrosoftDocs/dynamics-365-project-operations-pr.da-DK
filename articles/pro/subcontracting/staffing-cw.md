---
title: Bemanding af et projekt med kontraktmedarbejdere og kapacitet, der er omfattet af en underentreprise
description: I denne artikel forklares det, hvordan projektkrav kan bemandes ved hjælp af kontraktmedarbejdere eller kapacitet, der er omfattet af en underentreprise, i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522428"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Bemanding af et projekt med kontraktmedarbejdere og kapacitet, der er omfattet af en underentreprise

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Generiske projektteammedlemmer kan bemandes med medarbejdere eller kontraktmedarbejdere. Når du bemander et projekt med kontraktmedarbejdere, kan du begrænse medarbejderindstillingerne til bestemte kontraktmedarbejdere, der er tildelt en underentrepriselinje. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Søg efter medarbejderressourcekrav med kontraktmedarbejdere, der tilhører en bestemt underentrepriselinje

For at søge efter og bemande med medarbejderressourcekrav med kontraktmedarbejdere, der tilhører en bestemt underentrepriselinje, skal du gøre følgende:

1. Oprette et generisk projektteammedlem, som henviser til en underleverandør og en underentrepriselinje.
2. Oprette et ressourcekrav for dette generiske projektteammedlem ved hjælp af knappen **Opret krav** i undergitteret for projektteammedlemmer.
3. Markér rækken for teammedlemmet, og vælg derefter knappen **Reserver** i undergitteret. 
4. Derved åbnes planlægningsoversigten med kravkonteksten. Sammen med andre attributter, f.eks. dato-, rolle- og organisationsenhedsfelter, udfyldes filtrene i planlægningsoversigt også automatisk med felterne leverandør, underleverandør og underentrepriselinje fra ressourcekravet.
5. Systemet søger efter ressourcer, der opfylder filterkriterierne, og angiver dem. 
6. Vælg en af de filtrerede ressourcer, og reservér ressourcen for kravet. 
7. Et projektteammedlem oprettes og opdateres med henvisninger til underleverandør og underentrepriselinje. Gå til **Projektestimater**, og vælg **Opdater priser** for at se de opdaterede omkostninger for ressourcetildelingen. 

> [!NOTE]
> Det er muligvis ikke altid muligt at opdatere projektteammedlemmerne med en henvisning til en underleverandør og underentrepriselinje under reservationen, hvis ressourcen er tildelt flere underentrepriselinjer. Hvis systemet ikke kan opdatere projektteammedlemmerne med en underleverandør og underentrepriselinje, skal du åbne projektteammedlemsposten og manuelt opdatere disse felter, så det økonomiske omkostningsestimat korrekt afspejler underleverandøromkostningerne.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Søg efter og bemand medarbejderressourcekrav med kontraktmedarbejdere

For at søge efter og bemande medarbejderressourcekrav med kontraktmedarbejdere skal du gøre følgende:

1. Oprette et generisk projektteammedlem.
2. Oprette et ressourcekrav for dette generiske projektteammedlem ved hjælp af knappen **Opret krav** i undergitteret for projektteammedlemmer.
3. Markér rækken for teammedlemmet, og vælg derefter knappen **Reserver** i undergitteret. 
4. Derved åbnes planlægningsoversigten med kravkonteksten. Sammen med andre attributter, f.eks. dato-, rolle- og organisationsenhedsfelter, udfyldes filtrene i planlægningsoversigt også automatisk med felterne leverandør, underleverandør og underentrepriselinje fra ressourcekravet. Da kravet ikke har nogen værdi for underleverandør eller underentrepriselinje, vil disse attributter være tomme i filterruden.
5. Systemet søger efter ressourcer, der opfylder filterkriterierne, og angiver dem.
6. Opdater feltet **Medarbejdertype** i filterruden til **Kontraktmedarbejder** for at begrænse søgningen til kontraktmedarbejdere. Opdater **Leverandør** i filterruden for at vælge en leverandør for at begrænse søgningen til kun at vise kontraktmedarbejdere, der tilhører en bestemt leverandørvirksomhed.
7. Vælg en kontraktmedarbejder på listen, og reservér ressourcen til kravet.
8. Et projektteammedlem er blevet oprettet. Medlemmer af projektteamet opdateres dog ikke med en underleverandør eller underentrepriselinje, og omkostningerne ved ressourcetildelingen beregnes derfor ikke ved hjælp af prisfastsættelsen for underleverandører. Opdater manuelt projektteammedlemmet med en underentrepriselinje og gå til **Projektestimater**, og vælg **Opdater priser** for at få vist de opdaterede omkostninger for ressourcetildelingen.

> [!NOTE]
> Medlemmer af projektteam, der har **Medarbejdertypen** **Kontraktmedarbejder**, men ikke har en underleverandørreference, markeres som **Ugyldige** i gitteret **Projektteammedlemmer**. Hvis der findes et projektteammedlem med denne status, skal du åbne projektteammedlemsposten og manuelt opdatere felterne for underleverandøren og underentrepriselinjen, så det økonomiske omkostningsestimat korrekt afspejler underleverandøromkostningerne på fanen **Estimater**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
