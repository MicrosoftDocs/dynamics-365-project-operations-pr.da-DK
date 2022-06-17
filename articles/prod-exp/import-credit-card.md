---
title: Importer og vedligehold kreditkorttransaktioner
description: Denne artikel forklarer, hvordan du importerer og vedligeholder udgiftsrelaterede kreditkorttransaktioner. Disse transaktioner kan konfigureres, så de automatisk importeres i en tilbagevendende tidsplan, eller de kan importeres manuelt, efterhånden som der er behov for dem.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 44aac1db60ef8f0e3f25612d03b46520dd09ee9e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916787"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importer og vedligehold kreditkorttransaktioner

Udgiftsrelaterede kreditkorttransaktioner kan konfigureres, så de automatisk importeres i forbindelse med en tilbagevendende tidsplan. Alternativt kan transaktionerne importeres manuelt, efterhånden som behovet herfor opstår. Kreditkorttransaktionerne importeres via dataobjektet for kreditkorttransaktionerne.

Du kan finde flere oplysninger om dataobjekter i [Dataobjekter](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Import af kreditkorttransaktioner

1. På siden **Kreditkorttransaktioner** skal du vælge **Importer transaktioner**. Hvis du åbner datastyring for første gang, skal systemet opdatere listen over dataobjekter, før du kan fortsætte.
2. Angiv en entydig beskrivelse af det importerede job i feltet **Navn**.
3. I feltet **Dataformat for kilde** skal du vælge formatet for den fil, der indeholder de kreditkorttransaktioner, der skal importeres.
4. Vælg **Upload**, og find og vælg derefter den fil, der skal importeres.
5. Når filen er blevet uploadet, skal du validere tilknytningen af kreditkorttransaktionsfilen og kolonnerne i dataobjektet for kreditkorttransaktioner ved at vælge linket **Vis tilknytning** i feltet. Hvis der er tilknytningsfejl, eller hvis du skal ændre tilknytningen, skal du foretage tilknytningen fra enten fanen **Tilknytningsvisualisering** eller fanen **Tilknytningsdetaljer**.
6. Hvis du vil automatisere kreditkorttransaktionerne, skal du vælge **Opret gentagende datajob**. Du kan derefter angive den gentagelse, der definerer, hvor ofte der skal importeres kreditkorttransaktioner. Vælg **OK**, når du er færdig.
7. Hvis du vil importere den valgte fil nu, skal du vælge **Importér**.
8. Hvis der opstår fejl under importen, kan du gennemgå kørselsloggen eller de midlertidige data for at se de fejl, du skal løse for at sikre en vellykket import.

> [!NOTE]
> Hvis du skal importere mere end ét filformat, skal du oprette separate importjob for de enkelte formattyper.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Gentildele kreditkorttransaktioner for fratrådte medarbejdere

Når en medarbejderpost er blevet afsluttet, deaktiveres brugerens Active Directory-domæneservices-konto (AD DS). Der kan dog være aktive kreditkorttransaktioner, der stadig skal udgiftsføres og refunderes. På siden **Kreditkorttransaktioner** kan du gentildele medarbejderen i forbindelse med alle de kreditkorttransaktioner, hvor den tilknyttede medarbejder er blevet afsluttet.

Vælg en eller flere kreditkorttransaktioner, og vælg derefter **Tildel transaktioner igen**. Du kan derefter vælge en anden medarbejder, som kreditkorttransaktionerne skal tildeles til. Når kreditkorttransaktionerne er blevet tildelt en anden, kan de vælges til en udgiftsrapport og betales via den sædvanlige proces for refusion af udgiftsrapporter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]