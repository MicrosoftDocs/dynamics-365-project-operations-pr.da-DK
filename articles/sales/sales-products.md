---
title: Produkter
description: Dette emne indeholder oplysninger om det produktkatalog, som du kan bruge til at give oplysninger til kunder om de produkter og prisfastsættelser, som din organisation tilbyder.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 085b7e4d9274f8c8d94d7a84109cfa782acf3dbb9241bfd25ecb8c2f329e1bb8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986844"
---
# <a name="products"></a>Produkter

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Produkter er grundstenen i din virksomhed. Produktkataloget i Dynamics 365 Sales Professional er en samling af produkter og prisoplysninger. Gør det lettere for dine sælgere at øge deres salg ved hurtigt at oprette et produktkatalog.

## <a name="add-a-product"></a>Tilføj et produkt

1.  Kontrollér, at du har rollen som Professional salgschef eller systemadministrator, så du kan tilføje produkter i Dynamics 365 Sales Professional.
2.  I oversigten over webstedet skal du under **Konfiguration** vælge **Produkter**.
3.  Vælg **Tilføj produkt**, og angiv følgende oplysninger:

    -  **Navn**
    -  **Produkt-id**
    -  **Overordnet**: Vælg en overordnet produktfamilie til produktet. Hvis du vil oprette et underordnet produkt i en produktfamilie, angives navnet på den overordnede produktfamilie her. Dette kan ikke ændres, efter at posten er gemt.
    -  **Gyldig fra**/**Gyldig til**: Definerer den periode, produktet er gyldigt i, ved at vælge datoer for **Gyldig fra** og **Gyldig til**.
    -  **Enhedsgruppe**: Vælg en enhedsgruppe. En enhedsgruppe er en samling af forskellige enheder, som et produkt sælges i, og definerer, hvordan de enkelte varer er grupperet i større mængder. Hvis du f.eks. vil tilføje frø som et produkt, har du muligvis oprettet en enhedsgruppe, kaldet "Frø", og defineret dens primære enhed som "pakke".
    -  **Standardenhed**: Vælg den mest almindelige enhed, som produktet sælges i. Enheder er det antal eller målinger, som du kan sælge dine produkter i. Hvis du har tilføjet frø som et produkt, kan du for eksempel sælge dem i pakker, kasser eller paller. Hver af disse bliver en enhed af produktet. Hvis frø sælges hovedsageligt i pakker, kan du vælge det som enheden.
    -  **Standardprisliste**: Hvis det er et nyt produkt, er dette felt skrivebeskyttet. Før du kan vælge en standardprisliste, skal du udfylde de obligatoriske felter og derefter gemme posten. Når du har gemt produktposten, er det en god ide at angive en standardprisliste for hvert produkt, selvom standardprislisten ikke er obligatorisk. Så kan Sales bruge standardprislisten til at generere tilbud, ordrer og fakturaer, hvis en kundepost ikke indeholder en prisliste.
    -  **Understøttede decimaler**: Du skal indtaste et heltal mellem 0 og 5. Hvis produktet ikke kan deles op i mindre mængder, skal du skrive 0. Præcisionstallet i feltet **Antal** i tilbuds-, ordre- eller fakturaproduktposten valideres i forhold til værdien i dette felt, hvis produktet ikke har en tilknyttet prisliste.
    -  **Emne**: Knyt dette produkt til et emne. Du kan bruge emner til at kategorisere produkterne og til at filtrere rapporter.

4.  Vælg **Gem**.
5.  På fanen **Flere detaljer** i sektionen **Prislisteelementer** skal du vælge **Flere kommandoer** og dernæst vælge **Tilføj nyt prislisteelement**.
7.  På fanen **Supplerende oplysninger** skal du i sektionen **Produktrelation** vælge ikonet **Flere kommandoer** og derefter vælge **Tilføj ny produktrelation**.
8.  I formularen **Tilføj ny produktrelation** skal du angive følgende detaljer og på kommandolinjen vælge **Gem og luk**:

    -   **Relateret produkt**: Vælg et produkt, som du vil tilføje som et produkt, der er relateret til den eksisterende produktpost, du arbejder på.
    -   **Salgsrelationstype**: Vælg, om du vil tilføje produktet som et mersalg, salg på tværs, tilbehør eller et erstatningsprodukt.
    -   **Retning**: Vælg, om forholdet mellem produkterne bliver envejs eller tovejs. Når du vælger envejs, vises det produkt, du vælger i **Relaterede produkter**, som en anbefaling for det eksisterende produkt, men ikke omvendt.

9.  Vælg **Gem** i formularen Produkt.

## <a name="import-products"></a>Importere produkter

Du kan bruge importskabeloner til at hente masseproduktdata til Dynamics 365 Sales.

## <a name="revise-a-product"></a>Revidere et produkt

Hold produktlageret opdateret ved hurtigt at revidere egenskaber for produkterne, som kræves, og genudgive oplysningerne, så dine salgsagenter kan se de seneste ændringer til lageret.

1.  Kontrollér, at du har en af følgende sikkerhedsroller eller tilsvarende tilladelser: Systemadministrator, Systemtilpasser, Salgschef, Salgsdirektør, Vicedirektør for salg eller Administrerende direktør/virksomhedsleder.
2.  Vælg **Produkter** i oversigt over websted.
3.  Åbn et aktivt produkt, som du vil ændre, og vælg **Revider** på kommandolinjen.
4.  Vælg **Bekræft** i dialogboksen **Bekræft revision**. Dette vil ændre produktstatus til **Under revision**.
5.  Vælg **Udgiv** på kommandolinjen, når du er færdig med at foretage ændringer.

    > [!TIP]
    > Hvis du fortryder ændringerne og vil fortsætte med den seneste aktive version af produktet, skal du vælge **Omdan**. Dette ændrer status for produktet tilbage til **Aktiv**.

## <a name="clone-a-product"></a>Klon et produkt 

Når du opretter et nyt produkt, kan du spare tid ved at klone et eksisterende produkt. Der oprettes en kopi af den oprindelige post med alle detaljer med undtagelse af navn og ID.

1.  Kontrollér, at du har en af følgende sikkerhedsroller eller tilsvarende tilladelser: Systemadministrator, Systemtilpasser, Salgschef, Salgsdirektør, Vicedirektør for salg eller Administrerende direktør/virksomhedsleder.
2.  Vælg **Produkter** i oversigt over websted.
3.  Vælg en produktfamilie, du vil klone, og vælg **Klon** på kommandolinjen. En bekræftelsesdialogboks åbnes.
4.  Vælg **Bekræft**.

Der åbnes en ny produktpost med de samme oplysninger som den oprindelige, med undtagelse af navn og ID.

## <a name="retire-a-product"></a>Lade et produkt udgå 

Hvis din organisation ikke længere sælger et produkt, kan du lade produktet udgå, så det ikke længere er tilgængeligt for dine salgsagenter.

1.  Kontrollér, at du har sikkerhedsrollen Systemadministrator eller Sales Professional-administrator eller tilsvarende tilladelser.
2.  Vælg **Produkter** i oversigt over websted.
3.  Åbn et aktivt produkt, som du vil lade udgå, og vælg **Lad udgå** på kommandolinjen.
4.  Vælg **Bekræft** i dialogboksen **Bekræft Lad udgå**.


## <a name="delete-a-product"></a>Slette et produkt

Hvis du vil stoppe med at sælge et produkt, skal du slette det.

> [!IMPORTANT]
> Det er ikke muligt at gendanne en slettet post.

1.  Kontrollér, at du har sikkerhedsrollen Systemadministrator eller Sales Professional-administrator eller tilsvarende tilladelser.
2.  Vælg **Produkter** i oversigt over websted.
3.  Vælg en produktfamilie, du vil slette, og vælg **Slet** på kommandolinjen.
4.  Vælg **Fortsæt** i dialogboksen **Bekræft sletning**.
 
 ## <a name="quantity-factors-for-products"></a>Mængdefaktorer for produkter

Mængdefaktorer understøtter salget af abonnementsbaserede produkter. I forbindelse med abonnementsbaserede produkter udtrykkes antallet i tilbuds- eller projektkontraktlinjen som antallet af brugermåneder.

Prisen for abonnementsprogrammer gemmes som regel i kataloget som pris pr. bruger pr. måned. Men du kan også bruge andre tidsbeskrivelser i stedet. Under salgsprocessen er prisen i tilbudslinjen som regel den pris pr. bruger, pris pr. måned, som blev forhandlet og fratrukket af IT-salgsagenten. Hver handel har et forskelligt antal brugere og et forskelligt antal abonnementsmåneder. Det antal, der bruges til at beregne beløbet i tilbudslinjen, er et produkt af antallet af brugere og antallet af abonnementsmåneder.

Mængdefaktorer er baseret på produktattributter. Når du konfigurerer bestemte egenskaber for et produkt, kan du markere et undersæt af disse egenskaber eller alle egenskaberne som mængdefaktorer.

Systemet validerer, at kun numeriske egenskaber eller produktegenskaber med numerisk datatype markeres som mængdefaktorer. Når et produkt, som der konfigureres mængdefaktorer for, føjes til en tilbudslinje, bliver feltet **Antal** i tilbudslinjen et skrivebeskyttet felt. Når du har angivet værdier for produktegenskaber, der er mængdefaktorer, beregnes antallet i tilbudslinjen.

Hvis følgende egenskaber eksempelvis er til stede: 

- **Antal brugere**: Antallet af brugere 
- **Antal måneder**: Antallet af abonnementsmåneder
- **Produkt-SKU** 

Egenskaberne **Antal brugere** og **Antal måneder** kan mærkes som mængdefaktorer ved at redigere egenskaberne for produktlinjen. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]