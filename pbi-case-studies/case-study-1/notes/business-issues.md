# Business Issues – Data Quality & Reporting Risks

## Přehled

Během analýzy a čištění dat bylo identifikováno několik business problémů, které by mohly negativně ovlivnit:
- reporting,
- KPI,
- dashboardy,
- business rozhodování,
- kvalitu analytických výstupů.

Cílem bylo nejen technicky vyčistit data, ale také pochopit jejich business dopad.

---

# 1. Duplicitní zákazníci

## Problém
V datasetu customers byli nalezeni duplicitní zákazníci se stejným:
- jménem,
- emailem,
- regionem.

---

## Business riziko
Duplicitní zákazníci mohou způsobit:
- nesprávný počet zákazníků,
- zkreslenou segmentaci,
- nepřesné customer analytics,
- chybné KPI.

---

## Riziko při merge
Při spojení orders a customers by duplicity mohly:
- duplikovat objednávky,
- nafouknout revenue,
- vytvořit many-to-many problémy.

---

## Řešení
- validace emailů,
- odstranění duplicitních záznamů,
- zachování clean customer dimension.

---

# 2. Duplicitní objednávky

## Problém
Byla nalezena duplicitní objednávka se stejným:
- order_id,
- customer_id,
- revenue.

---

## Business riziko
Duplicitní objednávky mohou:
- zdvojit revenue,
- zkreslit počet objednávek,
- poškodit KPI reporting,
- ovlivnit forecasting.

---

## Řešení
- odstranění technických duplicit,
- validace uniqueness order_id.

---

# 3. Missing Customer Data

## Problém
Některé objednávky neměly validního zákazníka nebo obsahovaly:
- null customer_id,
- chybějící region.

---

## Business riziko
Nekvalitní customer data komplikují:
- regionální reporting,
- customer segmentation,
- CRM analýzu,
- marketing reporting.

---

## Řešení
- vytvoření validation flagů,
- zachování objednávek pomocí Left Join,
- identifikace unmatched records.

---

# 4. Invalid Email Addresses

## Problém
Některé emaily měly nevalidní formát.

Příklad:
```text
karel.email.cz
```

---

## Business riziko
Nevalidní emaily mohou způsobit:
- nefunkční marketing kampaně,
- problémy v CRM,
- špatnou komunikaci se zákazníky.

---

## Řešení
- email validation,
- vytvoření email_status flagu.

---

# 5. Mixed Date Formats

## Problém
Objednávky obsahovaly různé formáty dat.

Příklad:
```text
2025-01-02
02.01.2025
2025/01/03
```

---

## Business riziko
Nekonzistentní datumy mohou:
- rozbít time intelligence,
- poškodit trend analýzu,
- způsobit chyby ve filtrech,
- ovlivnit DAX calculations.

---

## Řešení
- standardizace datových typů,
- převod na jednotný date format.

---

# 6. Suspicious Revenue

## Problém
Byly nalezeny extrémní revenue hodnoty.

Příklad:
```text
999999
```

---

## Business riziko
Extrémní hodnoty mohou:
- zkreslit průměry,
- poškodit KPI,
- ovlivnit forecasting,
- indikovat:
  - fraud,
  - import error,
  - currency mismatch.

---

## Řešení
- vytvoření revenue_flag,
- označení suspicious orders,
- doporučení další business validace.

---

# 7. Negative Quantity

## Problém
Některé objednávky obsahovaly záporné quantity.

---

## Business interpretace
Záporné quantity nemusí být chyba.

Může znamenat:
- refund,
- vrácení zboží,
- storno objednávky,
- skladovou korekci.

---

## Riziko
Automatické odstranění by mohlo:
- poškodit reporting,
- zkreslit business realitu.

---

## Řešení
- vytvoření quantity_status,
- interpretace pomocí business logiky.

---

# 8. Nekonzistentní Product Categories

## Problém
Kategorie produktů měly různé zápisy.

Příklad:
```text
Electronics
electronics
```

---

## Business riziko
Nekonzistentní názvy:
- vytvářejí duplicitní kategorie,
- rozbíjejí dashboardy,
- komplikují agregace.

---

## Řešení
- standardizace textu,
- sjednocení naming conventions.

---

# 9. Missing Product Categories

## Problém
Některé produkty neměly přiřazenou kategorii.

---

## Business riziko
Produkty bez kategorií:
- komplikují reporting,
- rozbíjejí vizualizace,
- snižují kvalitu dashboardů.

---

## Řešení
- category_status validation,
- identifikace incomplete records.

---

# 10. Many-to-Many Merge Risk

## Problém
Duplicitní produkty způsobily:
- many-to-many merge problém.

---

## Business riziko
Many-to-many vztahy mohou:
- zdvojovat revenue,
- vytvářet nesprávné agregace,
- poškodit KPI reporting.

---

## Řešení
- validace uniqueness dimension tables,
- odstranění technických duplicit,
- kontrola merge logiky.

---

# Hlavní Business Lessons Learned

## Data nejsou automaticky správná
Analytik musí:
- data validovat,
- zpochybňovat,
- kontrolovat business logiku.

---

## Špatná data = špatná rozhodnutí
Garbage In = Garbage Out.

---

## Data cleaning je business disciplína
Nejde pouze o technické čištění, ale o:
- ochranu KPI,
- kvalitu reportingu,
- důvěryhodnost dat.

---

# Celkový výsledek

Výsledkem projektu byl:
- čistější dataset,
- stabilnější reporting,
- lepší kvalita dat,
- připravený základ pro dashboarding a KPI reporting.
