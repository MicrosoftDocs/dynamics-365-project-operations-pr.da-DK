---
title: Metoder til færdiggørelsesomkostninger
description: Dette emne indeholder oplysninger om de metoder, der bruges til at beregne omkostningerne for at fuldføre et projekt.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fe42ea0e1a5c562ec648fbf2a2924648af80381b9db8ffe0c209cb5247bb2ba2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997959"
---
# <a name="cost-to-complete-methods"></a>Metoder til færdiggørelsesomkostninger

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Dette emne indeholder oplysninger om de metoder, der bruges til at beregne omkostningerne for at fuldføre et projekt. Der findes flere metoder, som du kan bruge til at beregne omkostningerne for at fuldføre et projekt. 

Når du opretter et estimat for et projekt, kan du på siden **Opret estimat** i feltet **Metoden for omkostninger for at færdiggøre** vælge en af følgende metoder til færdiggørelsesomkostninger.

| Metode til færdiggørelsesomkostninger    | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Samlede omkostninger-faktiske            | Angiv de estimerede omkostningerne manuelt i felterne **Samlede omkostninger** eller **Samlet antal** ved hjælp af knappen **Omkostningsestimat** på **Estimatsiden**. Systemet trækker de faktiske omkostninger fra de totaler, du har angivet. Det samlede beløb er omkostningerne til at færdiggøre projektet. Denne metode bruger ikke de udgiftsestimater og ressourcetildelinger, der er oprettet i Project Operations og bygget ind i Microsoft Dataverse. De samlede omkostninger eller det samlede antal kan opdateres manuelt efter behov.  |
| Samlet prognose - faktisk        | Ressourcetildelinger og udgiftsestimater bruges til at udregne det samlede beløb for projektprognosen. De faktiske omkostninger sammenlignes med dette budget for at beregne færdiggørelsesomkostningerne.                                                                                                                                                                                                                                                                          |
| Som forrige estimat         | De samme estimeringsmetoder, der blev brugt i den foregående periode, bruges her. Denne metode kræver en prognosemodel, hvis den forrige periode krævede en prognosemodel.                                                                                                                                                                                                                                                                                                                           |
| Angiv færdiggørelsesomkostninger til nul | Denne metode, der som regel bruges før det forkalkulerede projekt udelukkes, svarer til de samlede estimater med bogførte faktiske transaktioner og rydder kolonnen med **Færdiggørelsesomkostninger**. Når det er fuldført, er resultatet altid 100 procent. For hver omkostningslinje, du opretter, fjernes markeringen i afkrydsningsfeltet **Prognose**, og det samlede estimat kopieres fra det forrige omkostningsestimat. Det faktiske forbrug i estimatperioden trækkes fra færdiggørelsesomkostningerne for projektet.              |
| Fra omkostningsskabelon           | Den metode til færdiggørelsesomkostninger, som er konfigureret i den omkostningsskabelon, der er knyttet til det valgte forkalkulerede projekt.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]