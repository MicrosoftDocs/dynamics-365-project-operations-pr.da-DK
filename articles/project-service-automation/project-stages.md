---
title: Projektfaser
description: Dette emne indeholder oplysninger om projektfaser.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750519"
---
# <a name="project-stages"></a>Projektfaser 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektfaserne opdateres, så de afspejler projektets tilstand, mens det skrider frem. I standardforretningsprocesforløbet opdateres nogle faser i projektet automatisk, mens andre opdateres manuelt af projektlederen. 

Følgende faser er defineret i standard-BPF-forløbet:

- Ny
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

Når arbejdet på projektet er fuldført, kan projektlederen opdatere fasen til **Fuldført.** Ved at opdatere projektfasen til **Fuldført**indikerer projektlederen, at arbejdet er 100 % fuldført, men at projektet holdes åbent, så alle uafsluttede tids- eller udgiftsposter kan registreres.

## <a name="close"></a>Luk

Når alle transaktioner er registreret for projektet, kan projektlederen opdatere fasen til **Luk.** På dette tidspunkt kan der ikke registreres flere transaktioner, og projektet får indstillingen skrivebeskyttet.
