---
title: Vurderinger
description: Dette emne indeholder oplysninger om estimater i Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 95f739f0c724ff93c4d588776f9e49687bac2035
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132712"
---
# <a name="estimates"></a>Vurderinger

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I et projektbaseret tilbud kan du bruge objektet Tilbudslinjedetaljer til at estimere det arbejde, der kræves for at levere et projekt. Du kan derefter dele dette estimat med kunden.

Der behøver ikke være nogen tilbudslinjedetaljer for projektbaserede tilbudslinjer. De kan i stedet have mange tilbudslinjedetaljer. Tilbudslinjedetaljer bruges til at estimere tid, udgifter eller gebyrer. PSA tillader ikke materialeestimater på tilbudslinjedetaljer. Disse kaldes transaktionsklasser. Estimerede momsbeløb kan også angives på en transaktionsklasse.

Udover transaktionsklasser har tilbudslinjedetaljer en transaktionstype. PSA understøtter to transaktionstyper for tilbudslinjedetaljer: **Omkostning** og **Projektkontrakt**.

## <a name="estimate-by-using-a-contract"></a>Estimere ved hjælp af en kontrakt

Hvis du brugte et PSA-tilbud, da du oprettede en projektbaseret kontrakt, kopieres det estimat, som du har for hver tilbudslinje i tilbuddet, til projektkontrakten. Strukturen i en projektkontrakt er ligesom strukturen i et projekttilbud, der indeholder linjer, linjedetaljer og fakturaplaner.

Estimater kan ske direkte i en projektkontrakt ligesom i et projekttilbud. I forbindelse med et projekttilbud sker estimatet ved hjælp af kontraktlinjer og kontraktlinjedetaljer. Kontraktlinjedetaljer kan også genereres ud fra en projektplan, der er oprettet ved hjælp af estimatet nedefra og op.

Kontraktlinjedetaljer kan bruges til at estimere tid, udgifter eller gebyrer. Estimerede momsbeløb kan også angives på en kontraktlinjedetalje.

PSA tillader ikke materialeestimater på kontraktlinjedetaljer.

De processer, der understøttes i en projektkontrakt, er oprettelse og bekræftelse af fakturaer. Oprettelse af faktura opretter en kladde af en projektbaseret faktura, der omfatter alle ikke-fakturerede faktiske salg til dags dato.

Bekræftelse gør kontrakten skrivebeskyttet og ændrer dens status fra **Kladde** til **Bekræftet**. Når du har udført denne handling, kan du ikke fortryde den. Da denne handling er permanent, er det en god ide at bevare kontrakten i **Kladde**-status.

De eneste forskelle mellem kladdekontrakter og bekræftede kontrakter er deres status, og det faktum, at kladdekontrakter kan redigeres, mens bekræftede kontrakter ikke kan. Det er muligt at oprette fakturaer og spore faktiske oplysninger på både kladdekontrakter og bekræftede kontrakter.

PSA understøtter ikke ændring af ordrer på kontrakter eller projekter.

## <a name="estimating-projects"></a>Estimering af projekter

Du kan estimere tid og udgifter på projekter. PSA tillader ikke estimater for materialer eller gebyrer på projekter.

Der genereres tidsestimater, når du opretter en opgave og identificerer attributterne for en generisk ressource, der kræves til at udføre opgaven. Tidsestimater genereres ud fra planlagte opgaver. Tidsestimater oprettes ikke, hvis du opretter generiske teammedlemmer uden for konteksten af tidsplanen.

Udgiftsestimater angives i gitteret på siden **Estimater**.

## <a name="understanding-estimation"></a>Om estimering

Brug følgende tabel som vejledning til at forstå forretningslogikken i estimeringsfasen.

| Scenarie                                                                                                                                                                                                                                                                                                                                          | Objektpost                                                                                                                                                                                                       | Transaktionstype | Transaktionsklasse | Yderligere oplysninger                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Når du har brug for at estimere salgsværdien af tid på et tilbud                                                                                                                                                                                                                                                                                    | Posten med tilbudslinjedetaljer oprettes                                                                                                                                                                               | Projektkontrakt | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningssidens tilbudslinjedetaljer |
|                                                                                                                                                                                                                                                                                     | Systemet opretter endnu en post med tilbudslinjedetaljer til lagring af de tilsvarende omkostningsværdier. Alle felter, der ikke er penge, kopieres fra salgets tilbudslinjedetaljer til omkostningens tilbudslinjedetaljer.                                                                                                                                                                               | Omkostning | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningssidens tilbudslinjedetaljer |
| Når du har brug for at estimere salgsværdien af tid på en kontrakt                                                                                                                                                                                                                                                                                 | Posten med projektkontraktlinjedetaljer oprettes                                                                                                                                                                    | Projektkontrakt | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningens tilbudslinjedetaljer      |
|                                                                                                                                                                                                                                                                                  | Systemet opretter endnu en post med tilbudslinjedetaljer til lagring af de tilsvarende omkostningsværdier. Alle felter, der ikke er penge, kopieres fra salgets tilbudslinjedetaljer til omkostningens tilbudslinjedetaljer.                                                                                                                                                                    | Omkostning | Tidspunkt        | Feltet Transaktionsoprindelse i rækken med tilbudslinjedetaljer på salgssiden refererer til omkostningens tilbudslinjedetaljer      |
| Når brugeren beskriver en ressource på en projektopgave                                                                                                                                                                                                                                                                                            | Estimatlinjepost til visning af opgavens salgsværdi oprettes, når en opgave oprettes med alle påkrævede prisdimensioner. Rolle- og organisationsenheder er OOB Project Service-prisdimensionerne | Projektkontrakt | Tidspunkt        |                                                                                   |
|     | Estimatlinjepost til visning af opgavens omkostningsværdi oprettes, når en opgave oprettes med alle påkrævede prisdimensioner. Alle felter, der ikke er penge, kopieres fra salgets estimatlinje til omkostningens estimatlinje. Rolle og organisationsenhed er OOB PSA-prisdimensionerne for både omkostning og fakturasatser.                                                                                                                                                                                                                | Omkostning             | Tidspunkt           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Tilpasning af tilbudslinjedetalje- og kontraktlinjedetaljeobjekter

Hvis du har tilføjet et brugerdefineret felt på tilbudslinjedetaljen og ønsker, at systemet skal angive værdien af feltet som en standardværdi på den relaterede omkostningslinje, der oprettes, skal du bruge plug-in-registreringsværktøjerne PreOperationContractLineDetailUpdate og PreOperationQuoteLineDetailUpdate. Disse plug-ins skal registreres igen, når tilbudslinjedetaljer eller kontraktlinjedetaljer er ændret. Udfør disse trin for at fuldføre processen.

1. Åbn PluginRegistrationTool, og opret forbindelse til din onlineforekomst.
2. Vælg **Søg**, og søg efter den plug-in, der skal opdateres.

    ![Dialogboks med søgetræ](media/basic-guide-19.png)

3. Vælg plug-in'en, og vælg derefter **Vælg** på hovedsiden.
4. Vælg trinnet for plug-in'en, du vil opdatere, højreklik, og vælg derefter **Opdater**.

    ![Valg af et trin i plug-in'en](media/basic-guide-20.png)

5. Vælg ellipseknappen (**...**) i feltet **Filtreringsattributter** i dialogboksen **Opdater eksisterende trin**:
 
    ![Dialogboksen Opdater eksisterende trin](media/basic-guide-21.png)

6. Markér afkrydsningsfelterne for de brugerdefinerede attributter i dialogboksen **Vælg attributter**.

    ![Dialogboksen Vælg attributter](media/basic-guide-22.png)

7. Vælg **OK** for at lukke dialogboksen, og vælg derefter **Opdater trin**.
 
    ![Knappen Opdater trin](media/basic-guide-23.png)

8. Gentag trin 1 til 7 for den anden plug-in.
9. Luk PluginRegistrationTool.
