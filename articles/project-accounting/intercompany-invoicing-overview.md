---
title: Oversigt over intern fakturering
description: Dette emne indeholder oplysninger om og eksempler på intern fakturering for projekter.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002634"
---
# <a name="intercompany-invoicing-overview"></a>Oversigt over intern fakturering

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Din organisation kan have flere afdelinger, datterselskaber og andre juridiske enheder, som overfører produkter og tjenester til hinanden i forbindelse med projekter. Den juridiske enhed, der leverer servicen eller produktet, kaldes *den juridiske udlånsenhed*. Den juridiske enhed, der modtager servicen eller produktet, kaldes *den juridiske låneenhed*.

I følgende illustration vises et typisk scenario, hvor to juridiske enheder, Contoso Robotics USA (den låntagende juridiske enhed) og Contoso Robotics UK (den udlånende juridiske enhed) deler ressourcer med henblik på at levere et projekt til kunden, Adventure works. I dette scenario får Contoso Robotics USA til opgave at levere arbejdet til Adventure Works.

![Intern fakturering](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations bruger følgende flow til at behandle interne transaktioner:

1. Ressourcer fra den juridiske udlånsenhedspost for interne tids- eller udgiftstransaktioner ved at reservere tid og udgifter mod projekter i den juridiske låneenhed.
2. Omkostninger til tid og udgifter registreres i udlånsvirksomheden ved hjælp af det låntagende selskabs liste med enhedskostpris.
3. Ikke-fakturerede interne salgstransaktioenr registreres i det långivende selskab ved hjælp af det låntagende selskabs liste med enhedskostpris.
4. Ikke-faktureret omsætning registreres i det låntagende selskab ved hjælp af projektkontraktens salgsprisliste. Kunden kan faktureres, når der registreres ikke-faktureret omsætning. Kunden behøver ikke at vente til behandlingen af den interne faktura er fuldført.
5. Interne kundefakturaer oprettes periodisk i det långivende selskab. Fakturaerne oprettes manuelt eller ved hjælp af en periodisk automatiseret proces. Der kan oprettes en enkelt faktura for hver juridisk låneenhed, eller der kan oprettes separate fakturaer på hvert projekt.
6. Når den juridiske udlånsenhed bogfører den interne kundefaktura, oprettes den tilsvarende afventende leverandørfaktura i den juridiske låneenhed. Omkostningerne i den afventende leverandørfaktura registreres på projektets underfinanskonto, når fakturaen bogføres.

I følgende diagram illustreres den interne fakturering i sin sammenhæng med regnskabshændelser og de forventede posteringer i finanskladden.

![Internt flow](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Flere ressourcer

- [Konfigurer intern fakturering](configure-intercompany-invoicing.md)
- [Registrer interne transaktioner](create-intercompany-transactions.md)
- [Opret interne kunde- og kreditorfakturaer](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]