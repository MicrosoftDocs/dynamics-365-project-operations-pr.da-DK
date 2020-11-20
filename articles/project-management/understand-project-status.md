---
title: Få en forståelse for projektstatus
description: Dette emne indeholder oplysninger om den status, der tildeles projekter i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127286"
---
# <a name="understand-project-status"></a>Få en forståelse for projektstatus

_**Gælder for:** Project Operations for scenarier baseret på ressource/ikke-lager, lille udrulning - aftale til håndtering af proformafakturering_


Sektionen **Status** på siden **Projektobjekt** indeholder en oversigt over et projekts tilstand baseret på omkostninger og indsats.


## <a name="status-summary-fields"></a>Felter for statusoversigt

- Feltet **Overordnet projektstatus** er et felt, der kan redigeres, og som viser projektets overordnede status. Feltet bruger farvekodning, f.eks. grøn, gul og rød, for at angive øget risiko. 
- Feltet **Kommentarer** giver projektlederen mulighed for at komme med konkrete kommentarer til statussen. 
- Feltet **Status opdateret den** kan ikke redigeres. Værdien i dette felt er et tidsstempel, der angiver, hvornår statussen senest er opdateret.
- Felterne **Planlægningsresultat** og **Omkostningsresultat** angives fra sporingsgitteret. Når afvigelsen fra tidsplanen og omkostningerne for rodnoden i visningen **Indsatssporing** er positiv, opdateres disse felter til **Ahead** Når afvigelsen fra tidsplanen og omkostningerne for rodnoden er negativ, angives disse felter til **Bagud**.
