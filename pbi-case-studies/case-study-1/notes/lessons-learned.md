# Lessons Learned – Power BI ETL & Data Cleaning Case Study

## Přehled

Tato case study poskytla praktický pohled na:
- ETL workflow,
- data cleaning,
- business validaci dat,
- práci s relačními daty,
- přípravu datasetu pro reporting v Power BI.

Projekt ukázal, že kvalitní analytika nezačíná dashboardem, ale kvalitou dat.

---

# 1. Data nejsou automaticky správná

Jedna z nejdůležitějších lekcí projektu.

Data mohou obsahovat:
- duplicity,
- null hodnoty,
- nevalidní záznamy,
- nekonzistentní formáty,
- chybné business hodnoty.

Analytik musí:
- data validovat,
- zpochybňovat,
- kontrolovat jejich kvalitu.

---

# 2. Data cleaning je klíčová část BI workflow

Velká část práce analytika probíhá ještě před:
- dashboardingem,
- KPI reportingem,
- tvorbou vizualizací.

Bez kvalitního cleaning procesu:
- dashboardy nejsou důvěryhodné,
- KPI mohou být zkreslené,
- management může dělat špatná rozhodnutí.

---

# 3. Power Query není jen klikací nástroj

Power Query funguje jako:
- ETL engine,
- transformační pipeline,
- workflow systém pro přípravu dat.

Každý krok:
- se ukládá,
- lze upravit,
- automaticky se opakuje při refreshi.

---

# 4. Applied Steps jsou velmi důležité

Applied Steps představují:
- historii transformací,
- auditní stopu,
- automatizovaný workflow.

Dobře organizované kroky:
- zlepšují přehlednost,
- zjednodušují debugging,
- usnadňují údržbu projektu.

---

# 5. Trim a Clean jsou důležité i u jednoduchých datasetů

Skryté mezery nebo neviditelné znaky mohou:
- rozbít merge,
- vytvářet falešné duplicity,
- komplikovat grouping a relationships.

Použití:
- Trim,
- Clean,

je dobrý standard při práci s textovými daty.

---

# 6. Conditional Columns pomáhají vytvářet data quality logiku

Pomocí:
- conditional columns,
- custom columns,

lze vytvářet:
- validační pravidla,
- quality flagy,
- suspicious indicators.

Například:
- invalid email,
- suspicious revenue,
- missing region,
- refund orders.

---

# 7. Null values jsou velmi důležité

Rozdíl mezi:
- null,
- prázdným textem,
- nevalidní hodnotou,

má velký vliv na:
- reporting,
- DAX,
- relationships,
- KPI výpočty.

---

# 8. Duplicitní data mohou rozbít reporting

Duplicitní:
- zákazníci,
- objednávky,
- produkty,

mohou způsobit:
- double counting,
- nafouknuté revenue,
- nesprávné agregace,
- chybné dashboardy.

---

# 9. Ne každá duplicita je chyba

Velmi důležitý business insight.

Například:
- záporné quantity může znamenat refund,
- stejný produkt nemusí být automaticky duplicita.

Analytik musí:
- chápat business kontext,
- neodstraňovat data bez validace.

---

# 10. Left Join je klíčový pro BI reporting

Left Join:
- zachovává všechny objednávky,
- i když některá dimenze chybí.

To pomáhá:
- odhalovat problémy v datech,
- zachovat reporting integrity,
- identifikovat missing relationships.

---

# 11. Many-to-Many problémy jsou nebezpečné

Duplicitní klíče při merge mohou:
- násobit řádky,
- zdvojovat revenue,
- poškodit KPI.

Dimension tabulky by měly obsahovat:
- unikátní klíče,
- konzistentní data.

---

# 12. Business mindset je důležitější než samotné klikání

Cílem analytika není:
- pouze používat Power BI.

Ale:
- chápat business dopad dat,
- chránit kvalitu reportingu,
- vytvářet důvěryhodné analytické výstupy.

---

# 13. ETL workflow je základ moderní analytiky

Proces:
```text
Import → Validation → Cleaning → Transformation → Reporting
```

je základ:
- BI analytiky,
- datového modelování,
- dashboardingu,
- datového inženýrství.

---

# 14. Data quality ovlivňuje KPI

Nekvalitní data mohou poškodit:
- revenue reporting,
- forecasting,
- customer analytics,
- business rozhodování.

Proto:
- data quality není technický detail,
- ale business priorita.

---

# 15. Praktická práce je nejrychlejší způsob učení

Tato case study ukázala, že:
- learning by doing,
- řešení realistických problémů,
- práce s rozbitými daty,

pomáhá budovat:
- analytické myšlení,
- BI mindset,
- praktické zkušenosti.

---

# Celkové shrnutí

Během projektu byly procvičeny:
- importy dat,
- cleaning workflow,
- validace dat,
- merge queries,
- data quality analysis,
- business interpretace dat,
- ETL mindset.

Výsledkem byl:
- čistý analytický dataset,
- realistická BI zkušenost,
- základ pro budoucí dashboarding a KPI reporting.
