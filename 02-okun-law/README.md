# Úloha 2 — Okunov zákon a štrukturálne zlomy 📉

> 🇬🇧 *Team assignment from an Econometrics course (Masaryk University): estimating Okun's law with structural-break testing. Static and dynamic specifications, Chow breakpoint and forecast tests, an interaction-dummy break model, and an asymmetry test. Built in R. Write-up in Slovak.*

Tímová úloha z predmetu Ekonometria (Masarykova univerzita, Skupina 02, Tím 07). Odhadujeme a testujeme **Okunov zákon** — vzťah medzi cyklickým vývojom výstupu a nezamestnanosti — vrátane štrukturálnych zlomov a asymetrie.

## Obsah analýzy

- **Príklad 1 — príprava a cyklické premenné.** Vizualizácia radov, HP filter na získanie output gap a cyklickej nezamestnanosti.
- **Príklad 2 — odhad Okunovho vzťahu.** Základný statický odhad, Chowov test štrukturálneho zlomu aj predpovedný test, statický odhad s interaktívnou premennou pre zlom a test asymetrie Okunovho vzťahu (odlišná reakcia na rast vs. pokles).
- **Príklad 3 — dynamický model.** Dynamická špecifikácia s výberom optimálneho počtu oneskorení, štrukturálny zlom v dynamickej verzii, odchýlky a intervaly.

## Autorstvo

Tímová úloha, autori: **P.-J. N., V. K., A. B.** a **Dana Kozáková** (Skupina 02, Tím 07).

Môj podiel: odhad Okunovho vzťahu: základný statický model, Chowov test štrukturálneho zlomu a predpovedný test, model s interaktívnou premennou pre zlom a test asymetrie. Revízia a zjednotenie kódu a komentárov naprieč dokumentom.

## Dáta

Štvrťročný reálny HDP a miera nezamestnanosti z **OECD Data Explorer** (https://data-explorer.oecd.org). Konkrétne rady a obdobie sú uvedené v úvode dokumentu. Dátové súbory nie sú súčasťou repozitára — sú voľne dostupné cez OECD.

## Spustenie

Stiahnite príslušné rady z OECD do priečinka `data/` a spustite:

```r
install.packages(c("tidyverse", "lubridate", "broom", "kableExtra", "car"))
rmarkdown::render("okun_law.Rmd")
```

alebo otvorením `.Rmd` v RStudiu → **Knit**.
