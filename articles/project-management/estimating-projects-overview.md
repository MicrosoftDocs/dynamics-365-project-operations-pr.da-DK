---
title: Begreber for økonomiske estimater
description: Dette emne indeholder oplysninger om økonomiske estimater for projekter i Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 74b2499cc706e03658cadeb088df154100051cbc7cce386b2e4d50dbdb5c197f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989184"
---
# <a name="financial-estimation-concepts"></a>Begreber for økonomiske estimater

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I Dynamics 365 Project Operations kan du økonomisk estimere dine projekter i to faser: 
1. I før-salgsfasen, før handlen vindes. 
2. I udførelsesfasen, efter at projektkontrakten er oprettet. 

Du kan oprette et økonomisk estimat for projektbaseret arbejde ved hjælp af en af følgende tre sider:
- Siden **Tilbudslinje** ved hjælp af oplysninger om tilbudslinjen.  
- Siden **Projektkontraktlinje** ved hjælp af oplysninger om kontraktlinjer. 
- Siden **Projekt** ved hjælp af fanesiderne **Opgaver** eller **Udgiftsestimater**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Brug et projekttilbud til at oprette et estimat
I et projektbaseret tilbud kan du bruge objektet **Tilbudslinjedetaljer** til at estimere det arbejde, der kræves for at levere et projekt. Du kan derefter dele dette estimat med kunden.

Der kan være fra nul til adskillige tilbudslinjedetaljer i projektbaserede tilbudslinjer. Tilbudslinjedetaljer bruges til at estimere tid, udgifter eller gebyrer. Microsoft Dynamics 365 Project Operations tillader ikke materialeestimater på tilbudslinjedetaljer. Disse kaldes transaktionsklasser. Estimerede momsbeløb kan også angives på en transaktionsklasse.

Udover transaktionsklasser har tilbudslinjedetaljer en transaktionstype. Der understøttes to transaktionstyper for tilbudslinjedetaljer: **Omkostning** og **Projektkontrakt**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Brug en projektkontrakt til at oprette et estimat

Hvis du brugte et tilbud, da du oprettede en projektbaseret kontrakt, kopieres det estimat, som du har for hver tilbudslinje i tilbuddet, til projektkontrakten. Strukturen i en projektkontrakt er ligesom strukturen i et projekttilbud, der indeholder linjer, linjedetaljer og fakturaplaner.

Estimater kan ske direkte i en projektkontrakt ligesom i et projekttilbud. I forbindelse med et projekttilbud sker estimatet ved hjælp af kontraktlinjer og kontraktlinjedetaljer. Kontraktlinjedetaljer kan også genereres ud fra en projektplan, der er oprettet ved hjælp af estimatet nedefra og op.

Kontraktlinjedetaljer kan bruges til at estimere tid, udgifter eller gebyrer. Estimerede momsbeløb kan også angives på en kontraktlinjedetalje.

Materialeestimater er ikke tilladte på kontraktlinjedetaljer.

## <a name="use-a-project-to-create-an-estimate"></a>Brug et projekt til at oprette et estimat 

Du kan estimere tid og udgifter på projekter. Project Operations understøtter ikke estimater over materialer eller gebyrer for projekter.

Der genereres tidsestimater, når du opretter en opgave og identificerer attributterne for en generisk ressource, der kræves til at udføre opgaven. Tidsestimater genereres ud fra planlagte opgaver. Tidsestimater oprettes ikke, hvis du opretter generiske teammedlemmer uden for konteksten af tidsplanen.

Udgiftsestimater angives i gitteret på siden **Udgiftsestimater**.

Oprettelse af et estimat for et projekt betragtes som den bedste praksis, da du kan udarbejde detaljerede estimater over arbejde eller tid og udgifter for de enkelte opgaver i projektplanen. Du kan derefter bruge dette detaljerede estimat til at oprette estimater for hver tilbudslinje og udarbejde et mere troværdigt tilbud til kunden. Når du importerer eller opretter et detaljeret estimat på tilbudslinjen ved hjælp af projektplanen, importerer Project Operations salgsværdierne og omkostningsværdierne i disse estimater. Efter importen kan du se rentabilitets-, avance- og levedygtighedsmålepunkter i projekttilbuddet.

## <a name="understanding-estimates"></a>Forståelse for estimater

Brug følgende tabel som vejledning til at forstå forretningslogikken i estimatfasen.

| Scenarie                                                                                                                                                                                                                                                                                                                                          | Objektpost                                                                                                                                                                                                       | Transaktionstype | Transaktionsklasse | Yderligere oplysninger                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Når du har brug for at estimere salgsværdien af tid på et tilbud                                                                                                                                                                                                                                                                                    | Posten med tilbudslinjedetaljer oprettes                                                                                                                                                                               | Projektkontrakt | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningssidens tilbudslinjedetaljer |
|                                                                                                                                                                                                                                                                                     | Systemet opretter endnu en post med tilbudslinjedetaljer til lagring af de tilsvarende omkostningsværdier. Alle felter, der ikke er penge, kopieres fra salgets tilbudslinjedetaljer til omkostningens tilbudslinjedetaljer.                                                                                                                                                                               | Omkostning | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningssidens tilbudslinjedetaljer |
| Når du har brug for at estimere salgsværdien af tid på en kontrakt                                                                                                                                                                                                                                                                                 | Posten med projektkontraktlinjedetaljer oprettes                                                                                                                                                                    | Projektkontrakt | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningens tilbudslinjedetaljer      |
|                                                                                                                                                                                                                                                                                  | Systemet opretter endnu en post med tilbudslinjedetaljer til lagring af de tilsvarende omkostningsværdier. Alle felter, der ikke er penge, kopieres fra salgets tilbudslinjedetaljer til omkostningens tilbudslinjedetaljer.                                                                                                                                                                    | Omkostning | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningens tilbudslinjedetaljer      |
| Når brugeren beskriver en ressource på en projektopgave                                                                                                                                                                                                                                                                                            | Estimatlinjepost til visning af opgavens salgsværdi oprettes, når en opgave oprettes med alle påkrævede prisdimensioner. Rolle- og organisationsenheder er prisfastsættelsesdimensionerne | Projektkontrakt | Tidspunkt        |                                                                                   |
|     | Estimatlinjepost til visning af opgavens omkostningsværdi oprettes, når en opgave oprettes med alle påkrævede prisdimensioner. Alle felter, der ikke er penge, kopieres fra salgets estimatlinje til omkostningens estimatlinje. Rolle og organisationsenhed er prisfastsættelsesdimensionerne for både omkostning og fakturasatser.                                                                                                                                                                                                                | Omkostning             | Tidspunkt           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Tilpas tilbudslinjedetalje- og kontraktlinjedetaljeobjekterne

Hvis du har tilføjet et brugerdefineret felt på tilbudslinjedetaljen og ønsker, at systemet skal angive værdien af feltet som en standardværdi på den relaterede omkostningslinje, der oprettes, skal du bruge plug-in-registreringsværktøjerne **PreOperationContractLineDetailUpdate** og **PreOperationQuoteLineDetailUpdate**. Disse plug-ins skal registreres igen, når tilbudslinjedetaljer eller kontraktlinjedetaljer er ændret. Udfør disse trin for at fuldføre processen.

1. Åbn PluginRegistrationTool, og opret forbindelse til din onlineforekomst.
2. Vælg **Søg**, og søg efter den plug-in, der skal opdateres.
3. Vælg plug-in'et, og klik derefter på **Vælg** på hovedsiden.
4. Vælg trinnet for plug-in'en, du vil opdatere, højreklik, og vælg derefter **Opdater**.
5. I dialogboksen **Opdater eksisterende trin** i feltet **Filtrering af attributter** skal du vælge ellipseknappen (**...**):
6. Markér afkrydsningsfelterne for de brugerdefinerede attributter i dialogboksen **Vælg attributter**.
7. Vælg **OK** for at lukke dialogboksen, og vælg derefter **Opdater trin**.
8. Gentag trin 1 til 7 for den anden plug-in.
9. Luk **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
