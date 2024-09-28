# Installazione di boot9strap (super-skaterhax)

:::details Dettagli tecnici (opzionale)

Per i dettagli tecnici sugli exploit che utilizzerai in questa pagina, vedi [qui](https://github.com/zoogie/super-skaterhax).

:::

### Note di compatibilità

Super-skaterhax (quando utilizzato per avviare l'Homebrew Launcher) è compatibile con i modelli New dalla versione 11.15.0 in poi di tutte le regioni.

::: warning

Le istruzioni indicate si applicano solo a New 3DS, New 3DS XL e New 2DS XL. Assicurati che la console che stai modificando sia un New 3DS, New 3DS XL, o un New 2DS XL prima di continuare.

:::

### Cosa serve

- Il file `.zip` di [Super-skaterhax](https://skater.nintendohomebrew.com) per la regione e la versione di sistema della tua console

#### Sezione I - Preparazione

In questa sezione copierai i file necessari per attivare sia super-skaterhax che l'Homebrew Launcher.

1. Spegni la tua console

2. Inserisci la scheda SD nel tuo computer

3. Copia tutto il contenuto dell'archivio `.zip` di Super-skaterhax nella directory principale della tua scheda SD, sovrascrivendo eventuali file esistenti

   ::: info

   ![](/images/screenshots/skater-root-layout.png)

   :::

4. Reinserisci la scheda SD nella tua console

5. Accendi la tua console

6. Avvia le Impostazioni della console

7. Seleziona "Impostazioni generali"

8. Navigate to "Profile" -> "Region Settings"
   - If you get a [warning](/images/screenshots/skaterhax/country-change-notice.png) that tells you that you will lose access to Nintendo Network ID features, you can safely select OK to continue
   - After completing this page, you can restore the region settings back to normal

9. Seleziona le seguenti opzioni in base alla regione della tua console ([immagine](/images/screenshots/skaterhax/skater-lang.png))
   - USA: United States, Do Not Set
   - EUR: United Kingdom, Do Not Set
   - JPN: 日本, 設定しない
   - KOR: 대한민국, 설정하지 않음

10. Esci dalle Impostazioni della console

#### Section II - super-skaterhax

In questa sezione visiterai la pagina web dell'exploit del browser, che avvierà l'Homebrew Launcher.

::: info

Se non l'hai già fatto, assicurati di avere una connessione Internet funzionante configurata sulla tua console.

:::

1. Nel menu HOME, premi contemporaneamente i pulsanti dorsali L e R per avviare la fotocamera
   - If you are unable to open the camera, open the Internet Browser and manually type the URL instead (`https://zoogie.github.io/web/super/` for EUR/USA/JPN, `https://zoogie.github.io/web/korea` for KOR)
2. Tocca il pulsante "codice QR" e scansiona uno dei seguenti codici QR per la regione della tua console [qui](https://user-images.githubusercontent.com/28328903/226086338-585bfdac-0aac-44c0-b413-89206d2815d8.png)
   - If you get a security certificate warning, please ensure that the system date is today's
3. Premi il pulsante (Select) per aprire la pagina dei preferiti
   - If your (Select) button does not respond, tap the star icon on the bottom-left corner of the screen
4. Tocca "Aggiungi ai preferiti"
5. Premi (B) una volta per ritornare al browser
6. Press (ZR) to open the tab list
   - If your (ZR) button does not respond, tap the two overlapped squares near the bottom-right corner of the screen
7. Make sure that the only tab open is the super-skaterhax website
   - This tab should be highlighted in blue on the tab list
   - If other tabs are open, close them
8. Premi (B) una volta per ritornare al browser
9. Premi (Start) per aprire il menu contestuale
   - If your (Start) button does not respond, tap the 3-line menu on the bottom-right corner of the screen
10. Tocca su "Impostazioni"
11. Tocca su "Elimina cookie"
12. Premi il pulsante (A) per continuare
13. Premi (Home) per tornare al menu HOME e premi subito (A) per avviare nuovamente il browser
14. Select the "GO GO!" button on the top of the bottom screen
15. Press (A) to dismiss the [popup](/images/screenshots/skaterhax/skater-popup.png)
    - If your console freezes on a yellow screen, hold the POWER button until it turns off, then retry this section
    - If your console freezes on a red screen, hold the POWER button until it turns off, redo step 3 of Section II, then retry this section
    - If your console [shows the word Text on the top-left corner of the bottom screen](/images/screenshots/skaterhax/skater-old3ds.png), you have an Old 3DS and this exploit **will not work on your device**. In questo caso, dovresti usare invece [MSET9](installing-boot9strap-\(mset9\))
    - Se ottieni un altro errore riprova altre 5 volte, e se continua a non funzionare [segui questa guida per risolvere il problema](troubleshooting#installing-boot9strap-super-skaterhax)
16. La tua console avvierà l'Homebrew Launcher
17. Avvia nimdsphax dalla lista degli homebrew
18. Se l'exploit è andato a buon fine, si avvierà SafeB9SInstaller
    - If your console freezes on a red or green screen, hold the POWER button until it turns off, then retry this section
    - This may take up to five attempts

#### Sezione III - Installazione di boot9strap

In questa sezione installerai il custom firmware sulla tua console.

1. Quando richiesto, inserisci la combinazione di tasti richiesta sullo schermo superiore per installare boot9strap
   - Se una sezione nella schermata inferiore ha un testo di colore rosso, e non ti viene richiesto di inserire una combinazione di tasti, [segui questa guida per risolvere i problemi](troubleshooting#issues-with-safeb9sinstaller)
2. Una volta completato tutto, premi (A) per riavviare la console

<!--@include: ./_include/configure-luma3ds.md -->

<!--@include: ./_include/luma3ds-installed-note.md -->

___

::: info

You may now restore your region settings back to normal.

:::

::: tip

Prosegui con il [Completamento dell'installazione](finalizing-setup)

:::
