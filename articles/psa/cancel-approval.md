---
title: Annullere tidligere godkendte tids- og udgiftsposter
description: Dette emne indeholder oplysninger om, hvordan du kan annullere en godkendt projekttids- og udgiftstransaktion.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 9e3bc94b626b88a2167e3a61472b768e2fb5c731
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590753"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Annullere tidligere godkendte tids- eller udgiftsposter

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I den nyeste version af Dynamics 365 Project Service Automation kan godkendere annullere tids- eller udgiftsposter, som de tidligere har godkendt.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Annullere en tidligere godkendt tids- eller udgiftspost

Følg disse trin for at annullere en tids- eller udgiftspost, du tidligere har godkendt.

1. Gå til **Projekter** \> **Mit arbejde** \> **Godkendelser**.
2. Skift visningen til **Mine tidligere godkendelser** på listesiden **Godkendelser**. Der vises en liste over de poster for tid og udgift, som du tidligere har godkendt.
3. Vælg en eller flere poster, og vælg derefter **Annuller godkendelse**. Du modtager en advarselsmeddelelse.
4. Vælg **OK** for at annullere godkendelsen.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Forstå effekten af at annullere en godkendelse af en tids- eller udgiftspost

Når en godkendelse annulleres, har det både driftsmæssige og økonomiske konsekvenser.

### <a name="operational-impact"></a>Driftsmæssig konsekvens

Når en godkendelse annulleres på siden handlinger, nulstilles postens status til **Kladde**, og godkendelsen vises ikke længere i visningen **Mine tidligere godkendelser**. I stedet vises den annullerede godkendelse i enten visningen **Tidsregistreringer til godkendelse** eller **Udgiftsposteringer til godkendelse**, afhængigt af om det var en tidspost eller en udgiftspost. Derudover ændres status for den relaterede tids- eller udgiftspost til **Sendt**, så den relaterede post er i overensstemmelse med godkendelser, der har statussen **Kladde**.

Som godkender kan du redigere nogle af felterne i en godkendelse, der har statussen **Kladde**. Disse felter omfatter **Faktureringstype** og **Fakturerbare timer for tidsregistreringer**. Når du har foretaget ændringerne, kan du godkende posten igen. Du kan også vælge at afvise posten. Hvis du afviser godkendelsen af en tidsregistrering, ændres dens status til **Returneret**. Hvis du afviser godkendelsen af en udgiftspost, ændres dens status til **Afvist**. Både returnerede og afviste poster fungerer som en post, der har statussen **Kladde**. Et projektteammedlem kan enten foretage de nødvendige ændringer af posten og derefter sende den til godkendelse igen eller slette posten fuldstændigt.

### <a name="financial-impact"></a>Økonomisk konsekvens

Et projekt påvirkes også økonomisk, når en godkendelse annulleres. Først opdateres de tilsvarende faktiske værdier for omkostninger og salg på følgende måde:

- Justeringsstatus angives til **Justeret**.
- Faktureringsstatus angives til **Annulleret**.

Dernæst oprettes der tilbageførselsposter i tabellen med faktiske oplysninger. For at oprette tilbageførselsposter kopieres feltværdierne fra de oprindelige faktiske oplysninger i systemet. De eneste værdier, der ikke kopieres over, er antalsværdier. Disse værdier omgøres i stedet. Tilbageførte faktiske værdier oprettes for både faktiske **Omkostninger** og **Ikke-faktureret salg**. Feltet **Justeringsstatus** i de tilbageførte faktiske oplysninger angives til **Ikke-justerbar**, og faktureringsstatussen angives til **Annulleret**.

Når disse ændringer er foretaget, vil det beløb, der er registreret som brugt på projektet, og omsætningens ordrebeholdning på projektet ikke længere medtage de beløb, som disse faktiske værdier repræsenterer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
