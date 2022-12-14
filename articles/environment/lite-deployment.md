---
title: Udrulle Project Operations Lite
description: Denne artikel indeholder oplysninger om, hvordan du installerer Project Operations lille udrulning - aftale om proformafakturering.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810971"
---
# <a name="deploy-project-operations-lite"></a>Udrulle Project Operations Lite

_**Gælder for:** Lille udrulning - aftale til proformafakturering_



Project Operations understøtter flere udrulningsmodeller. Du kan finde den bedste udrulningsmodel under [Udrulningstyper](determine-deployment-type.md).


> [!IMPORTANT]
> Denne udrulning, lille udrulnings – aftale til proformafakturering, resulterer en **Dataverse-udrulning kun med Project Operations**.

- [Installer Project Operations i et nyt Dataverse-miljø](#new)
- [Installer i et eksisterende Dataverse-miljø](#existing)
- [Installer i et eksisterende Dataverse-miljø, der har dobbeltskrivningskomponenter](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Installer Project Operations Lite i et nyt Dataverse-miljø

1. Som [Global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations -licens kan du oprette et nyt Dataverse-miljø i [PowerPlatform Administration](https://admin.powerplatform.com). Sørg for, at **Opret en database til dette miljø** og **Dynamics 365-apps** er aktiveret. For flere oplysninger se [Opret og administrer miljøer i Power Platform Administrationen](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Vælg **Microsoft Dynamics 365 Project Operations** fra udrulningslisten for Dynamics 365-apps.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Installer Project Operations Lite i et eksisterende Dataverse-miljø 
1. Som [Global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens skal du finde det miljø i [PowerPlatform Administration](https://admin.powerplatform.com), hvor du vil installere Project Operations.
1. Installer **Microsoft Dynamics 365 Project Operations** fra udrulningslisten for Dynamics 365-apps. Du kan finde flere oplysninger i [Administrer Dynamics 365-apps](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Installer Project Operations Lite i et eksisterende Dataverse-miljø, hvor der allerede findes dobbeltskrivningsløsninger

Hvis du vil fortsætte med at køre Project Operations i Lite-udrulningstilstand, skal du benytte følgende fremgangsmåde:

1. Som [Global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-licens skal du finde det miljø i [PowerPlatform Administration](https://admin.powerplatform.com), hvor du vil installere Project Operations.
1. Installer **Microsoft Dynamics 365 Project Operations** fra udrulningslisten for Dynamics 365-apps. Du kan finde flere oplysninger i [Administrer Dynamics 365-apps](/power-platform/admin/manage-apps).
1. Da dit miljø indeholder dobbeltskrivningskomponenter, der kan hjælpe med at integrere installerede programmer til finans og drift, installerer Project Operations-installationen også de funktioner og udvidelser, der kræves for at integrere projektrelaterede data i programmer til finans og drift. Da du vil køre Project Operations i Lite-udrulningen, skal disse integrationskomponenter fjernes, da de vil oprette begrænsninger og afhængigheder for Lite-udrulningsscenarier. Fjern manuelt løsningerne **Dynamics 365 Project Operations-dobbeltskrivning** og **Dynamics 365 Project Operations-enhedstilknytning af dobbeltskrivning** for at fjerne disse komponenter.
1. Gå til **Project Operations -> Indstillinger -> Parametre**. Åbn detaljesiden **Projektparametre**, og angiv feltet **Funktion af løsningsopgradering** til **Kun Lite**. Derved sikres, at alle efterfølgende opgraderinger af Project Operations ikke henter integrationskomponenterne tilbage til Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
