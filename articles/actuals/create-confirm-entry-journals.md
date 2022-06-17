---
title: Opret og bekræft posteringskladder
description: Denne artikel beskriver, hvordan du opretter og bekræfter posteringskladder i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912325"
---
# <a name="create-and-confirm-entry-journals"></a>Opret og bekræft posteringskladder

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Du kan bruge posteringskladder til at registrere faktiske værdier direkte i Microsoft Dynamics 365 Project Operations. Når du bruger posteringskladder, behøver du ikke at angive tids-, udgifts- og materialeforbrugslogfiler i Project Operations.

En enkelt posteringskladde giver dig mulighed for at oprette flere kladdelinjer. Når posteringskladden er blevet bekræftet, registrerer en posteringskladdelinje den faktiske værdi for følgende detaljer:

- Omkostningen eller omsætningen afhængigt af den valgte transaktionstype.
- Den valgte transaktionsklasse. De tilgængelige klasser er **Tid**, **Udgifter**, **Materiale**, **Forskudshonorar**, **Milepæl** og **Moms**.
- Projektet og/eller en opgave, der er valgt på kladdelinjen.

Følg disse trin for at oprette posteringskladde i Project Operations.

1. Gå til **Salg** \> **Transaktioner** \> **Kladder**.
2. På listesiden **Posteringskladder** skal du i handlingsruden vælge **Ny** for at oprette en kladde.
3. På siden **Ny kladde** skal du i feltet **Beskrivelse** angive en beskrivelse af kladden.
4. Kontrollér, at feltet **Kladdetype** er angivet til **Postering**, og vælg derefter **Gem**. Når den nye posteringskladde er gemt, bør fanen **Kladdelinjer** fremgå af kladdesiden.
5. På fanen **Kladdelinjer** skal du på værktøjslinjen over gittteret vælge **Ny** for at oprettet en posteringskladdelinje.
6. I dialogboksen **Hurtigopret** for oprettelse af en posteringskladdelinje skal du angive felterne som beskrevet i følgende tabel.

    | Felt | Description | Funktionspåvirkning |
    | --- | --- | --- |
    | Transaktionsklasse | Kladdelinjen kan inddeles i en af de seks transaktionsklasser: **Tid**, **Udgifter**, **Materiale**, **Forskudshonorar**, **Milepæl** eller **Moms**. | Transaktionsklassen **Moms** er udfaset i Project Operations. <br> Hvis du opretter en transaktionsklasse **Moms**, behandles den ikke ved fakturering eller i omkostnings- eller omsætningsberegninger. **Milepæl** er en transaktionsklasse, som kun er en omsætningsklasse. <br>Transaktionsklassen **Forskudshonorar** repræsenterer et forskud, der er modtaget fra en kunde. Den skal altid oprettes som et sæt bestående af fakturerede salgskladdelinjer og ikke-fakturerede salgskladdelinjer. |
    | Transaktionstype | Transaktionstyperne **Omkostninger**, **Interorg-salg** og **Kostpris for ressource** bør bruges til at registrere omkostninger.<br> Transaktionstyperne **Ikke-faktureret salg** og **Faktureret salg** bør bruges til at registrere omsætning. | Transaktionsklassen **Forskudshonorar** fungerer kun med transaktionstyperne **Ikke-faktureret salg** og **Faktureret salg**.<br> Transaktionsklassen **Milepæl** fungerer kun med transaktionstypen **Faktureret salg**. <br>Transaktionstyperne **Interorg-salg** og **Kostpris for ressource** gælder kun for timetransaktionsklassen **Tid**, og de kan kun anvendes i posteringskladder i scenarier med lille udrulning og ikke, når Project Operations udrulles i ressource/ikke-lagerførte-scenarier. |
    | Vælg produkt | Når transaktionsklassen **Materiale** er valgt, kan du i dette felt angive, om den materialetransaktion, som du opretter kladdelinjen for, er et eksisterende produkt eller et produkt, der skal indkøbes. | Hvis du vælger **Produkt, der skal indkøbes**, kan du angive et navn til produktet. |
    | Produkt | En reference til produktet fra kataloget. | |
    | Description | En beskrivelse af kladdelinjen for at gøre det nemt at identificere den. | I forbindelse med kladdelinjer for ikke-fakturerede salg bruges værdien som beskrivelse, når der oprettes detaljer om fakturalinjen. |
    | Ekstern beskrivelse | En beskrivelse af den kladdelinje, der kan bruges til deling med eksterne interessenter. | I forbindelse med kladdelinjer for ikke-fakturerede salg bruges værdien som den eksterne beskrivelse, når der oprettes detaljer om fakturalinjen. Den kan også vises på den faktura, der sendes til kunden. |
    | Faktureringstype | En værdi, der angiver, om kladdelinjen skal anses for at være en fakturerbar, komplementerende eller ikke-fakturerbar komponent i projektet. | I et typisk flow er faktureringstypen afledt af de aftalte vilkår, der er angivet i kontrakten. Når du registrerer en kladdelinje, kan du dog angive en værdi i dette felt. |
    | Dokumentdato | Anvend en dato for, hvornår transaktionen fandt sted. | |
    | Startdato | Anvend datoen for, hvornår transaktionen fandt sted. | Dette felt bruges til at sammenligne med datoen for oprettelse af fakturaen for transaktioner af typen **Ikke-faktureret salg**. Denne sammenligning hjælper dig med at finde ud af, om transaktionen er dateret ud i fremtiden eller i fortiden. Der tilføjes kun tidligere transaktioner til fakturaen. |
    | Slutdato | Anvend datoen for, hvornår transaktionen fandt sted. | |
    | Regnskabsdato | Brug den dato, hvor den regnskabsmæssige påvirkning vil blive registreret. | |
    | Kontraktlinjekunde | Hvis der som standard kun er én kunde på kontraktlinjen, angives dette felt til kunden på kontraktlinjen, når kladdelinjen gemmes. Hvis kontraktlinjen har flere kunder, skal du vælge den rette kunde på kontraktlinjen. | Hvis systemet ikke kan udlede kontraktlinjekunden på kladdelinjen, og hvis den er tom på den faktiske værdi af typen **Ikke-faktureret salg**, der er oprettet fra kladdelinjen, faktureres den faktiske værdi ikke. |
    | Project | Vælg det projekt, som den faktiske værdi skal registreres på. | Afhængigt af det valgte projekt, den valgte transaktionsklasse og den valgte opgave forsøger systemet at fastslå kontrakten, kontraktlinjen og kontraktlinjekunden. |
    | Opgave | Vælg den opgave, som den faktiske værdi skal registreres på. | Hvis du knytter opgaver til kontraktlinjer under kontraktkonfigurationen, bruger systemet den valgte opgave sammen med en projekt- og transaktionsklasse til at bestemme kontrakten, kontraktlinjen og kontraktlinjekunden. |
    | Transaktionskategori | Vælg den transaktionskategori, som den faktiske værdi skal registreres på. | I forbindelse med udgifter bestemmer den valgte transaktionskategori den standardpris, der angives på kladdelinjen, når den gemmes. |
    | Rolle | Dette felt er relevant for tidskladdelinjer. Vælg rollen for den ressource, der har brugt tid på projektet og/eller opgaven. | Hvis du bruger standardkonfigurationen til indtastning af standardressourceomkostninger og -faktureringsrater i forbindelse med tidskladdelinjer, bruges den valgte rolle sammen med den enhed, der faktureres, til at bestemme den standardpris, der skal angives på kladdelinjen, når den gemmes. Hvis du bruger en brugerdefineret konfiguration til indtastning af standardpriser, skal du gennemse denne konfiguration for at finde ud af, om feltet **Rolle** bruges til at angive standardprisværdier. |
    | Underentreprise | Hvis kladdelinjen repræsenterer underleverandørkapacitet eller udgifter eller materiale, der er indkøbt via underleverandører, skal du vælge den relevante underentreprise. | Når omkostningskladdelinjer registreres, bestemmer den valgte underleverandør den prisliste, der bruges til at angive standardenhedens kostpris. |
    | Underentrepriselinje | Hvis kladdelinjen repræsenterer underleverandørkapacitet eller udgifter eller materiale, der er indkøbt via underleverandører, skal du vælge den relevante underentrepriselinje. | Når der registreres omkostningslinjer, sikrer den valgte underentrepriselinje, at de tilgængelige kapacitetsberegninger på underentrepriselinjen beregnes korrekt. |
    | Beløbsmetode | Som standard er dette felt angivet til **Gang mængde med pris**. Når denne metode bruges, beregnes beløbet som *Mængde* × *Pris*. Den anden understøttede metode er **Fast pris**. Når denne metode bruges, angives prisen til beløbet, og mængden bruges ikke i beregningen. | |
    | Enhedsplan og enhed | I enhedsplanlægningen og enheden identificeres enheden af antallet. | Kombinationen af enheden og transaktionskategorien bruges til at angive standardpriser for udgifter. I standardkonfigurationen af Project Operations bruges kombinationen af enheden, rollen og den ressourceenhed, der skal bruges til at angive standardpriser for tid. Hvis du har en brugerdefineret konfiguration til indtastningen af standardpriser, bruges den sammen med enheden. Kombinationen af produktet og enheden bruges til at angive standardpriser for materialer. |
    | Antal | Angiv antallet. | |
    | Pris | Hvis prisen ikke udfyldes, når kladdelinjen oprettes, bruges de relevante værdier til at angive standardpriserne, afhængigt af transaktionsklassen. Hvis der angives en pris, når kladdelinjen oprettes, anvendes den pågældende pris. | |
    | Skat | Angiv momsbeløb. | Afhængigt af det momsbeløb, der angives, beregnes det udvidede beløb som *Beløb* + *Moms*. |

## <a name="confirm-an-entry-journal"></a>Bekræft en kladdepostering

Når du har angivet alle kladdelinjer posteringskladden, kan du bekræfte kladden. I denne proces registreres hver kladdelinje som faktiske værdier for de relevante projekter.

Når en kladde er blevet bekræftet, kan du ikke længere redigere den eller nogen af dens linjer.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Faktiske værdier oprettet af bekræftelse af posteringskladde

Der er nogle få vigtige forskelle mellem faktiske værdier, der oprettes ved hjælp af bekræftelse af en posteringskladde, og de faktiske værdier, der oprettes under godkendelse af tids-, udgifts- og materialeforbrugslogfiler og fakturabekræftelse i Project Operations:

- Posteringskladder bruger ikke transaktionsforbindelser til at knytte de faktiske omkostninger til det faktiske ikke-fakturerede salg. De faktiske værdier, der oprettes, når tids-, udgifts- og materialeforbrugslogfiler godkendes, bruger altid transaktionsforbindelser til at sammenkæde kostprisen og de faktiske ikke-fakturerede salg.
- Posteringskladder bruger ikke transaktioners oprindelse til at knytte de faktiske omkostninger og det faktiske ikke-fakturerede salg til en oprindelig post. De faktiske værdier, der oprettes, når tids-, udgifts- og materialeforbrugslogfiler godkendes, bruger altid transaktioners oprindelse til at sammenkæde kostprisen og de faktiske ikke-fakturerede salg til den oprindelige tidsregistrering.
- Når faktiske ikke-fakturerede salg, der er oprettet ved hjælp af bekræftelsen af posteringskladden, faktureres, knyttes de fakturerede faktiske salgsværdier, der oprettes under fakturabekræftelsen, til de ikke-fakturerede faktiske salgsværdier på samme måde som de ikke-fakturerede faktiske salgsværdier, der oprettes, når tids-, udgifts- og materialeforbrugslogfiler godkendes.
- Posteringskladdelinjer, der oprettes for den tid, der angives af interne ressourcer, bevirker ikke, at de faktiske værdier for typerne **Kostpris for ressource** og **Interorg-salg** automatisk oprettes . Disse faktiske værdier skal oprettes manuelt. Denne funktionsmåde adskiller sig fra funktionsmåden for tidsposter, der registreres af interne ressourcer. Når tidspunktet godkendes, opretter applikationen automatisk faktiske værdier af typen **Omkostning** i projektet og faktiske værdier af typen **Ressources enhedsomkostning** og **Interorg-salg** for den medarbejder, der ejer divisionen. Derefter bruges transaktionsforbindelser til at knytte disse faktiske værdier sammen og transaktioners oprindelse for at knytte dem til den oprindelige tidsregistrering.
- Når posteringskladder bekræftes, oprettes faktiske værdier. Rettelseskladder kan dog ikke bruges til at korrigere de faktiske værdier. Denne funktionsmåde afviger fra funktionsmåden for faktiske værdier, der oprettes, når tids-, udgifts- og materialeforbrugslogfiler godkendes. Applikationen giver dig i sådanne tilfælde mulighed for at bruge rettelseskladder til at rette de faktiske værdier for at rette eventuelle fejl, hvis de pågældende faktiske værdier endnu ikke er faktureret. Hvis de allerede er blevet faktureret, kan du stadig rette en faktisk værdi, hvis du gennemfører en fuld kreditering af den faktiske værdi for kunden.

> [!NOTE]
> Posteringskladder gennemtvinger ikke strenge standardregler. Brug derfor disse posteringskladder så lidt som muligt, og udvis forsigtighed og omhu for at sikre, at du ikke opretter forkerte økonomiske data i systemet. Når du kan, skal du bruge konfigurationen for tids-, udgifts- og materialeforbrugslogfiler, milepælen og forskudshonorar på projektkontrakter og processen til bekræftelse af projektfakturaer i stedet for posteringskladder til at oprette faktiske værdier.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
