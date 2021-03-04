---
title: Opret interne kunde- og leverandørfakturaer
description: Dette emne indeholder oplysninger om, hvordan du opretter interne kunde- og leverandørfakturaer.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595448"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Opret interne kunde- og leverandørfakturaer

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

En projektbogholder i en juridisk udlånsenhed opretter en intern kundefaktura for de projektomkostninger, der overføres til den låneenhed. Når den interne kundefaktura er godkendt og bogført, sender den juridiske udlånsenhed den interne faktura til den juridiske låneenhed.

Projektbogholderen for den juridiske udlånsenhed kan konfigurere en batchproces til at oprette tilbagevendende interne fakturaer. Projektbogholderen angiver kriterierne såsom bestemte projekter til at oprette interne fakturaer i en batch.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Opret en intern kundefaktura manuelt til projekttransaktioner 

Brug denne procedure for at oprette en intern kundefaktura manuelt til projekttransaktioner. Søg efter timer, der er bogført af arbejdere på projekter i de juridiske låneenheder, og for udgifter, der er afholdt af din juridiske enhed på vegne af juridiske udlånsenheder. Du kan søge efter navn på juridiske enheder, projektkontraktnummer, projektnummer, datointerval eller en kombination af disse. Vælg de transaktioner, der skal tilføjes en intern faktura, i søgeresultaterne.

1. I Dynamics 365 Finance skal du gå til **Projektstyring og regnskab** > **Projektfakturaer** > **Interne kundefakturaer**. På listesiden **Interne kundefakturaer** skal du på i handlingsruden vælge **Ny.**
2. På siden **Opret intern faktura** skal du i feltet **Juridisk enhed** vælge en juridisk låneenhed.
3. Valgfrit: Angiv en bestemt projektkontrakt og et specifikt projektnummer.
4. Afgræns søgningen ved at vælge et datointerval. Angiv bestemte datoer i felterne **Startdato** og **Slutdato**. Det er kun interne transaktioner, der er bogført inden for dette datointerval, som vises i søgeresultaterne.
5. Angiv **Parameteren for projektets avancerede kladdelinje** til **Ja**, og vælg **Søg**.
6. Vælg de transaktioner, der skal inkluderes i det interne fakturaforslag, i søgeresultaterne, og vælg derefter **OK**.
7. På siden **Intern kundefaktura** vises de interne projekttransaktioner, som du har valgt i søgeresultaterne. Benyt følgende fremgangsmåde for at ændre transaktionerne, før du sender fakturaen til den juridiske låneenhed:
  
    1. Åbn siden **Opret fakturaforslag**. Vælg flere interne transaktioner for den aktuelle faktura, og vælg derefter **Tilføj linje**.
    2. Du kan fjerne en linje ved at markere den og derefter vælge **Fjern**.
    3. Få vist kommentarer, årsager, økonomiske dimensioner og andre oplysninger om en valgt linje i oversigtspanelet **Fakturalinjer**.
    
8. For at bogføre den interne kundefaktura skal du i handlingsruden vælge **Bogfør**.

> [!NOTE]
> Hvis organisationen kræver, at interne fakturaer gennemses, før de bogføres, kan en systemadministrator oprette en arbejdsproces for interne fakturaer. Hvis der ikke er konfigureret en arbejdsproces for interne fakturaer, kan du bogføre den interne faktura.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Opret et batchjob til interne fakturaer

Du kan oprette flere interne fakturaer på samme tid for alle juridiske låneenheder. Ved hjælp af søgefunktioner kan du f.eks. søge efter alle transaktioner, der er bogført af lånte arbejdere, og som er relateret til projekter, der administreres af andre juridiske enheder. For hver juridisk låneenhed kan du derefter oprette en intern faktura for de transaktioner, der er angivet i søgeresultaterne.

1. Gå til **Projektstyring og regnskab** > **Periodisk** > **Projektfakturaer** > **Opret interne kundefakturaer**.
2. På siden **Opret interne kundefaktura** skal du i feltet **Virksomhed** vælge en juridisk låneenhed, der skal faktureres. Hvis du ikke vælger en virksomhed, vises alle de transaktioner, der opfylder søgekriterierne, for alle juridiske låneenheder.
3. I **Opret en faktura pr.** skal du vælge, om du vil oprette en faktura for interne transaktioner, der er baseret på et projekt, eller som er baseret på en juridisk låneenhed.
4. Valgfrit: For at vælge et bestemt projekt og en bestemt projektkontrakt, der skal oprettes interne fakturaer for, skal du klikke på **Vælg**. På siden **Forespørgsel** skal du i feltet **Kriterier** vælge den projektkontrakt, det projektnummer eller begge og derefter vælge **OK**.
5. Under fanen **Batch** kan du konfigurere en batchproces for tilbagevendende interne fakturaer. Du kan finde flere oplysninger under [Indsend et job til batchbehandling fra en formular](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. For at bogføre de interne fakturaer skal du i handlingsruden vælge **Bogfør**.

> [!NOTE]
> Hvis organisationen kræver, at interne fakturaer gennemses, før de bogføres, kan en systemadministrator oprette en arbejdsproces for interne fakturaer. Hvis der ikke er konfigureret en arbejdsproces for interne fakturaer, kan du bogføre de interne fakturaer.

## <a name="post-the-intercompany-vendor-invoice"></a>Bogfør den interne leverandørfaktura

En projektbogholder i den juridiske låneenhed kan gennemgå interne afventende leverandørfakturaer, når den tilsvarende interne kundefaktura bogføres. I Finance skal du i den juridiske låneenhed gå til **Kreditor** > **Fakturaer** > **Afventende leverandørfaktura**. Det afventende fakturanummer stemmer overens med nummeret på den interne kundefaktura. Kontroller, at fakturaen er korrekt, og bogfør fakturaen. Bogføring af interne leverandørfakturaer opretter en underhovedbog på projektet og en transaktion i finanskladden, som afspejler transaktionsomkostningerne i den juridiske låneenhed.


[!INCLUDE[footer-include](../includes/footer-banner.md)]