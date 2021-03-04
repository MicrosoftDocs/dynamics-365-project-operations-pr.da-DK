---
title: Estimer projektsalg og -omkostninger, når en reserverbar ressource udfylder flere roller for et projekt
description: Dette emne indeholder oplysninger om, hvordan prisfastsættelsesdimensioner kan bruges til at understøtte prisfastsættelse og omkostningsfastsættelse for en ressource, der udfylder flere roller i et projekt.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 67e24156e960b9b09cf92f7f0cd77f6c74a982b8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145036"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a>Estimer projektsalg og -omkostninger, når en reserverbar ressource udfylder flere roller for et projekt 

[!include [banner](../includes/psa-now-project-operations.md)]

Projektbaserede virksomheder har ofte brug for, at en ressource varetager flere roller på et projekt. Hver af disse roller kan være have forskellige prisfastsættelser og omkostningsberegninger, hvilket betyder, at den samme ressources tid på projektet kan resultere i et andet økonomisk estimat, afhængigt af faktureringshyppighed og omkostningssatser for hver af rollerne. Project Service Automation gør det muligt at konfigurere værdierne på gruppemedlemmets posten for den navngivne ressource og for forskellige tilsidesættelser på hver af de opgaver, som teammedlemmet er tildelt til.

I følgende eksempel forklares det, hvordan en simpel tilsidesættelse af denne værdi gør det muligt for en ressource at have flere roller på et projekt med forskellige omkostninger og faktureringshyppighed.

## <a name="create-tasks"></a>Opret opgaver
Opret to projektopgaver på hver 40 timer, opgave A og opgave B. Vælg opgave A som forgænger for opgave B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Konfigurer Rolle og Afdeling for et generisk projektgruppemedlem

1. På siden **Planlægning** skal du for opgave A vælge rækken **Opgave**. 
2. Vælg feltet **Ressourcer**, og vælg **Opret** i rullelisten.
3. På siden **Hurtig oprettelse af teammedlem** skal du angive attributterne for det generiske teammedlem, der kan udføre denne opgave.
4. Vælg den relevante rolle og afdeling, og vælg derefter **Gem og luk**. Der oprettes et generisk gruppemedlem, og medlemmet tildeles til denne opgave. 

Gentag disse trin for opgave B, og kontrollér, at rollen og organisationsenheden for det generiske gruppemedlem, der er oprettet for opgave B, ikke er de samme som for opgave A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Konfigurer rolle og afdeling for en projektopgave

1. Når du har oprettet opgave A, skal du markere opgaven og derefter vælge **Rediger opgave**.
2. På siden **Opgavedetaljer** skal du finde felterne **Rolle** og **Afdeling** og tilføje de værdier, der kræves af en ressource, som skal udføre denne opgave. 

  > [!NOTE]
  > Hvis du fuldfører disse scenarier ved hjælp af demonstrationsdata for Project Service Automation, skal du vælge **Konsulterende kundeemne** for rollen, og **Fabrikam US** som afdeling.

3. Vælg opgave B, og vælg derefter **Rediger opgave**.
4. På siden **Opgavedetaljer** skal du finde felterne **Rolle** og **Afdeling** og tilføje de værdier, der kræves af en ressource, som skal udføre denne opgave. Sørg for, at værdierne i felterne **Rolle** og **Organisationsenhed** er forskellige for opgave B end værdierne for opgave A. 

  > [!NOTE]
  > Hvis du fuldfører disse scenarier ved hjælp af demonstrationsdata for Project Service Automation, skal du vælge **Netværksteknikker** for rollen, og **Fabrikam US** som afdeling.

5. Gem og luk, og vælg siden **Opgavedetaljer**. 

## <a name="team-member-and-estimates-behavior"></a>Funktionsmåde for teammedlemmer og estimater 

1. På siden **Opgavedetaljer** skal du under **Teammedlem** vælge de to generiske teammedlemmer og derefter vælge **Generer krav**. 
2. Vælg teammedlemmets række for **Konsulterende kundeemne**, og vælg derefter **Reserver**. Planlægningsområdet åbnes og reserverer en ressource i henhold til det pågældende krav.
3. Vælg teammedlemmets række for **Netværksteknikker**, og vælg derefter **Reserver**. Planlægningsområdet åbnes og reserverer den samme ressource i henhold til det pågældende krav.

### <a name="team-member-grid"></a>Teammedlemsgitter 
I gitteret **Teammedlem** skal du lægge mærke til, at de to generiske poster for teammedlemmet er blevet slettet og erstattet med en ressource. Der er ét sæt værdier for den ressource, som viser et standardsæt af værdier for **Rolle** og **Afdeling**.
Når du udvider rækken for det pågældende teammedlems post, kan du se de forskellige tildelinger i teammedlemmets post for begge disse opgaver. Hver tildelingsrække har opgavespecifikke værdier for **Rolle** og **Afdeling**. 

### <a name="estimates-grid"></a>Gitter til estimater 
Når du navigerer til gitteret **Estimater**, vil du bemærke, at tildelingerne til den samme ressource er prisfastsat forskelligt.
Tildelingen for ressourcen på opgave A er prisfastsat ved hjælp af **Rolle**-attributværdien for **Konsulterende kundeemne**. Tildelingen for den samme ressource på opgave B er prisfastsat ved hjælp af **Rolle**-attributværdien for **Netværkstekniker**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]