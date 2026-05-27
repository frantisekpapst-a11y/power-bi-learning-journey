# Cleaning Process – Power Query Workflow

## Cíl čištění dat

Cílem bylo vytvořit konzistentní a analyticky použitelný dataset pro budoucí reporting v Power BI.

Proces simuloval reálnou práci BI analytika při:
- přípravě dat,
- validaci kvality dat,
- detekci problémových záznamů,
- slučování více zdrojů,
- tvorbě ETL pipeline.

---

# 1. Import dat

Byly importovány 3 zdrojové soubory:

| Dataset | Formát |
|---|---|
| customers | JSON |
| orders | CSV |
| products | CSV |

Import proběhl pomocí Power Query v Power BI Desktop.

---

# 2. Čištění tabulky Customers

## Provedené kroky

### Čištění textových polí
Použity transformace:
- Trim
- Clean

Důvod:
- odstranění skrytých mezer,
- odstranění neviditelných znaků,
- prevence problémů při JOIN operacích.

---

### Validace emailů
Vytvořen podmíněný sloupec:

```text
email_status
```

Logika:
- valid
- invalid

Důvod:
- kontrola kvality zákaznických dat,
- prevence problémů v CRM a marketingových reportech.

---

### Kontrola regionů
Vytvořen podmíněný sloupec:

```text
region_status
```

Logika:
- valid
- missing region

Důvod:
- regionální reporting vyžaduje kompletní geografická data.

---

### Odstranění duplicit
Detekováni duplicitní zákazníci podle emailu.

Provedeno:
- odstranění duplicitních řádků.

Business důvod:
- duplicity mohou zkreslit:
  - počet zákazníků,
  - KPI,
  - segmentaci,
  - customer analytics.

---

# 3. Čištění tabulky Orders

## Provedené kroky

### Kontrola quantity
Detekovány záporné hodnoty quantity.

Vytvořen sloupec:

```text
quantity_status
```

Logika:
- valid
- return/refund

Business interpretace:
- záporné quantity může znamenat:
  - vrácení zboží,
  - refund,
  - storno objednávky.

---

### Kontrola statusů objednávek
Vytvořen validační sloupec:

```text
status_quality
```

Logika:
- valid
- invalid

Důvod:
- sjednocení business logiky workflow objednávek.

---

### Detekce suspicious revenue
Vytvořen sloupec:

```text
revenue_flag
```

Logika:
- normal
- suspicious
- missing revenue

Business důvod:
- identifikace extrémních hodnot,
- detekce potenciálních chyb,
- fraud detection mindset.

---

### Odstranění duplicitních objednávek
Byly odstraněny duplicitní order_id.

Důvod:
- prevence zkreslení:
  - revenue,
  - počtu objednávek,
  - KPI reportingu.

---

# 4. Čištění tabulky Products

## Provedené kroky

### Standardizace textu
Použity:
- Trim
- Clean
- Capitalize Each Word

Důvod:
- sjednocení kategorií produktů.

---

### Kontrola kategorií
Vytvořen sloupec:

```text
category_status
```

Logika:
- valid
- missing category

Důvod:
- produkt bez kategorie komplikuje reporting i dashboarding.

---

### Analýza duplicit produktů
Byly analyzovány duplicitní produkty.

Poznatek:
- duplicita nemusí být vždy chyba,
- může reprezentovat:
  - stejný produkt,
  - různé SKU,
  - různé varianty.

---

# 5. Merge datasetů

Proveden Left Join:

| Zdroj | Cíl | Klíč |
|---|---|---|
| orders | customers_clean | customer_id |
| orders | products_clean | product_id |

---

# 6. Problémy při merge

Během merge byly identifikovány:
- null hodnoty,
- chybějící reference,
- problémy s relacemi,
- riziko many-to-many vztahů.

Business dopad:
- nekonzistentní reporting,
- chybné KPI,
- nesprávné agregace.

---

# 7. Výsledný dataset

Výsledkem byl:
- očištěný,
- validovaný,
- propojený dataset připravený pro:
  - dashboarding,
  - KPI reporting,
  - datové modelování,
  - DAX analýzu.

---

# Hlavní learning outcomes

## Technické
- Power Query workflow
- ETL mindset
- Data cleaning
- Conditional columns
- Merge queries
- Validace dat
- Business logic v datech

---

## Business
- pochopení dopadu nekvalitních dat,
- analytické přemýšlení nad outliers,
- práce s datovou kvalitou,
- reporting mindset,
- prevence zkreslení KPI.
