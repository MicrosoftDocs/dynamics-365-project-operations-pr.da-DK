---
title: Omsætningsestimat for projekter med fast pris
description: Dette emne indeholder oplysninger om fastprisomsætning i projekter.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278906"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Omsætningsestimat for projekter med fast pris 

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Når du opretter en projektkontraktlinje med følgende attributter i Dynamics 365 Project Operations på Microsoft Dataverse, opretter systemet automatisk et projekt for estimering af fastprisomsætning. Oplysningerne i dette projekt er baseret på følgende:

  - En faktureringsmetode med fast pris.
  - Et tilknyttet projekt.
  - Mindst én milepæl, der er angivet under fanen **Fakturaplan** på siden **Projektkontraktlinje**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Gennemse projekter med fastprisomsætningsestimater
Hvis du vil have vist estimater for omsætning i fastprisprojekter, skal du udføre følgende trin:

1. I Dynamics 365 Finance-miljøet skal du gå til **Projektstyring og regnskab** > **Projekter** > **Estimater for omsætning i fastprisprojekter**.
2. Vælg det projekt, du vil have vist, og dobbeltklik på det **Estimerede projekt-id** for at åbne posten, og gennemse detaljerne for projektet.
3. Udvid fanen **Projekt**. Der vises ét projekt i gitteret for **Valgte projekter**. Systemet bruger dette som standardprojekt, da det er det projekt, der er knyttet til projektkontraktlinjen. 
4. Hvis du vil ændre tilknytningen, skal du vælge flere projekter og føje dem til gitteret **Valgte projekter**. Hvis der er valgt flere projekter i dette gitter, beregnes de færdiggørelsesgraden og omsætningsestimater for projektet sammen for alle de valgte projekter.

  Projektomkostninger, omsætningsprofil, omkostningsskabelon og periodekode kan angives manuelt. Hvis de ikke angives manuelt, anvendes standardværdierne under beregning af første estimat for projektet ved hjælp af de regler, der er konfigureret for projektomkostnings- og omsætningsprofiler.



[!INCLUDE[footer-include](../includes/footer-banner.md)]