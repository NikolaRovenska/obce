# Scraper Volebních Výsledků z Obcí

Tento Python skript slouží k **automatickému získávání volebních výsledků** z webu [volby.cz](https://www.volby.cz) v rámci **jednotlivých obcí**. Prochází HTML strukturu stránek, extrahuje základní statistiky a výsledky jednotlivých politických stran, a vše ukládá do CSV formátu pro další zpracování.

---

## Funkce

*  **Stahování HTML stránek** pomocí `requests`
*  **Parsers obcí** – extrahuje kódy, názvy a URL odkazující na detailní výsledky
*  **Získání statistiky obce** – počet voličů, vydané obálky, platné hlasy
*  **Získání hlasů pro strany** – z každé obce stáhne výsledky hlasování
*  **Výstup do CSV** – každá obec na jednom řádku, sloupce obsahují statistiky a hlasy stran
*  **Ošetření běžných chyb** – jako nedostupnost stránky nebo chybějící data

---

## Ukázka struktury výstupu

| Kód obce | Název obce | Voliči | Obálky | Platné hlasy | Strana A | Strana B | ... |
| -------- | ---------- | ------ | ------ | ------------ | -------- | -------- | --- |
| 123456   | Obecnice   | 654    | 623    | 619          | 300      | 150      | ... |

---

## Požadavky

* Python 3.x
* Knihovny: `requests`, `csv`, `re`, `bs4`
  (nainstaluješ např. přes `pip install requests beautifulsoup4`)

---

## Použití

Skript se spouští z příkazové řádky. Potřebuješ zadat:

1. **URL hlavní stránky kraje** (např. výsledky voleb v daném kraji)
2. **Název výstupního souboru CSV**

### Spuštění:

```bash
python scraper.py https://www.volby.cz/pls/ps2021/ps3?xkraj=14 výstup.csv
```

Po spuštění skript stáhne data pro všechny obce z dané stránky a uloží je do přehledného CSV.


