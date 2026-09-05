# 📊 Power BI & Business Intelligence Portfolio

Portfolio projektů zaměřených na **Power BI, Power Query, DAX, datové modelování a Business Intelligence reporting**.

Repozitář obsahuje praktické Power BI case studies od datové přípravy a modelování až po návrh interaktivních management dashboardů.

Hlavní oblasti:

- Power Query a ETL,
- data quality a transformace,
- datové modelování,
- Star Schema,
- DAX measures,
- KPI reporting,
- dashboard design,
- interaktivní reporting,
- drill-through a slicery,
- business-oriented data visualization.

---

## 📂 Struktura repozitáře

```text
power-bi-portfolio/
│
├── pbi-case-studies/
│   ├── case-study-1/
│   ├── case-study-2/
│   ├── case-study-3/
│   └── case-study-4/
│
├── pbi-cheatsheets/
│   ├── pbi-cheatsheet.md
│
├── pbi-mini-tests/
│   └── pbi-cheatsheet-mini-tests.md
│
├── pbi-notes.md
├── pbi-certificate.pdf
└── README.md
```

---

## 🎯 Zaměření portfolia

Repozitář demonstruje práci s Power BI v rámci celého BI workflow:

```text
Data Sources
→ Power Query
→ Data Cleaning & Transformation
→ Data Model
→ DAX
→ KPI
→ Visualization
→ Interactive Reporting
→ Business Interpretation
```

Jednotlivé case studies se zaměřují na různé části tohoto procesu — od datové přípravy přes modelování až po komplexnější management reporting.

---

# 📁 Case Studies

Case studies jsou níže seřazeny **od nejpokročilejšího a nejreprezentativnějšího projektu po jednodušší projekty**.

Důvodem je portfolio-oriented prezentace, kdy je na prvním místě projekt, který nejlépe reprezentuje moji aktuální úroveň zkušeností a práce s Power BI, datovým modelem, DAX, interaktivitou a management reportingem. Číslování projektů zůstává zachováno, takže je stále patrný jejich vývoj v čase.

---

## Case Study 04 — Acquisition Performance Dashboard

Management Power BI report zaměřený na sledování výkonu akvizice nových smluv vůči plánovaným cílům.

Projekt navazuje na samostatně připravenou SQL/Python datovou vrstvu a v Power BI se soustředí především na:

- Power Query ingestion,
- datový model se sdílenými dimenzemi,
- DAX KPI,
- Actual vs. Target analýzu,
- management dashboard design,
- conditional formatting,
- synchronizované slicery,
- drill-through,
- detailní performance analysis.

Report obsahuje dvě hlavní stránky:

```text
Executive Overview
Performance Drivers
```

Hlavní KPI:

- počet smluv,
- plán smluv,
- plnění plánu,
- odchylka od plánu,
- aktivní smlouvy,
- podíl stornovaných smluv.

➡️ [Otevřít Case Study 04](pbi-case-studies/case-study-4/)

---

## Case Study 03 — Czech E-commerce Analytics Dashboard

Komplexní Power BI projekt zaměřený na obchodní, marketingovou a zákaznickou analytiku českého e-commerce prostředí.

Report obsahuje:

- **Sales & Marketing Dashboard**,
- **Customer Insights Dashboard**,
- **Region Detail drill-through**,
- KPI cards,
- DAX measures,
- Star Schema,
- interaktivní slicery,
- regionální analýzu,
- marketingovou analýzu,
- zákaznickou analýzu.

Projekt propojuje datové modelování, DAX a vizualizaci do vícestránkového analytického reportu.

➡️ [Otevřít Case Study 03](pbi-case-studies/case-study-3/)

---

## Case Study 02 — TechStore Sales Dashboard

Power BI dashboard zaměřený na analýzu prodejních dat fiktivního obchodu TechStore.

Hlavní témata:

- základní datový model,
- DAX measures,
- KPI reporting,
- slicery a filtry,
- interaktivní vizualizace,
- sales dashboard design.

➡️ [Otevřít Case Study 02](pbi-case-studies/case-study-2/)

---

## Case Study 01 — Data Cleaning & ETL with Power Query

Projekt zaměřený především na přípravu dat pomocí Power Query.

Hlavní témata:

- import dat,
- data quality checks,
- datové typy,
- missing values,
- duplicity,
- textové transformace,
- filtrování,
- Merge Queries,
- přípravu dat pro analytický model.

➡️ [Otevřít Case Study 01](pbi-case-studies/case-study-1/)

---

# 🧩 Power BI Skills

## Power Query & Data Preparation

Prakticky pokryté oblasti:

- import z různých datových zdrojů,
- CSV, Excel a JSON,
- kontrola datových typů,
- missing values,
- duplicity,
- text cleaning,
- filtrování,
- třídění,
- Group By,
- Merge Queries,
- join logika,
- Applied Steps,
- reprodukovatelné transformační workflow.

Důraz je kladen na princip:

```text
clean and validate data
before building the report
```

---

## Data Modeling

Portfolio zahrnuje práci s:

- faktovými a dimenzními tabulkami,
- primary a foreign keys,
- relationships,
- kardinalitou `1:*`,
- Star Schema,
- sdílenými dimenzemi,
- filter contextem,
- návrhem modelu pro analytický reporting.

Cílem není pouze vizualizace dat, ale vytvoření modelu, nad kterým lze spolehlivě stavět DAX a reporting.

---

## DAX

Použité koncepty a funkce zahrnují například:

```DAX
SUM()
AVERAGE()
COUNT()
COUNTROWS()
DISTINCTCOUNT()
DIVIDE()
IF()
CALCULATE()
FILTER()
```

Dále:

- measures,
- calculated columns,
- row context,
- filter context,
- dynamické KPI,
- agregace,
- business logiku,
- Actual vs. Target výpočty.

Důležitou součástí práce s DAX je rozlišení mezi:

```text
Power Query
→ příprava dat

DAX
→ dynamická analytická logika
```

---

## KPI & Business Reporting

Portfolio obsahuje práci s KPI, jako jsou například:

- Revenue,
- Orders,
- Customers,
- Average Order Value,
- ROI,
- Actual vs. Target,
- Target Attainment,
- Variance,
- Active Contracts,
- Cancellation Rate.

KPI nejsou používána izolovaně, ale jako součást konkrétní business otázky a rozhodovacího kontextu.

---

## Dashboard Design & Data Visualization

Při návrhu reportů je kladen důraz na:

- jasnou informační hierarchii,
- omezený počet vizualizací,
- konzistentní layout,
- vhodnou volbu typu grafu,
- whitespace,
- čitelnost,
- management-oriented reporting,
- minimalizaci vizuálního šumu.

Použité vizualizace zahrnují například:

- KPI Cards,
- Column / Bar Charts,
- Line Charts,
- Combo Charts,
- Matrix,
- Tables,
- Scatter Plot,
- Treemap.

Základní princip:

```text
Dashboard není galerie grafů.

Dashboard je nástroj pro rozhodování.
```

---

## Interaktivní reporting

V projektech jsou využívány například:

- slicery,
- visual / page / report filters,
- synchronizované slicery,
- drill-down,
- drill-through,
- interaktivní filtrování,
- conditional formatting.

Tyto funkce umožňují přechod od statického reportu k self-service analytickému prostředí.

---

## AI & Predictive Analytics Concepts

Součástí pokrytých témat jsou také vybrané AI-assisted funkce Power BI:

- Q&A,
- Automated Insights,
- forecasting,
- confidence intervals,
- AI-assisted analytics,
- základní principy prediktivní analytiky,
- možnosti integrace Pythonu a R.

Důraz je kladen také na limity těchto funkcí:

```text
AI output
≠
automaticky validní business insight
```

Výsledky je nutné posuzovat v kontextu kvality dat, datového modelu a business problému.

---

# 📚 Knowledge Base

## pbi-cheatsheets

Vlastní strukturovaná reference pro Power BI a Business Intelligence.

Obsahuje témata například z oblastí:

- datová analytika,
- ETL,
- Power Query,
- data cleaning,
- transformace,
- datové modelování,
- vizualizace,
- dashboard design,
- DAX,
- filter context,
- AI funkce a forecasting,
- BI best practices.

➡️ [Power BI Cheatsheets](pbi-cheatsheets/)

---

## pbi-mini-tests

Sada znalostních testů zaměřených na Power BI, DAX, Power Query a související BI principy.

Obsahuje:

- otázky založené na Power BI cheatsheetu,
- samostatné certification-oriented mini-tests.

➡️ [Power BI Mini Tests](pbi-mini-tests/)

---

## pbi-notes.md

Pracovní znalostní báze obsahující poznámky, praktické principy a reference k Power BI.

➡️ [Power BI Notes](pbi-notes.md)

---

## 📜 Certificate

Repozitář obsahuje také certifikát související s absolvovaným Power BI kurzem.

➡️ [Power BI Certificate](pbi-certificate.pdf)

---

# 🛠 Technologie a koncepty

```text
Microsoft Power BI
Power Query
DAX
Data Modeling
Star Schema
ETL
Data Quality
KPI Reporting
Business Intelligence
Data Visualization
Interactive Reporting
Git
GitHub
```

V navazujících projektech je Power BI kombinováno také s dalšími analytickými technologiemi, zejména:

```text
SQL
Python
pandas
SQLite
JSON
```

Každý nástroj je používán podle role, pro kterou je v analytickém workflow nejvhodnější.

---

# 💡 BI přístup

Portfolio vychází z principu:

```text
Business Question
→ Relevant Data
→ Data Quality
→ Data Model
→ Metrics
→ Visualization
→ Interpretation
→ Decision Support
```

Cílem není pouze vytvořit technicky funkční `.pbix` soubor.

Report má:

- odpovídat na konkrétní business otázky,
- používat správně definované metriky,
- umožnit uživateli pracovat s kontextem dat,
- zvýraznit důležité trendy a problémy,
- podpořit rozhodování.

---

# 📈 Další rozvoj

Repozitář je rozšiřován o další praktické BI projekty a pokročilejší analytická témata.

Mezi navazující oblasti patří například:

- pokročilejší DAX,
- Time Intelligence,
- Power BI Service,
- scheduled refresh,
- Row-Level Security,
- tooltip pages,
- bookmarks,
- datové pipeline,
- SQL / Python → Power BI integrace,
- automatizace reportingu.