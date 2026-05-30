# Notes

## Přehled projektu

Tato případová studie byla zaměřena na vytvoření kompletního Power BI řešení pro analýzu e-commerce dat.

Projekt pokrývá celý proces od načtení dat přes jejich transformaci až po tvorbu interaktivních dashboardů a business analýz.

---

## Co jsem se během projektu naučil

### Power Query

- Import dat z CSV souborů
- Kontrola datových typů
- Čištění textových hodnot
- Identifikace chybějících hodnot
- Kontrola kvality dat

### Datový model

- Návrh hvězdicového schématu (Star Schema)
- Tvorba relací mezi tabulkami
- Faktové a dimenzní tabulky
- Princip filtračního kontextu

### DAX

Během projektu jsem si procvičil:

- SUMX()
- RELATED()
- DISTINCTCOUNT()
- DIVIDE()
- CALCULATE()
- AVERAGE()

a jejich využití při tvorbě KPI metrik.

### Dashboarding

Vytvořil jsem:

- Sales & Marketing Dashboard
- Customer Insights Dashboard
- Region Detail Drill-through stránku

Použil jsem:

- KPI karty
- sloupcové grafy
- donut grafy
- slicery
- drill-through navigaci

---

## Vytvořené metriky

### Obchodní metriky

- Celkové tržby
- Počet objednávek
- Počet zákazníků
- Průměrná objednávka

### Marketingové metriky

- ROI kampaně
- Tržby podle kampaní

### Zákaznické metriky

- Průměrný věk zákazníků
- Průměrná útrata zákazníka
- Počet regionů

---

## Problémy během projektu

### Chybějící hodnota kampaně

Jedna marketingová kampaň neobsahovala název.

Možné řešení:

- doplnění hodnoty po konzultaci s business uživatelem
- označení jako datový problém

### Relace Customers → Orders

Model zobrazoval relaci 1:1.

Po kontrole dat se ukázalo, že ukázkový dataset obsahoval pouze jednu objednávku na zákazníka.

V reálném prostředí by relace byla 1:N.

### DAX syntaxe

Při vytváření metrik vznikaly chyby způsobené:

- nesprávným oddělovačem argumentů
- přebytečnými závorkami

Řešení:

- kontrola syntaxe
- postupné testování výrazů

### Power BI UI

Při tvorbě projektu se ukázalo, že některé návody již neodpovídají nejnovější verzi Power BI Desktop.

Největší komplikace způsobilo:

- nové rozhraní vizualizací
- změny v nastavení tooltipů
- změny v nastavení karet (Cards)

---

## Co bych vylepšil

Pokud bych projekt dále rozšiřoval:

### Power BI

- Custom Tooltip Pages
- Bookmarks
- Navigační tlačítka
- Podmíněné formátování KPI

### DAX

- Time Intelligence
- Meziroční srovnání
- Running Total
- Podíl tržeb podle regionů

### Business analýza

- Segmentace zákazníků
- RFM analýza
- Customer Lifetime Value
- Analýza retence zákazníků

---

## Celkové zhodnocení

Tento projekt představuje první kompletní end-to-end Power BI case study.

Pokryté oblasti:

- Data Cleaning
- Power Query
- Data Modeling
- DAX
- Dashboard Design
- Business Analysis
- Drill-through Reporting
- GitHub dokumentace

Projekt byl vytvořen samostatně jako součást přípravy na junior pozici Data Analyst / BI Analyst.
