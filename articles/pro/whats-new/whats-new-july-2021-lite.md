---
title: Nyheder i juli 2021 – Project Operations lille udrulning
description: Denne artikel indeholder oplysninger om de kvalitative opdateringer, der er tilgængelige i juli 2021-udgivelsen af Project Operations lille udrulning.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7964f38c1bc7a8e0440e2e922ff153fd9bede131
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913981"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Nyheder i juli 2021 – Project Operations lille udrulning

_Gælder for: Lille udrulning - aftale til proformafakturering_

Denne artikel gælder for følgende komponenter og versioner af Dynamics 365 Project Operations:

  - Project Operations på Dataverse-miljø version 4.12.0.148 or 4.12.0.152.

## <a name="quality-updates"></a>Kvalitetsopdateringer
| **Funktionsområde**              | **Referencenummer** | **Kvalitetsopdatering**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fakturering og prisfastsættelse           | 2224046              | Feltet **Transaktionsklasse** kan redigeres under fanen **Tilbudslinjedetaljer**, men er låst, hvis du arbejder fra siden **Tilbudslinjedetaljer**.                                                                     |
| Fakturering og prisfastsættelse           | 2224400              | Handlingen **Luk tilbud som vundet** mislykkes, når der ikke er nogen datomilepæle for et tilbud.                                                                                                                                    |
| Fakturering og prisfastsættelse           | 2234089              | Når du manuelt angiver en produktbeskrivelse, ryddes der ikke, når du har angivet et antal for et materialeestimat.                                                                                                                         |
| Fakturering og prisfastsættelse           | 2234100              | Gitteret **Opgavefaktureringsopsætning** inkluderer ikke kolonnen **Materiale** og dens værdi under fanen **Opgavefakturering** i projektet.                                                                                                       |
| Fakturering og prisfastsættelse           | 2277409              | Produkt-id'et er ikke tilgængeligt i kontraktlinjedetaljerne for en materialetypelinje.                                                                                                                                        |
| Fakturering og prisfastsættelse           | 2281728              | Hvis du unødvendigt opretter en kontraktlinje, revurderes de faktiske værdier, hvilket medfører en betydelig stigning i datamængden og påvirker ydeevnen.                                                                                |
| Fakturering og prisfastsættelse           | 2298668              | Kladdelinjer, der er knyttet til en tilbagekaldt eller slettet udgift, fjernes ikke.                                                                                                                                     |
| Fakturering og prisfastsættelse           | 2300192              | Når flere brugere redigerer en faktura, kan der oprettes en ny fakturalinjedetalje på en bekræftet faktura.                                                                                   |
| Fakturering og prisfastsættelse           | 2301569              | Fakturaer kan ikke korrigeres, hvis et tilbageholdt forskudsbeløb på \$0 er blevet anvendt.                                                                                                                                        |
| Fakturering og prisfastsættelse           | 2307965              | Der opstår en fejl, hvis der oprettes en kategoripris med manglende værdier.                                                                                                                           |
| Fakturering og prisfastsættelse           | 2326870              | Der opstår en fejl i **Microsoft.Dynamics.ProjectService.Plugins.PostInvoserieLineDelete**, hvis **producttypecode** er null.                                                                            |
| Fakturering og prisfastsættelse           | 2332732              | Der opstår en fejl, hvis der oprettes en kontraktlinjemilepæl uden en ordrelinje.                                                                                                                |
| Projektplanlægning og -sporing | 2181094              | Project Scheduling-API'en understøtter nu PSS-logfiler og logfiler med operationssæt, der gemmes i 90 dage.                                                                                                                  |
| Projektplanlægning og -sporing | 2254201              | Etiketten **Planlægningstilstand** opdateres med detaljer, der beskriver standardlogikken.                                                                                                                                      |
| Projektplanlægning og -sporing | 2300252              | Responscachen **openProject** opdateres og inkluderer tokenejeren i cachenøglen, **den grundlæggende URL-adresse** og **URL-adressen for segment**, så **Anmod om URL-adresse** altid kan oprettes igen, hvis den **Grundlæggende URL-adresse** ændres. |
| Projektplanlægning og -sporing | 2301312              | **msdyn_membershipstatus** er blevet fjernet fra visningen **Medlemmer af projektteam**.                                                                                                                                        |
| Projektplanlægning og -sporing | 2302759              | Produkter hentes unødvendigt under fanerne **Ressourcetildelinger**, **Estimater** og **Udgiftsestimater**.                                                                                                        |
| Projektplanlægning og -sporing | 2308050              | **CopyProject** mislykkes på grund af fejlen "Det lykkedes ikke at få token til at tale med fjerntjeneste".                                                                                                                           |
| Projektplanlægning og -sporing | 2322650              | Visningen **Projektopgaveliste** er blevet opdateret, så datoen for opgaven vises som standard.                                                                                                            |
| Projektplanlægning og -sporing | 2327266              | **CopyProject** genererer fejlen "Nøglen blev ikke fundet i en ordbog", når der kopieres estimater.                                                                                                      |
| Projektplanlægning og -sporing | 2328123              | **CopyProject** genererer fejlen "Det lykkedes ikke at få token til at tale med fjerntjeneste".                                                                                                                          |
| Projektplanlægning og -sporing | 2336258              | **CopyProject** kopierer ikke ressourceplaceringsnavnene korrekt.                                                                                                                                                 |
| Fakturering og prisfastsættelse           | 2224476              | Feltet **Reserverbar ressource** går ikke korrekt tilbage til standarden for den bruger, der er logget på siden **Materialeforbrug**.                                                                                                            |
| Ressourcestyring           | 2277249              | Der opstår en fejl, når et ikke-projektbaseret ressourcekrav opdateres.                                                                                                            |
| Ressourcestyring           | 2323869              | Ressourcetidsforbrug genkendes ikke korrekt i filtrerede ressourcer.                                                                                                                                             |
| Tid og udgift              | 2176538              | Der anvendes forkerte filteroperatorer på kontrolelementet **Tidsregistrering**.                                                                                                                                                   |
| Tid og udgift              | 2177462              | Hvis du sletter en tidsregistrering i gitteret, opdateres statussen for knappen **Indsend**, **Tilbagekald**, **Slet** og **Rediger registrering** ikke som forventet.                                                                                        |
| Tid og udgift              | 2299985              | **TimeEntriesImportFromResourceAssignment** bevarer ikke start-/sluttiderne fra tildelingerne.                                                                                                  |
| Tid og udgift              | 2318426              | Når en tidsregistrering er indsendt, kan låste felter stadig redigeres.                                                                                                                                   |
| Tid og udgift              | 2323749              | Der opstår en fejl, når der oprettes en udgift under fanen **Relateret** for en ressource, der kan reserveres.                                                                                                      |
| Tid og udgift              | 2327678              | Når du opretter en tidsregistrering under fanen **Relateret** for en ressource, der kan reserveres, overføres den overordnede ressource ikke til kontrolelementet for tidsregistrering.                                                                            |
| Generelt                       | 2296857              | Sporing af status for langvarige job.                                                                                                                                                                        |
| Generelt                       | 2253682              | Løsningen Project Operations med dobbelt skrivning bør ikke installeres, når dobbeltskrivningskernen installeres i et miljø uden løsningen til organisering af dobbelt skrivning.                                                |
| Generelt                       | 2316420              | Klargøring af kernen i Project Service mislykkes, hvis programmets brugers afdeling ændres.                                                                                                                     |
| Generelt                       | 2376405              | Løst problem med udgiverstyret opdatering (kvalitetsopdatering er tilgængelig i version 4.12.0.152)                                                                                                                     |
