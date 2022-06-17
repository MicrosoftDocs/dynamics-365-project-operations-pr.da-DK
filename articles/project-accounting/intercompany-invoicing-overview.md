---
title: Oversigt over intern fakturering
description: Denne artikel indeholder oplysninger om og eksempler på intern fakturering af projekter.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd17f6542558bae9d4b97d0a92aefae52571cfa8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913567"
---
# <a name="intercompany-invoicing-overview"></a>Oversigt over intern fakturering

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Din organisation kan have flere afdelinger, datterselskaber og andre juridiske enheder, som overfører produkter og tjenester til hinanden i forbindelse med projekter. Den juridiske enhed, der leverer servicen eller produktet, kaldes *den juridiske udlånsenhed*. Den juridiske enhed, der modtager servicen eller produktet, kaldes *den juridiske låneenhed*.

I følgende illustration vises et typisk scenarie, hvor to juridiske enheder, Contoso Robotics USA (den juridiske låneenhed) og Contoso Robotics UK (den juridiske udlånsenhed) deler ressourcer for at levere et projekt til kunden, Adventure Works. I dette scenario er der indgået aftale med Contoso Robotics USA om at levere arbejdet til Adventure Works.

![Intern fakturering.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations bruger følgende flow til at behandle interne transaktioner:

1. Ressourcer fra den juridiske udlånsenhedspost for interne tids- eller udgiftstransaktioner ved at reservere tid og udgifter mod projekter i den juridiske låneenhed.
2. Omkostninger til tid og udgifter registreres i udlånsvirksomheden ved hjælp af det låntagende selskabs liste med enhedskostpris.
3. Ikke-fakturerede interne salgstransaktioenr registreres i det långivende selskab ved hjælp af det låntagende selskabs liste med enhedskostpris.
4. Ikke-faktureret omsætning registreres i det låntagende selskab ved hjælp af projektkontraktens salgsprisliste. Kunden kan faktureres, når der registreres ikke-faktureret omsætning. Kunden behøver ikke at vente til behandlingen af den interne faktura er fuldført.
5. Interne kundefakturaer oprettes periodisk i det långivende selskab. Fakturaerne oprettes manuelt eller ved hjælp af en periodisk automatiseret proces. Der kan oprettes en enkelt faktura for hver juridisk låneenhed, eller der kan oprettes separate fakturaer på hvert projekt.
6. Når den juridiske udlånsenhed bogfører den interne kundefaktura, oprettes den tilsvarende afventende leverandørfaktura i den juridiske låneenhed. Omkostningerne i den afventende leverandørfaktura registreres på projektets underfinanskonto, når fakturaen bogføres.

I følgende diagram illustreres den interne fakturering i sin sammenhæng med regnskabshændelser og de forventede posteringer i finanskladden.

![Internt flow.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Flere ressourcer

- [Konfigurer intern fakturering](configure-intercompany-invoicing.md)
- [Registrer interne transaktioner](create-intercompany-transactions.md)
- [Opret interne kunde- og kreditorfakturaer](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]