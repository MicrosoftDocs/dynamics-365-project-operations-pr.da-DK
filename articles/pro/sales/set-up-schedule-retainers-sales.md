---
title: Konfigurer en plan for forskudshonorarer
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer en plan for forskudshonorar i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d90781407f11c93b9fb9e0cd2446e102e216b8db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272247"
---
# <a name="set-up-a-retainer-schedule"></a>Konfigurer en plan for forskudshonorarer

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Planer for forskudshonorarer konfigureres på siden **Projektkontrakt** i Dynamics 365 Project Operations.

1. På siden **Projektkontrakt** skal du på fanen **Forskud og forskudshonorarer** vælge **Konfigurer plan for forskudshonorar**.
2. På den åbne dialogside vises følgende felter i tabellen. Tabellen giver en ide om, hvordan de indtastede værdier påvirker eller influerer på den oprettede plan for forskudshonorar.

| Felt | Beskrivelse | Downstream-virkning |
| --- | --- | --- |
| Projektkontraktkunde | Kunden på kontrakten, som dette forskudshonorar eller forskud skal faktureres til. | Hvis der er flere kunder på kontrakten, og du har brug for at fakturere hver af dem et bestemt forskudshonorarer eller forskudsbeløb, skal du manuelt oprette en faktura for hver enkelt kunde. |
| Start af planlægning af forskudshonorarer | Angiv startdatoen for planen for forskudshonorar. | Denne dato kan ikke være den dato, hvor det første forskudshonorar eller forskud oprettes. Den dato, hvor det første forskudshonorar eller forskud oprettes, påvirkes også af fakturafrekvensen. |
| Slut på planlægning af forskudshonorarer | Angiv slutdatoen for planen for forskudshonorar. | Denne dato kan ikke være den dato, hvor det sidste forskudshonorar eller forskud oprettes. Den dato, hvor det sidste forskudshonorar eller forskud oprettes, påvirkes også af fakturafrekvensen. |
| Antal forskudshonorarer, der skal oprettes | Når du angiver antallet af forskudshonorarer, der skal oprettes, bruger systemet startdatoen og hyppigheden til at oprette antallet i dette felt. | Når dette felt opdateres manuelt, ignorerer systemet værdien i feltet **Slutdato for plan for forskudshonorar**, og der oprettes i stedet et bestemt antal forskudshonorarer eller forskud. |
| Fakturahyppighed | Hvor ofte opretter programmet forskudshonorar og forskud. | Denne værdi påvirker antallet af forskudshonorarer og forskud og de oprettede datoer direkte. |
| Samlet beløb | Det samlede beløb er det beløb, der er opdelt i individuelle forskudshonorar eller forskud, som vil blive oprettet. | Dette felt har ingen afledt virkning. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]