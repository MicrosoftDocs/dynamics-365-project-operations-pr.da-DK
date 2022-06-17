---
title: Synkroniser projektkontrakter og projekter direkte fra Project Service Automation til Finance
description: I denne artikel beskrives den skabelon og de underliggende opgaver, der bruges til at synkronisere projektkontrakter og projekter direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: Yowelle
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 62a24f3af823d474cbb4d63f8d079c708256a75e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933853"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Synkroniser projektkontrakter og projekter direkte fra Project Service Automation til Finance 

[!include[banner](../includes/banner.md)]



I denne artikel beskrives den skabelon og de underliggende opgaver, der bruges til at synkronisere projektkontrakter og projekter direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

> [!NOTE] 
> Hvis du bruger Enterprise Edition 7.3.0, skal du installere KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflow for Project Service Automation til Finance

> [!NOTE]
> Før du kan bruge integrationsløsninger for Project Service Automation til Finance, skal du være bekendt med dataintegrationsfunktionen i Dynamics 365.

Integrationsløsningen for Project Service Automation til Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster med Project Service Automation og Finance. Den integrationsskabelon, der er tilgængelig sammen med dataintegrationsfunktionen, muliggør dataflow om projektkontrakter, projekter, projektkontraktlinjer og milepæle for projektkontraktlinje fra Project Service Automation til Finance.

I følgende illustration vises, hvordan dataene synkroniseres mellem Project Service Automation og Finance.

[![Dataflow til integration af Project Service Automation med Finance.](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Hvis du vil have adgang til den tilgængelige skabelon, skal du i Microsoft Power Apps Administration vælge **Projekter** og derefter vælge **Nyt projekt** i øverste højre hjørne for at vælge offentligt tilgængelige skabeloner.

Følgende skabeloner og underliggende opgaver bruges til at synkronisere projektkontrakter og projekter fra Project Service Automation til Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integration med Dynamics 365 Project Service Automation v2.x
- **Navnet på skabelonen i Dataintegration:** Projekter og kontrakter (Project Service Automation til Finance)
- **Navnet på opgaverne i projektet:**

    - Projektkontrakter Project Service Automation til Finance
    - Projekter Project Service Automation til Finance
    - Projektkontraktlinjer Project Service Automation til Finance
    - Milepæle for projektkontraktlinjer Project Service Automation til Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integration med Dynamics 365 Project Service Automation v3.x
Der er en skemaændring i Project Service Automation, som påvirker skabelonen for milepæle for projektkontraktlinjer, og brugen af skabelonens v2-version er nødvendig for at integrere Project Service Automation v3.x med Dynamics 365.

- **Navnet på skabelonen i Dataintegration:** Projekter og kontrakter (Project Service Automation 3.x til Finance) - v2
- **Navnet på opgaverne i projektet:**

    - Projektkontrakter Project Service Automation til Finance
    - Projekter Project Service Automation til Finance
    - Projektkontraktlinjer Project Service Automation til Finance
    - Milepæle for projektkontraktlinjer Project Service Automation til Finance

Inden synkroniseringen mellem projektkontrakter og projekter kan ske, skal du synkronisere kontiene.

## <a name="entity-set"></a>Objektsæt

| Project Service Automation       | Økonomi                                                |
|----------------------------------|--------------------------------------------------------|
| Ordrer                           | Objekt til integration af projektkontrakt                |
| Projekter                         | Objekt til integration af projekt                         |
| Ordrelinjer                      | Objekt til integration af projektkontraktlinje           |
| Milepæle for projektkontraktlinjer | Objekt til integration af projektkontraktlinjers milepæl |

## <a name="entity-flow"></a>Objektflow

Projektkontrakter administreres i Project Service Automation, og de synkroniseres med Finance som projektkontrakter. Som en del af integrationsskabelonen kan du angive integrationskilden i Finance for projektkontrakten.

Tids- og materiale- og fastprisprojekter administreres i Project Service Automation og synkroniseres til Finance som projekter. Som en del af skabelonintegrationen kan du angive integrationskilden for projektet i Finance. I øjeblikket er det kun tid- og materiale- og fastprisprojekter, der understøttes.


Projektkontraktlinjer administreres i Project Service Automation, og de synkroniseres med Finance som faktureringsregler for projektkontrakter. Hvis faktureringsmetoden adskiller sig fra standardprojekttypen, opdaterer synkroniseringen projekttypen for kontraktlinjeprojektet og projektgruppen.

Projektkontraktlinjers milepæle administreres i Project Service Automation, og de synkroniseres med Finance som faktureringsregler for projektkontrakters milepæle.

## <a name="project-service-automation-to-finance-integration-solution"></a>Integrationsløsning for Project Service Automation til Finance

Feltet **Projektkontrakt-id** er tilgængeligt på siden **Projektkontrakter**. Dette felt er gjort til en naturlig og unik nøgle, som understøtter integrationen.

Når der oprettes en ny projektkontrakt, oprettes der automatisk en værdi for **Projektkontrakt-id** ved hjælp af en nummerserie, hvis der ikke allerede findes en sådan. Værdien består af **ORD** efterfulgt af en stigende nummerserie og derefter et suffiks på seks tegn. Her er et eksempel: **ORD-01022-Z4M9Q0**.

Feltet **Projektnummer** er tilgængeligt på siden **Projekter**. Dette felt er gjort til en naturlig og unik nøgle, som understøtter integrationen.

Når der oprettes et nyt projekt, oprettes der automatisk en værdi for **Projektnummer** ved hjælp af en nummerserie, hvis der ikke allerede findes en sådan. Værdien består af **PRJ** efterfulgt af en stigende nummerserie og derefter et suffiks på seks tegn. Her er et eksempel: **PRJ-01049-CCNID0**.

Når integrationsløsningen for Project Service Automation til Finance anvendes, indstiller et opgraderingsscript feltet **Projektkontrakt-id** for eksisterende projektkontrakter og feltet **Projektnummer** for eksisterende projekter i Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Opsætning af forudsætninger og tilknytning

- Inden synkroniseringen mellem projektkontrakter og projekter kan ske, skal du synkronisere kontiene.
- I dit forbindelsessæt skal du tilføje en tilknytning for integrationsnøglefeltet for **msdyn\_afdelinger** til **msdyn\_navn \[Navn\]**. Du skal måske først tilføje et projekt til forbindelsessættet. Du kan finde flere oplysninger under [integration af data i Common Data Service til apps](/powerapps/administrator/data-integrator).
- I dit forbindelsessæt skal du tilføje en tilknytning for integrationsnøglefeltet for **msdyn\_projekter** til **msdynce\_projektnummer \[Projektnummer\]**. Du skal måske først tilføje et projekt til forbindelsessættet. Du kan finde flere oplysninger under [integration af data i Common Data Service til apps](/powerapps/administrator/data-integrator).
- **SourceDataID** for projektkontrakter og projekter kan opdateres til en anden værdi eller fjernes fra tilknytningen. Standardskabelons værdi er **Project Service Automation**.
- Tilknytningen **Betalingsbetingelser** skal opdateres, så den afspejler gyldige betalingsbetingelser i Finance. Du kan også fjerne tilknytningen fra projektopgaven. Tilknytningens standardværdi indeholder standardværdier for demonstrationsdata. I følgende tabel vises værdierne i Project Service Automation.

    | Værdi | Description   |
    |-------|---------------|
    | 0     | Netto 30 dage        |
    | 2     | 2% 10, netto 30 dage |
    | 3     | Netto 45 dage        |
    | 4     | Netto 60 dage        |

## <a name="power-query"></a>Power Query

Brug Microsoft Power Query til Excel til at filtrere data, hvis følgende betingelser er opfyldt:

- Du har salgsordrer i Dynamics 365 Sales.
- Du har flere afdelinger i Project Service Automation, og disse afdelinger knyttes til flere juridiske enheder i Finance.

Hvis du skal bruge Power Query, skal du følge disse retningslinjer:

- Skabelonen for projekter og kontrakter (PSA til Fin og Ops) har et standardfilter, der kun indeholder salgsordrer af typen **Arbejdsenhed (msdyn\_ordretype = 192350001)**. Dette filter er med til at sikre, at der ikke oprettes projektkontrakter for salgsordrer i Finance. Hvis du opretter din egen skabelon, skal du tilføje dette filter.
- Opret et Power Query-filter, der kun indeholder de kontraktorganisationer, der skal synkroniseres til den juridiske enhed for integrationsforbindelsessættet. F.eks. bør de projektkontrakter, som du har med den kontraktlige afdeling af Contoso US, synkroniseres med USSI's juridiske enhed, men de projektkontrakter, som du har med den kontraktlige afdeling af Contoso Global, skal synkroniseres med USMF's juridiske enhed. Hvis du ikke tilføjer dette filter til din opgavetilknytning, synkroniseres alle projektkontrakter med den juridiske enhed, der er defineret for forbindelsessættet, uanset kontraktafdelingen.

## <a name="template-mapping-in-data-integration"></a>Skabelon for tilknytning i dataintegration

> [!NOTE] 
> Felterne **Kundereference**, **AdresseBy**, **AdresseLandOmrådeId**, **AdresseBeskrivelse**, **Addresselinje1**, **Addresselinje2**, **AddresseRegion** og **AddressePostnummer** er ikke medtaget i standardtilknytningen for projektkontrakter. Du kan tilføje tilknytningerne, hvis du har brug for, at disse data synkroniseres i forbindelse med projektkontrakter.
>
> Felterne **Beskrivelse**, **Overordnetid**, **Projektgruppe**, **ProjektledersPersonalenummer** og **Projekttype** medtages ikke i standardtilknytningen for projekter. Du kan tilføje tilknytningerne, hvis du har brug for, at disse data synkroniseres i forbindelse med projekter.

I følgende illustrationer vises eksempler på tilknytninger mellem skabelonopgaver i dataintegration. I tilknytningen vises de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.

[![Tilknytning af projektkontraktskabelon.](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Tilknytning af projektskabelon.](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Tilknytning af skabelon for projektkontraktlinje.](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Tilknytning af skabelon for milepæl for projektkontraktlinje.](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Tilknytning af projektkontraktlinjers milepæle i skabelonen for projekter og kontrakter (PSA 3.x til Dynamics) - v2:

[![Tilknytning af milepæl for projektkontraktlinje med version 2 af skabelon.](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]