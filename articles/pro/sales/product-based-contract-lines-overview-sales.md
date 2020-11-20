---
title: Oversigt over produktbaserede kontraktlinjer - lille
description: Dette emne indeholder oplysninger om produktbaserede kontraktlinjer.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177864"
---
# <a name="product-based-contract-lines-overview---lite"></a>Oversigt over produktbaserede kontraktlinjer - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

Du kan oprette produktbaserede kontraktlinjer i Dynamics 365 Project Operations. Produktbaserede kontraktlinjer kan være manuelt oprettede linjer, eller de kan være elementer fra produktkataloget.

## <a name="product-catalog"></a>Produktkatalog

Produkterne i produktkataloget har en standardenhed og enhedsgruppe. Hvis flere produkter deler det samme sæt attributter, kan du oprette en produktfamilie, der også har de pågældende attributter. Alle produkter i én produktfamilie arver det samme sæt attributter.

Et firma sælger f.eks. abonnementslicenser til forskellige typer af software. Alle abonnementsprogrammer har følgende to attributter:

- Antal brugere
- Abonnements varighed (i måneder)

Hvis du vil bibeholde denne type katalog, skal du oprette en produktfamilie kaldet **Abonnementssoftware**. Tilføj attributterne **Antal brugere** og **Abonnementsvarighed** til produktfamilien. Tilføj derefter de enkelte produkter til produktfamilien **Abonnementssoftware**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Tilføj produktkatalogelementer til en projektkontrakt

Projektkontrakter indeholder afsnit til to typer linjer, nemlig projektbaserede linjer og produktbaserede linjer. Produktbaserede linjer omfatter alle produkter og enheder i produktprislisten på kontrakten. Produkter, der ikke er en del af en kontrakts produktprisliste, kan tilføjes.

Du kan vælge produkter fra andre prislister eller direkte fra produktkataloget. Når du vælger produkter direkte fra et produktkatalog, bruges standardprislisten for produktet som produktets salgspris. Hvis der ikke er angivet en standardprisliste, angives prisen til 0 (nul).

Hvis en kontraktlinje er baseret på et produktkatalog, kan du tilsidesætte salgsprisen direkte på linjen. En kontraktlinje indeholder feltet **Prisfastsættelse** med de to værdier:

- **Tilsidesæt prisfastsættelse**
- **Benyt standard**

Hvis du angiver feltet **Prisfastsættelse** til **Tilsidesæt prisfastsættelse**, angives standardprisen ikke. Angiv en pris for produktet på kontraktlinjen. Hvis du angiver feltet som **Brug standard**, bruges standardsalgsprisen, og feltet kan ikke redigeres.

Når du har installeret Project Operations, angives standardsalgspriserne på de produktbaserede linjer i en kontrakt. Feltet **Prisfastsættelse** indstilles til **Tilsidesæt prisfastsættelse**, så du kan redigere standardprisen i kontraktlinjerne. Dette er en tilsidesættelse specifik for Project Operations for produktbaserede linjers funktion i Dynamics 365 Sales.
