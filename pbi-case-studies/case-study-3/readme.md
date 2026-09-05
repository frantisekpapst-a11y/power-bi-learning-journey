# Case Study 03 - Czech E-commerce Analytics Dashboard

## Přehled projektu

Tato případová studie demonstruje vytvoření kompletního analytického řešení v Power BI nad simulovanými daty českého e-commerce prostředí.

Cílem projektu bylo navrhnout datový model, vytvořit DAX metriky a připravit interaktivní dashboardy pro analýzu obchodního výkonu, zákazníků a regionů.

Projekt zahrnuje:

- datový model ve stylu hvězdicového schématu (Star Schema)
- transformace dat v Power Query
- tvorbu DAX metrik
- analytické dashboardy
- drill-through stránku pro detailní analýzu regionů.

---

# Struktura projektu

```text
case-study-3/
│
├── data/
│   ├── campaigns.csv
│   ├── customers.csv
│   ├── order_details.csv
│   ├── orders.csv
│   ├── products.csv
│   └── regions.csv
│
├── dashboard/
│   └── czech_ecommerce.pbix
│
├── screenshots/
│   ├── dashboard.png
│   ├── customer_dashboard.png
│   └── data_model.png
│
├── README.md
└── notes.md
```

---

## Použité technologie

- Power BI Desktop
- Power Query
- DAX
- CSV Data Sources
- GitHub

---

## Datový model

Projekt využívá hvězdicové schéma složené z následujících tabulek:

### Faktové tabulky

- `orders`
- `order_details`

### Dimenzní tabulky

- `customers`
- `products`
- `campaigns`
- `regions`

Model umožňuje analyzovat:

- tržby
- objednávky
- zákazníky
- regiony
- marketingové kampaně

---

## Vytvořené DAX metriky

### Celkové tržby

```DAX
Celkové tržby =
SUMX(
    order_details,
    order_details[quantity] * RELATED(products[price])
)
```

### Počet objednávek

```DAX
Počet objednávek =
DISTINCTCOUNT(orders[order_id])
```

### Počet zákazníků

```DAX
Počet zákazníků =
DISTINCTCOUNT(customers[customer_id])
```

### Průměrná objednávka

```DAX
Průměrná objednávka =
DIVIDE(
    [Celkové tržby],
    [Počet objednávek]
)
```

### Průměrná útrata zákazníka

```DAX
Průměrná útrata =
DIVIDE(
    [Celkové tržby],
    [Počet zákazníků]
)
```

### ROI kampaně

```DAX
ROI kampaně =
DIVIDE(
    [Celkové tržby] -
    SUM(campaigns[budget]),
    SUM(campaigns[budget])
)
```

### Průměrný věk zákazníků

```DAX
Průměrný věk =
AVERAGE(customers[age])
```

### Počet regionů

```DAX
Počet regionů =
DISTINCTCOUNT(regions[region_name])
```

---

# Dashboard Pages

## 1. Sales & Marketing Dashboard

Hlavní stránka zaměřená na obchodní výkon a marketingové kampaně.

### KPI

- Celkové tržby
- Počet objednávek
- Počet zákazníků
- Průměrná objednávka

### Vizualizace

- Tržby podle regionu
- Průměrná objednávka podle regionu
- ROI marketingových kampaní
- Tržby podle kampaně

### Filtry

- Region
- Marketingová kampaň
- Měsíc objednávky

---

## 2. Customer Insights Dashboard

Dashboard zaměřený na analýzu zákazníků.

### KPI

- Počet zákazníků
- Průměrný věk
- Průměrná útrata
- Počet regionů

### Vizualizace

- Počet zákazníků podle regionu
- Počet zákazníků podle pohlaví
- Průměrná útrata podle regionu
- Tržby podle zákazníka

### Filtry

- Region
- Pohlaví
- Věk zákazníků

---

## 3. Region Detail (Drill-through)

Detailní stránka dostupná pomocí Drill-through z hlavního dashboardu.

### KPI

- Celkové tržby regionu
- Počet zákazníků regionu
- Průměrná objednávka regionu

### Vizualizace

- Tržby podle kampaně
- Tržby podle zákazníka

### Funkcionalita

- Drill-through z regionálních grafů
- Automatické filtrování podle vybraného regionu

---

# Screenshoty

## Sales & Marketing Dashboard

Souhrnný pohled na obchodní výkon, regiony a marketingové kampaně.

## Customer Insights Dashboard

Analýza zákaznické základny, regionů a zákaznické hodnoty.

## Data Model

Datový model navržený ve formě hvězdicového schématu.

---

# Klíčové dovednosti procvičené v projektu

- Datové modelování
- Power Query transformace
- Tvorba DAX metrik
- KPI reporting
- Dashboard design
- Interaktivní filtry
- Drill-through analýza
- Business Intelligence reporting
- GitHub dokumentace projektů

---

# Možná budoucí rozšíření

- Custom Tooltip Pages
- Bookmarks a navigační tlačítka
- Pokročilé DAX metriky
- Time Intelligence analýzy
- Forecasting a trendové analýzy
- Publikace do Power BI Service