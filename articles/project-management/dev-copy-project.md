---
title: Udarbejd projektskabeloner med Kopier projekt
description: Dette emne indeholder oplysninger om, hvordan du opretter projektskabeloner ved hjælp af den brugerdefinerede handling Kopier projekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074112"
---
# <a name="develop-project-templates-with-copy-project"></a>Udarbejd projektskabeloner med Kopier projekt

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Dynamics 365 Project Operations understøtter muligheden for at kopiere et projekt og tilbageføre eventuelle tildelinger til de standardressourcer, der repræsenterer rollen. Kunder kan bruge denne funktion til at oprette grundlæggende projektskabeloner.

Når du vælger **Kopier projekt** , opdateres statussen for destinationsprojektet. Brug **Statusårsag** til at bestemme, hvornår kopieringen er fuldført. Hvis du vælge **Kopier projekt** , opdateres startdatoen for projektet også til den aktuelle startdato, hvis der ikke er registreret nogen destinationsdato i destinationsprojektobjektet.

## <a name="copy-project-custom-action"></a>Den brugerdefinerede handling for Kopier projekt 

### <a name="name"></a>Navn 

**msdyn_KopierProjektV2**

### <a name="input-parameters"></a>Inputparametre
Der er tre inputparametre:

| Parameter          | Skriv   | Værdier                                                   | 
|--------------------|--------|----------------------------------------------------------|
| IndstillingKopierProjekt  | String | **{"fjernNavngivneRessourcer":sand}** eller **{"RydTeamsOgTildelinger": sand}** |
| KildeProjekt      | Objektreference | Kildeprojekt |
| Destination             | Objektreference | Destinationsprojekt |


- **{"RydTeamsOgTildelinger":sand}** : Tre standardfunktionsmåder for Project til internettet og fjerner alle tildelinger og teammedlemmer.
- **{"fjernNavngivneRessourcer": sand}** Standardfunktionsmåden for Project Operations og vil gendanne tildelinger til generiske ressourcer.

Du kan finde flere oplysninger om handlinger under [Anvend WEB-API-handlinger](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Angiv de felter, der skal kopieres 
Når handlingen kaldes, kigger **Kopier projekt** på projektvisningen **Kopier projektkolonner** for at afgøre, hvilke felter der skal kopieres, når projektet kopieres.
