# Lekce 1 — Cheatsheet
## Úvod do datové analytiky s Power Query a Power BI

---

# Datová analytika

Datová analytika je proces:
1. sběru dat,
2. čištění dat,
3. transformace dat,
4. analýzy,
5. vizualizace,
6. interpretace výsledků.

Cíl:
- získat užitečné informace,
- podpořit rozhodování,
- identifikovat trendy a problémy.

---

# Power Query

Power Query slouží pro:
- import dat,
- cleaning dat,
- transformace,
- ETL proces.

Používá se hlavně pro:
- odstraňování duplicit,
- změny datových typů,
- spojování tabulek,
- práci s null hodnotami,
- automatizaci přípravy dat.

## Klíčová myšlenka
Power Query = příprava dat.

---

# Power BI

Power BI slouží pro:
- tvorbu dashboardů,
- reporting,
- KPI monitoring,
- vizualizace dat,
- business storytelling.

Umožňuje:
- interaktivní filtry,
- slicery,
- DAX výpočty,
- tvorbu metrik,
- sdílení reportů.

## Klíčová myšlenka
Power BI = interpretace a prezentace dat.

---

# ETL proces

## Extract
Načtení dat:
- Excel,
- SQL,
- CSV,
- API,
- cloudové služby.

## Transform
Úprava dat:
- cleaning,
- převody typů,
- sjednocení formátů,
- odstranění chyb.

## Load
Nahrání dat:
- do modelu,
- dashboardu,
- reportingu.

---

# Business mindset

Cílem analytiky není:
- vytvářet hezké grafy.

Cílem je:
- podpořit rozhodování,
- identifikovat trendy,
- pomoci businessu.

---

# Typické KPI

- Revenue
- Profit
- Orders
- Conversion Rate
- Customer Satisfaction
- Average Order Value

---

# Typické chyby junior analytiků

- příliš mnoho grafů,
- absence business otázky,
- špatná kvalita dat,
- ignorování datového modelu,
- chaos v dashboardu.

---

# Důležité pravidlo

Power Query = kuchyně  
Power BI = restaurace
Nejdřív musí být kvalitní data.
Teprve potom vzniká kvalitní dashboard.

---

# Lekce 2 — Cheatsheet
## Import dat do Power BI

---

# Import dat

Import dat je:
- první krok analytického workflow,
- základ ETL procesu,
- kritická část BI pipeline.

---

# Nejčastější datové zdroje

## Excel
Výhody:
- jednoduchost,
- dostupnost.

Nevýhody:
- manuální chyby,
- nekonzistence,
- špatná škálovatelnost.

---

## CSV

Výhody:
- univerzálnost,
- rychlost,
- jednoduchý formát.

Důležité:
- správný delimiter,
- encoding,
- datové typy.

---

## SQL databáze

Výhody:
- vysoký výkon,
- centralizace dat,
- škálovatelnost,
- možnost filtrování při importu.

Profesionální BI workflow používá primárně databáze.

---

# Důležitý BI princip

Neimportuj:
- všechna data,
- všechny sloupce,
- nepotřebnou historii.

Importuj:
- pouze relevantní data.

---

# Power Query Editor

Možnost:
- „Transformovat data“

otevírá:
- cleaning,
- ETL workflow,
- transformace dat.

V praxi se používá téměř vždy.

---

# Důležité kontroly po importu

- null values,
- duplicates,
- delimiters,
- encoding,
- datové typy,
- datumové formáty.

---

# Typické chyby junior analytiků

- import všeho,
- ignorování datových typů,
- práce bez validace dat,
- používání Excelu jako databáze,
- špatné delimitery.

---

# Důležité pravidlo

Data preview ≠ kvalitní data

Vždy validuj:
- strukturu,
- konzistenci,
- kvalitu dat.

---
