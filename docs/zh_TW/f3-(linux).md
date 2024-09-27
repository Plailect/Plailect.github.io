# F3 (Linux)

## Required Reading

本篇為透過 F3 來檢查您 SD 卡是否有任何問題的附加章節。

根據您的 SD 卡的大小和電腦的速度，本過程可能將花費數小時才能完成 ！

本教學僅適用於 Linux 使用者。 如果您不在 Linux 平台上，請參閱 [H2testw (Windows)](h2testw-\(windows\)) 或 [F3XSwift (Mac)](f3xswift-\(mac\))。

## What You Need

- The latest version of [F3](https://github.com/AltraMayor/f3/releases/tag/v8.0)

## Instructions

1. 解壓 f3 `.zip`
2. `cd` 至 f3 目錄中
3. 運行 `make` 以編譯 F3
4. 將 SD 卡插入至電腦中
5. 掛載 SD 卡
6. 輸入 `./f3write <您 SD 卡的掛載點>`
7. 等到檢查完畢為止。 可以參考底下的範例。

```bash
$ ./f3write /media/michel/6135-3363/
Free space: 29.71 GB
Creating file 1.h2w ... OK!
...
Creating file 30.h2w ... OK!
Free space: 0.00 Byte
Average Writing speed: 4.90 MB/s
```

1. 輸入 `./f3read <您 SD 卡的掛載點>`
2. 等到檢查完畢為止。 可以參考底下的範例。

```bash
$ ./f3read /media/michel/6135-3363/
									SECTORS      ok/corrupted/changed/overwritten
Validating file 1.h2w ... 2097152/        0/      0/      0
...
Validating file 30.h2w ... 1491904/        0/      0/      0

	Data OK: 29.71 GB (62309312 sectors)
Data LOST: 0.00 Byte (0 sectors)
					Corrupted: 0.00 Byte (0 sectors)
	Slightly changed: 0.00 Byte (0 sectors)
				Overwritten: 0.00 Byte (0 sectors)
Average Reading speed: 9.42 MB/s
```

___

::: tip

If the test shows the result `Data LOST: 0.00 Byte (0 sectors)`, your SD card is good and you can delete all `.h2w` files on your SD card.

:::

::: danger

如果出現任何其他結果，您的 SD 卡可能是有問題且需要更換的！

:::

::: tip

Return to [Get Started](get-started)

:::
