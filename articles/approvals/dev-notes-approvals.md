---
title: Udviklers bemærkninger til godkendelser
description: Dette emne indeholder yderligere oplysninger til udviklere om, hvordan man arbejder med godkendelser.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: c02778c4ed79a8750d207b5870300ebf0f479be7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579713"
---
# <a name="developer-notes-for-approvals"></a>Udviklers bemærkninger til godkendelser

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations omfatter valideringslogik, som sikrer korrekt postomstilling via godkendelsesfaserne. Korrekte postoverførsler sikrer: 

  - At alle understøttende rækker oprettes i relaterede tabeller, som f.eks. kladder og faktiske værdier.
  - Godkenderen er markeret som en **Projektgodkender** i projektet, før der fortsættes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]