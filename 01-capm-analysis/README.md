# Úloha 1 — Analýza modelu CAPM 📈

> 🇬🇧 *Team assignment from an Econometrics course (Masaryk University): estimating and testing the Capital Asset Pricing Model (CAPM) on S&P 500 stocks. Characteristic lines and beta estimation, tests of Jensen's alpha, the security market line, the Fama-MacBeth specification, Chow tests for structural breaks, and a dual-beta asymmetry model. Built in R (tidyverse). Write-up in Slovak.*

Tímová úloha z predmetu Ekonometria (Masarykova univerzita, Skupina 02, Tím 07). Odhadujeme a testujeme **model oceňovania kapitálových aktív (CAPM)** na akciách indexu S&P 500 (dataset 505 titulov, 2013–2018, mesačné výnosy).

## Obsah analýzy

- **Príklad 1 — beta koeficienty a charakteristické krivky.** Načítanie a príprava dát, výpočet mesačných logaritmických výnosov, konštrukcia trhového portfólia, odhad beta koeficientu pre každý titul a test nulovosti konštanty α (Jensenova alfa) na 5 % hladine.
- **Príklad 2 — testovanie platnosti CAPM.** Tvorba portfólií zoradených podľa beta, odhad security market line, Waldov test γ₀, test linearity vzťahu a špecifikácia podľa Fama-MacBeth.
- **Príklad 3 — štrukturálne zlomy a asymetria.** Chowov test štrukturálneho zlomu aj predpovedný test v beta koeficientoch, platnosť CAPM na dvoch podobdobiach a dual-beta model (odlišná reakcia beta na rastúci vs. klesajúci trh).

Výstup je RMarkdown, ktorý sa generuje do interaktívneho HTML dokumentu (`code_folding`, plávajúci obsah).

## Autorstvo

Tímová úloha, autori: **P.-J. N., V. K., A. B.** a **Dana Kozáková** (Skupina 02, Tím 07).

Môj podiel: **Príklad 1** — získanie a príprava dát, výpočet výnosov, odhad beta koeficientov a charakteristických kriviek, test nulovosti konštanty α. 
Revízia a zjednotenie kódu a komentárov naprieč dokumentom.

## Dáta

Verejný dataset **S&P 500 stock data** (denné ceny 505 titulov, 2013–2018), dostupný na Kaggle: https://www.kaggle.com/datasets/camnugent/sandp500

Bezriziková sadzba je predpokladaná nulová; trhový index je konštruovaný ako rovnako vážený priemer mesačných výnosov všetkých titulov.

## Spustenie

Stiahnite `all_stocks_5yr.csv` z odkazu vyššie a uložte do priečinka projektu. Potom:

```r
# potrebné balíky
install.packages(c("tidyverse", "lubridate", "quantmod",
                   "PerformanceAnalytics", "broom", "kableExtra",
                   "car", "moments"))

# vygenerovanie dokumentu
rmarkdown::render("capm_analysis.Rmd")
```

alebo otvorením `.Rmd` v RStudiu a kliknutím na **Knit**.
