---
title: Udviklers bemærkninger til godkendelser
description: Dette emne indeholder yderligere oplysninger til udviklere om, hvordan man arbejder med godkendelser.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483941"
---
# <a name="developer-notes-for-approvals"></a>Udviklers bemærkninger til godkendelser

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations inkluderer valideringslogik, der sikrer korrekt postoverførsel gennem godkendelsesfaserne. Korrekte postoverførsler sikrer: 

  - At alle understøttende rækker oprettes i relaterede tabeller, som f.eks. kladder og faktiske værdier.
  - Godkenderen er markeret som en **Projektgodkender** i projektet, før der fortsættes.
