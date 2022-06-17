---
title: Overskriftdetaljer for leverandørfakturaer
description: I denne artikel forklares de funktioner, der findes i leverandørfakturaoverskriften i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929851"
---
# <a name="header-details-for-vendor-invoices"></a>Overskriftdetaljer for leverandørfakturaer

[!include [banner](../../includes/dataverse-preview.md)]

_**Gælder for:** Lille udrulning - aftale til proformafakturering_

I denne artikel forklares de funktioner, der findes i leverandørfakturaoverskriften i Microsoft Dynamics 365 Project Operations.

Når projektledere planlægger og udfører projekter, kan de ansætte underleverandører og købe produkter og tjenester fra leverandører. Under et projekts udførelse påløber omkostningerne i kategorierne tjenester, materialer og udgifter, som er indkøbt via underentrepriser med leverandører. Leverandører fakturerer disse omkostninger til projekter ved at oprette leverandørfakturaer.

Følgende tabel indeholder oplysninger om felterne i leverandørfakturaoverskrifter i Project Operations.

| Felt | Description | Funktionspåvirkning |
| --- | --- | --- |
| Name | Navnet på leverandørfakturaen. | I alle rullelister for leverandørfakturaer vises navnet på leverandørfakturaen i første kolonne for at hjælpe dig med at identificere leverandørfakturaen. Når en leverandørfaktura oprettes fra en underentreprise, angives feltet **Navn** på leverandørfakturaen som standard til en værdi, der består af navnet på underentreprisen og den aktuelle dato. |
| Description | En kort beskrivelse af de tjenester og produkter, der faktureres på leverandørfakturaen. | None |
| Leverandør | Navnet på den virksomhed, der fakturerer produkterne og servicen. Dette firma bør være en firmapost, der har relationstypen **Leverandør** eller **Forsyningsvirksomhed**. | <p>På baggrund af den valgte leverandør angives automatiske standardværdier i følgende felter:</p><ul><li>Valuta</li><li>Prislister</li><li>Betalingsbetingelser</li><li>Betalingsadresse</li></ul> |
| Underentreprise | En reference til underentreprisen til leverandørfakturaen. | <p>På baggrund af den valgte underentreprise angives automatiske standardværdier i følgende felter:</p><ul><li>Valuta</li><li>Prislister</li><li>Betalingsbetingelser</li><li>Betalingsadresse</li></ul><p>Den underentreprise, der er valgt i leverandørfakturaens overskrift, angives som standard på leverandørfakturalinjerne og kan ikke ændres der.</p> |
| Fakturadato | Datoen for de faktiske omkostninger, der oprettes, når leverandørfakturaen bekræftes. | Fakturadatoen bruges også til at vælge den rette købsprisliste fra enten de prislister, der er knyttet til den relaterede leverandør, eller fra projektparametre. |
| Statusårsag | Statussen af leverandørfakturaen. | <p>Statussen bestemmer, hvor leverandørfakturaen befinder sig i forretningsprocessen, og om den kan redigeres. Her er nogle af de tilgængelige værdier:</p><ul><li>**Kladde** - Leverandørfakturaen kan redigeres.</li><li>**Bekræftet** – Leverandørfakturaen blev godkendt og bekræftet. Leverandørfakturaer med denne status kan ikke redigeres eller slettes.</li><li>**Igangværende** – Leverandørfakturaen gennemses. Leverandørfakturaer med denne status kan redigeres, men kan ikke slettes.</li><li>**Annulleret** – Leverandørfakturaen blev annulleret. Leverandørfakturaer med denne status kan ikke redigeres eller slettes.</li></ul> |
| Valuta | Den valuta, som leverandøren fakturerer for produkterne og servicer på leverandørfakturaen. | På en leverandørfaktura, der refererer til en underentreprise, angives valutaen for underentreprisen som standard som valutaen for leverandørfakturaen. På en leverandørfaktura, der ikke refererer til en underentreprise, angives standardværdien fra leverandørfirmaposten og kan ændres. Når en leverandørfaktura er gemt, kan valutaen ikke længere redigeres. |
| Kontraktenhed | Den division af virksomheden, der er ansvarlig for at modtage tjenester og/eller produkter fra leverandøren. | None |
| Betalingsbetingelser | Betalingsbetingelserne på leverandørfakturaer, der er udstedt. Standardværdien angives automatisk fra leverandørens firmapost. | Betalingsbetingelser fra en underentreprise kopieres til alle leverandørfakturaer, der er relateret til underentreprisen. Betalingsbetingelserne kan opdateres, hvis leverandørfakturaen har statussen **Kladde**. |
| Betalingsadresse | Adressen på den leverandør, som betalinger skal sendes til. Standardværdien angives automatisk fra leverandørens firmapost. | Betalingsadressen fra en underentreprise kopieres som betalingsadresse til alle de leverandørfakturaer, der er oprettet for underentreprisen. Betalingsadressen kan opdateres, hvis leverandørfakturaen har statussen **Kladde**. |
| Subtotal | Hvis leverandørfakturaen ikke indeholder nogen linjer, skal du angive delsummen for fakturaen eksklusiv moms. Hvis leverandørfakturaen indeholder linjer, er dette felt skrivebeskyttet. Det viste beløb vil i så fald være delsummen for alle linjer på leverandørfakturaen. | None |
| Samlet moms | Hvis leverandørfakturaen ikke indeholder nogen linjer, skal du angive den samlede moms for underentreprisen. Hvis leverandørfakturaen indeholder linjer, er dette felt skrivebeskyttet. Det viste beløb vil i så fald summen for moms for alle linjer på leverandørfakturaen. | None |
| Samlet beløb | I dette beregnede felt vises det samlede beløb for leverandørfakturaen, når momsen er inkluderet. | None |

> [!NOTE]
> Følgende felter på en leverandørfaktura kan ikke ændres, når leverandørfakturaen er gemt: **Leverandør**, **Underentreprise**, **Valuta**, **Kontraktenhed** og **Betalingsbetingelser**. Hvis der kræves ændringer af disse felter på en leverandørfaktura, skal du slette leverandørfakturaen og oprette en ny leverandørfaktura.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
