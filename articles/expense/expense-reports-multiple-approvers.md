---
title: Udgiftsrapporter og flere godkendere
description: Dette emne indeholder oplysninger om udgiftsrapporter, der kræver godkendelse af mere end én person.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002049"
---
# <a name="expense-reports-and-multiple-approvers"></a>Udgiftsrapporter og flere godkendere

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Afhængigt af din organisations politikker for godkendelse af udgifter kan mere end én person godkende en indsendt udgiftsrapport. Når du konfigurerer arbejdsprocessen for godkendelse af udgiftsrapporter, kan du tilføje de arbejdsproceselementer, der indeholder opgaver eller trin for en eller flere godkendere af udgiftsrapporter. Du kan f.eks. kræve, at alle udgiftsrapporter skal godkendes af to forskellige personer, chefen for den medarbejder, der har indsendt rapporten, og kreditorkoordinatoren.

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