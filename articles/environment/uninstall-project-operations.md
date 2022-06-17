---
title: Fjerne Dynamics 365 Project Operations
description: Denne artikel indeholder oplysninger om, hvordan du afinstallerer Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911957"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Fjerne Dynamics 365 Project Operations 

_**Finder anvendelse for:** Project Operations for ressource-/ikke-lagerbaserede scenarier_

For at afinstallere Dynamics 365 Project Operations skal du tildeles administratorrollen.

1. Gå til **Indstillinger** > **Løsninger**.

    ![Indstillingsside.](./media/uninstall-proj-ops-solutions.png)
  
2. Fjern løsningerne i nøjagtig den rækkefølge, de er angivet i følgende tabel. 

    | Trin | Løsningsnavn                                    | Bemærk!                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 0 | msdyn_ProjectServiceUpgrade_managed.cab            | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 2 | ProjectOperations_Anchor                           | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 5 | ProjectService                                     | Ingen yderligere bemærkninger.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Ingen yderligere bemærkninger.                                                                         |
    | 7 | ProjectServiceCore                                 | Ingen yderligere bemærkninger.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 9 | FieldServiceCommon                                 | Kræves til dobbeltskrivning med Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Kræves til dobbeltskrivning med Dynamics 365 Finance eller Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Kræves til Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Kræves til Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Kræves til Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Kræves til Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Kræves til Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Kræves til Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Kræves til Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 19 | Dynamics365Notes                                   | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 21 | DualWriteCore                                      | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 23 | Dynamics365AssetManagement                         | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 26 | HCMCommon                                          | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 28 | Part                                              | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 29 | Dynamics365Company                                 | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 30 | CurrencyExchangeRates                              | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
    | 31 | AssetCommon                                        | Hvis den ikke blev fundet, kan du springe denne løsning over.                                                            |
