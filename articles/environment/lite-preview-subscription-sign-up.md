---
title: Tilmelding til et prøveversionsabonnement - lille
description: Denne artikel indeholder oplysninger om, hvordan du abonnerer på og udruller Project Operations - lille udrulning - aftale om proformafakturering.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410004"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Tilmelding til et prøveversionsabonnement - lille 

Denne artikel redegør for, hvordan du abonnerer på prøvetilbuddet og udruller Dynamics 365 Project Operations - lille udrulning - aftale om proformafakturering.

> [!NOTE]
> Denne proces ændres i de kommende versioner af Project Operations.

## <a name="prerequisites"></a>Forudsætninger
- Den bruger, der udruller prøveversionen, skal have globale Azure-lejer administratorrettigheder. Du kan oprette en lejer under indløsningen af første tilbud.

> [!IMPORTANT]
> Kun én person, lejeradministratoren, i en organisation skal udføre denne opgave. Hvis du ikke abonnerer på denne udgivelse, skal du vente, til din organisation er blevet tilmeldt, og du har modtaget dine brugerlegitimationsoplysninger.
> 
> Prøveversioner er til engangsbrug i lejeren. Du kan kun køre en prøveversion én gang. Det anbefales, at du opretter en ny lejer med henblik på prøveversionen.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations-prøveversion 

Før du går i gang, skal du sikre dig, at du er logget på en browser med brugerens arbejdskonto i lejeren, hvor du vil installere prøveversionen af Project Operations.

1. Gå til [Project Operations-prøveversion](https://aka.ms/try-po) for at indløse den første tilbudskode, **Dynamics 365 Project Operations**.
2. Bekræft din ordre..

  Du kan se, at bekræftelsestilbuddet blev gennemført korrekt.

## <a name="assign-licenses"></a>Tildele licenser

> [!IMPORTANT]
> Du skal have administratoradgang til din organisations Microsoft 365-portal for at fuldføre følgende trin.


1. Gå til [Microsoft 365 Administration](https://portal.office.com/) for at tildele licenserne til brugerne.
2. På siden **Aktive brugere** skal du vælge de brugere, du vil tildele en licens til.
3. Kontrollér, at **Dynamics 365 Project Operations**-licensen er valgt. 
4. Vælg **Gem ændringer**.

## <a name="create-a-new-dataverse-environment"></a>Opret et nyt Dataverse-miljø

1. Klargør et nyt Project Operations Dataverse-udrulningsmiljø ved at følge instruktionerne i artiklen [Udrulningsmodel til Dataverse](lite-deployment.md). Når du vælger miljøtypen, skal du sørge for at bruge **Prøveversion (abonnementsbaseret)**.

  ![Nyt miljø.](./media/19CreateEnvironment.png)

2. Vælg indstillingen **Aktivér Dynamics 365-apps**, og lad **Udrul automatisk disse apps** være tom.  
3. Vælg **Gem** for at oprette miljøet.

  ![Tilføj database.](./media/20CreateEnvironment1.png)

4. Når miljøet er oprettet, skal du installere **Microsoft Dynamics 365 Project Operations**-løsningen. 

![Installer løsningen.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Konfigurere demodata

Konfigurer demodata ved at følge instruktionerne i artiklen [Anvend demokonfiguration og konfigurationsdata](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
