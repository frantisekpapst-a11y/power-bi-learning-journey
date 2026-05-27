# Power BI Case Study 1 – Data Cleaning and ETL in Power Query

## Přehled projektu
Tato case study je zaměřena na praktický ETL workflow a čištění dat v Power BI pomocí Power Query.

Hlavní cíle:
- import raw dat z více zdrojů,
- čištění a validace dat,
- práce s duplicitami a chybějícími hodnotami,
- standardizace formátů,
- tvorba validačních flagů,
- slučování datasetů,
- vytvoření čistého analytického datasetu.

Projekt simuluje realistickou práci junior BI analytika.

---

# Struktura projektu

```text
power-bi-case-study-1/
│
├── data/
│   ├── raw/
│   │   ├── customers.json
│   │   ├── orders.csv
│   │   └── products.csv
│   │
│   └── clean/
│       ├── customers_clean.png
│       ├── orders_clean.png
│       ├── products_clean.png
│       └── merged_dataset.png
│
├── notes/
│   ├── cleaning-process.md
│   ├── business-issues.md
│   └── lessons-learned.md
│
├── screenshots/
│   ├── power-query-editor.png
│   ├── merge-customers.png
│   ├── merge-products.png
│   └── duplicate-problem.png
│
├── pbix/
│   └── case-study-1.pbix
│
└── README.md
```

---

# Použité technologie

- Power BI Desktop
- Power Query
- JSON
- CSV
- ETL workflow
- Data validation
- Data cleaning
- Relační datové modelování

---

# Úkoly čištění dat

## Customers
- trim a clean textu,
- validace emailů,
- detekce chybějících regionů,
- odstranění duplicitních zákazníků.

## Orders
- detekce duplicitních objednávek,
- flagování suspicious revenue,
- validace záporného quantity,
- validace neplatných statusů,
- práce s null hodnotami.

## Products
- standardizace kategorií,
- validace chybějících kategorií,
- analýza duplicit produktů.

---

# Hlavní learning outcomes

- pochopení ETL workflow,
- tvorba čistých datasetů,
- aplikace business logiky při čištění dat,
- práce s many-to-many problémy při merge,
- používání Left Join v BI workflow,
- zlepšení kvality dat před reportingem.

---

# Business pohled

Cílem projektu nebylo pouze technické čištění dat, ale také:
- zabránění chybným KPI výpočtům,
- zachování integrity reportingu,
- detekce problémů v kvalitě dat,
- pochopení business dopadu nekvalitních dat.

---

# Další kroky

Plánované pokračování:
- KPI reporting,
- návrh dashboardů,
- Power BI vizualizace,
- základy DAX,
- business storytelling,
- star schema modelování.
