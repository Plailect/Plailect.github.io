# Flashing ntrboot (3DS Single System)

## Required Reading

לפני שאתם ממשיכים, שימו לב שקראתם את כל המידע ב [ntrboot](ntrboot)

שיטה זו דורשת כלום חוץ מה3DS הלא פרוץ שלכם וכרטיס פריצה תואם. שיטה זאת משתמשת בכרטיס פריצה כדי להריץ את קובץ ה`.nds` של צורב הNTRBOOT על ה3DS שלכם. זה אומר שכרטיס הפריצה שלכם חייב לתמוך בהרצת קבצי `.nds` על הגרסה של ה3DS שלכם. תסתכלו על הטבלה ב[ntrboot](ntrboot) למידע נוסף.

::: danger

שימו לב שבמקרים נדירים, יתכן שתהליך הצריבה **ישבור** כרטיס פריצה מזוייף ויגרום לו לא לעבוד. This is unlikely, but nevertheless, only original listed flashcarts are supported. To reduce the chance of receiving a counterfeit card, it is recommended that you use a reputable site to buy your flashcart (such as [NDS Card](https://www.nds-card.com/)).

:::

## What You Need

- Your ntrboot compatible flashcart
- The v1.3 release of [boot9strap-ntr](https://github.com/SciresM/boot9strap/releases/download/1.3/boot9strap-1.3-ntr.zip) (direct download)
- The latest release of [ntrboot_flasher_nds](https://github.com/jason0597/ntrboot_flasher_nds/releases/latest) (`ntrboot_flasher_nds.nds`)

## Instructions

### Section I - Prep Work

1. Power off your console
2. תכניסו את כרטיס ה- SD של כרטיס הפריצה שלכם אל המחשב
3. Create a folder named `ntrboot` on the root of your flashcart's SD card
4. Copy `boot9strap_ntr.firm` from the boot9strap ntr `.zip` to the `/ntrboot/` folder on your flashcart's SD card
5. Copy `ntrboot_flasher_nds.nds` to your flashcart's SD card
6. תכניסו בחזרה את כרטיס ה- SD של כרטיס הפריצה שלכם אל כרטיס הפריצה
7. Insert your ntrboot compatible DS / DSi flashcart into your console

### Section II - Flashing ntrboot

1. Launch `ntrboot_flasher_nds.nds` on your console using your flashcart
2. תלחצו (A) כדי להמשיך
3. תשתמשו ב (Up) וב(Down) כדי לבחור את הכרטיס פריצה שלכם
4. תלחצו (A) כדי להמשיך
5. Select "Dump flash" to make a backup of your flashcart's memory
6. Input the key combo given to confirm
7. תלחצו (A) כדי להמשיך
8. תשתמשו ב (Up) וב(Down) כדי לבחור את הכרטיס פריצה שלכם
9. תלחצו (A) כדי להמשיך
10. Select "Inject FIRM" to install boot9strap to your flashcart
11. Input the key combo given to confirm
12. תלחצו (A) כדי להמשיך
13. Power off your console

___

::: tip

Continue to [Installing boot9strap (ntrboot)](installing-boot9strap-\(ntrboot\))

:::
