---
title: Administrer projektbaserede salgsmuligheder
description: Dette emne indeholder oplysninger om, hvordan du arbejder med salgsmuligheder, der er relateret til projekter.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d1f9b29e0e9516ff78517e47694a2385c083ec7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277826"
---
# <a name="manage-project-based-opportunities"></a>Administrer projektbaserede salgsmuligheder

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Projektbaserede virksomheder leverer typisk på tværs af flere lande og geografi. Omkostningerne til projektudførelse og levering kan variere, afhængigt af hvilken geografi eller hvilken afdeling der administrerer leveringen. Det kan således påvirke margenerne i handlen. Levering af projektbaserede tjenester indebærer typisk store mængder af menneskelige ressourcers tid, høje udgifter til rejser, materialeomkostninger og andre udgifter.

Projektbaserede salgsmuligheder i Dynamics 365 Project Operations er udviklet med udvidelser til Dynamics 365 Sales. Dette emne indeholder oplysninger om de forskellige felter og den forretningslogik, der er inkluderet i de ekstra funktioner, som projektbaserede virksomheder kræver for at administrere projektbaserede salgsmuligheder.

## <a name="view-all-project-based-opportunities"></a>Se alle projektbaserede salgsmuligheder

Du kan se en liste over alle de projektbaserede salgsmuligheder på listesiden **Salgsmulighed**. 

1. Gå til **Salg** > **Salgsmuligheder**.
2. Brug **Skift visning** til at vælge andre filtrerede visninger for salgsmulighederne. Du kan oprette dine egne visninger med brugerdefinerede filterkriterier for at konfigurere disse visninger og navigationsindstillinger.

Projektbaserede salgsmuligheder kan oprettes eller slettes fra denne listeside eller på detaljesiden.

## <a name="business-process-flow-for-project-based-deals"></a>Forretningsprocesflow for projektbaserede handler

Følgende forretningsprocesflow understøttes i forbindelse med projektbaserede handler i Project Operations:

- Forretningsproces for kundeemne til salgsmulighed
- Salgsproces for salgsmulighed

### <a name="lead-to-opportunity-business-process"></a>Forretningsproces for kundeemne til salgsmulighed 
Forretningsprocessen for kundeemne til salgsmuligheder understøtter følgende faser:

| Trin | Tilknyttet objekt | Funktionalitet |
| --- | --- | --- |
| Kvalificer | Potentiel kunde | Kvalificering af kundeemnet for at oprette et firma, en kontakt og en salgsmulighed. |
| Opstil tilbud | Salgsmulighed | Udarbejd salgsmuligheden for at tilføje flere oplysninger om det involverede arbejde, interessenter og konkurrenter. |
| Afgiv tilbud | Salgsmulighed | Udarbejd forslaget, og få godkendelse fra det interne vurderingsteam. |
| Luk | Salgsmulighed | Vind salgsmuligheden for lukke handlen. |

### <a name="opportunity-sales-process"></a>Salgsproces for salgsmulighed
Salgsprocessen for salgsmuligheder i Project Operations er en udvidelse af forretningsprocesforløb i salgsproces for salgsmulighed i Sales-programmet. Denne forretningsproces er designet til at kunne bruges til at understøtte følgende trin i en projektbaseret salgsmulighed.

| Trin | Tilknyttet objekt | Funktionalitet |
| --- | --- | --- |
| Kvalificer | Salgsmulighed | Kvalificering af kundeemnet for at oprette et firma, en kontakt og en salgsmulighed. |
| Afgiv tilbud | Tilbud | Udarbejd forslaget ved hjælp af projekttilbud, og få godkendelse fra det interne vurderingsteam. |
| Kontrakt | Projektkontrakt | Vind tilbuddet for at oprette kontrakten, og påbegynd arbejdet med at udføre og levere projektet. |
| Luk | Projektkontrakt | Afslut arbejdet, og luk projektkontrakten. |

> [!NOTE]
> Hvis din projektbaserede aftale er startet med et kundeemne, har forretningsprocessen for kundeemne til salgsmulighed forrang.
>
> Hvis din projektbaserede aftale er startet med en salgsmulighed, har salgsprocessen for salgsmulighed forrang.

Du kan redigere produktets forretningsprocesforløb eller oprette dine egne forretningsprocesforløb for at spore din salgsproces efter behov. Du kan finde flere oplysninger om forretningsprocesforløb i [Oversigt over forretningsprocesforløb](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]