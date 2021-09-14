---
title: Milepæle for underentrepriselinje
description: I dette emne forklares det, hvordan du kan oprette og vedligeholde en milepælsbaseret fakturaplan for en underleverandør med en leverandør.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323769"
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

    | Felt | Beskrivelse |
    | --- | --- |
    | Navn på milepæl | Navnet på milepælen. |
    | Beskrivelse | En beskrivelsen af milepælen.  |
    | Milepælsdato | Den dato, hvor den automatiske fakturaoprettelsesproces skal søge efter statussen for denne milepæl for tage den i betragtning i forbindelse med fakturering. Denne værdi medtages på fakturalinjen for leverandøren, når denne underentreprise faktureres. |
    | Beløb | Beløbet eller værdien af den milepæl, der vil blive faktureret kunden. Denne værdi medtages på fakturalinjen for leverandøren, når denne underentreprise faktureres. |
    | Skat | Det momsbeløb, der anvendes på milepælen. Denne værdi medtages på fakturalinjen for leverandøren, når denne underentreprise faktureres. |
    | Beløb efter moms | Dette skrivebeskyttede felt beregnes som Beløb + Moms. Denne værdi medtages på fakturalinjen for leverandøren, når denne underentreprise faktureres. |
    | Fakturastatus | Når milepælen oprettes, angives denne status altid til **Ikke klar til fakturering**.  Når statussen er **Klar til fakturering**, medtager oprettelsen af leverandørfakturaen denne milepæl på leverandørfakturaen. |

5. Vælg **Gem og luk**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
