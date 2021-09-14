---
title: Underentrepriselinjeressourcer
description: I dette emne forklares det, hvordan du kan angive de dedikerede ressourcer, der leveres af leverandøren, for en bestemt underentrepriselinje for tid.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323364"
---
# <a name="subcontract-line-resources"></a>Underentrepriselinjeressourcer

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I Dynamics 365 Project Operations kan en leverandør angive ressourcer, der skal bruges til at levere den ressourcekapacitet, der købes på underentrepriselinjen for tid.

## <a name="create-subcontract-line-resources"></a>Opret underentrepriselinjeressourcer

Udfør disse trin for at oprette underentrepriselinjeressourcer.

1. I navigationsruden skal du vælge **Underentrepriser** og åbne den underentreprise, som du vil arbejde med.
2. Åbn den underentrepriselinje for tid, hvor du vil angive leverandørressourcer.
3. På fanen **Underentrepriselinjeressourcer** skal du i undergitteret vælge **+Ny underentrepriselinjeressource**.
4. På siden **Ny milepæl for underentrepriselinje** skal du angive de krævede oplysninger og derefter vælge **Gem og luk**.

I følgende tabel forklares felterne på underentrepriselinjeressourcen.

| Felt |  Beskrivelse |
| ----- | ------------ |
| Reserverbar ressource | Vælg en reserverbar ressource af typen "Kontraktansat medarbejder", som du vil bruge som ressourcen på underentrepriselinjen. Hvis du endnu ikke har oprettet en reserverbar ressource for den kontraktansatte medarbejder, skal dette felt være tomt. Der oprettes en reserverbar ressource, når du gemmer posten.  |
| Kontakt | Hvis feltet **Reserverbar ressource** er tomt, kan du oprette underentrepriselinjeressourcen ud fra en eksisterende kontaktperson. Brug opslaget til at få vist listen over aktive kontaktpersoner i systemet. Vælg en kontaktperson for leverandøren af denne underentreprise. Den kontaktperson, som du vælger, valideres, når du gemmer posten. Hvis den valgte kontaktperson ikke er en gyldig kontaktperson, gemmes posten ikke. Hvis der ikke findes en reserverbar ressource for den valgte kontaktperson, opretter systemet en reserverbar ressource for den valgte kontaktperson, inden det opretter underentrepriselinjeressourcen. |
| Bruger | Hvis feltet **Reserverbar ressource** er tomt, kan du oprette en underentrepriselinjeressource ved at vælge en aktiv bruger. Brug opslaget til at få vist listen over aktive brugere i systemet. Hvis der ikke findes en reserverbar ressource for den valgte bruger, opretter systemet en reserverbar ressource for den valgte bruger, inden underentrepriselinjeressourcen oprettes. |
| Startdato | Den dato, hvor underentreprisens arbejders tildeling starter. Hvis ressourcen er reserveret for en periode, der ligger forud for datointervallet, vises der en advarsel. |
| Slutdato | Den dato, hvor underentreprisens arbejders tildeling slutter. Hvis ressourcen er reserveret for en periode, der ligger efter datointervallet, vises der en advarsel. |
| Indsats | Det samlede antal arbejdstimer, som underentreprisens arbejder bruger på denne underentrepriselinje. Hvis ressourcen reserveres ud over den arbejdstid, den er tildelt til på denne underentreprise, vises der en advarsel. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
