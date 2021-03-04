---
title: Projektfaser
description: Dette emne indeholder oplysninger om de projektstadier, der er tilgængelige i Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127466"
---
# <a name="project-stages"></a>Projektfaser

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Projektfaser er udformet, så de afspejler projektets tilstand, mens det skrider frem. Tilpasninger kan bruges til automatisk at opdatere faserne med forretningsprocesforløb, Power Automate eller plug-in-udvidelser.

Følgende faser er defineret i standardforretningsprocesforløbet:

- Nyt
- Tilbud
- Abonnement
- Levér
- Afsluttet
- Luk 

## <a name="new"></a>Nyt

Når du opretter et projekt, indstilles projektfasen til **Ny**. Hvis projektet blev oprettet ud fra en skabelon, kan det indeholde planlægnings-, estimat- og teamdata. Ellers er det en kontur for projektet, og de resterende komponenter skal angives.

## <a name="quote"></a>Tilbud

Når du knytter et projekt til et tilbud, eller når du opretter et projekt fra et tilbud, angives projektfasen til **Tilbud**, og de forventede start- og slutdatoer opdateres. Når projektet befinder sig i fasen **Tilbud**, vises oplysninger om tilbuddet under fanen **Salg** på siden **Projektenhed**.

## <a name="plan"></a>Planlæg

Når du vinder et tilbud, der er knyttet til et projekt, og projektet flyttes til fasen **Kontrakt**, opdateres projektfasen til **Plan**. Når projektet befinder sig i fasen **Plan**, vises oplysninger om kontrakten på fanen **Projektenhed**.

## <a name="deliver"></a>Levér

Når projektplanen er fuldført, og du er klar til at starte projektet, skal projektlederen opdatere projektfasen for **Levér** for at vise, at projektet er startet.

## <a name="complete"></a>Fuldført 

Når arbejdet på projektet er fuldført, kan projektlederen opdatere fasen til **Fuldført.** Ved at opdatere projektfasen til **Fuldført** indikerer projektlederen, at arbejdet er 100 % fuldført, men at projektet holdes åbent, så alle uafsluttede tids- eller udgiftsposter kan registreres.

## <a name="close"></a>Luk

Når alle transaktioner er registreret for projektet, kan projektlederen opdatere fasen til **Luk.** På dette tidspunkt kan der ikke registreres flere transaktioner, og projektet får indstillingen skrivebeskyttet.



[!INCLUDE[footer-include](../includes/footer-banner.md)]