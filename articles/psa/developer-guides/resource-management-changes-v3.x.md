---
title: Ændringer i ressourcestyringen (Project Service Automation 3.x)
description: Dette emne indeholder oplysninger om ændringerne i ressourcestyringsområdet.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
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
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074363"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Ændringer i ressourcestyringen (Project Service Automation 3.x)

Sektionerne i dette emne indeholder oplysninger om de ændringer, der er foretaget i ressourcestyringsområdet i Dynamics 365 Project Service Automation version 3.x.

## <a name="project-estimates"></a>Projektestimater

I stedet for at være baseret på **msdyn\_projecttask** -objektet ( **Projektopgave** ) baseres projektestimater på objektet **msdyn\_ressourceassignment** ( **Ressourcetildeling** ). Ressourcetildelinger er blevet "kilden til sandhed" for opgaveplanlægning og prisfastsættelse.

## <a name="line-tasks"></a>Linjeopgaver

I PSA 3.x er linjeopgaver forældede (frarådes). Tildelinger peger nu på hele opgaven i stedet for linjeopgaver.

I det følgende eksempel kan du se, hvordan en opgave med navnet "Testopgave" tildeles til teammedlemmer A og B i tidligere versioner af PSA og i PSA 3.x.

- **Før PSA 3.x:**

    - Testopgave

        - Testopgave – Linjeopgave 1

            - Tildeling til A

        - Testopgave – Linjeopgave 2

            - Tildeling til B

- **PSA 3.x:**

    - Testopgave

        - Tildeling til A
        - Tildeling til B

## <a name="unassigned-assignment"></a>Ikke-tildelt tildeling

I PSA 3.x er en ikke-tildelt tildeling en tildeling, der er tildelt til et **NULL** -teammedlem og **NULL** -ressource. Ikke-tildelte tildelinger kan forekomme i et par scenarier:

- Hvis en opgave er blevet oprettet, men endnu ikke er tildelt til et teammedlem, oprettes der altid en ikke-tildelt tildeling. 
- Hvis alle modtagere af en opgave fjernes, oprettes der en ikke-tildelt tildeling igen for den pågældende opgave.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Planlægningsfelter på objektet Projektopgave

Felterne på **msdyn\_projecttask** -objektet er forældede eller flyttet til objektet **msdyn\_resourceassignment** , eller der henvises nu til dem fra objektet **msdyn\_projectteam** ( **Projektteammedlem** ).

| Feltet frarådes i msdyn\_projecttask (projektopgave) | Nyt felt i msdyn\_resourceassignment (ressourcetildeling) | Kommentar |
|---|---|---|
| msdyn\_assignedresources | Ingen | |
| msdyn\_assignedteammembers | Ingen | |
| msdyn\_numberofresources | Ingen | |
| msdyn\_scheduledhours | Ingen | |
| msdyn\_effortcontour | msdyn\_plannedwork | Formatet for JavaScript Object Notation-datastrukturen (JSON), der er gemt i feltet, er blevet ændret. |

## <a name="schedule-contour"></a>Planlægge en profil

Planlægningsprofilen gemmes i feltet **Planlagt arbejde** ( **msdyn\_plannedwork** ) for hvert enkelt **ressourcetildelings** -objekt ( **msdyn\_resourceassignment** ).

### <a name="structure"></a>Struktur

Den nye struktur i planlægningsprofilen består af fleksible tidsrum, der defineres for hver dag i tidsplanen. Hvert tidsrum har følgende egenskaber:

- **Start** – Start på arbejdstimerne for dagen ifølge projektkalenderen.
- **Slut** – Slut på arbejdstimerne for dagen ifølge projektkalenderen.
- **Timer** – Det antal timer, der er tildelt på dagen.

**Eksempel**

I dette eksempel bruges der en projektkalender, hvor arbejdsdagen er kl. 9-17 i tidszonen UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatisk planlægning og manuel planlægning

Hvis en opgave planlægges automatisk, indlæses timerne i forvejen, og opgavevarigheden reduceres måske.

**Eksempel**

Den følgende opgave planlægges automatisk i 18 timer over tre dage (3. december 2018 til 5. december 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Hvis en opgave planlægges manuelt, fordeles timerne jævnt over alle datoer.

**Eksempel**

Den følgende opgave er planlagt automatisk til 18 timer over tre dage (3. december 2018 til 5. december 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Tildelingsenhed

Tildelingsenheden er udeladt i PSA 3.x. Tiden for opgaven fordeles nu ligeligt pr. dag mellem alle de tildelte ressourcer.

**Eksempel**

I dette eksempel tildeles opgaven til to ressourcer, og den planlægges automatisk til 36 timer over tre dage (3. december 2018 til 5. december 2018).

- Tildeling 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Tildeling 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Prisfastsættelsesdimensioner

I PSA 3.x er felterne for ressourcespecifikke prisfastsættelsesdimensioner (f.eks. **Rolle** og **Afdeling** ) blevet fjernet fra objektet **msdyn\_projecttask**. Disse felter kan nu hentes fra det aktuelle projektteammedlem ( **msdyn\_projectteam** ) i ressourcetildelingen ( **msdyn\_resourceassignment** ), når der genereres projektestimater. Der er føjet et nyt felt, **msdyn\_organizationalunit** , til objektet **msdyn\_projectteam**.

| Feltet frarådes i msdyn\_projecttask (projektopgave) | Felt fra msdyn\_projectteam (projektteammedlem), der bruges i stedet |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Profiler

Profilfelterne for prisfastsættelse og estimerng er udeladt i objektet **msdyn\_projecttask**. De er blevet flyttet til objektet **msdyn\_resourceassignment**.

| Feltet frarådes i msdyn\_projecttask (projektopgave) | Nyt felt i msdyn\_resourceassignment (ressourcetildeling) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

De følgende felter er blevet føjet til objektet **msdyn\_resourceassignment**.

* msdyn\_plannedcost
* msdyn\_plannedsales

De følgende felter for planlagte, faktiske og resterende omkostninger og salg er uændrede i objektet **msdyn\_projecttask** :

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales
