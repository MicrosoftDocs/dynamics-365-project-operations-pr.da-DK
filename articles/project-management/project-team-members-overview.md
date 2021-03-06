---
title: Projektteamets medlemmer
description: Dette emne indeholder oplysninger om, hvordan du kan arbejde med oplysninger om teammedlemmer, attributter og planlægning.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f4941803c657fab55ee2702d9f58d6e333592889
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908009"
---
# <a name="project-team-members"></a>Projektteamets medlemmer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Projektteammedlemmer er de projektdeltagere, som udfører arbejdet på et projekt. Målet med teammedlemsgitteret er at oprette en liste over navngivne ressourcer, der er engagerede i forpligtelsen, og generiske teammedlemmer, der fungerer som pladsholderressourcer og bliver ansat på et senere tidspunkt.

I teamets medlemsgitter har projektlederen og de andre projektdeltagere mulighed for at se, hvem der er blevet tilknyttet projektet. De kan også få vist en oversigt over deres reservationer, planlagte indsats og individuelle ressourcetildelinger. Teammedlemsgitteret gør det muligt for projektledere at definere ressourcekrav til generiske teammedlemmer og administrere de eksisterende teammedlemmers reservationer.

I følgende tabel vises nøgleattributterne for et projektteammedlem.

| Feltnavn          | Beskrivelse                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Allokeringsmetode        | Den fordelingsmetode, der bruges til at reservere ressourcer på projektet.                                                                         |
| Faktureringstype             | Vælg, om teammedlemmet skal klassificeres som fakturerbart.                                                                                                                                       |
| Reserverbar ressource        | Den reserverbare ressource, der er valgt til at erstatte den generiske ressource.                                                                                                                   |
| Slettestatus            | Slettestatus for teammedlemmet for at spore, hvorvidt der er sendt en anmodning om sletning til PSS, og om PSS sender tilbagesvar og inden for det forventede tidsvindue. |
| Indsats i alt (timer)     | Summen af teammedlemmernes indsats på deres tildelinger.                                                                                                                         |
| Fuldført indsats (timer) | En sporing af den indsats, som teammedlemmerne har udført på deres tildelinger.                                                                                           |
| Resterende indsats (timer) | En sporing af den indsats, som teammedlemmerne endnu ikke har udført på deres tildelinger.                                                                                    |
| Afslut                   | Slutdatoen for ressourceteammedlemskabet.                                                                                                                                            |
| Definitivt reserverede timer        | Det definitivt reserverede timetal for teammedlemmet.                                                                                                                                                                |
| Stillingsnavn            | Det navn, der bruges til at identificere den generiske ressource.                                                                                                                                   |
| Ressourceenhed          | Afdelingen for den ressource, der udfører arbejdet.                                                                                                                      |
| Projektgodkender         | Vælg, om teammedlemmet skal kunne godkende tid og udgifter.                                                                                                                     |
| Krævede timer           | Det krævede antal timer teammedlemmet i teammedlemskravet.                                                                                                                       |
| Rolle                     | Rollen, som teammedlemmet udfylder i dette team.                                                                                                                                |
| Beskrivelse af position     | Angiv en beskrivelse af rollen for dette teammedlem.                                                                                                                             |
| Foreløbigt reserverede timer        | Det foreløbigt reserverede timetal for teammedlemmet.                                                                                                                                                                 |
| Start                    | Angiv startdatoen for medlemskab af ressourceteamet.                                                                                                                                          |

Fra teammedlemsgitteret kan følgende handlinger udføres:

- **Reserver**: For organisationer, der anvender metoden til hybrid-reservering, kan reservationshandlingen gøre det muligt for brugere at reservere en navngivet ressource på baggrund af de krav, der er opstået som følge af det generiske teammedlem
- **Generer krav**: Denne handling genererer kravet.
- **Angiv mønster**: Giver projektledere mulighed for at tilpasse ressourcekravsprofilerne på et detaljeret niveau. Projektledere kan justere i forhold til projektets specifikke behov i de tilfælde, hvor standardfordelingen ikke passer.
- **Indsend anmodning**: For organisationer, der bruger den centrale reservationsmetode.
- **Rediger**: Attributter for teammedlemmer kan redigeres, herunder afdeling, rolle og stillingsbetegnelse.
- **Fasthold reservationer**: Når ressourcereservationer skal opdateres, kan projektleder fastholde reservationer for at kunne justere:

    - Start
    - Afslut
    - Fordeling af den samlede indsats

- **Nyt**: Ud over at tilføje ressourcer direkte fra tidsplanen kan projektledere tilføje nye navngivne eller generiske teammedlemmer fra teammedlemsgitteret.
- **Slet**: Ved at vælge en eller flere teammedlemmer kan projektlederen slette ressourcer, der ikke længere skal deltage i projektet. Hvis du sletter et teammedlem, slettes alle tilknyttede ressourcetildelinger også, og alle eksisterende reservationer annulleres.
