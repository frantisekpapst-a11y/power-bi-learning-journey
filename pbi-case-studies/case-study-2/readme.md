# Case Study 02 – TechStore Sales Dashboard (Power BI)

## Přehled projektu

Cílem této případové studie bylo vytvořit interaktivní dashboard v Power BI pro analýzu prodejních dat fiktivního obchodu TechStore.

Projekt demonstruje celý základní analytický workflow:

- datový model
- relace mezi tabulkami
- tvorbu DAX metrik
- návrh dashboardu
- interpretaci business výsledků

Dashboard umožňuje sledovat výkonnost prodeje podle regionů, produktů a času a zároveň poskytuje základní KPI metriky pro management.

---

## Použité nástroje

- Power BI Desktop
- DAX
- Microsoft Excel

---

## Datový model

Projekt využívá tři propojené tabulky:

### Customers

| Sloupec |
|----------|
| customer_id |
| customer_name |
| region |

### Orders

| Sloupec |
|----------|
| order_id |
| customer_id |
| product_id |
| quantity |
| order_date |

### Products

| Sloupec |
|----------|
| product_id |
| product_name |
| category |
| price |

### Relace

```text
customers_techstore (1) ────── (*) orders_techstore

products_techstore  (1) ────── (*) orders_techstore
```

Model odpovídá základnímu hvězdicovému schématu (Star Schema), které je standardem v Power BI a Business Intelligence.

---

## Vytvořené DAX metriky

### Celkové tržby

```DAX
Total Revenue =
SUMX(
    orders_techstore,
    orders_techstore[quantity] *
    RELATED(products_techstore[price])
)
```

Výpočet celkových tržeb jako:

```text
Množství × Cena produktu
```

pro každou objednávku.

---

### Počet objednávek

```DAX
Total Orders =
DISTINCTCOUNT(orders_techstore[order_id])
```

Počet unikátních objednávek.

---

### Průměrná hodnota objednávky

```DAX
Average Order Value =
DIVIDE(
    [Total Revenue],
    [Total Orders]
)
```

Průměrná hodnota jedné objednávky.

---

### Počet unikátních zákazníků

```DAX
Unique Customers =
DISTINCTCOUNT(orders_techstore[customer_id])
```

Počet unikátních zákazníků.

---

## Dashboard

Dashboard obsahuje následující části:

### KPI metriky

- Celkové tržby
- Celkové objednávky
- Průměrná objednávka
- Unikátní zákazníci

### Vizualizace

#### Tržby podle regionu

Zobrazuje rozložení tržeb mezi jednotlivými regiony.

#### Tržby podle produktu

Porovnání výkonnosti jednotlivých produktů.

#### Měsíční vývoj tržeb

Vývoj tržeb v čase.

#### Detailní tabulka objednávek

Obsahuje detailní přehled jednotlivých transakcí.

### Filtry (Slicery)

- Region
- Produkt

---

## Hlavní zjištění

### Regiony

Praha generuje nejvyšší tržby ze všech regionů.

Podíl Prahy na celkových tržbách činí přibližně:

```text
58 %
```

### Produkty

Notebook představuje nejvýkonnější produkt z pohledu tržeb.

### Zákazníci

Celkem bylo obslouženo:

```text
5 unikátních zákazníků
```

kteří vytvořili:

```text
10 objednávek
```

---

## Dashboard Preview

Soubor:

```text
dashboard/techstore_dashboard.png
```

obsahuje náhled finálního dashboardu.

---

## Struktura projektu

```text
case-study-02-techstore-powerbi/
│
├── README.md
│
├── dashboard/
│   ├── techstore.pbix
│   └── techstore_dashboard.png
│
├── data/
│   ├── customers_techstore.xlsx
│   ├── orders_techstore.xlsx
│   └── products_techstore.xlsx
│
└── notes/
    └── business_findings.md
```

---

## Co jsem si v projektu procvičil

- Import dat do Power BI
- Datové modelování
- Relace 1:N
- Star Schema
- DAX
- SUMX
- RELATED
- DISTINCTCOUNT
- DIVIDE
- KPI metriky
- Dashboard Design
- Slicery a filtrování
- Business interpretaci dat

---

## Autor

Projekt vznikl jako součást přípravy na pozici Data Analyst / BI Analyst a slouží jako ukázka práce s Power BI, DAX a datovým modelováním.
