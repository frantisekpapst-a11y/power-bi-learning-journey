# Notes

## Co jsem se naučil

Během tohoto projektu jsem si znovu prakticky vyzkoušel celý BI proces:

1. Import dat z CSV souborů
2. Čištění dat v Power Query
3. Kontrolu datových typů
4. Návrh hvězdicového schématu
5. Tvorbu relací mezi tabulkami
6. Vytváření DAX metrik
7. Práci s funkcemi:
   - SUMX
   - RELATED
   - DISTINCTCOUNT
   - DIVIDE
   - CALCULATE
8. Tvorbu dashboardu v Power BI

---

## Problémy během projektu

### Chybějící hodnota kampaně

V tabulce campaigns chyběl název jedné kampaně.

Řešení:
- identifikace problému v Power Query
- rozhodnutí zdokumentovat datový problém

### Relace zákazník -> objednávka

Model zobrazoval relaci 1:1.

Důvod:
- ukázková data obsahovala pouze jednu objednávku na zákazníka

V reálném prostředí by relace byla 1:N.

### DAX syntaxe

Při tvorbě CALCULATE metriky vznikla chyba způsobená nadbytečnou závorkou.

Řešení:
- kontrola syntaxe
- oprava uzavíracích závorek

---

## Co bych vylepšil

Pokud bych projekt dále rozšiřoval:

- časovou analýzu prodejů
- meziroční srovnání
- segmentaci zákazníků
- RFM analýzu
- detailnější marketingovou atribuci
- KPI stránku pro management
- pokročilé DAX metriky

---

## Celkové zhodnocení

Projekt pokrývá kompletní workflow Power BI:

Data → Power Query → Datový model → DAX → Dashboard → Business Insights

Jedná se o první kompletní end-to-end BI case study vytvořenou samostatně v Power BI.
