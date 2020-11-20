---
title: Sikkerhedsmodellen
description: Dette emne indeholder oplysninger om sikkerhedsmodellen i Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 3fc4101d0ea4b8e2a4ba8f1d43540d57239cf402
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124361"
---
# <a name="security-model"></a>Sikkerhedsmodel

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Microsoft Dynamics 365 Project Operations indeholder en entydig sikkerhedsmodel, der giver mulighed for en rollebaseret forretningssikkerhedsmodel, som samarbejder med Microsoft Office Grupper. 


## <a name="security-roles"></a>Sikkerhedsroller
Project Operations-frontendfunktioner omfatter følgende roller:

| Rolle                          | Beskrivelse                                                                                                                                                                 | Område |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Praksisadministrator              | Understøtter rapportering på tværs af projekter.                                                                                                            | Forretningsenhed              |
| Projektgodkender              | Godkender tid og udgifter i forhold til et projekt.                                                                                                                              | Forretningsenhed |
| Projektfaktureringsadministrator | Opretter fakturaforslaget.                                                                                                                                                 | Forretningsenhed |
| Projektleder               | Opretter projektplanen og anmoder om ressourcer.                                                                                                                              | Forretningsenhed |
| Projektressource              | Teammedlemmer, der kan være reserveret og rapportere tid.                                                                                                          | Forretningsenhed|
| Resource Manager              | Alle funktioner for ressourcestyring, f.eks. opfyldelse af ressourceanmodninger og -reservationer, er adskilt for at understøtte en hybridprojektleder + konfiguration af Resource Manager og en fælles og central rolle for Resource Manager. | Forretningsenhed |


Microsoft Project til internettet indeholder følgende roller:

| Rolle           | Beskrivelse                                                                                                        | Område  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Projektbruger   | En samarbejdende bruger i et projekt, der er i stand til at oprette deres egne projekter, og som kan se alle projekter, der deles med dem. | Bruger   |
| Projektsystem | Rolle, der bruges til programkontekst. Brugere bør ikke bruge denne systemrolle.                                    | Global |

## <a name="security-enforcement"></a>Sikkerhedshåndhævelse
Handlinger, der udføres på projektniveau, udføres i sammenhæng med den bruger, der er logget på. Dette betyder, at hvis det er nødvendigt at oprette, åbne eller slette et projekt, skal brugeren have tilgængelig adgang I CDS. Der kan gives adgang til CDS via en hvilken som helst af de mulige mekanismer, der findes i platformen. En bruger, der har et større område, kan f.eks. få adgang til projektet, eller hvis der er udført en eksplicit projektdelingshandling, som giver brugeren adgang.

Det er vigtigt at tage højde for dette, når der oprettes projekter i Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Moderne gruppesamarbejde med Project Operations
Projekt til internettet og Project Operations understøtter moderne samarbejdsgrupper. Brugere, der er tilføjet til projektet via en gruppe, kan redigere projektplanen.

Project til internettet tilføjer automatisk brugere til gruppen ved tildelingen.

Grupper gør det muligt at arbejde sammen om tilladelserne for projektet og understøtter, at der arbejdes med samarbejdsartefakter sammen. I følgende diagram vises de arrangementer og tilstandsændringer, der er foretaget under gruppetildelingsprocessen.

Project Operations opretter ikke en gruppe gennem implicit handling, og gør det kun, når der udtrykkeligt trykkes på grupper.

Søgning efter gruppemedlemmer i dialogen **Gruppestyring** er begrænset til dem, der er angivet som en del af miljøets sikkerhedsgruppe. Du kan finde flere oplysninger under [Kontroller brugeradgang til miljøer: sikkerhedsgrupper og licenser](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Gruppetilstand](./media/groupsmode.png)

1. Projektet oprettes og ejes af brugeren, der opretter det.
2. Projektejeren opdateres til teamet.
3. Ejerteamet er knyttet til den angivne eller oprettede Office Gruppe.
4. Den oprindelige ejer af projektet tilføjes til Office Gruppen.

## <a name="deployment-recommendation"></a>Anbefaling af installation
Da Office Gruppens samarbejdsmodel udvikler sig, vil funktionaliteten blive tilføjet for at give mere detaljeret kontrol over tid. Kunder, der anvender Project Operations i dag, opfordres til at fokusere på en traditionel Microsoft Dynamics 365-sikkerhedsmodel.

Du kan finde flere oplysninger under [Sikkerhed i Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Sikkerhed i Project Operations og Microsoft Dynamics 365 Finance
Project Operations omfatter følgende roller:

- Projektleder
- Projektbogholder

Du kan finde flere oplysninger om sikkerhed i Finance under [Rollebaseret sikkerhed](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


