---
title: Flere godkendere af en udgiftsrapport
description: Dette emne indeholder oplysninger om udgiftsrapporter, der kræver godkendelse af flere personer.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 383ce9eda6d0604ce0dd090e27a5c6fd569bd9e5
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685279"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Flere godkendere af en udgiftsrapport

Afhængigt af din organisations politikker for godkendelse af udgifter kan mere end én person godkende en udgiftsrapport, der er indsendt af en medarbejder. Når du konfigurerer arbejdsprocessen for godkendelse af udgiftsrapporter, kan du tilføje de arbejdsproceselementer, der indeholder opgaver eller trin for en eller flere godkendere af udgiftsrapporter. Du kan f.eks. kræve, at alle udgiftsrapporter først skal godkendes af chefen for den medarbejder, der har indsendt rapporten, og dernæst af kreditorkoordinatoren.

Hvis du beslutter dig for at kræve flere godkendere af udgiftsrapporter, kan du tilføje arbejdsproceselementer på en af følgende måder:

- Tilføj ét godkendelseselement, der indeholder ét trin. Trinnet kan f.eks. kræve, at der tildeles en udgiftsrapport til en brugergruppe, og at den godkendes af 50 procent af brugergruppens medlemmer.
- Tilføj ét godkendelseselement, der indeholder flere trin. Godkendelseselementet kan f.eks. indeholde følgende trin:

    1. Chefen for den medarbejder, der har indsendt udgiftsrapporten, godkender den.
    2. Kreditormedarbejderen bekræfter kvitteringerne og udgiftsrapportelementerne.
    3. Budgetejeren godkender udgiftsrapporten.

- Tilføj flere godkendelseselementer, der hver især har et trin. Du kan f.eks. tilføje et separat godkendelseselement for hvert af følgende trin:

    1. Medarbejderens leder godkender udgiftsrapporten.
    2. Budgetejeren godkender udgiftsrapporten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]