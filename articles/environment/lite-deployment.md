---
title: Udrul Project Operations - lille
description: Denne artikel indeholder oplysninger om, hvordan du installerer Project Operations lille udrulning - aftale om proformafakturering.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930311"
---
# <a name="deploy-project-operations---lite"></a>Udrul Project Operations - lille

_**Gælder for:** Lille udrulning - aftale til proformafakturering_



Project Operations understøtter flere udrulningsmodeller. Du kan finde den bedste udrulningsmodel under [Udrulningstyper](determine-deployment-type.md).


> [!IMPORTANT]
> Denne udrulning, lille udrulnings – aftale til proformafakturering, resulterer en **Dataverse-udrulning kun med Project Operations**.

- [Installer Project Operations i et nyt Dataverse-miljø](#new)
- [Installer i et eksisterende Dataverse-miljø](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Installer Project Operations i et nyt Dataverse-miljø

1. Som [Global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations -licens kan du oprette et nyt Dataverse-miljø i [PowerPlatform Administration](https://admin.powerplatform.com). Sørg for, at **Opret en database til dette miljø** og **Dynamics 365-apps** er aktiveret. For flere oplysninger se [Opret og administrer miljøer i Power Platform Administrationen](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Vælg **Microsoft Dynamics 365 Project Operations** fra udrulningslisten for Dynamics 365-apps.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Installer Project Operations i et eksisterende Dataverse-miljø
1. Kontrollér, at miljøet ikke er konfigureret med [dobbelt skrivning](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), da installationen installerer funktionerne [Project Operations til ressourcebaserede/ikke-lagerbaserede scenarier](project-operations-integrated-deployment-overview.md).
2. Som [Global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens skal du finde det miljø i [PowerPlatform Administration](https://admin.powerplatform.com), hvor du vil installere Project Operations.
3. Installer **Microsoft Dynamics 365 Project Operations** fra udrulningslisten for Dynamics 365-apps. Du kan finde flere oplysninger i [Administrer Dynamics 365-apps](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
