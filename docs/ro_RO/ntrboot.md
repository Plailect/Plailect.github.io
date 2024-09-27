# ntrboot

::: tip

Dacă aveți ntrboot deja instalat pe flashcart, (sau ați instalat deja ntrboot pe flashcart), puteți sări la [Instalând boot9strap (ntrboot)](installing-boot9strap-\(ntrboot\)) pentru instrucțiuni despre cum să-l folosiți.

:::

## Required Reading

Instalând boot9strap cu ntrboot necesită un flashcart DS/DSi compatibil pentru a instala ntrboot. Țineți cont că unele dintre flashcart-uri se vind cu ntrboot preinstalat.

While the ntrboot exploit works independently of the system version, the ntrboot flasher (which installs the exploit to the cart) is not. This means that, depending on the versions and consoles supported by your flashcart, only certain methods may be available to you.

Țineți cont că cardurile cu "Bombă cu Ceas" nu vor mai putea să pornească fișiere `.nds` când vor detecta că ceasul sistemului a trecut o dată stabilită de firmware-ul flashcart-ului. O metodă pentru a ocoli acest lucru este de a seta ceasul sistemului la o dată veche.

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

Ensure your flashcart is able to launch `.nds` files on your console before beginning. Unele flashcart-uri ar putea avea nevoie ca fișierele de firmware sau "kernel" să fie copiate în cardul SD al flashcart-ului. Consultați instrucțiunile specifice ale flashcart-ului pentru mai multe informații.

Țineți cont că metodele specifice pot avea informații suplimentare despre compatibilitate.

The usage of this exploit, regardless of the flashing method, requires access to a small magnet if the target console is of a folding style (any 3DS family system that is not the old 2DS with a sleep switch). This is because the exploit requires your console to enter sleep mode while still having access to the buttons.

::: info

To test if a magnet will work, hold it on or around the (A)(B)(X)(Y) buttons while the console is powered on to see if it triggers sleep mode. Dacă e așa, ambele ecrane se vor stinge cât timp magnetul este ținut în același loc.

:::

Țineți cont că flashcart-ul nu va putea fi folosit pentru funcțiile lui obişnuite cât timp exploit-ul este instalat pe el (excepție în cazul unui Acekard 2i, care rămâne funcțional _numai pe dispozitivele NDS și 3DS care au custom firmware instalat_). This means that, for most flashcarts, it will not even display on the HOME Menu. Există paşi opționali la sfârșitul instrucțiunilor pentru instalarea ntrboot-ului cu scopul de a-l şterge de pe flashcart după ce ați terminat.

::: danger

Țineți cont că în anumite cazuri rare, poate fi posibil ca procesul de instalare să facă **brick** unui flashcard contrafăcut și să devină complet nefolositor. This is unlikely, but nevertheless, only original listed flashcarts are supported. To reduce the chance of receiving a counterfeit card, it is recommended that you use a reputable site to buy your flashcart (such as [NDS Card](https://www.nds-card.com/)).

:::

___

## Methods

___

### Flashing ntrboot (3DS Single System)

Această metodă necesită nimic mai mult decât un 3DS stoc nemodat şi un flashcart compatibil. Această metodă folosește flashcart-ul pentru a rula fişierul ntrboot flasher `.nds` pe 3DS-ul dumneavoastră. Asta înseamnă că flashcart-ul trebuie să poată porni fişiere `.nds` pe versiunea 3DS-ului dumneavoastră. Vedeți tabelul de flashcart-uri de mai sus pentru mai multe informații.

::: tip

Continuați la [Instalând ntrboot (Un 3DS)](flashing-ntrboot-\(3ds-single-system\))

:::

___

### Flashing ntrboot (3DS Multi System)

This method requires temporary access to a second 3DS family console that is already running boot9strap. Aceasta nu are nevoie de flashcart pentru a susține oricare dintre 3DS-uri.

::: tip

Continuați la [Instalând ntrboot (Două 3DS-uri)](flashing-ntrboot-\(3ds-multi-system\))

:::

___

### Flashing ntrboot (NDS)

Această metodă necesită acces temporar la un Nintendo DS sau Nintendo DS Lite care este compatibil cu flashcart-ul dumneavoastră. Această metodă folosește flashcart-ul pentru a rula fişierul ntrboot flasher `.nds` pe NDS-ul dumneavoastră.

::: tip

Continuați la [Instalând ntrboot (NDS)](flashing-ntrboot-\(nds\))

:::

___

### Flashing ntrboot (DSi)

Această metodă necesită acces temporar la un Nintendo DSi care este compatibil cu flashcart-ul dumneavoastră. Această metodă folosește flashcart-ul pentru a rula fişierul ntrboot flasher `.nds` pe DSi-ul dumneavoastră. Asta înseamnă că flashcart-ul trebuie să poată porni fişiere `.nds` pe versiunea DSi-ului dumneavoastră. Vedeți tabelul de flashcart-uri de mai sus pentru mai multe informații.

::: tip

Continuați la [Instalând ntrboot (DSi)](flashing-ntrboot-\(dsi\))

:::
