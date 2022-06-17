---
title: Udviklers bemærkninger til godkendelser
description: Denne artikel indeholder yderligere oplysninger til udviklere om, hvordan du arbejder med godkendelser.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924745"
---
# <a name="developer-notes-for-approvals"></a>Udviklers bemærkninger til godkendelser

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations omfatter valideringslogik, som sikrer korrekt postomstilling via godkendelsesfaserne. Korrekte postoverførsler sikrer: 

  - At alle understøttende rækker oprettes i relaterede tabeller, som f.eks. kladder og faktiske værdier.
  - Godkenderen er markeret som en **Projektgodkender** i projektet, før der fortsættes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]