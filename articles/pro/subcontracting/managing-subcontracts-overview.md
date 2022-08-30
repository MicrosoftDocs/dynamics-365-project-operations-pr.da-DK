---
title: Administration af underleverandører i Project Operations
description: Denne artikel indeholder en oversigt over hele processen for administration af underleverandører, som typisk findes i projektbaserede organisationer.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 783ab1b642bb8cfe2fb3b977a95c8064f33a7994
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261188"
---
# <a name="subcontract-management-in-project-operations"></a>Administration af underleverandører i Project Operations


_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Denne artikel indeholder en oversigt over hele processen for administration af underleverandører, som findes i projektbaserede organisationer. Underentrepriser for tjenester følger typisk forretningsprocesforløbet, der vises i følgende diagram.

![Procesflow for underleverancer](../media/SubcontractingProcessFlow.png)

Følgende liste giver en trinvis beskrivelse af processen for Underentrepriser.

1. Projektlederen opretter en underleverance med en leverandør. De prislister, der er tilknyttet kreditorposten, bruges som standard til underleverancen. Leverandørkontoen har relationstypen **Kreditor** eller **Leverandør**.
2. Projektlederen kan specificere alle køb som linjeelementer i underleverancen. Underleverancelinjer kan indeholde tid, udgifter eller produkter. Transaktionsklassen for underentrepriselinjen, bestemmer, hvad linjen er beregnet til.
3. Administratoren af leverandørkontoen og projektlederen kan gentage valget for hele underleverancen. Prisfastsættelse kan justeres i købsprislister, der er tilknyttet underleverancen.
4. Hvis underentrepriselinjen på dette tidspunkt eller senere i processen omhandler tid, knytter administratoren af leverandørkontoen leverandørkontakter til hver underentrepriselinje. Denne tilknytning indeholder oplysninger til den projektleder, der arbejder med underleverancen. Når en leverandørkontakt er knyttet til en underentrepriselinje, opretter systemet automatisk en reserverbar ressource ud fra kontaktpersonen, hvis der ikke allerede findes en reserverbar ressource.
5. Faktureringsmetoden på hver underleverancelinje kan være **Fast pris** eller **Tid og materiale**. Der konfigureres en milepælsbaseret faktureringsplan for underentrepriselinjer med faste priser.
6.  Når underentreprisen er konfigureret, og forhandlingen er færdig, bekræftes det. Bekræftede underentrepriser kan ikke redigeres, men hvis der sker ændringer, kan en underentreprise "genåbnes for redigeringer", hvilket ændrer statussen fra **Bekræftet** til **Kladde**, og forhandlinger kan genåbnes. 
7.  Når du opretter et generisk teammedlem på et projekt, kan teammedlemmet knyttes til en underentrepriselinje. Dette angiver behovet for at udstyre det generiske teammedlem med underentreprisekapacitet.
8.  Navngivne teammedlemmer kan enten oprettes direkte på et projekt eller ved at reservere dem ved hjælp af ressourceplanlægningsoplevelsen. Hvis et navngivet projektteammedlem er en kontraktansat medarbejder, er det muligt at knytte dette til en underentrepriselinje. Derved hentes den tilgængelige kapacitet ned på en underentrepriselinje.
9.  Underentrepriselinjeressourcer kan registrere tid, udgifter og materialeforbrug på projekter og projektopgaver og derefter indsende det til godkendelse. Dette samme gør sig gældende for medarbejdere. Når en kontraktansat medarbejder registrerer tid, kan vedkommende vælge en bestemt underentreprise og underentrepriselinje.
10. Når en underleverandør har godkendt tid, registreres de faktiske projektomkostninger på baggrund af indkøbsprisen for den kontraktansatte medarbejder eller den rolle, som de har spillet på projektet.
11. Leverandørfakturaer og linjeelementer i en leverandørfaktura kan registreres i systemet for det arbejde, der udføres af leverandørressourcer eller produkter, der er leveret af leverandøren. Fakturalinjer for leverandører skal være specifikke for et projekt og for en transaktionsklasse såsom for tid, udgifter, produkt/materiale, milepæl eller gebyr. Leverandørfakturalinjer kan også henvise til en underentrepriselinje.
12. Systemet knytter automatisk alle faktiske omkostninger, der svarer til underentrepriselinjen og projektet, sammen med leverandørfakturaen. Dette vil fremme en trevejsoverensstemmelses- og verifikationsproces.
13. Projektlederen kan derefter gennemse de automatisk matchede faktiske projektværdier, fjerne eller tilføje andre faktiske projektomkostninger og fuldføre verifikationsprocessen.
14. Når verifikationsprocessen er fuldført på alle linjer, markeres leverandørfakturaen som **Klar til betaling**. I dette trin kan leverandørfakturaen og -linjerne overføres til et regnskabs- eller faktureringssystem for at behandle betalingen til leverandøren. Tidligere registrerede projektomkostninger tilbageføres, og faktiske omkostninger fra leverandørfakturalinjerne registreres i projektet.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Mængdebaserede underentrepriselinjer og arbejdsbaserede underentrepriselinjer

En underentrepriselinje kan være mængdebaseret eller arbejdsbaseret. 

Når en underentrepriselinje er **mængdebaseret**, kan det antal, der købes på underentrepriselinjen for tid, udgifter eller materialer, bruges på et hvilket som helst projekt.

Når en underentrepriselinje er **arbejdsbaseret**, knyttes underentrepriselinjen til et arbejdsprojekt, der repræsenteres af en node i projektplanen. Værdien af underentrepriselinjen er summen af alle de komponenter, der kræves for at levere det pågældende arbejdsprojekt. Disse er udformede som detaljer om underentrepriselinjer og kan være en samling tid, udgifter eller materialer. For en arbejdsbaseret underentrepriselinje er underentrepriselinjen også dedikeret til et enkelt projekt. Disse typer underentrepriser understøttes ikke af Project Operations.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

