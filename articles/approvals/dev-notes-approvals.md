---
title: Udviklers bemærkninger til godkendelser
description: Dette emne indeholder yderligere oplysninger til udviklere om, hvordan man arbejder med godkendelser.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996784"
---
# <a name="developer-notes-for-approvals"></a>Udviklers bemærkninger til godkendelser

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations omfatter valideringslogik, som sikrer korrekt postomstilling via godkendelsesfaserne. Korrekte postoverførsler sikrer: 

  - At alle understøttende rækker oprettes i relaterede tabeller, som f.eks. kladder og faktiske værdier.
  - Godkenderen er markeret som en **Projektgodkender** i projektet, før der fortsættes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]