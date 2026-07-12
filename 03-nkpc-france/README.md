# Úloha 3 — Novokeynesovská Phillipsova krivka (NKPC) 🇫🇷

> 🇬🇧 *Team assignment from an Econometrics course (Masaryk University): estimating the New Keynesian Phillips Curve for France, replicating the approach of Galí & Gertler (1999). GMM estimation (forward-looking and hybrid, reduced and structural forms) with J-tests, restricted models for long-run verticality, plus NLS and ML estimates (normal and t-distributed errors) and likelihood-ratio tests. Built in R. Write-up in Slovak.*

Tímová úloha z predmetu Ekonometria (Masarykova univerzita, Skupina 02, Tím 07). Odhadujeme **novokeynesovskú Phillipsovu krivku (NKPC)** pre Francúzsko a porovnávame výsledky s pôvodným článkom Galí & Gertler (1999). Štvrťročné dáta 2003–2025 (~88 pozorovaní) z OECD/FRED/ECB.

## Obsah analýzy

- **Príklad 1 — voľba ekonomiky a príprava dát.** Zlúčenie radov (CPI, HDP, jednotkové náklady práce, úrokové miery, mzdy) z viacerých databáz, harmonizácia frekvencie a obdobia.
- **Príklad 2 — odhad NKPC.** Transformácia premenných a HP filter; GMM odhady dopredu pozerajúcej aj hybridnej NKPC v redukovanej i štrukturálnej forme s J-testom; obmedzené modely pre β = 1 (test dlhodobej vertikality); odhady metódou nelineárnych najmenších štvorcov (NLS) a maximálnej vierohodnosti (ML, normálne aj t-rozdelenie); porovnanie metód a LR testy vertikality.

## Autorstvo

Tímová úloha, autori: **P.-J. N., V. K., A. B.** a **Dana Kozáková** (Skupina 02, Tím 07).

Môj podiel: GMM odhady (redukovaná aj štrukturálna forma, dopredu pozerajúca aj hybridná), obmedzené modely pre test vertikality, NLS a ML odhady (vrátane t-rozdelenia) a LR testy naprieč metódami. Revízia a zjednotenie kódu a komentárov naprieč dokumentom.

## Dáta

Štvrťročné makroekonomické rady pre Francúzsko z **OECD**, **FRED** a **ECB** (CPI, reálny HDP, jednotkové náklady práce, dlhodobá a krátkodobá úroková miera, mzdy, deflátor). Konkrétne série a zdroje sú vymenované v úvode dokumentu. Dátové súbory nie sú súčasťou repozitára — sú voľne dostupné cez uvedené databázy.

## Spustenie

Stiahnite uvedené rady do priečinka `data/` a spustite:

```r
install.packages(c("tidyverse", "lubridate", "gmm", "broom",
                   "kableExtra", "sandwich"))
rmarkdown::render("nkpc_france.Rmd")
```

alebo otvorením `.Rmd` v RStudiu → **Knit**.

## Referencia

Galí, J., & Gertler, M. (1999). *Inflation dynamics: A structural econometric analysis.* Journal of Monetary Economics, 44(2), 195–222.
