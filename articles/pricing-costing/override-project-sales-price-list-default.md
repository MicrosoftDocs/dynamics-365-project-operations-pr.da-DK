---
title: Tilsidesæt projektsalgsprislister
description: Dette emne indeholder oplysninger om oprettelse af brugerdefinerede salgsprislister.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 16c2b53283b8aa2a243b55a0b887bb5bb461a5fb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585555"
---
# <a name="override-project-sales-price-lists"></a>Tilsidesæt projektsalgsprislister

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

## <a name="customer-specific-project-price-lists"></a>Kundespecifikke projektprislister

Kundespecifikke prisaftaler kan konfigureres som projektprislister på en kontopost i Dynamics 365 Project Operations.

Hvis du vil oprette en kundespecifik projektprisliste, skal du i området **Salg** går til kontoposten.

1. Åbn listesiden med **Konti**.
2. Find og dobbeltklik på en kundepost for at åbne detaljesiden for **Konto**.
3. På fanen **Projektprislister** skal du vælge **+ Ny projektprisliste**.
4. På siden **Ny projektprisliste** skal du vælge en prisliste i rullemenuen. Kun prislister, hvor konteksten er angivet til **Salg**, og hvis valuta matcher kontovalutaen, medtages.
5. Navngiv tilknytningen og vælg derefter **Gem**. Der oprettes en kundespecifik projektprisliste. Denne prisliste bruges som standard for projektpriser på projekttilbud eller kontrakter, der er oprettet for denne kunde, når den oprettede dato for tilbuddet eller projektkontrakten falder inden for prislistens ikraftrædelsesdato.

## <a name="custom-pricing-on-project-quotes"></a>Brugerdefineret prisfastsættelse på projekttilbud

På projekttilbud kan du have projektprisfastsættelser, som starter med en standardprisliste, der som standard hentes fra kunden eller fra projektparametrene.

Når du har brug for brugerdefinere prisfastsættelse for projektrelateret arbejde på et bestemt tilbud, kan du opnå dette ved hjælp af den tilknyttede enhed med projektprislister.

Udfør følgende trin for at konfigurere tilbudsspecifik projektprisfastsættelse.

1. Åbn projekttilbud, og vælg fanen **Projektprislister**.
2. I undergitteret skal du vælge **Opret brugerdefineret prisfastsættelse**.

Alle de projektprislister, der er knyttet til tilbuddet, kopieres til nye prislister. Navnene på de nye prislister afspejler navnet på tilbuddet med et datotidsstempel for det tidspunkt, hvor disse prislister blev oprettet.

Du kan bruge hver af disse prislister og foretage opdateringer til arbejdskraftpriser (rollepris) og udgiftspriser (kategoripris). Disse priser gælder kun for dette projekttilbud.

## <a name="price-lists-on-a-project-contract"></a>Prislister på en projektkontrakt

På en projektkontrakt er projektprisfastsættelse som standard altid en brugerdefineret prisliste med navnet på kontrakten og tidspunkt for oprettelse, der er føjet til navnet. Dette gælder, uanset om kontrakten blev oprettet, da tilbuddet blev vundet, eller om kontrakten blev oprettet fra bunden. Hvis det er nødvendigt, kan du fjerne denne tilknytning til den brugerdefinerede prisliste og knytte en standardprisliste til projektkontrakten i stedet.

Når du knytter en standardprisliste til projektprislisterne på et tilbud eller en kontrakt, vil eventuelle ændringer af priserne i prislisten påvirke alle tilbud og kontrakter, der bruger prislisten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]