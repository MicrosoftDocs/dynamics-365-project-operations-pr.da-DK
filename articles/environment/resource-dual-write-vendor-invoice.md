---
title: Integration af leverandørfaktura
description: Dette emne indeholder oplysninger om integration af leverandørfaktura i Project Operations.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8650eed2230b99b821c1635fdc88252bb65c5583
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591168"
---
# <a name="vendor-invoice-integration"></a>Integration af leverandørfaktura

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

Projektrelaterede indkøb i Dynamics 365 Project Operations kan registreres ved at gå til **Kreditorer** > **Fakturaer** > **Afventende leverandørfakturaer** og anvende et afventende leverandørfakturadokument. Du kan finde flere oplysninger i [Køb ikke-lagerførte materialer ved hjælp af en afventende leverandørfaktura](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Før du bruger den funktion, der er beskrevet i dette emne, skal du gennemse og anvende de påkrævede konfigurationer. Du kan finde flere oplysninger i [Aktiver ikke-lagerførte materialer og afventende leverandørfakturaer](../procurement/configure-materials-nonstocked.md).

I Project Operations bogføres projektrelaterede leverandørfakturaer ved hjælp af særlige bogføringsregler:

- Projektrelaterede omkostninger (herunder ikkeinddrivelig moms) bogføres ikke straks til projektomkostningskontoen i hovedbogen. Omkostningen bogføres i stedet for på **Indkøbsintegrationskontoen**. Denne konto er konfigureret i **Projektstyring og regnskab** > **Opsætning** > **Projektstyrings- og regnskabsparametre** på fanen **Project Operations på Dynamics 365 Customer Engagement**.
- Dobbelteskrivning synkroniserer leverandørfakturaoplysninger med Microsoft Dataverse ved hjælp af følgende tabeltilknytning:

     - **Integrationsobjekt for eksport af projektleverandørfaktura i Project Operations (msdyn_projectvendorinvoices)**: Denne tabeltilknytning synkroniserer oplysninger i leverandørfakturaens overskrift. Kun leverandørfakturaer med mindst én linje, der indeholder et projekt-id, synkroniseres med Dataverse.
     - **Integrationsobjekt for eksport af projektleverandørfakturalinje i Project Operations (msdyn_projectvendorinvoicelines)**: Denne tabeltilknytning synkroniserer oplysninger i leverandørfakturalinjen. Kun linjer, der indeholder et projekt-id, synkroniseres med Dataverse.

     > [!NOTE]
     > Oplysninger om leverandørens faktura i Dataverse kan ikke redigeres.

Momsregnskaber, leverandørregnskaber og andre økonomiske bogføringer registreres efter behov i Dynamics 365 Finance, når leverandørfakturaen er bogført.

![Integration af leverandørfaktura.](media/DW7VendorInvoice.png)

Når der skrives poster til et objekt for **Leverandørfaktura** i Dataverse, starter en automatisk godkendelsesproces for posterne. Den automatiserede godkendelsesprocesstatus kan gennemses i Dataverse, hvis det er nødvendigt, ved at gå til **Avancerede indstillinger** > **System** > **Systemjob**. Når godkendelsen er fuldført, opretter systemet materialetransaktionsklasseposter i objektet **Faktiske værdier**.

Materialerelaterede faktiske værdier behandles derefter ved hjælp af dobbeltskrivning-tabeltilknytningen **Integration af faktiske værdier i Project Operations (msdyn_faktiske)**. Du kan finde flere oplysninger under [Projektestimater og faktiske værdier](resource-dual-write-estimates-actuals.md).

Den periodiske proces **Importér fra midlertidig lagring** opretter leverandørfakturarelaterede integrationskladdelinjer til Project Operations. Modregningskontoen bruges som standard til indkøbsintegrationskontoen. Når integrationskladden er bogført, ryddes kontosaldoen for leverandørfakturatransaktionen, og linjebeløbet flyttes til projektomkostningskontoen. Underkonto til projekttransaktioner oprettes også til downstream-fakturering og omsætningsgenkendelse.
