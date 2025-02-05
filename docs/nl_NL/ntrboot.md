# ntrboot

::: tip

Als je flashkaart al geflashed is met ntrboot bij aankoop (of je hebt je flashkaart al geflashed met ntrboot), kan je doorgaan naar [Boot9strap installeren (ntrboot)](installing-boot9strap-\(ntrboot\)) voor instructies over hoe het te gebruiken.

:::

## Required Reading

Om Boot9strap te installeren heb je een ondersteunde NDS / DSi flashkaart nodig om ntrboot op te installeren. Merk op dat sommige van deze flashkaarten vooraf geflasht worden met ntrboot.

Terwijl de ntrboot exploit onafhankelijk van de systeemversie werkt, is de ntrboot flasher (die de exploit op de kaart installeert) dat niet. This means that, depending on the versions and consoles supported by your flashcart, only certain methods may be available to you.

Sommige flashkaarten met een "Time Bomb" zullen niet meer `.nds` bestanden starten wanneer ze detecteren dat de systeem klok een bepaalde datum heeft behaald. Deze tijd wordt bepaald door de flashkaart firmware. Een manier om dit te omzeilen, is om de systeemklok op een eerdere datum in te stellen.

| Flashcart Name                                                                                                              |          Current Price |                       "Time Bomb"?                       |                                 3DS Versions?                                 |                           DSi Versions?                           | Other Notes                                                                                                                                                                                                                                                                                                |
| --------------------------------------------------------------------------------------------------------------------------- | ---------------------: | :------------------------------------------------------: | :---------------------------------------------------------------------------: | :---------------------------------------------------------------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**Ace3DS X**](https://www.nds-card.com/ProShow.asp?ProID=575)                                                              | $17.99 |                            No                            |                                      ALL                                      |                                ALL                                | **Comes pre-flashed with ntrboot** (external switch to switch between ntrboot ("3DS") and NDS modes); do not manually flash with ntrboot. This cart needs an SD card inserted to function for both ntrboot and regular NDS firmware. |
| [**R4i-SDHC B9S** (r4i-sdhc.com)](http://www.nds-card.com/ProShow.asp?ProID=574)         | $16.99 |                     September 3, 2024                    |                                      ALL                                      |                                ALL                                | **Comes pre-flashed with ntrboot**; can be flashed back to an NDS flashcart.                                                                                                                                                                                                               |
| [**DSTT** (ndstt.com)](http://www.nds-card.com/ProShow.asp?ProID=157)                    | $11.99 |                            No                            |                                      None                                     |                                None                               | Only models with [certain flash chips](https://gist.github.com/aspargas2/fa2a70aed3a7fe33f1f10bc264d9fab6) are compatible with ntrboot.                                                                                                                                                    |
| [**R4i-SDHC 3DS RTS** (r4i-sdhc.com)](http://www.nds-card.com/ProShow.asp?ProID=146)     | $15.99 | 1.85b: September 3, 2024 |                                      ALL                                      |                                ALL                                |                                                                                                                                                                                                                                                                                                            |
| [**R4iSDHC GOLD Pro 20XX** (r4isdhc.com)](http://www.nds-card.com/ProShow.asp?ProID=490) | $17.99 |  4.0b: September 3, 2024 |                                      ALL                                      |                                ALL                                | Only r4isdhc **.com** carts marked with a year of 2014 or later are compatible.                                                                                                                                                                                            |
| **Ace3DS Plus**                                                                                                             |                        |                            No                            |                                      ALL                                      |                                ALL                                | This cart needs an SD card inserted to function for both ntrboot and regular NDS firmware.                                                                                                                                                                                                 |
| **Acekard 2i**                                                                                                              |                        |                            No                            |       <= 4.3.0       | <= 1.4.4 |                                                                                                                                                                                                                                                                                                            |
| **Gateway Blue**                                                                                                            |                        |                            No                            | 4.1.0 - 4.5.0 |                                ALL                                |                                                                                                                                                                                                                                                                                                            |
| **Infinity 3 R4i** (r4infinity.com)                                                      |                        |                            No                            |                                      ALL                                      |                                ALL                                |                                                                                                                                                                                                                                                                                                            |
| **R4 3D Revolution**                                                                                                        |                        |                            No                            |                                      None                                     |                                None                               |                                                                                                                                                                                                                                                                                                            |
| **R4i Gold 3DS Plus** (r4ids.cn)                                                         |                        |                            No                            |                                      ALL                                      |                                ALL                                | **Comes pre-flashed with ntrboot** ([internal switch to switch between ntrboot and NDS modes](/images/screenshots/r4i-gold-3ds-plus.png)); do not manually flash with ntrboot.                                                                                          |
| **R4i Gold 3DS** (r4ids.cn)                                                              |                        |                            No                            |                                      ALL                                      |                                ALL                                | All carts are compatible.                                                                                                                                                                                                                                                                  |
| **R4i Ultra** (r4ultra.com)                                                              |                        |                            No                            |       <= 4.3.0       |                                ALL                                |                                                                                                                                                                                                                                                                                                            |
| **R4i-SDHC 3DS RTS Deluxe Edition**                                                                                         |                        |                          Unknown                         |                                      ALL                                      |                                ALL                                | Only the Deluxe Edition with the blue sticker is compatible.                                                                                                                                                                                                                               |
| **R4iSDHC RTS LITE 20XX** (r4isdhc.com)                                                  |                        |  4.0b: September 3, 2024 |                                      ALL                                      |                                ALL                                | Only r4isdhc **.com** carts marked with a year of 2014 or later are compatible.                                                                                                                                                                                            |
| **R4iSDHC Dual-Core 20XX** (r4isdhc.com)                                                 |                        |  4.0b: September 3, 2024 |                                      ALL                                      |                                ALL                                | Only r4isdhc **.com** carts marked with a year of 2014 or later are compatible.                                                                                                                                                                                            |

::: info

![](/images/screenshots/ntrboot-flashcarts.png)

:::

Ensure your flashcart is able to launch `.nds` files on your console before beginning. Sommige flashkaarten hebben misschien firmware of "kernel" bestanden nondig op de SD kaart. Controlleer uw specefieke flashkaart's instructies voor meer informatie.

Sommige methoden kunnen extra informatie hebben over welke kaarten geschikt zijn.

The usage of this exploit, regardless of the flashing method, requires access to a small magnet if the target console is of a folding style (any 3DS family system that is not the old 2DS with a sleep switch). This is because the exploit requires your console to enter sleep mode while still having access to the buttons.

::: info

To test if a magnet will work, hold it on or around the (A)(B)(X)(Y) buttons while the console is powered on to see if it triggers sleep mode. Als het werkt, gaan beide schermen uit zolang de magneet op de goede plaats gehouden wordt.

:::

Onthoud dat de flashkaart niet meer zijn normale functies kan gebruiken terwijl ntrboot er op geinstalleerd is (behalve voor de Acekard 2i, die werkt nog normaal _alleen op NDS mode en custom firmware 3DS systemen_). Dit betekent dat voor de meeste flashkaarten het niet eens zal worden weergegeven in het HOME-menu. Op het einde van de intructies van ntrboot flashen, zijn er instructies hoe je ntrboot van je flashkaart kan verwijderen.

::: danger

Merk op dat je namaak flashkaarten in zeldzame gevallen kan **bricken** tijdens het flashproces en hem dus onbruikbaar maakt. Dat is onwaarschijnlijk, maar toch worden alleen originele opgesomde flashkaarten ondersteund. To reduce the chance of receiving a counterfeit card, it is recommended that you use a reputable site to buy your flashcart (such as [NDS Card](https://www.nds-card.com/)).

:::

___

## Methods

___

### Flashing ntrboot (3DS Single System)

Deze methode vereist niets meer dan je stock, unhacked 3DS en een compatibele flashkaart. Deze methode gebruikt de flashcart voor het uitvoeren van het ntrboot flasher '.nds' bestand op uw 3DS. Dit betekent dat uw flashcart `.nds` bestanden moet kunnen starten op jouw 3DS's versie. Zie het flashkaart tabel hier boven voor meer informatie.

::: tip

Ga verder naar [ntrboot installeren (3DS 1 systeem)](flashing-ntrboot-\(3ds-single-system\))

:::

___

### Flashing ntrboot (3DS Multi System)

This method requires temporary access to a second 3DS family console that is already running boot9strap. Hiervoor hoeft je flashkaart niet de beide 3DS versies ondersteunen.

::: tip

Ga verder naar [ntrboot installeren (3DS meerdere systemen)](flashing-ntrboot-\(3ds-multi-system\))

:::

___

### Flashing ntrboot (NDS)

Met deze methode heb je tijdelijk toegang nodig tot een Nintendo DS of een Nintendo DS Lite die werkt met jouw flashkaart. Deze methode gebruikt de flashkaart voor het uitvoeren van het ntrboot flasher '.nds' bestand op je NDS.

::: tip

Ga verder naar [ntrboot installeren (NDS)](flashing-ntrboot-\(nds\))

:::

___

### Flashing ntrboot (DSi)

Voor deze methode heb je tijdelijk toegang nodig tot een Nintendo DSi die werkt met jouw flashkaart. Deze methode gebruikt de flashkaart om het ntrboot flasher `.nds` bestand te gebruiken op uw DSi. Dat betekend dat uw flashkaart `.nds` bestanden moet kunnen starten op uw DSi's versie. Zie het flashkaart tabel hier boven voor meer informatie.

::: tip

Ga verder naar [ntrboot installeren (DSi)](flashing-ntrboot-\(dsi\))

:::
