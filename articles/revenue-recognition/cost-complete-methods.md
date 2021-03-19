---
title: Metoder til færdiggørelsesomkostninger
description: Dette emne indeholder oplysninger om de metoder, der bruges til at beregne omkostningerne for at fuldføre et projekt.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 837cb3abe33e6e74087b8aae8b072bf4a21dc933
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279041"
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