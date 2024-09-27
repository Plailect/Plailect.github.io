# ntrboot

::: tip

Jeżeli Twój flashcart posiada już fabrycznie zainstalowany ntrboot (lub jeśli już go wgrałeś poprzednio), możesz przeskoczyć do [Instalacja boot9strap (ntrboot)](installing-boot9strap-\(ntrboot\)).

:::

## Required Reading

Instalacja boot9strap przy użyciu ntrboot wymaga kompatybilnego flashcarta NDS / DSi na którego można wgrać exploit ntrboot. Zauważ, że niektóre flashcarty są sprzedawane z fabrycznie wgranym ntrboot.

While the ntrboot exploit works independently of the system version, the ntrboot flasher (which installs the exploit to the cart) is not. This means that, depending on the versions and consoles supported by your flashcart, only certain methods may be available to you.

Zauważ, że flashcarty z "Time Bomb" nie będą w stanie uruchamiać plików `.nds` kiedy wykryją, że zegar systemowy przekroczył pewną datę wyznaczoną przez firmware flashcarta. Jedną z metod na obejście tego problemu jest przestawienie zegara systemowego na wcześniejszą datę.

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

Ensure your flashcart is able to launch `.nds` files on your console before beginning. Niektóre flashcarty mogą wymagać dodatkowych plików "kernel" skopiowanych na kartę SD flashcarta. Zobacz instrukcje dla poszczególnych flashcartów aby dowiedzieć się więcej.

Zauważ, że niektóre metody mogą zawierać dodatkowe informacje o kompatybilności.

The usage of this exploit, regardless of the flashing method, requires access to a small magnet if the target console is of a folding style (any 3DS family system that is not the old 2DS with a sleep switch). This is because the exploit requires your console to enter sleep mode while still having access to the buttons.

::: info

To test if a magnet will work, hold it on or around the (A)(B)(X)(Y) buttons while the console is powered on to see if it triggers sleep mode. Jeśli tak, to oba ekrany wygasną dopóki magnes będzie trzymany w tym miejscu.

:::

Zauważ, że flashcart nie będzie mógł być użyty do standardowych funkcji, gdy zainstalowany jest na nim exploit ntrboot (z wyjątkiem przypadku Acekard 2i, który pozostaje funkcjonalny _tylko w systemach 3DS z zainstalowanym niestandardowym oprogramowaniem układowym_). This means that, for most flashcarts, it will not even display on the HOME Menu. Na końcu instrukcji instalacji ntrboot znajdują się opcjonalne kroki, aby usunąć go z flashcarta po zakończeniu.

::: danger

Zauważ, że w niektórych rzadkich przypadkach proces wgrywania ntrboot na podrobiony flashcart może go **"zbrickować"** i permanentnie uszkodzić. This is unlikely, but nevertheless, only original listed flashcarts are supported. To reduce the chance of receiving a counterfeit card, it is recommended that you use a reputable site to buy your flashcart (such as [NDS Card](https://www.nds-card.com/)).

:::

___

## Methods

___

### Flashing ntrboot (3DS Single System)

Ta metoda wymaga tylko 3DS'a którego chcesz przerobić oraz kompatybilnego z ntrboot flashcarta. Ta metoda używa flashcarta aby uruchomić plik ntrboot flasher `.nds` na twoim 3DSie. Oznacza to, że twój flashcart musi obsługiwać uruchamianie plików `.nds` na twoim 3DSie. Zobacz powyższą tabelę aby dowiedzieć się więcej.

::: tip

Przejdź do [Wgrywanie ntrboot (Pojedynczy System 3DS)](flashing-ntrboot-\(3ds-single-system\))

:::

___

### Flashing ntrboot (3DS Multi System)

This method requires temporary access to a second 3DS family console that is already running boot9strap. Dzięki tej metodzie flashcart nie musi obsługiwać wersji systemu żadnego 3DS'a.

::: tip

Przejdź do [Wgrywanie ntrboot (Kilka Systemów 3DS)](flashing-ntrboot-\(3ds-multi-system\))

:::

___

### Flashing ntrboot (NDS)

Ta metoda wymaga tymczasowego dostępu do konsoli Nintendo DS lub DS lite kompatybilnej z twoim flashcartem. Ta metoda używa flashcarta aby uruchomić plik ntrboot flasher `.nds` na twoim NDS.

::: tip

Przejdź do [Wgrywanie ntrboot (NDS)](flashing-ntrboot-\(nds\))

:::

___

### Flashing ntrboot (DSi)

Ta metoda wymaga tymczasowego dostępu do konsoli Nintendo DSi kompatybilnej z twoim flashcartem. Ta metoda używa flashcarta aby uruchomić plik ntrboot flasher `.nds` na twoim DSi. Oznacza to, że twój flashcart musi obsługiwać uruchamianie plików `.nds` na twoim DSi. Zobacz powyższą tabelę aby dowiedzieć się więcej.

::: tip

Przejdź do [Wgrywanie ntrboot (DSi)](flashing-ntrboot-\(dsi\))

:::
