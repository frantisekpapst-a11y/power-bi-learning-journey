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

