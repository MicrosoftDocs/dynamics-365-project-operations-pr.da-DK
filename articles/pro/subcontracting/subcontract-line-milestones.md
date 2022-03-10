---
title: Milepæle for underentrepriselinje
description: I dette emne forklares det, hvordan du kan oprette og vedligeholde en milepælsbaseret fakturaplan for en underleverandør med en leverandør.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7f99853f5f649f96225b7d72580db97bb92de7c5
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558495"
---
# <a name="subcontract-line-milestones"></a>Milepæle for underentrepriselinje

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I Dynamics 365 Project Operations kan en underentrepriselinje med en fastprisfaktureringsmetode angive en milepælsbaseret fakturaplan med leverandøren.

Milepæle for leverandørfakturering kan oprettes automatisk ved hjælp af en fastsat hyppighed, eller du kan oprette dem manuelt.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Automatisk oprettelse af en milepælsbaseret fakturaplan for en underentrepriselinje

Fuldfør følgende trin for automatisk at oprette en milepælsbaseret fakturaplan for et fast sæt ligeligt fordelte milepæle.

1. Gå til **Indstillinger** > **Fakturahyppighed**, og angiv fakturahyppigheden for underentrepriselinjerne.
2. Åbn siden **Underentrepriser**, åbn den underentreprise, som du vil arbejde sammen med, og åbn derefter den fastprisunderentrepriselinje, som du vil oprette en milepælsplan for.
3. På fanen **Milepæle for underentrepriselinje** skal du vælge **Opret periodiske milepæle**.
4. Angiv eller vælg et datointerval, antallet af milepæle og fakturahyppigheden i dialogboksen. Du kan vælge en startdato, eller du kan vælge antallet af milepæle og fakturahyppigheden eller startdatoen, eller du kan vælge slutdatoen og fakturahyppigheden. Du kan ikke vælge slutdatoen og antallet af milepæle.
Ved hjælp af disse oplysninger opretter systemet milepæle og poster, der vises i gitteret **Milepæle**.

   - **Milepælsnavn** - Navnet på milepælen angives til datoen for milepælen baseret på fakturahyppigheden.
   - **Milepælsdato** - Datoen er baseret på fakturahyppigheden.
   - **Milepælsbeløb** - Beregnet ved at dividere delsummer på underentrepriselinjen med antallet af milepæle.

Hvis underentrepriselinjen har en værdi i feltet **Anslået momsbeløb**, tilføjes denne værdi ligeligt til hver milepæl, når der oprettes periodiske milepæle.

Summen af milepælsbeløbene for en underentrepriselinje, skal være lig med værdien af underentrepriselinjen. Hvis de ikke er overensstemmende, opstår der en fejl. Du kan rette fejlen og kontrollere, at den samlede sum for milepælen svarer til værdien på underentrepriselinjen ved at oprette, redigere eller slette milepæls- og momsbeløb. Når ændringerne er foretaget, skal du gemme og opdatere siden for at sikre dig, at der ikke opstår flere fejl.

## <a name="manually-create-subcontract-line-milestones"></a>Manuel oprettelse af milepæle for underentrepriselinjer

Fastprismilepæle på en underentrepriselinje kan oprettes manuelt, når de ikke opdeles ligeligt over en periode. Hvis du vil oprette en milepæl på en underentrepriselinje manuelt, skal du fuldføre følgende trin.

1. I navigationsruden skal du vælge **Underentrepriser** og åbne den underentreprise, som du vil arbejde med.
2. Åbn den fastprisunderentrepriselinje, som du vil oprette en milepæl for.
3. På fanen **Milepæle for underentrepriselinjer** skal du i undergitteret vælge **+Ny milepæl for underentrepriselinje**.
4. På siden **Ny milepæl for underentrepriselinje** skal du angive de krævede oplysninger på baggrund af følgende tabel.

    | Felt | Beskrivelse |Funktionspåvirkning|
    | --- | --- |----------------------|
    | Navn på milepæl | Navnet på milepælen. |Dette vises som den første kolonne i alle opslag baseret på milepæle for underentrepriselinjer. På den leverandørfakturalinje, der oprettes på baggrund af denne milepæl, bruges navnet på milepælen for underentrepriselinjen også som standardnavn på leverandørens fakturalinje.|
    | Beskrivelse | En beskrivelsen af milepælen. |På den leverandørfakturalinje, der oprettes på baggrund af denne milepæl, bruges beskrivelsen af milepælen for underentrepriselinjen også som beskrivelsen af leverandørens fakturalinje.|
    | Milepælsdato | Den dato, hvor den automatiske fakturaoprettelsesproces skal søge efter statussen for denne milepæl for tage den i betragtning i forbindelse med fakturering.| Denne værdi bruges som standarddatoen for leverandørens fakturalinje, når der faktureres for denne underentrepriselinje. |
    | Beløb | Beløbet eller værdien af den milepæl, der vil blive faktureret kunden. |Denne værdi bruges som standardværdien på leverandørens fakturalinje, når der faktureres for denne underentrepriselinje. |
    | Skat | Det momsbeløb, der anvendes på milepælen.| Denne værdi bruges som standardmomsværdien på leverandørens fakturalinje, når der faktureres for denne underentrepriselinje. |
    | Beløb efter moms | Dette skrivebeskyttede felt beregnes som Beløb + Moms.|Denne værdi bruges som standarden på leverandørens fakturalinje, når der faktureres for denne underentrepriselinje. |
    | Fakturastatus | Når milepælen oprettes, angives denne status altid til **Ikke klar til fakturering**.|  Når statussen er **Klar til fakturering**, medtager oprettelsen af leverandørfakturaen denne milepæl på leverandørfakturaen. |

5. Vælg **Gem og luk**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
