---
title: Ændring af objekter, kontrolelementer og brugergrænsefladen (Project service Automation 3.x)
description: I denne emne beskrives løsningsændringer for Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 48062eda1f524dd3ca0d5feccf11fd5577521275
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148726"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Ændring af objekter, kontrolelementer og brugergrænsefladen (Project service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Med udgivelsen af Microsoft Dynamics Project Service Automation (PSA) 3.x er der foretaget mange ændringer af objekterne, kontrolelementerne, visningerne og brugergrænsefladen. I dette emne findes oplysninger om disse vigtige ændringer:

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Overordnet-underordnet-relationer for salgsdokument, salgsdokumentlinje, salgsdokumentlinjedetaljer
I versioner af Dynamics 365 Project Service Automation (PSA), der er udgivet før version 3.0, er nogle af relationerne mellem salgsdokumenter, salgsdokumentlinjer og salgsdokumentlinjedetaljer blevet implementeret via strengfelter, der kan indeholde en strengrepræsentation af GUID for det relaterede objekt. Dette skyldes platformsbegrænsninger, der krævede vigtig brugerdefineret kode på server- og klientsiden af løsningen for at få disse relationer til at fungere på samme måde som typiske Dynamics CRM-objektrelationer og for at få strengfelter til at virke som opslagsfelter.

PSA 3.0 er blevet opdateret til at udnytte de nye objektrelationer mellem salgsdokument- og salgsdokumentlinjeobjekter.

Da opslagsfelter nu kan bruges til at angive referencer til objekter, er de felter, der opbevarede strengværdien af GUID for det relaterede objekt i tidligere versioner, ikke længere nødvendige, og de frarådes derfor. Den brugerdefinerede kode på klient- og serversiden, der håndterer relationer, der er defineret i ældre strengfelter, er også frarådet.

### <a name="entity-schema-changes"></a>Ændringer af objektskema
I følgende tabel vises en en-til-en-liste med de frarådede strengfelter og de nye opslagsfelter for objekterne. 

 Objekt |   Frarådet felt (streng) | Nyt felt (opslag)
--- | --- | ---
invoicedetail (fakturalinje) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (faktisk) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (fakturaplanlægning for projektkontraktlinje) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (milepæl i projektkontraktlinje) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (fakta) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (fakturalinjedetalje) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (kladdelinje) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (projektkontraktlinjes ressourcekategori) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (projektkontraktlinjedetalje) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (projektkontraktlinjes transaktionskategori) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (projektkontraktlinjes transaktionsklassificering) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (fakturaplanlægning for tilbudslinje) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (ressourcekategori for tilbudslinje) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (milepæl for tilbudslinje) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (tilbudslinjedetalje) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (transaktionskategori for tilbudslinje) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (transaktionsklassificering for tilbudslinje) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (ordrelinje) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Frarådede brugerdefinerede visninger og kontrolelementer
Følgende brugerdefinerede visninger og kontrolelementer og de relaterede artefakter er blevet frarådet.

- Visning af fakturerbarhed.
- Brugerdefinerede gitterkontrolelementer til visning af tilbudslinjedetaljer på siden **Projektoplysninger** for tilbudslinjen.
- Brugerdefinerede gitterkontrolelementer til visning af projektkontraktlinjedetaljer på siden **Projektoplysninger** for salgsordrelinjen.

> [!NOTE]
> Du kan finde en komplet liste over frarådede ressourcer under [Frarådede webressourcer i Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Unified Client Interface-appmodul
Med introduktionen af appmoduler til Unified Client interface (UCI) er PSA-oversigten over webstedet blevet fjernet fra systemet.  
Funktionalitet med relation til formularskift for salgsmulighed, tilbud, ordre, faktura er frarådet, da den ikke længere er nødvendig, fordi UCI-appmodulet kun indeholder PSA-versioner af formularerne.  

Følgende webressourcer er blevet frarådet:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Du kan finde en komplet liste over frarådede ressourcer under [Frarådede webressourcer i Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).


