---
title: Konfigurer integration af kreditkort
description: I dette emne forklares det, hvordan du kan arbejde med udgiftsrelaterede kreditkorttransaktioner.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51c364dff41d856e493581e1b87fd29571f641c70e7233bdebb910efbc64b983
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996204"
---
# <a name="set-up-credit-card-integration"></a>Konfigurer integration af kreditkort

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Udgiftsrelaterede kreditkorttransaktioner kan konfigureres, så de automatisk importeres i forbindelse med en tilbagevendende tidsplan. Alternativt kan transaktionerne importeres manuelt, efterhånden som behovet herfor opstår. Kreditkorttransaktionerne importeres via dataobjektet for kreditkorttransaktionerne.

## <a name="import-credit-card-transactions"></a>Import af kreditkorttransaktioner

Hvis du vil importere kreditkorttransaktioner, skal du følge disse trin:

1. På siden **Kreditkorttransaktioner** skal du vælge **Importer transaktioner**. Hvis du åbner datastyring for første gang, skal systemet opdatere listen over dataobjekter, før du kan fortsætte.
2. Angiv en entydig beskrivelse for det importerede job i feltet **Navn**.
3. I feltet **Dataformat for kilde** skal du vælge formatet for den fil, der indeholder de kreditkorttransaktioner, der skal importeres.
4. Vælg **Upload**, og find og vælg derefter den fil, der skal importeres.
5. Når filen er blevet uploadet, skal du validere tilknytningen af kreditkorttransaktionsfilen og kolonnerne i dataobjektet for kreditkorttransaktioner ved at vælge linket **Vis tilknytning** i feltet. Hvis der er tilknytningsfejl, eller hvis du skal ændre tilknytningen, skal du foretage tilknytningen fra enten fanen **Tilknytningsvisualisering** eller fanen **Tilknytningsdetaljer**.
6. Hvis du vil automatisere kreditkorttransaktionerne, skal du vælge **Opret gentagende datajob**. Du kan derefter angive den gentagelse, der definerer, hvor ofte der skal importeres kreditkorttransaktioner. Vælg **OK**, når du er færdig.
7. Hvis du vil importere den valgte fil nu, skal du vælge **Importér**.
8. Hvis der opstår fejl under importen, kan du få vist logfilen for udførelsen eller midlertidige lagringsdata for at se de fejl, du skal rette for at sikre en vellykket import.

> [!NOTE]
> Hvis du skal importere mere end ét filformat, skal du oprette separate importjob for de enkelte formattyper.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Gentildele kreditkorttransaktioner for fratrådte medarbejdere

Når en medarbejderpost er blevet afsluttet, deaktiveres brugerens Active Directory-domæneservices-konto (AD DS). Der kan dog være aktive kreditkorttransaktioner, der stadig skal udgiftsføres og refunderes. På siden **Kreditkorttransaktioner** kan du gentildele medarbejderen til enhver kreditkorttransaktion, hvor den tilknyttede medarbejder er blevet afsluttet.

Vælg en eller flere kreditkorttransaktioner, og vælg derefter **Tildel transaktioner igen**. Du kan derefter vælge en anden medarbejder, som kreditkorttransaktionerne skal tildeles til. Når kreditkorttransaktionerne er blevet tildelt en anden, kan de vælges til en udgiftsrapport og betales via den sædvanlige proces for refusion af udgiftsrapporter.

## <a name="delete-credit-card-transactions"></a>Slet kreditkorttransaktioner 

Når kreditkorttransaktioner er importeret, kan det undertiden være nødvendigt at slette visse transaktioner. Dette kan skyldes, at transaktionerne er dubletter, eller at dataene muligvis ikke er nøjagtige. Administratorer kan bruge funktionen **"Slet kreditkorttransaktioner"** til at vælge og slette kreditkorttransaktioner, der **ikke er knyttet til** en udgiftsrapport. 

1. Gå til **Periodiske opgaver** > **Slet kreditkorttransaktioner**.
2. Vælg **Filter**, og angiv oplysninger for at identificere de poster, der skal inkluderes.
3. Vælg **OK** for at slette posterne. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
