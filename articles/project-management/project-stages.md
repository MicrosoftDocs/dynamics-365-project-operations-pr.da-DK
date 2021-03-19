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
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286781"
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