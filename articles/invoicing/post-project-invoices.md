---
title: Oversigt over faktureringsprocessen
description: Dette emne indeholder oplysninger om en oversigt over processen for fakturering i Project Operations for ressource-/ikke-lagerbaserede scenarier.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089223"
---
# <a name="invoicing-process-overview"></a>Oversigt over faktureringsprocessen

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Project Operations for ressource/ikke-lagerbaserede scenarier tilbyder omfattende funktioner, der er skræddersyet til at passe til behovene for både projektlederen og regnskabsassistenten/projektets bogholder. I faktureringsprocessen administrerer projektlederen efterslæbet af projektfakturering, og regnskabsassistenten/projektets bogholder opretter en overensstemmende og korrekt kundeorienteret faktura.

![Diagram over faktureringsflow](./media/invoicing-flow.png)

I projektkontraktlinjen defineres faktureringsmetoden for tilknyttede projekttransaktioner. Når projektlederen godkender tids- og udgiftstransaktioner, registrerer systemet transaktionerne i objektet **Faktiske projektoplysninger** og sender oplysningerne til modulet **Projektstyring og regnskab** i Dynamics 365 Finance. Projektets bogholder gennemgår og bogfører derefter posterne ved hjælp af [Integrationskladden til Project Operations](../project-accounting/project-operations-integration-journal.md). Kladden omfatter vigtige regnskabsdetaljer for faktiske projektoplysninger, f.eks. fakturering, momsgruppe, fakturering af varemomsgruppe samt økonomiske dimensioner.

Projektlederen kan gennemse ikke-fakturerede salgstransaktioner ved hjælp af tids- og materialefaktureringsmetoden i [Efterslæbet af tids- og materialefakturering](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) og fastprisfakturering i [Fastprismilepæle](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Disse visninger giver dig mulighed for at filtrere og vælge transaktioner, der skal inkluderes i den næste faktureringscyklus, og derefter markere dem som **Klar til at blive faktureret**.

Du kan [oprette en proformafaktura manuelt](../proforma-invoicing/create-manual-proforma-invoice.md) eller bruge en [periodisk proces](../proforma-invoicing/configure-automated-invoice-creation.md). Projektlederen kan [justere en kladdeproformafaktura](../proforma-invoicing/manage-proforma-invoice.md) efter behov og derefter bekræfte den.

Den bekræftede proformafaktura sendes til modulet **Projektstyring og regnskab** i Finance. Projektets bogholder formaterer og opdaterer projektfakturaforslaget og bogfører og udskriver derefter dokumentet. Bogførte projektfakturaer registreres i finanskladden samt i kunde- og projektreskonti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]