---
title: Indstillinger for salgsmuligheder - lille
description: Dette emne indeholder oplysninger om projektbaserede handler og projektbaserede salgsmulighedslinjer.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6631e136572b958ca616d708a5e3c3c2d9f2675c
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663812"
---
# <a name="header-details-for-project-opportunities"></a>Overskriftsdetaljer for salgsmuligheder i et projekt

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I salgsmulighedsoverskriften registreres de overordnede oplysninger om en projektbaseret handel, der gælder for alle linjer i den projektbaserede salgsmulighed.

Projektbaserede salgsmuligheder i Dynamics 365 Project Operations er udvidelser til muligheder i Dynamics 365 Sales. Disse udvidelser indeholder yderligere funktioner, der er specifikke for og nødvendige for projektbaserede salgsmuligheder. Disse udvidelser kan inkludere nye felter og handlinger på båndet, der er tilgængelige i projektbaserede salgsmuligheder. Du kan opleve, at nogle af de felter, funktioner og standardlogikler, der findes i Sales, ikke er tilgængelig i Project Operations.

I følgende tabel medtages felterne i en projektbaseret salgsmulighed, der enten er entydig for Project Operations, eller som er vigtige ændringer af funktionsmåder fra salgsmuligheder i Sales.

| **Felt** | **Placering** | **Beskrivelse** | **Downstream-virkning** |
| --- | --- | --- | --- |
| Skriv | Fanen Generelt (skjult) | Feltet med grupperet indstilling har følgende indstillinger:</br>- Arbejdsbaseret (kun tilgængelig sammen med Project Operations)</br>- Enhedsbaseret (kun tilgængelig, når Project Operations og Sales er installeret)</br>- Servicevedligeholdelsesbaseret (tilgængelig, når Field Service er installeret) | Når du bruger Project Operations, angives værdien i dette felt automatisk til **Arbejdsbaseret**, hvilket klassificerer salgsmuligheden som projektbaseret. En salgsmulighed bør være projektbaseret for at aktivere alle projektspecifikke udvidelser og funktioner i den efterfølgende salgsproces for denne aftale. |
| Kontaktperson | Fanen Generelt | Reference til kundens primære kontaktperson for denne handel. | |
| Konto | Fanen Generelt | Reference til kundens firma eller firmapost. | |
| Account manager | Fanen Generelt | Navnet på Account manager for denne projektbaserede salgsmulighed. | Account manageren er ansvarlig for at administrere relationen til kunden ved at fuldføre dette projekt. På basis af den reserverbare ressourcepost, der er knyttet til Account manager, angives standarden for kontraktenheden. |
| Kontraktenhed | Fanen Generelt | Den organisationsenhed, der er ansvarlig for leveringen af det projekt eller de projekter, der er knyttet til denne handel. | Kontraktenheden er afdelingen i det firma, der skal gennemføre projekterne, når handlen er indgået. Alle kontraherende enheder har en valuta, og denne valuta bruges til at rapportere de anslåede og faktiske omkostninger, der er påløbet i løbet af projektet. |

For alle andre felter og sektioner under fanen **Oversigt** for salgsmuligheden se [Opret eller rediger salgsmuligheder (Salg og Salgshub)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
