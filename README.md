# Ekonometria — projekty v R a gretli 📊

> 🇬🇧 *Econometrics projects from graduate coursework (Masaryk University). One solo project — a LOGIT analysis of emergency-care determinants in type-1 diabetes — plus three team assignments (CAPM, Okun's law, the New Keynesian Phillips Curve). Built in R and gretl. Write-ups are in Slovak.*

Zbierka ekonometrických projektov z magisterského štúdia (Masarykova univerzita). Jeden samostatný projekt a tri tímové úlohy.

---

## ⭐ [Determinanty urgentných návštev pri diabete 1. typu](t1d-urgent-care-logit/) — samostatný projekt

Binárny **LOGIT model** determinantov urgentných návštev (ťažká hypoglykémia / DKA) u pacientov s diabetom 1. typu na dátach registra T1D Exchange (n = 2 454). Postupný výber prediktorov spomedzi 70+ špecifikácií, diagnostika kolinearity (VIF, BKW) a porovnanie s probit modelom. Samostatná práca, v gretli.

*11 významných prediktorov · McFadden R² 0,159 · dáta podliehajú podmienkam T1D Exchange (nie sú v repe)*

---

## Tímové úlohy (Skupina 02, Tím 07)

Nasledujúce tri úlohy sú tímová práca autorov **P.-J. N., V. K., A. B.** a **Dana Kozáková**.

### [1 — Analýza modelu CAPM](01-capm-analysis/)
Odhad a test modelu oceňovania kapitálových aktív na akciách S&P 500: charakteristické krivky, beta koeficienty, test Jensenovej alfy, security market line, Fama-MacBeth špecifikácia, Chow testy a dual-beta model asymetrie. V R (tidyverse).
> **Môj podiel:* — príprava dát, výpočet výnosov, odhad beta koeficientov a charakteristických kriviek, test nulovosti konštanty α; plus revízia kódu naprieč dokumentom.

### [2 — Okunov zákon (Švajčiarsko)](02-okun-law/)
Odhad Okunovho vzťahu pre Švajčiarsko so štrukturálnymi zlomami: HP filter, Chowov test a predpovedný test, model s interaktívnou premennou pre zlom, test asymetrie a dynamická špecifikácia. V R.
> **Môj podiel:** — odhad Okunovho vzťahu: statický model, Chowov test štrukturálneho zlomu a predpovedný test, model s premennou pre zlom, test asymetrie.

### [3 — Novokeynesovská Phillipsova krivka (Francúzsko)](03-nkpc-france/)
Odhad NKPC pre Francúzsko podľa Galí & Gertler (1999): GMM (dopredu pozerajúca aj hybridná, redukovaná i štrukturálna forma) s J-testom, obmedzené modely pre test dlhodobej vertikality, NLS a ML odhady (normálne aj t-rozdelenie) a LR testy. V R.
> **Môj podiel:** — celý odhadový blok NKPC: GMM odhady, obmedzené modely, NLS a ML (vrátane t-rozdelenia) a LR testy naprieč metódami.

---

## Použité technológie

`R` (tidyverse, gmm, car, broom, PerformanceAnalytics) · `gretl` · RMarkdown

Každý projekt má vlastný priečinok s notebookom/skriptom, dátami alebo návodom na ich získanie a vlastným README s podrobnosťami.

## Autorka

Mgr. Dana Kozáková — matematika, štatistika, dáta, AI. [GitHub profil](https://github.com/danakozakova)·
