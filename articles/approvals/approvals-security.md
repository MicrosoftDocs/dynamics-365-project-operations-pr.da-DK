---
title: Sikkerhed og godkendelser
description: Denne artikel indeholder oplysninger om konfiguration af sikkerhed i forbindelse med arbejdet med godkendelser i Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841916"
---
# <a name="security-and-approvals"></a>Sikkerhed og godkendelser

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Microsoft Dynamics 365 Project Operations bruger to sikkerhedsroller til at tillade godkendelse af tids-, udgifts- og materialeposter:

- Projektgodkender
- Projektgodkenderadministrator

## <a name="project-approver"></a>Projektgodkender

Du skal have sikkerhedsrollen **Projektgodkender** for at godkende tids-, udgifts- og materialeposter for projektet. Du skal også have adgang til de relevante tilknyttede objekter, f.eks. **Projekt**. Denne adgang kan tildeles af en person, der har rollen **Projektleder**. Derudover skal du være teammedlem af projektet og være markeret som godkender.

Hvis du vil godkende poster, der ikke er projektposter, skal du være afsenderens leder.

## <a name="project-approver-admin"></a>Projektgodkenderadministrator

> [!NOTE]
> Funktionen [Godkendelsessæt](approval-sets.md) skal aktiveres, før du kan bruge funktionen Projektgodkenderadministrator.

Sikkerhedsrollen **Projektgodkenderadministrator** giver brugere mulighed for at tilsidesætte politikker, så de kan godkende poster på tværs af alle projekter. Tildeling af denne rolle tilsidesætter den valideringslogik, der kræver teammedlemskab, og som er markeret som godkender. Du skal have adgang til de relevante relaterede tabeller, f.eks. **Projekt**, via de sikkerhedsroller, der er tildelt til dig.

SYSTEM-brugerkonteksten tilsidesætter validering på samme måde som sikkerhedsrollen Projektgodkenderadministrator.
