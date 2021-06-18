---
title: Opret estimater på en tilbudslinje
description: Dette emne indeholder oplysninger om, hvordan du opretter et estimat på en tilbudslinje i et projekt.
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: f4010f7599b66c9ad9e49943c1c0d7d165493d60
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010284"
---
# <a name="create-estimates-on-a-quote-line"></a>Opret estimater på en tilbudslinje

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

I et projektbaseret tilbud kan du bruge objektet Tilbudslinjedetaljer til at estimere det arbejde, der kræves for at levere et projekt. Du kan derefter dele dette estimat med kunden.

Der behøver ikke være nogen tilbudslinjedetaljer for projektbaserede tilbudslinjer. De kan i stedet have mange tilbudslinjedetaljer. Tilbudslinjedetaljer bruges til at estimere tid, udgifter eller gebyrer. Dynamics 365 Project Operations tillader ikke materialeestimater på tilbudslinjedetaljer. Disse kaldes transaktionsklasser. Estimerede momsbeløb kan også angives på en transaktionsklasse.

Udover transaktionsklasser har tilbudslinjedetaljer en transaktionstype. Der findes to transaktionstyper for tilbudslinjedetaljer, **Omkostning** og **Projektkontrakt**.

## <a name="estimate-by-using-a-contract"></a>Estimere ved hjælp af en kontrakt

Hvis du brugte et Project Operations-tilbud, da du oprettede en projektbaseret kontrakt, kopieres det estimat, som du har for hver tilbudslinje i tilbuddet, til projektkontrakten. Strukturen i en projektkontrakt er ligesom strukturen i et projekttilbud, der indeholder linjer, linjedetaljer og fakturaplaner.

Estimater kan ske direkte i en projektkontrakt ligesom i et projekttilbud. I forbindelse med et projekttilbud sker estimatet ved hjælp af kontraktlinjer og kontraktlinjedetaljer. Kontraktlinjedetaljer kan også genereres ud fra en projektplan, der er oprettet ved hjælp af estimatet nedefra og op.

Kontraktlinjedetaljer kan bruges til at estimere tid, udgifter eller gebyrer. Estimerede momsbeløb kan også angives på en kontraktlinjedetalje.

Materialeestimater er ikke tilladte på kontraktlinjedetaljer.

De processer, der understøttes i en projektkontrakt, er oprettelse og bekræftelse af fakturaer. Oprettelse af faktura opretter en kladde af en projektbaseret faktura, der omfatter alle ikke-fakturerede faktiske salg til dags dato.

Bekræftelse gør kontrakten skrivebeskyttet og ændrer dens status fra **Kladde** til **Bekræftet**. Når du har udført denne handling, kan du ikke fortryde den. Da denne handling er permanent, er det en god ide at bevare kontrakten i **Kladde**-status.

De eneste forskelle mellem kladdekontrakter og bekræftede kontrakter er deres status, og det faktum, at kladdekontrakter kan redigeres, mens bekræftede kontrakter ikke kan. Det er muligt at oprette fakturaer og spore faktiske oplysninger på både kladdekontrakter og bekræftede kontrakter.

Du kan ikke ændre ordrer på kontrakter eller projekter.

## <a name="estimating-projects"></a>Estimering af projekter

Du kan estimere tid og udgifter på projekter, men ikke materialer eller gebyrer.

Der genereres tidsestimater, når du opretter en opgave og identificerer attributterne for en generisk ressource, der kræves til at udføre opgaven. Tidsestimater genereres ud fra planlagte opgaver. Tidsestimater oprettes ikke, hvis du opretter generiske teammedlemmer uden for konteksten af tidsplanen.

Udgiftsestimater angives i gitteret på siden **Estimater**.

## <a name="understand-estimation"></a>Få indblik i estimering

Brug følgende tabel som vejledning til at forstå forretningslogikken i estimeringsfasen.

| Scenarie                                                                                                                                                                                                                                                                                                                                          | Objektpost                                                                                                                                                                                                       | Transaktionstype | Transaktionsklasse | Yderligere oplysninger                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Når du har brug for at estimere salgsværdien af tid på et tilbud                                                                                                                                                                                                                                                                                    | Posten med tilbudslinjedetaljer oprettes                                                                                                                                                                               | Projektkontrakt | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningssidens tilbudslinjedetaljer |
|                                                                                                                                                                                                                                                                                     | Systemet opretter endnu en post med tilbudslinjedetaljer til lagring af de tilsvarende omkostningsværdier. Alle felter, der ikke er penge, kopieres fra salgets tilbudslinjedetaljer til omkostningens tilbudslinjedetaljer.                                                                                                                                                                               | Omkostning | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningssidens tilbudslinjedetaljer |
| Når du har brug for at estimere salgsværdien af tid på en kontrakt                                                                                                                                                                                                                                                                                 | Posten med projektkontraktlinjedetaljer oprettes                                                                                                                                                                    | Projektkontrakt | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningens tilbudslinjedetaljer      |
|                                                                                                                                                                                                                                                                                  | Systemet opretter endnu en post med tilbudslinjedetaljer til lagring af de tilsvarende omkostningsværdier. Alle felter, der ikke er penge, kopieres fra salgets tilbudslinjedetaljer til omkostningens tilbudslinjedetaljer.                                                                                                                                                                    | Omkostning | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningens tilbudslinjedetaljer      |
| Når brugeren beskriver en ressource på en projektopgave                                                                                                                                                                                                                                                                                            | Estimatlinjepost til visning af opgavens salgsværdi oprettes, når en opgave oprettes med alle påkrævede prisdimensioner. Rolle- og organisationsenheder er prisfastsættelsesdimensionerne | Projektkontrakt | Tidspunkt        |                                                                                   |
|     | Estimatlinjepost til visning af opgavens omkostningsværdi oprettes, når en opgave oprettes med alle påkrævede prisdimensioner. Alle felter, der ikke er penge, kopieres fra salgets estimatlinje til omkostningens estimatlinje. Rolle og organisationsenhed er prisfastsættelsesdimensionerne for både omkostning og fakturasatser.                                                                                                                                                                                                                | Omkostning             | Tidspunkt           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Tilpas tilbudslinjedetalje- og kontraktlinjedetaljeobjekterne

Hvis du har tilføjet et brugerdefineret felt på tilbudslinjedetaljen og ønsker, at systemet skal angive værdien af feltet som en standardværdi på den relaterede omkostningslinje, der oprettes, skal du bruge plug-in-registreringsværktøjerne PreOperationContractLineDetailUpdate og PreOperationQuoteLineDetailUpdate. Disse plug-ins skal registreres igen, når tilbudslinjedetaljer eller kontraktlinjedetaljer er ændret. Udfør disse trin for at fuldføre processen.

1. Åbn PluginRegistrationTool, og opret forbindelse til din onlineforekomst.
2. Vælg **Søg**, og søg efter den plug-in, der skal opdateres.
3. Vælg plug-in'en, og vælg derefter **Vælg** på hovedsiden.
4. Vælg trinnet for plug-in'en, du vil opdatere, højreklik, og vælg derefter **Opdater**.
5. I dialogboksen **Opdater eksisterende trin** i feltet **Filtrering af attributter** skal du vælge ellipseknappen (**...**):
6. Markér afkrydsningsfelterne for de brugerdefinerede attributter i dialogboksen **Vælg attributter**.
7. Vælg **OK** for at lukke dialogboksen, og vælg derefter **Opdater trin**.
8. Gentag trin 1 til 7 for den anden plug-in.
9. Luk PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]