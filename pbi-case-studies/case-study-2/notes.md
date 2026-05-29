# Business Findings

## Souhrn

Dashboard byl vytvořen za účelem analýzy prodejních dat společnosti TechStore.

Analýza se zaměřila na:

- celkové tržby
- počet objednávek
- průměrnou hodnotu objednávky
- počet zákazníků
- výkonnost regionů
- výkonnost produktů
- vývoj tržeb v čase

---

## Klíčové KPI

| KPI | Hodnota |
|-------|-------:|
| Celkové tržby | 125 000 Kč |
| Celkové objednávky | 10 |
| Průměrná objednávka | 12 500 Kč |
| Unikátní zákazníci | 5 |

---

## Analýza regionů

Praha dosahuje nejvyšších tržeb ze všech sledovaných regionů.

Přibližně:

```text
58 % celkových tržeb
```

pochází právě z Prahy.

Ostatní regiony (Brno, Plzeň a Ostrava) vykazují výrazně nižší objemy tržeb.

### Doporučení

- Prověřit důvody vysoké výkonnosti Prahy.
- Identifikovat možnosti přenosu úspěšných obchodních aktivit do ostatních regionů.
- Zaměřit marketingové kampaně na regiony s nižší výkonností.

---

## Analýza produktů

Nejvyšší tržby generuje produkt:

```text
Notebook
```

S výrazným odstupem za ním následují:

- Monitor
- Klávesnice
- Myš

### Doporučení

- Podpořit prodej notebooků marketingovými aktivitami.
- Analyzovat, zda jsou vysoké tržby způsobeny vyšší cenou produktu nebo vyšším objemem prodaných kusů.
- Zvážit cross-sell příslušenství k notebookům.

---

## Vývoj tržeb v čase

Tržby se v jednotlivých měsících liší a nevykazují stabilní růstový trend.

Byly zaznamenány měsíce s vyšším i nižším objemem tržeb.

### Doporučení

- Sledovat sezónnost prodejů.
- Rozšířit dataset o delší časové období.
- Vyhodnotit případné marketingové kampaně nebo promo akce ovlivňující prodeje.

---

## Zákazníci

Celkem bylo identifikováno:

```text
5 unikátních zákazníků
```

kteří vytvořili:

```text
10 objednávek
```

To znamená, že někteří zákazníci nakoupili více než jednou.

### Doporučení

- Sledovat opakované nákupy zákazníků.
- Zavést metriky zákaznické retence.
- Analyzovat zákaznickou loajalitu na větším datasetu.

---

## Závěr

Na základě dostupných dat lze identifikovat dva hlavní faktory ovlivňující výkon společnosti:

1. Dominantní postavení regionu Praha.
2. Vysoký podíl produktu Notebook na celkových tržbách.

Dashboard poskytuje managementu rychlý přehled o výkonnosti prodeje a umožňuje interaktivní filtrování podle regionů a produktů.

Projekt zároveň demonstruje využití Power BI pro:

- datové modelování
- tvorbu DAX metrik
- návrh dashboardů
- business reporting
- základní analytickou interpretaci dat
