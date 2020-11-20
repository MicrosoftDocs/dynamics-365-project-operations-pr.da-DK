---
title: Konfigurer arbejdsprocesser for udgiftsstyring
description: Du kan konfigurere en arbejdsproces, der bruges til at gennemse og godkende dokumenter for rejser og udgifter.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127691"
---
# <a name="set-up-workflows-for-expense-management"></a>Konfigurer arbejdsprocesser for udgiftsstyring

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Du kan konfigurere en arbejdsproces til at gennemse og godkende dokumenter for rejser og udgifter. Du kan definere arbejdsprocesser til udgiftsrapporter, rejserekvisitioner og anmodninger om kontantforskud.

En arbejdsproces repræsenterer en forretningsproces, der definerer, hvordan et dokument bevæger sig gennem systemet. Arbejdsprocessen angiver også, hvem der skal udføre en opgave eller godkende et dokument. Der er flere fordele ved at bruge arbejdsprocessystemet i din organisation:

- **Ensartede processer** : Du kan definere godkendelsesprocessen for bestemte dokumenter, f.eks. indkøbsrekvisitioner og udgiftsrapporter. Arbejdsprocessystemet er med til at sikre, at dokumenter behandles og godkendes på en ensartet og effektiv måde.
- **Processynlighed** : Du kan spore status, historik og performanceværdier for en bestemt arbejdsprocesforekomst. Det hjælper dig med at afgøre, om der skal foretages ændringer af arbejdsprocessen for at forbedre effektiviteten.
- **Centraliseret opgaveliste** : Brugere kan se en centraliseret opgaveliste for at få vist de arbejdsprocesopgaver og -godkendelser, de har fået tildelt. 

## <a name="workflow-types"></a>Arbejdsprocestyper

I følgende tabel vises de arbejdsprocestyper, som du kan oprette i **Udgiftsstyring**.


|              <strong>Skriv</strong>              |                   <strong>Brug denne type for at</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Automatisk godkende udgiftsrapporter</strong> |            Opret godkendelsesarbejdsprocesser for udgiftsrapporter.             |
|  <strong>Automatisk bogføring af udgiftsrapporter</strong>   |        Opret automatiske arbejdsprocesser for bogføring af udgiftsrapporter.        |
|       <strong>Udgiftslinjeelement</strong>        |     Opret godkendelsesarbejdsprocesser for linjeelementer i udgiftsrapporter.      |
| <strong>Automatisk bogføring af udgiftslinjeelement</strong> | Opret automatiske arbejdsprocesser for bogføring af linjeelementer i udgiftsrapporter. |
|       <strong>Rejserekvisition</strong>       |          Opret godkendelsesarbejdsprocesser for rejserekvisitioner.           |
|      <strong>Anmodning om kontantforskud</strong>      |         Opret godkendelsesarbejdsprocesser for anmodninger om kontantforskud.          |
|        <strong>Moms- og skatteinddrivelse</strong>        | Opret godkendelsesarbejdsprocesser for inddrivelse af moms.  |
