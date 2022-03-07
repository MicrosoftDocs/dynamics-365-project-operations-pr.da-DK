---
title: Typer af projektfaser
description: Dette emne indeholder oplysninger om projektfaser.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e4f50d12b4f0bf1586d0a5702bcd38b891590bffe0d3f9661d7f5d170877b54e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996879"
---
# <a name="project-stage-types"></a>Typer af projektfaser 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektfaser er udformet, så de afspejler projektets tilstand, mens det skrider frem. Tilpasninger kan bruges til automatisk at opdatere faserne med forretningsprocesforløb, Power Automate eller plug-in-udvidelser.

Følgende faser er defineret i standard-BPF-forløbet:

- Nyt
- Tilbud
- Planlæg
- Levér
- Afsluttet
- Luk 

## <a name="new"></a>Ny

Når du opretter et projekt, indstilles projektfasen til **Ny**. Hvis projektet blev oprettet ud fra en skabelon, kan det indeholde planlægnings-, estimat- og teamdata. Ellers er det blot en kontur for projektet, og de resterende komponenter skal angives.

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