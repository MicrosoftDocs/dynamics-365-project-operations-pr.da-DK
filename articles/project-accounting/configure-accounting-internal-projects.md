---
title: Konfigurer regnskab for interne projekter
description: Dette emne indeholder oplysninger om, hvordan du konfigurerer regnskabspraksis for interne projekter i Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9da72d8dbf720e380a49a1010caca472ee024783
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597837"
---
# <a name="configure-accounting-for-internal-projects"></a>Konfigurer regnskab for interne projekter

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Interne projekter gør det muligt for virksomheder at spore omkostninger i forbindelse med aktiviteter, der ikke faktureres til en kunde. Som eksempel på interne projekter kan nævnes:

- Udvikling af et produkt, f.eks. en mobilapp, og sporing af de omkostninger, der er forbundet med udviklingen.
- Administrering af tid og omkostninger før salg. Dette interne før salgsprojekt kan senere konverteres til et fakturerbart projekt, hvis tilbuddet bliver vundet.

Alle projekter, der ikke er knyttet til en kontrakt i Dynamics 365 Project Operations, behandles som interne. Projektomkostnings- og indtægtsprofiler anvendes ikke til at fastsætte regnskabsreglerne for projektet. Interne projektomkostninger bogføres altid ved hjælp af driftsprincipper. Hovedbogskonti til bogføring defineres på siden **Opsætning af bogføring i hovedbog**.

- Tidstransaktioner bogføres ved at debitere kontoen **Omkostning** og kreditere kontoen **Lønfordeling**.
- Udgiftstransaktioner bogføres ved at debitere kontoen **Omkostning** og kreditere kontoen **Modkontoen for udgifter**.
- Varetransaktioner bogføres ved at debiterede kontoen **Omkostninger** og kreditere kontoen **Omkostning - vare**.

Hvis projektet er knyttet til en projektkontrakt, tilbageføres alle akkumulerede transaktioner automatisk, når der er bogført transaktioner, og der oprettes nye fakturerbare transaktioner i systemet. De fakturerbare transaktioner følger de regnskabsregler, der er defineret i de respektive udgifts- og indtægtsprofiler for projektet.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
