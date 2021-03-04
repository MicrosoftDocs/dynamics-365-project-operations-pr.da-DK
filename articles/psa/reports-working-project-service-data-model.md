---
title: Arbejde med Project Service Automation-datamodellen
description: Dette emne indeholder oplysninger om, hvordan du arbejder med datamodellen.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8c212ef2c9fd9dcd6be0b8f0a31aa5a948176bc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147646"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Arbejde med Project Service Automation-datamodellen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation udvider andre app-objekter og introducerer sine egne objekter i Common Data Service-datamodellen. I dette emne beskrives nogle af de objekter, du møder i typiske PSA-rapporteringsscenarier.

## <a name="reporting-on-opportunities"></a>Rapportering om salgsmuligheder

Project service Automation udvider objektet Dynamics 365 Sales **mulighed** ved at tilføje felter, der aktiverer projektbaserede scenarier. Disse felter identificeres ved hjælp af et skemanavn, der indledes med **msdyn.\_** Et nyt felt, der er vigtigt for at rapportere om PSA-salgsmuligheder, er **Ordretype**. En værdi for **Arbejdsbaseret,** der er baseret på dette felt, angiver, at salgsmuligheden er en PSA-mulighed. Andre felter, der er føjet til objektet, omfatter **Kontraktorganisation**, som registrerer den organisation, der er indehaver af salgsmuligheden, og **Account Manager**, som registrerer navnet på den chef, der er ansvarlig for salgsmuligheden.

Objektet **Salgsmulighedslinjer** indeholder også felter, der er relateret til Project Service. **Faktureringsmetode** angiver, om der skal faktureres for salgsmulighedslinjen på grundlag af tidspunkt og materiale, eller det skal ske på grundlag af fast pris, og **Projekt** registrerer navnet på det projekt, der giver grundlag for salgsmuligheden. Andre felter, hvor du kan rapportere om registreringsomkostninger og kundens budgetterede beløb for linjeelementet.

## <a name="reporting-on-quotes"></a>Rapportering om tilbud

PSA udvider salgsobjektet **Tilbud** ved at tilføje projektrelaterede felter. **Ordretype** adskiller PSA-tilbud fra ikke-PSA-tilbud. En værdi for **Arbejdsbaseret,** der er baseret på dette felt, angiver, at tilbuddet er et PSA-tilbud. Andre felter, der kan være relevante for rapportering om PSA-tilbud, omfatter beløbsfelter som f.eks. **Fakturerbare omkostninger**, **Ikke-fakturerbare omkostninger**, **Bruttoavance**, **Estimater** og **Budget**. Andre nyttige felter angiver, om tilbuddet er rentabelt, om det vil blive fuldført efter planen, og om det lever op til kundens budgetforventninger.

PSA udvider også salgsobjektet **Ordrelinje**. Et af de felter, som PSA tilføjer, er **Faktureringsmetode**, som angiver, hvordan tilbudslinjen bliver faktureret (tid og materialer eller fast pris). Andre felter, der er føjet til objektet, registrerer det relaterede projekt, der understøtter tilbudslinjen, fakturering, omkostninger og budget.

PSA føjer også nye tilbudsrelaterede objekter til Dynamics 365-datamodellen. Her er nogle eksempler:

- **Tilbudslinjedetalje** – Dette objekt indeholder detaljer om projektestimatet i tilbudslinjen. Den indeholder to poster for hver tilbudslinje. Den ene post indeholder oplysninger om omkostninger og omkostningsdetaljer i tilbudslinjen, og den anden post indeholder salgsbeløbet og salgsdetaljer i tilbudslinjen.
- **Fakturaplanlægning for tilbudslinje** – Dette objekt indeholder faktureringsplanen for tilbudslinjen. Denne plan genereres på baggrund af den faktureringshyppighed, der er tildelt tilbudslinjen.
- **Milepæl for tilbudslinje** – Dette objekt indeholder milepæle for faktureringen for tilbudslinjer med fast pris.
- **Analysehierarki for tilbudslinje** – Dette objekt indeholder økonomiske oplysninger om tilbudslinjen. Disse oplysninger kan være nyttige for rapportering af tilbudte salgsbeløb og anslåede omkostningsbeløb efter forskellige dimensioner.

Andre objekter, som PSA føjer til tilbud, er **Projektprisliste for tilbudslinje**, **Ressourcekategori for tilbudslinje** og **Transaktionskategori for tidbudslinje**.

![Diagram, der viser tilbud, tilbudslinje og projektrelationer](media/PS-Reporting-image2.png "Diagram, der viser tilbud, tilbudslinje og projektrelationer")

## <a name="reporting-on-project-contracts"></a>Rapportering om projektkontrakter

PSA udvider det salgsobjektet **Ordre**, der bruges, når der registreres projektkontrakter. Der tilføjes et vigtigt nyt felt, **Ordretype**, der identificerer kontrakten som en PSA-projektkontrakt i stedet for en salgsordre. En værdi for **Arbejdsbaseret,** der er baseret på dette felt, angiver, at ordren er en PSA-projektkontrakt. Andre nye felter, der er føjet til objektet **Ordre**, registrerer oplysninger om omkostninger, PSA-kontraktstatus og den organisation, der ejer kontrakten.

PSA udvider også objektet **Salgsordrelinje**. Blandt de felter, der tilføjes, er felter, der registrerer faktureringsmetoden (tid og materialer eller fast pris), kundens budgetterede beløb og det underliggende projekt.

PSA tilføjer også nye objekter, der er udviklet til projektkontrakter. Her er nogle eksempler:

- **Projektkontraktlinjedetalje** – Dette objekt indeholder detaljer på linjeniveau, der er akkumuleret op til kontraktlinjebeløbet. Disse kan være lige så detaljerede som linjeelementer, der genereres fra en projektplan på opgaveniveau.
- **Fakturaplanlægning for projektkontraktlinje** – Dette objekt indeholder den faktureringsplan, der genereres på baggrund af den fakturafrekvens, der er tildelt til kontraktlinjen.
- **Kontraktmilepæl** – Dette objekt indeholder faktureringsmilepæle for kontraktlinjer, hvor fakturering sker ud fra faste priser.

Andre objekter, som PSA føjer til kontrakter, er **Projektprisliste for projektkontaktlinje**, **Ressourcekategori for projektkontraktlinje** og **Transaktionskategori for projektkontraktlinje**.

![Diagram, der viser ordre, ordrelinje og projektrelationer](media/PS-Reporting-image3.png "Diagram, der viser ordre, ordrelinje og projektrelationer")

## <a name="reporting-on-projects"></a>Rapportering om projekter

Objektet **Projekter** og de tilhørende objekter er eksklusive for PSA. **Projekt** er det objekt på øverste niveau, der bruges til at registrere arbejdet og omkostningssiden for operationer. Her er en liste over tilknyttede objekter:

- **Projektgruppemedlem** – Dette objekt indeholder oplysninger om de reservérbare ressourcer, der er tildelt til projektet. Disse ressourcer kan være reserverbare generiske ressourcer, eller de kan have navnet reserverbare ressourcer, der enten er angivet af projektlederen eller er genereret ud fra projektplanen.
- **Projektopgave** – Dette objekt indeholder de opgaver, der udgør projektplanen eller tidsplanen.
- **Ressourcetildeling** – Dette objekt indeholder opgavetildelingen for den reserverbare ressource.
- **Ressourcekrav** – Dette objekt indeholder kravene til alle generiske ressourceteammedlemmer.
- **Estimat** og **Estimatlinje** – Disse objekter har en overskrift/linjerelation og indeholder udgiftsestimater for projektet. Opgaveestimater gemmes i objektet **Ressourceestimat**.

![Diagram, der viser ressource, krav og projektrelationer](media/PS-Reporting-image4.png "Diagram, der viser ressource, krav og projektrelationer")

## <a name="reporting-on-resources"></a>Rapportering om ressourcer

Projektressourcer bruger de **Reserverbare ressource**-objekter fra Universal Resource Scheduling (URS), der deles med andre apps, f.eks. Microsoft Dynamics 365 Field Service. Her er en liste over de objekter, du måske skal bruge, når du rapporterer om projektressourcer:

- **Reserverbar ressource** – Dette objekt repræsenterer den bruger, kontaktperson, standardressource, firmagruppe eller udstyr, der bruges i projektteamet.
- **Egenskaber for reserverbare ressourcer** – Dette objekt omfatter færdigheder, certificeringer eller uddannelse af ressourcen. Egenskaberne kan have klassificeringsværdier, der er defineret af klassificeringsmodellen.
- **Kategori af reserverbare ressourcer** – Dette objekt repræsenterer rollen for den reserverbare ressource.
- **Reserverbare ressourcereservationer** – Dette objekt repræsenterer den tid, der er reserveret til projekterne for ressourcen. Hver reservation har både et overskriftsobjekt og linjeobjekter, og de enkelte linjer har en status, der repræsenterer statussen for reservationen.

![Diagram, der viser relationer for reserverbare ressourceegenskaber](media/PS-Reporting-image5.png "Diagram, der viser relationer for reserverbare ressourceegenskaber")

## <a name="reporting-on-actual-transactions"></a>Rapportering om faktiske transaktioner

Når du godkender en timeseddel eller udgift eller fakturerer en kontrakt i PSA, registreres forretningstransaktionen i objektet **Faktisk**. Dette objekt kan bruges som udgangspunkt for næsten alle finansrelaterede rapporter i PSA. Objektet **Faktisk** registrerer omkostnings- og salgstransaktioner for forretningshændelsen. Den registrerer også mange relevante attributter.

Når du arbejder med objektet **Faktisk**, er det vigtigt, at du forstår, hvilken transaktion eller hvilke transaktioner der registreres i objektet, og hvornår transaktionerne registreres. Her er det almindelige flow, når du arbejder med tidsregistreringer (flowet for udgiftsposter minder herom):

1. Når tidsregistreringen gemmes, oprettes der ingen poster i objektet **Faktisk**.
2. Når tidsregistreringen er sendt, oprettes der ingen poster i objektet **Faktisk**.
3. Når tidsregistreringen er godkendt, oprettes der en post i objektet **Faktisk,**, og der kan også oprettes en anden post. I den første post gemmes omkostningerne for den registrerede tid. I den anden post gemmes det ikke-fakturerede salgsbeløb for den registrerede tid. Den anden post er afhængig af projektet, der enten har en kunde, et tilbud eller en kontraktlinje tilknyttet.

    | Dokumentdato | Transaktionstype | Transaktionsklasse | Kunde         | Kontrakt   | Ressource     | Ressourcerolle | Faktureringstype | Antal | Enhedspris | Beløb |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Omkostning             | Tidspunkt              | Alpine Ski House | Alpine CRM | Anne-Marie Jespersen | Projektleder   | Fakturerbar   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Ikke-faktureret salg   | Tidspunkt              | Alpine Ski House | Alpine CRM | Anne-Marie Jespersen | Projektleder   | Fakturerbar   | 8.0      | 100.00     | 800.00 |

    Disse to poster er separate, men relaterede poster. De er hverken debet eller kredit.

4. Hvis der er knyttet en kontrakt til projektet, oprettes der yderligere to poster i objektet **Faktisk**, når tidsregistreringen faktureres. For det første oprettes der et negativt beløb for den ikke-fakturerede salgspost. Denne post tilbagefører grundlæggende det ikke-fakturerede salg. Dernæst oprettes der en transaktion for det fakturerede salg. Disse poster er ligeledes separate, men relaterede poster, hverken debet eller kredit.

    | Dokumentdato | Transaktionstype | Transaktionsklasse | Kunde         | Kontrakt   | Ressource     | Ressourcerolle | Faktureringstype | Antal | Enhedspris | Beløb   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Ikke-faktureret salg   | Tidspunkt              | Alpine Ski House | Alpine CRM | Anne-Marie Jespersen | Projektleder   | Fakturerbar   | - 8,0    | 100.00     | - 800,00 |
    | 2/4/18        | Faktureret salg     | Tidspunkt              | Alpine Ski House | Alpine CRM | Anne-Marie Jespersen | Projektleder   | Fakturerbar   | 8.0      | 100.00     | 800.00   |

Objektet **Transaktionsoprindelse** registrerer oprindelsen for posten **Faktisk**, og objektet **Transaktionsforbindelse** registrerer de relaterede poster for posten **Faktisk**. Derudover indeholder posten **Faktisk** referencer til projektet, projektkontrakten (ordren), den reserverbare ressource og kunden.

![Diagram, der viser transaktionsforbindelse, oprindelse og faktiske relationer](media/PS-Reporting-image6.png "Diagram, der viser transaktionsforbindelse, oprindelse og faktiske relationer")


[!INCLUDE[footer-include](../includes/footer-banner.md)]