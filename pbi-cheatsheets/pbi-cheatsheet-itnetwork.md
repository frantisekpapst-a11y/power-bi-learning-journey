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

# Lekce 3 — Cheatsheet
## Seznámení s Power Query a úvod do čištění dat

---

# Hlavní princip

Garbage In = Garbage Out

Špatná data:
- → špatná analýza,
- → špatné KPI,
- → špatná business rozhodnutí.

---

# Proč čistíme data

- zajištění kvality dat,
- odstranění duplicit,
- sjednocení formátů,
- odstranění nevalidních hodnot,
- lepší výkon modelu,
- lepší interpretace dat.

---

# Nejčastější problémy v datech

## Duplicity
- zkreslují agregace a KPI.

## Null values
- chybějící data mohou rozbíjet výpočty.

## Nekonzistentní formáty
- různé datumy,
- různé zápisy textu.

## Nevalidní hodnoty
- záporné quantity,
- neplatné emaily,
- nesmyslné hodnoty.

## Mezery v textu
- problémy s groupingem a relationships.

---

# Kdy čistíme data

- při slučování více zdrojů,
- před reportingem,
- při migraci systémů,
- při automatizaci,
- při modelování a predikci.

---

# Power Query

Power Query slouží pro:
- ETL workflow,
- cleaning dat,
- transformace,
- automatizaci přípravy dat.

---

# Hlavní části Power Query

## Queries panel
- seznam tabulek/dotazů.

## Data preview
- náhled dat.

## Applied Steps
- historie transformací.

## Ribbon
- transformační nástroje.

---

# Applied Steps

Každý krok:
- se ukládá,
- lze upravit,
- lze odstranit,
- lze automaticky zopakovat.

To umožňuje:
- automatizaci,
- reprodukovatelnost,
- ETL pipeline.

---

# Jazyk M

- každý krok generuje M kód,
- umožňuje pokročilé transformace,
- zatím není nutné memorovat.

---

# Profesionální přístup

✔️ cleaning v Power Query  
❌ ruční úpravy v Excelu

---

# Performance mindset

Menší a čistší dataset:
- rychlejší refresh,
- nižší RAM usage,
- lepší výkon dashboardů.

---

# Typické chyby junior analytiků

- ignorování null values,
- chaos v Applied Steps,
- ruční cleaning,
- špatné datové typy,
- absence validace dat.

---

# Důležitý mindset

Analytik:
- nevěří datům automaticky,
- data validuje a kontroluje.

---

# Lekce 4 — Cheatsheet
## Základní úpravy a transformace dat v Power Query

---

# Hlavní princip

Power Query = ETL workflow builder

Každá transformace:
- je automatizovaná,
- reprodukovatelná,
- součást datové pipeline.

---

# Nejčastější transformace

- Merge Queries
- Rename Columns
- Filtering
- Change Data Types
- Remove Duplicates
- Sorting
- Group By

---

# Merge Queries

Slouží pro:
- spojení tabulek pomocí společného klíče.

Příklad:
- orders + customers
- products + categories

---

# Důležité pojmy

## Primary Key
Jedinečný identifikátor.

## Foreign Key
Odkaz na jinou tabulku.

---

# Left Outer Join

Nejčastější BI join.

Zachová:
- všechny záznamy z levé tabulky.

---

# Rename Columns

Cíl:
- lepší čitelnost,
- business-friendly názvy,
- přehlednější reporting.

---

# Filtering

Použití:
- odstranění null values,
- odstranění nevalidních dat,
- omezení datasetu,
- zvýšení výkonu.

---

# Data Types

Kriticky důležité pro:
- DAX,
- agregace,
- relationships,
- time intelligence.

---

# Typické datové typy

- text
- whole number
- decimal number
- date
- datetime
- boolean

---

# Remove Duplicates

Odstraňuje:
- duplicitní záznamy.

Pozor:
- ne každá duplicita je chyba.

---

# Sorting

Pomáhá:
- validaci dat,
- hledání outliers,
- přehlednosti dat.

---

# Group By

Slouží pro:
- agregace,
- sumarizace,
- KPI thinking.

Podobné:
- SQL GROUP BY.

---

# Applied Steps

Každá transformace:
- se ukládá,
- lze ji upravit,
- lze ji odstranit,
- automaticky se opakuje při refreshi.

---

# Duplikace query

Profesionální přístup:
- originální query zachovat,
- experimentovat na kopii.

---

# PBIX soubor

.pbix obsahuje:
- Power Query transformace,
- data model,
- relationships,
- DAX,
- dashboardy,
- vizualizace.

---

# Typické chyby junior analytiků

- špatné joins,
- ignorování datových typů,
- mazání validních duplicit,
- chaos v Applied Steps,
- absence validace merge výsledků.

---

# Performance mindset

Filtrovat a čistit data:
- co nejdříve,
- co nejblíže zdroji dat.

To zlepšuje:
- výkon,
- refresh,
- stabilitu modelu.

---

# Důležitý mindset

Power Query není:
- jen klikání.

Je to:
- ETL,
- workflow,
- datová pipeline,
- základ profesionální BI analytiky.

---

# Cheatsheet – Lekce 5: Prostředí Power BI a základní vizualizace

# Hlavní cíl lekce
Naučit se:
- orientovat v prostředí Power BI,
- vytvářet základní vizualizace,
- používat filtry a slicery,
- chápat business význam dashboardů.

---

# Hlavní části Power BI

## Report View
Hlavní pracovní plocha pro:
- dashboardy,
- grafy,
- KPI,
- reporty.

---

## Data View
Zobrazení:
- tabulek,
- sloupců,
- datových typů.

Používá se pro:
- kontrolu dat,
- validaci dat,
- práci s calculated columns.

---

## Model View
Zobrazuje:
- vztahy mezi tabulkami,
- relace,
- datový model.

Klíčové pro:
- star schema,
- relationship management,
- DAX.

---

# Pravý panel

## Vizualizace
Výběr:
- grafů,
- tabulek,
- slicerů,
- KPI cards.

---

## Data
Obsahuje:
- tabulky,
- sloupce,
- measures.

Pole se přetahují do vizualizací.

---

## Filtry
Filtry lze aplikovat:
- na vizuál,
- stránku,
- celý report.

---

# Nejčastější vizualizace

## KPI Card
Použití:
- hlavní KPI,
- rychlý přehled.

Příklady:
- Total Revenue,
- Orders Count,
- Profit,
- Customers.

---

## Sloupcový graf
Použití:
- porovnání kategorií.

Příklady:
- Revenue by Category,
- Revenue by Region,
- Orders by Status.

---

## Spojnicový graf
Použití:
- vývoj v čase,
- trendy.

Příklady:
- Revenue Over Time,
- Orders Over Time,
- Monthly Growth.

---

## Tabulka
Použití:
- detailní data,
- drill-down analýza.

---

# Filtry vs Slicery

## Filtr
Používá se:
- na pozadí reportu,
- pro omezení dat.

Může být:
- Visual level,
- Page level,
- Report level.

---

## Slicer
Interaktivní filtr přímo v dashboardu.

Použití:
- region,
- datum,
- kategorie,
- zákazník.

Výhoda:
- management si může report filtrovat sám.

---

# Typické chyby junior analytiků

## Příliš mnoho grafů
Výsledek:
- chaos,
- nepřehlednost,
- cognitive overload.

---

## Příliš mnoho barev
Barvy mají:
- zvýrazňovat,
- ne rušit.

---

## Špatný typ grafu
Příklad:
- trend v pie chartu,
- časová řada v koláčovém grafu.

---

## Dashboard bez business otázky
Dashboard musí odpovídat:
- na problém,
- na KPI,
- na business otázku.

---

# Business mindset

## Dashboard není jen hezký obrázek
Dashboard má:
- pomáhat rozhodování,
- ukazovat trendy,
- zvýraznit problémy,
- zjednodušit interpretaci dat.

---

## Špatná data = špatný dashboard
Ani nejlepší graf:
- neopraví nekvalitní data.

Proto:
```text
Data Quality > Vizualizace
```

---

# Doporučený workflow

```text
Import dat
→ Cleaning
→ Transformace
→ Datový model
→ KPI
→ Vizualizace
→ Storytelling
```

---

# Důležité koncepty

## KPI
Klíčový business ukazatel.

Příklady:
- revenue,
- profit,
- conversion rate,
- orders count.

---

## Storytelling
Vizualizace mají:
- vyprávět příběh,
- vysvětlovat business situaci,
- ukázat insight.

---

## Interaktivita
Power BI dashboard:
- není statický,
- uživatel s ním pracuje pomocí:
  - slicerů,
  - filtrů,
  - drill-downu.

---

# Hlavní learning outcomes

Po lekci:
- orientace v Power BI,
- tvorba základních vizualizací,
- práce s filtry,
- práce se slicery,
- pochopení dashboard mindsetu,
- základ business storytellingu.

---

# Cheatsheet – Lekce 6: Efektivní vizualizace a dashboard design

# Hlavní cíl lekce
Naučit se:
- vybírat správné vizualizace,
- navrhovat přehledné dashboardy,
- zlepšit čitelnost reportů,
- podporovat business rozhodování pomocí dat.

---

# Hlavní princip

```text
Dashboard není galerie grafů.
Dashboard je nástroj pro rozhodování.
```

---

# Výběr správného typu grafu

## Sloupcový graf (Bar/Column Chart)
Použití:
- porovnání kategorií,
- regionů,
- produktů,
- oddělení.

Příklady:
- Revenue by Region
- Orders by Category

---

## Pruhový graf
Použití:
- dlouhé názvy kategorií,
- větší počet položek.

Výhoda:
- lepší čitelnost textu.

---

## Spojnicový graf (Line Chart)
Použití:
- trendy,
- vývoj v čase,
- sezónnost.

Příklady:
- Revenue Over Time
- Orders Over Time

---

## Koláčový graf (Pie Chart)
Použití:
- podíly na celku,
- malé množství kategorií.

Nevhodné:
- příliš mnoho segmentů.

---

## Histogram
Použití:
- rozložení dat,
- četnosti.

Příklady:
- věk zákazníků,
- velikost objednávek.

---

## Scatter Plot (Bodový graf)
Použití:
- vztah mezi dvěma proměnnými.

Příklady:
- cena vs počet objednávek,
- marketing spend vs revenue.

---

## Treemap
Použití:
- hierarchická data,
- podíly v rámci kategorií.

Příklady:
- revenue podle kategorií a podkategorií.

---

# Nejčastější chyby

## 3D grafy
Nevýhody:
- zkreslení dat,
- horší čitelnost,
- nepřesné porovnávání.

---

## Příliš mnoho barev
Výsledek:
- chaos,
- horší orientace,
- cognitive overload.

Doporučení:
- používat jednotnou barevnou paletu.

---

## Příliš mnoho grafů
Dashboard:
- nesmí zahlcovat,
- musí mít jasnou hierarchii.

---

## Špatný typ grafu
Příklad:
- trend v pie chartu,
- časová osa v tabulce bez vizualizace.

---

# Minimalismus a čitelnost

## Less is More
Každý prvek:
- musí mít smysl,
- musí podporovat interpretaci dat.

---

## Whitespace
Prázdné místo:
- zvyšuje přehlednost,
- odděluje sekce,
- pomáhá fokusovat pozornost.

---

## Konzistentní design
Používat:
- stejné fonty,
- stejné barvy,
- stejné spacingy.

---

# Dashboard Layout

## Hierarchie informací

### Nahoře:
- hlavní KPI,
- nejdůležitější insighty.

### Uprostřed:
- trendy,
- hlavní grafy.

### Dole:
- detailní tabulky,
- doplňující analýza.

---

# Eye Flow

Lidé čtou:
```text
Zleva doprava
Shora dolů
```

Proto:
- nejdůležitější informace vlevo nahoře.

---

# KPI Cards

Použití:
- rychlý přehled hlavních metrik.

Příklady:
- Revenue
- Profit
- Orders
- Customers

---

# Filtry a slicery

## Filtry
Použití:
- omezení datasetu,
- page/report filtering.

---

## Slicery
Použití:
- interaktivní dashboard,
- self-service analytics.

Příklady:
- region,
- datum,
- produkt,
- zákazník.

---

# Drill-down

Umožňuje:
- přechod z agregace do detailu.

Příklad:
```text
Rok → Kvartál → Měsíc → Den
```

---

# Business storytelling

Dashboard má:
- odpovídat na otázky,
- zvýraznit problémy,
- ukázat trendy,
- podpořit rozhodování.

---

# Data-Ink Ratio

Každý vizuální prvek:
- musí mít význam.

Odstranit:
- zbytečné rámečky,
- přebytečné ikony,
- dekorace bez informační hodnoty.

---

# Profesionální dashboard

Typické vlastnosti:
- minimalistický,
- čistý,
- konzistentní,
- přehledný,
- business-oriented.

---

# Doporučený dashboard layout

```text
[KPI CARDS]
Revenue | Profit | Orders | Customers

----------------------------

[MAIN TREND]
Revenue Over Time

----------------------------

[COMPARISON]
Revenue by Region | Revenue by Category

----------------------------

[DETAIL TABLE]
Top Products | Order Details
```

---

# Hlavní learning outcomes

Po lekci:
- správný výběr grafů,
- dashboard UX mindset,
- business storytelling,
- minimalismus v reportingu,
- práce s hierarchií informací,
- pochopení dashboard design principů.

---


