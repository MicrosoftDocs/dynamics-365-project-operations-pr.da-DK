---
title: Udviklers bemærkninger til godkendelser
description: Dette emne indeholder yderligere oplysninger til udviklere om, hvordan man arbejder med godkendelser.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991659"
---
# <a name="developer-notes-for-approvals"></a>Udviklers bemærkninger til godkendelser

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations omfatter valideringslogik, som sikrer korrekt postomstilling via godkendelsesfaserne. Korrekte postoverførsler sikrer: 

  - At alle understøttende rækker oprettes i relaterede tabeller, som f.eks. kladder og faktiske værdier.
  - Godkenderen er markeret som en **Projektgodkender** i projektet, før der fortsættes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]