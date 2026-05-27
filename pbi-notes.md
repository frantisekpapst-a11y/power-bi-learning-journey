# Lekce 1 — Notes

---

# Hlavní poznatky

- Datová analytika není jen o grafech.
- Nejdůležitější je pochopit business problém.
- Dashboard je nástroj pro rozhodování.
- Kvalita dat je důležitější než vizualizace.

---

# Rozdíl mezi Power Query a Power BI

## Power Query
- příprava dat,
- cleaning,
- transformace,
- ETL proces.

## Power BI
- dashboardy,
- reporting,
- KPI,
- business interpretace.

---

# ETL mindset

ETL:
1. Extract
2. Transform
3. Load

Transformace dat bývá nejdůležitější část analytické práce.

---

# Business otázky

Dashboard by měl odpovídat například na:
- Které produkty vydělávají nejvíce?
- Který region má nejlepší výkon?
- Která věková skupina nejvíce nakupuje?
- Jaké platební metody dominují?
- Kde firma ztrácí výkon?

---

# KPI thinking

Důležitá KPI:
- tržby,
- zisk,
- počet objednávek,
- spokojenost zákazníků,
- průměrná hodnota objednávky.

---

# Důležité uvědomění

Skvělý analytik:
- nepřemýšlí v grafech,
- přemýšlí v rozhodnutích.

---

# Lekce 2 — Notes

---

# Hlavní poznatky

- Import dat je základ BI workflow.
- Kvalita dat ovlivňuje celý reporting.
- SQL databáze jsou profesionální datový zdroj.
- CSV vyžaduje správné nastavení delimiteru.
- Power Query Editor je klíčový pro ETL proces.

---

# Rozdíly mezi zdroji dat

## Excel
- jednoduchý,
- vhodný pro menší data,
- náchylný k chybám.

## CSV
- lehký formát,
- často používaný pro exporty,
- důležitý delimiter.

## SQL
- nejvýkonnější řešení,
- vhodné pro enterprise BI.

---

# Důležitý mindset

Nejdřív:
- validace dat,
- kontrola struktury,
- cleaning.

Teprve potom:
- dashboard,
- KPI,
- vizualizace.

---

# Power Query workflow

Transformovat data:
- otevře Power Query,
- umožní cleaning,
- umožní ETL proces.

---

# Typické problémy

- špatný delimiter,
- datum jako text,
- duplicitní data,
- neaktuální cache,
- příliš velký dataset.

---

# Profesionální BI přístup

Filtrovat data:
- už při SQL importu,
- ne až v dashboardu.

To zlepšuje:
- výkon,
- refresh,
- efektivitu modelu.

---

# Lekce 3 — Notes

---

# Hlavní myšlenka lekce

Garbage In = Garbage Out

Pokud jsou špatná vstupní data:
- budou špatné KPI,
- budou špatné dashboardy,
- budou špatná business rozhodnutí.

Cleaning dat je jedna z nejdůležitějších částí datové analytiky.

---

# Co je cleaning dat

Cleaning dat znamená:
- validaci dat,
- kontrolu kvality,
- standardizaci,
- odstranění chyb a nekonzistencí.

Nejde jen o kosmetické úpravy.

---

# Nejčastější problémy v datech

## Duplicity
- stejné objednávky vícekrát,
- zkreslené revenue,
- špatné agregace.

---

## Null values
- chybějící věk,
- region,
- revenue,
- customer ID.

Mohou rozbíjet:
- KPI,
- DAX,
- relationships,
- vizualizace.

---

## Nekonzistentní formáty
Například:
- datum jako text,
- různé formáty datumů,
- různý zápis regionů.

---

## Nevalidní hodnoty
Například:
- záporné quantity,
- neplatné emaily,
- věk 300 let.

---

## Mezery a špatný text
Například:
- "Praha"
- " Praha "
- "praha"

To může rozbít:
- grouping,
- relationships,
- agregace.

---

# Power Query Editor

Power Query není jen importní nástroj.

Je to:
- ETL prostředí,
- transformační engine,
- workflow systém pro přípravu dat.

---

# Hlavní části Power Query

## Queries panel
- seznam tabulek/dotazů.

## Data preview
- náhled aktuálního stavu dat.

## Applied Steps
- historie transformací,
- automatizace workflow,
- reprodukovatelnost.

## Ribbon
- transformační nástroje.

---

# Applied Steps mindset

Každý krok:
- se ukládá,
- lze upravit,
- lze odstranit,
- lze automaticky zopakovat.

To je základ:
- ETL pipeline,
- automatizace,
- profesionální BI práce.

---

# Jazyk M

Každý klik v Power Query:
- generuje M kód.

M language:
- umožňuje pokročilé transformace,
- poskytuje větší kontrolu,
- není zatím nutné memorovat.

Důležité je:
- chápat logiku transformací.

---

# Profesionální přístup

Nečistit data:
- ručně v Excelu.

Ale:
- automatizovaně,
- reprodukovatelně,
- v Power Query.

---

# Performance mindset

Čistší dataset:
- rychlejší refresh,
- menší RAM usage,
- lepší výkon modelu,
- rychlejší dashboardy.

---

# Důležitý mindset analytika

Data nejsou automaticky pravda.

Analytik musí:
- data validovat,
- kontrolovat,
- zpochybňovat,
- hledat nekonzistence.

---

# Typické chyby junior analytiků

- ruční cleaning v Excelu,
- ignorování null values,
- ignorování datových typů,
- chaos v Applied Steps,
- přepisování source dat,
- absence validace.

---

# Real-world BI mindset

Skvělý analytik:
- nepřemýšlí v grafech,
- přemýšlí v kvalitě dat a business rozhodnutích.

---

# Lekce 4 — Notes

---

# Hlavní myšlenka lekce

Power Query není jen nástroj na klikání.

Je to:
- ETL workflow,
- transformační engine,
- základ datové pipeline v Power BI.

---

# Transformace dat

Cíl transformací:
- připravit data pro reporting,
- zvýšit kvalitu dat,
- sjednotit strukturu,
- zlepšit výkon modelu.

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

Spojování tabulek pomocí:
- společného klíče.

Příklad:
- orders + customers
- products + categories

---

# SQL mindset v Power Query

Merge Queries fungují podobně jako:
- SQL JOIN.

Důležité:
- validní klíče,
- správná cardinality,
- kontrola duplicit.

---

# Left Outer Join

Nejčastější BI join.

Použití:
- zachovat všechny záznamy hlavní tabulky,
- doplnit data z druhé tabulky.

---

# Rizika Merge operací

- duplicity klíčů,
- null klíče,
- many-to-many relationships,
- nafouknuté tabulky,
- zkreslené KPI.

---

# Rename Columns

Důležité pro:
- business uživatele,
- čitelnost dashboardu,
- konzistentní naming.

---

# Profesionální naming

✔️ Celková částka  
✔️ Revenue  
✔️ Order Date

❌ col_1  
❌ temp_final_new2

---

# Filtering

Použití:
- odstranění null values,
- odstranění testovacích dat,
- omezení datasetu,
- zvýšení výkonu.

---

# Performance mindset

Filtrovat data:
- co nejdříve,
- co nejblíže zdroji dat.

---

# Data Types

Extrémně důležitá část BI workflow.

Power BI musí správně chápat:
- čísla,
- datumy,
- text,
- boolean hodnoty.

---

# Typické problémy datových typů

- revenue jako text,
- datum jako string,
- čísla s nesprávným locale formátem.

---

# Remove Duplicates

Důležité:
- ne každá duplicita je chyba.

Analytik musí chápat:
- business logiku dat.

---

# Sorting

Pomáhá:
- validaci dat,
- hledání outliers,
- kontrole kvality dat.

---

# Group By

Slouží pro:
- agregace,
- sumarizace,
- první business insights.

Podobné:
- SQL GROUP BY.

---

# Applied Steps

Každá transformace:
- se ukládá,
- lze ji upravit,
- lze ji odstranit,
- automaticky se opakuje při refreshi.

To umožňuje:
- automatizaci,
- reprodukovatelnost,
- ETL pipeline.

---

# Duplikace query

Profesionální workflow:
- originální query zachovat,
- experimentovat na kopii.

---

# PBIX soubor

.pbix obsahuje:
- data model,
- Power Query transformace,
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

# Real-world BI mindset

Analytik:
- nepřemýšlí jen o dashboardu,
- ale o kvalitě celé datové pipeline.

---

# Notes – Lekce 6: Efektivní vizualizace a dashboard design

# Hlavní myšlenka lekce

Dashboard není jen sada grafů.

Je to:
- nástroj pro rozhodování,
- komunikační vrstva mezi daty a businessem,
- způsob, jak rychle předat důležité informace.

---

# Co je cílem dobrého dashboardu

Dobrý dashboard:
- rychle komunikuje insight,
- je přehledný,
- vede pozornost uživatele,
- pomáhá rozhodování,
- minimalizuje chaos.

---

# Každý graf musí odpovídat na otázku

Před vytvořením vizualizace je důležité vědět:

```text
Co chci tímto grafem ukázat?
```

Příklady:
- Který region generuje nejvyšší revenue?
- Jak se vyvíjí tržby v čase?
- Jaký podíl mají jednotlivé kategorie?
- Existuje vztah mezi cenou a počtem objednávek?

---

# Výběr správného grafu

## Bar/Column Chart
Použití:
- porovnání kategorií,
- regionů,
- produktů,
- oddělení.

---

## Line Chart
Použití:
- trendy,
- časové řady,
- vývoj v čase.

---

## Pie Chart
Použití:
- podíly na celku,
- malé množství kategorií.

Nevhodné:
- velké množství segmentů.

---

## Scatter Plot
Použití:
- vztahy mezi proměnnými.

---

## Treemap
Použití:
- hierarchická data,
- podíly kategorií.

---

# Nejčastější chyby

## 3D grafy
Problémy:
- zkreslení dat,
- horší čitelnost,
- složitější interpretace.

---

## Příliš mnoho barev
Výsledek:
- chaos,
- přetížení uživatele,
- horší orientace.

---

## Dashboard overload
Příliš:
- grafů,
- KPI,
- tabulek,
- informací.

Výsledek:
- dashboard je nepřehledný,
- uživatel neví, kam se dívat.

---

## Špatný typ grafu
Příklad:
- trend v pie chartu,
- časová řada v tabulce bez vizualizace.

---

# Minimalismus

Princip:
```text
Less is More
```

Dashboard:
- nemá být dekorace,
- každý prvek musí mít význam.

---

# Whitespace

Prázdné místo:
- odděluje sekce,
- zvyšuje čitelnost,
- pomáhá fokusovat pozornost.

Whitespace:
≠ ztracené místo.

---

# Eye Flow

Lidé čtou:
- zleva doprava,
- shora dolů.

Proto:
- nejdůležitější KPI nahoře vlevo,
- trendy uprostřed,
- detailní data dole.

---

# Hierarchie informací

## Nahoře
- hlavní KPI,
- nejdůležitější metriky.

---

## Uprostřed
- trendy,
- hlavní grafy.

---

## Dole
- detailní tabulky,
- doplňující analýza.

---

# KPI Cards

Použití:
- rychlý přehled hlavních metrik.

Příklady:
- Revenue,
- Profit,
- Orders,
- Customers.

---

# Filtry a slicery

## Filtry
Použití:
- omezení datasetu,
- filtrování reportu.

---

## Slicery
Použití:
- interaktivní dashboard,
- self-service analytics.

Výhoda:
- management si může report filtrovat sám.

---

# Drill-down

Umožňuje:
- přechod z agregovaných dat do detailu.

Příklad:
```text
Rok → Kvartál → Měsíc → Den
```

---

# Business storytelling

Dashboard:
- má vyprávět příběh,
- ukázat problém,
- zvýraznit trend,
- podpořit rozhodnutí.

---

# Data-Ink Ratio

Každý vizuální prvek:
- musí mít význam.

Odstranit:
- zbytečné dekorace,
- přebytečné rámečky,
- rušivé efekty.

---

# Profesionální dashboard

Typické vlastnosti:
- minimalistický,
- čistý,
- konzistentní,
- business-oriented,
- snadno čitelný.

---

# Důležitý mindset

```text
Dobrý dashboard ukazuje důležité.
Ne všechno.
```

---

# Hlavní learning outcomes

Po lekci:
- správný výběr grafů,
- dashboard UX mindset,
- business storytelling,
- práce s hierarchií informací,
- minimalismus v reportingu,
- pochopení dashboard design principů.

---

# Notes – Lekce 7: Základy jazyka DAX v Power BI

# Hlavní myšlenka lekce

DAX:
- není jen „vzorce v Power BI“,
- ale analytický jazyk pro práci s datovým modelem.

DAX umožňuje:
- vytvářet KPI,
- business logiku,
- dynamické výpočty,
- analytické metriky.

---

# Co je DAX

DAX = Data Analysis Expressions

Použití:
- Power BI,
- Power Pivot,
- SSAS Tabular.

---

# Hlavní využití DAX

## Measures
Dynamické výpočty:
- reagující na slicery,
- filtry,
- vizualizace,
- kontext reportu.

---

## Calculated Columns
Výpočty:
- po jednotlivých řádcích,
- uložené v modelu,
- statické.

---

# Measure vs Calculated Column

## Measure
- dynamická,
- počítá se při zobrazení,
- reaguje na filter context,
- neukládá se fyzicky do modelu.

Příklad:
```DAX
Total Revenue = SUM(orders[revenue])
```

---

## Calculated Column
- statická,
- počítá se při refreshi,
- ukládá se do modelu,
- funguje po řádcích.

Příklad:
```DAX
price_with_vat = products[price] * 1.21
```

---

# Nejdůležitější DAX funkce

# SUM()
Součet hodnot.

```DAX
Total Revenue = SUM(orders[revenue])
```

---

# COUNT()
Počet neprázdných hodnot ve sloupci.

```DAX
COUNT(orders[order_id])
```

Podobné:
```sql
COUNT(column)
```

---

# COUNTROWS()
Počet řádků tabulky.

```DAX
COUNTROWS(orders)
```

Podobné:
```sql
COUNT(*)
```

---

# AVERAGE()
Průměr hodnot.

```DAX
Average Revenue = AVERAGE(orders[revenue])
```

---

# IF()
Podmínka.

```DAX
IF(
    SUM(orders[revenue]) > 2500,
    "Yes",
    "No"
)
```

---

# CALCULATE()

Nejdůležitější funkce DAX.

Použití:
- změna filter contextu,
- aplikace podmínek,
- business logika.

Příklad:
```DAX
CZ Revenue =
CALCULATE(
    SUM(orders[revenue]),
    regions[country] = "Czech Republic"
)
```

---

# FILTER()

Použití:
- vytvoření podmnožiny dat,
- složitější filtrace.

Příklad:
```DAX
Big Orders =
CALCULATE(
    COUNTROWS(orders),
    FILTER(orders, orders[revenue] > 2500)
)
```

---

# Kontext v DAX

# Row Context

Výpočet:
- řádek po řádku.

Použití:
- calculated columns.

Příklad:
```DAX
discount_price =
orders[price] * (1 - orders[discount])
```

---

# Filter Context

Kontext vytvořený:
- slicery,
- filtry,
- vizualizacemi,
- výběrem uživatele.

Measures:
- reagují na filter context.

Příklad:
- jiný revenue pro Prahu,
- jiný revenue pro Brno.

---

# Důležitý mindset

## Excel mindset
```text
Buňka → vzorec → výsledek
```

---

## DAX mindset
```text
Context → calculation → dynamic result
```

---

# Power Query vs DAX

## Power Query
Použití:
- ETL,
- cleaning,
- transformace,
- příprava dat.

---

## DAX
Použití:
- KPI,
- analytika,
- business logika,
- agregace.

---

# Nejčastější chyby juniorů

## Používání calculated columns místo measures
Výsledek:
- větší model,
- horší performance,
- pomalejší refresh.

---

## Nechápání filter contextu
Výsledek:
- špatné KPI,
- nesprávné výpočty,
- zmatené výsledky.

---

## Dělání všeho v Power Query
Některé výpočty:
- mají být v DAX,
- ne v ETL vrstvě.

---

# Důležité principy

## Measures jsou základ BI reportingu
Protože:
- jsou dynamické,
- reagují na kontext,
- podporují interaktivní dashboardy.

---

## CALCULATE() je srdce DAXu
Většina pokročilého DAX:
- stojí na CALCULATE().

---

## Filter Context určuje výsledek measure
Stejná measure:
- může vracet různé výsledky,
- podle filtrů a slicerů.

---

# Typické KPI v DAX

## Total Revenue
```DAX
Total Revenue = SUM(orders[revenue])
```

---

## Orders Count
```DAX
Orders Count = COUNTROWS(orders)
```

---

## Average Order Value
```DAX
Average Revenue = AVERAGE(orders[revenue])
```

---

## High Value Orders
```DAX
High Value Orders =
CALCULATE(
    COUNTROWS(orders),
    FILTER(orders, orders[revenue] > 2500)
)
```

---

# Hlavní learning outcomes

Po lekci:
- pochopení DAX mindsetu,
- rozdíl mezi measures a calculated columns,
- práce s SUM, COUNT, AVERAGE,
- pochopení CALCULATE a FILTER,
- pochopení row context a filter context,
- základ pro pokročilý DAX a KPI reporting.

---

# Notes – Lekce 8: AI funkce a prediktivní analýzy v Power BI

# Hlavní myšlenka lekce

AI v Power BI:
- neslouží jako náhrada analytika,
- ale jako nástroj pro:
  - rychlejší analýzu,
  - hledání vzorů,
  - generování insightů,
  - predikci trendů.

---

# Co znamená AI v Power BI

AI funkce umožňují:
- analyzovat data automaticky,
- hledat souvislosti,
- vytvářet forecasty,
- pracovat s přirozeným jazykem,
- generovat doporučení.

---

# K čemu se AI používá

## Automatická analýza dat
AI hledá:
- trendy,
- odchylky,
- vztahy mezi daty,
- změny výkonu.

---

## Predikce budoucího vývoje
Například:
- budoucí revenue,
- forecast objednávek,
- vývoj zákazníků.

---

## Q&A nad daty
Uživatel:
- píše otázky běžným jazykem,
- Power BI generuje:
  - grafy,
  - tabulky,
  - přehledy.

---

# Důležitý princip

## Garbage In = Garbage Out

Špatná data:
- znamenají špatné AI výstupy.

AI:
- neumí opravit nekvalitní model,
- neumí pochopit business kontext,
- neumí validovat KPI.

Proto:
- quality data fundamentals jsou klíčové.

---

# Vestavěné AI funkce v Power BI

# Q&A vizualizace

Umožňuje:
- pokládat otázky přirozeným jazykem.

Například:
```text
Show revenue by region
```

Power BI:
- automaticky vytvoří vizualizaci.

---

# Výhody Q&A

- rychlá explorace dat,
- self-service BI,
- vhodné pro management,
- není nutné manuálně tvořit grafy.

---

# Nevýhody Q&A

Funguje dobře pouze pokud:
- model je čistý,
- relationships fungují,
- názvy tabulek dávají smysl,
- KPI jsou správně definované.

---

# Automated Insights

Power BI:
- automaticky analyzuje změny v datech,
- hledá důvody růstu nebo poklesu.

Například:
```text
Proč vzrostly tržby v září?
```

AI:
- navrhne možné vysvětlení.

---

# Forecasting (Prognóza)

Forecast:
- odhad budoucího vývoje,
- založený na historických datech.

Používá:
- trend,
- časové řady,
- statistické modely.

---

# Forecast není magie

Forecast může být nepřesný pokud:
- je málo dat,
- data obsahují outliery,
- trend není stabilní,
- data jsou noisy,
- chybí sezónnost.

---

# Interval spolehlivosti

Forecast obsahuje:
```text
confidence interval
```

Tedy:
- pravděpodobné rozmezí budoucích hodnot.

---

# Horizontální forecast

Pokud:
- Power BI nenajde trend,

forecast:
- může být pouze vodorovná čára.

To znamená:
- systém neidentifikoval jasný vývoj.

---

# AI v Power Query

Pokročilé AI funkce:
- sentiment analysis,
- kategorizace textů,
- keyword extraction.

Použití:
- recenze,
- e-maily,
- zákaznická komunikace,
- dotazníky.

---

# Azure Cognitive Services

Tyto AI funkce:
- využívají Azure AI služby,
- často vyžadují Power BI Premium.

---

# Python a R v Power BI

Pokročilejší AI scénáře:
- lze řešit přes:
  - Python,
  - R.

Použití:
- machine learning,
- pokročilé statistiky,
- custom vizualizace,
- vlastní modely.

---

# BI vs AI analytika

## Klasická BI analytika
Odpovídá:
```text
Co se stalo?
```

---

## Prediktivní analytika
Odpovídá:
```text
Co by se mohlo stát?
```

---

## Prescriptive analytics
Odpovídá:
```text
Co bychom měli udělat?
```

---

# Role analytika

AI:
- nenahrazuje analytika.

Analytik:
- chápe business,
- validuje výsledky,
- interpretuje data,
- kontroluje kvalitu,
- rozhoduje.

AI:
- pouze asistuje.

---

# Praktické využití AI v BI

## Sales forecasting
Predikce:
- tržeb,
- objednávek,
- sezónnosti.

---

## Customer analytics
Analýza:
- zákaznického chování,
- churnu,
- segmentace.

---

## Marketing analytics
AI může:
- hledat nejvýkonnější kampaně,
- odhalovat trendy,
- analyzovat engagement.

---

# Důležité principy

## AI potřebuje kvalitní data
Bez kvalitního:
- ETL,
- modelu,
- KPI,
- relationships,

budou výsledky špatné.

---

## AI urychluje analytiku
Ale:
- nenahrazuje business thinking.

---

## Forecast je odhad
Ne:
- jistota,
- ani „věštění budoucnosti“.

---

# Nejčastější chyby juniorů

## Slepá důvěra AI
AI:
- může interpretovat data špatně.

---

## Špatné názvy tabulek a sloupců
Q&A:
- pak nerozumí modelu.

---

## Použití forecastu na nekvalitní data
Výsledkem:
- nesmyslná predikce.

---

# Hlavní learning outcomes

Po lekci:
- pochopení AI funkcí v Power BI,
- práce s Q&A,
- pochopení forecastingu,
- understanding AI limitations,
- pochopení rozdílu BI vs prediktivní analytika,
- základ AI-assisted analytics.
