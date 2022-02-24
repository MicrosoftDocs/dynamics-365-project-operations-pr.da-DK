---
title: Undermoduler og enhedsgrupper
description: Dette emne indeholder oplysninger om, hvordan du opretter enheder og enhedsgrupper i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 3f588e41d001befeac87bb6a4e28a83cf5cfa865
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131021"
---
# <a name="units-and-unit-groups"></a>Undermoduler og enhedsgrupper

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_

Enheder er det antal eller målinger, som du kan sælge dine produkter eller tjenester i. Hvis du for eksempel sælger haveartikler, kan du sælge frø i enheder af pakker, kasser og paller. En enhedsgruppe er en samling af disse forskellige enheder.

Hvis du vil udføre trinnene i dette emne, skal du sørge for, at du er tildelt rollen som systemadministrator eller rollen som Sales Professional Manager eller har tilsvarende tilladelser.

## <a name="create-a-unit-group"></a>Oprette en enhedsgruppe

1. Vælg **Enheder** i oversigten over webstedet.
2. Vælg **Ny** og i dialogboksen **Opret enhedsgruppe** skal du angive enhedens navn.
3. Angiv den laveste almindelige måleenhed, som produktet sælges i, i feltet **Primær enhed**. Du kan f.eks. angive "stk." eller "kg.".
4. Vælg **OK**.

## <a name="add-units-to-a-unit-group"></a>Tilføj enheder til en enhedsgruppe

1. Åbn en enhedsgruppe, og på fanen **Relateret** skal du vælge **Enheder**. Du vil se, at den primære enhed allerede er tilføjet.
2. Vælg **Tilføj ny enhed**, og på siden **Opret hurtig: enhed** skal du i feltet **Navn** angive navnet på enheden.
3. I feltet **Antal** skal du angive det antal, som enheden skal indeholde. Hvis f.eks. en boks indeholder to styk, skal du angive "2". 
4. I feltet **Basisenhed** skal du vælge en basisenhed for at oprette den mindste måleenhed for enheden. Du kan f. eks. vælge "stk.".
5. Vælg **Gem**:
