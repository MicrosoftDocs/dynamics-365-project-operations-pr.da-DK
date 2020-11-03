---
title: Få en forståelse for projektstatus
description: Dette emne indeholder oplysninger om den status, der tildeles projekter i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074044"
---
# <a name="understand-project-status"></a>Få en forståelse for projektstatus

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


Sektionen **Status** på siden **Projektobjekt** indeholder en oversigt over et projekts tilstand baseret på omkostninger og indsats.


## <a name="status-summary-fields"></a>Felter for statusoversigt

- Feltet **Overordnet projektstatus** er et felt, der kan redigeres, og som viser projektets overordnede status. Feltet bruger farvekodning, f.eks. grøn, gul og rød, for at angive øget risiko. 
- Feltet **Kommentarer** giver projektlederen mulighed for at komme med konkrete kommentarer til statussen. 
- Feltet **Status opdateret for** kan ikke redigeres. Værdien i dette felt er et tidsstempel, der angiver, hvornår statussen senest er opdateret.
- Felterne **Planlægningsresultat** og **Omkostningsresultat** angives fra sporingsgitteret. Når afvigelsen fra tidsplanen og omkostningerne for rodnoden i visningen **Indsatssporing** er positiv, opdateres disse felter til **Forud**. Når afvigelsen fra tidsplanen og omkostningerne for rodnoden er negativ, angives disse felter til **Bagud**.
