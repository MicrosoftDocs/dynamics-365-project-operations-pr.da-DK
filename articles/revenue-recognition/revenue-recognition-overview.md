---
title: Oversigt over omsætningsanerkendelse
description: Denne artikel indeholder oplysninger om omsætningsgenkendelse i Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 22486693226256f765589b272e6df36aceaf9c1c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926263"
---
# <a name="revenue-recognition-overview"></a>Oversigt over omsætningsanerkendelse

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

I Dynamics 365 Project Operations varierer principperne for omsætningsanerkendelse på baggrund af den valgte faktureringsmetode for et projekt eller en del af projektet. Denne artikel indeholder oplysninger om omsætningsgenkendelse i Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transaktioner, der bogføres i regnskabet, og som anvender faktureringsmetoden for tids- og materialer

- Omkostnings- og omsætningsanerkendelse er forbundet. Transaktionsomkostninger og ikke-fakturerede salg bogføres ved hjælp af [Integrationskladden til Project Operations](../project-accounting/project-operations-integration-journal.md).
- Projektomkostnings- og indtægtsprofil bestemmer, om ikke-fakturerede salgstransaktioner bogføres i finanskladden. Hvis **Periodisering af omsætning** er valgt, bruger systemet kontiene **Salgsværdien for IGVA** og **Salgsværdi af periodiseret omsætning** under bogføringen. Følgende eksempel viser denne metode.  

  | Transaktionstype | Debet/kredit | Beløb |
  | --- | --- | --- |
  | Salgsværdi af IGVA | Debet | 100 |
  | Salgsværdi af periodiseret omsætning | Kredit | 100 |

- Omsætning anerkendes under fakturering. Systemet bruger kontoen **Faktureret omsætning** under bogføringen. Følgende eksempel viser denne metode.  

  | Transaktionstype | Debet/kredit | Beløb |
  | --- | --- | --- |
  | Kundesaldo | Debet | 120 |
  | Skyldig moms | Kredit | 20 |
  | Faktureret omsætning | Kredit | 100 |

- Hvis omsætningen blev periodiseret, da det ikke-fakturerede salg blev bogført, tilbageføres den periodiserede omsætning ved fakturering.

  | Transaktionstype | Debet/kredit | Beløb |
  | --- | --- | --- |
  | Salgsværdi af IGVA | Kredit | 100 |
  | Salgsværdi af periodiseret omsætning | Debet | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transaktioner, der bogføres i regnskabet, og som anvender faktureringsmetoden for fast pris

- Omkostnings- og omsætningsanerkendelse er adskilt. Transaktionsomkostninger bogføres ved hjælp af [Integrationskladden til Project Operations](../project-accounting/project-operations-integration-journal.md). Der oprettes ikke ikke-fakturerede salgstransaktioner.
- Omsætning kan anerkendes under fakturering, hvis projektomkostnings- og omsætningsprofilen har **Princip, der bruges til projektfuldførelsesberegninger**, angivet til **Ingen IGVA**. Brug kun denne metode til kortsigtede, enkle projekter.
- Omsætning kan anerkendes ved hjælp af estimater for fastprisomsætning enten med metoden **Fuldført kontrakt** eller metoden **Omsætningsanerkendelse ved hjælp af procentvis færdiggørelse**.

## <a name="additional-resources"></a>Flere ressourcer
[Konfigurer regnskab for fakturerbare projektatikler](../project-accounting/configure-accounting-billable-projects.md)

[Omsætningsestimat for projekter med fast pris](rev-rec-percentage-completion-method.md)

[Administrer omsætningsestimater](rev-rec-completed-contract-method.md)

[Metoder til færdiggørelsesomkostninger](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]