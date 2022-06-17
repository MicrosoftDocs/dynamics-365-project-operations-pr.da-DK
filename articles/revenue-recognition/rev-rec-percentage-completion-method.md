---
title: Omsætningsestimat for projekter med fast pris
description: Denne artikel indeholder oplysninger om fastprisomsætning på projekter.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928379"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Omsætningsestimat for projekter med fast pris 

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Når du opretter en projektkontraktlinje med følgende attributter i Dynamics 365 Project Operations på Microsoft Dataverse, opretter systemet automatisk et projekt for estimering af fastprisomsætning. Oplysningerne i dette projekt er baseret på følgende:

  - En faktureringsmetode med fast pris.
  - Et tilknyttet projekt.
  - Mindst én milepæl, der er angivet under fanen **Fakturaplan** på siden **Projektkontraktlinje**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Gennemse projekter med fastprisomsætningsestimater
Hvis du vil have vist estimater for omsætning i fastprisprojekter, skal du udføre følgende trin:

1. I Dynamics 365 Finance-miljøet skal du gå til **Projektstyring og regnskab** > **Projekter** > **Omsætningsestimater på fast pris-projekter**.
2. Vælg det projekt, du vil have vist, og dobbeltklik på det **Estimerede projekt-id** for at åbne posten, og gennemse detaljerne for projektet.
3. Udvid fanen **Projekt**. Der vises ét projekt i gitteret for **Valgte projekter**. Systemet bruger dette som standardprojekt, da det er det projekt, der er knyttet til projektkontraktlinjen. 
4. Hvis du vil ændre tilknytningen, skal du vælge flere projekter og føje dem til gitteret **Valgte projekter**. Hvis der er valgt flere projekter i dette gitter, beregnes de færdiggørelsesgraden og omsætningsestimater for projektet sammen for alle de valgte projekter.

  Projektomkostninger, omsætningsprofil, omkostningsskabelon og periodekode kan angives manuelt. Hvis de ikke angives manuelt, anvendes standardværdierne under beregning af første estimat for projektet ved hjælp af de regler, der er konfigureret for projektomkostnings- og omsætningsprofiler.



[!INCLUDE[footer-include](../includes/footer-banner.md)]