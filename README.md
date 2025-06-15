
# Jednoduchý Scraper Volebních Výsledků

Tento Python skript slouží k **jednoduchému získávání (scrapování) volebních výsledků** z webových stránek volby.cz, jejich zpracování a následnému uložení do souboru CSV. Umožňuje rychle extrahovat data o voličích, vydaných obálkách, platných hlasech a výsledky jednotlivých politických stran pro obce v zadaném kraji.

---

## Funkce

* **Stahování HTML:** Bezpečné stahování HTML obsahu z libovolné URL pomocí knihovny `requests`.
* **Extrakce dat o obcích:** Automatické nalezení názvů, kódů a URL pro detailní výsledky jednotlivých obcí v rámci zadaného kraje.
* **Extrakce základních statistik:** Získání počtu voličů, vydaných obálek a platných hlasů pro každou obec.
* **Extrakce výsledků stran:** Sebrání hlasů pro jednotlivé politické strany z detailních stránek obcí.
* **Ukládání do CSV:** Export všech získaných dat do přehledného CSV souboru, kde každý řádek reprezentuje jednu obec a sloupce obsahují základní statistiky a hlasy pro jednotlivé strany.
* **Robustní zpracování chyb:** Základní ošetření chyb při stahování stránek a parsování dat.

---

## Jak to spustit?

Skript se spouští z příkazové řádky a vyžaduje dva argumenty: **URL hlavní stránky kraje** na volby.cz a **název výstupního CSV souboru**.

### Požadavky

* Python 3.x
* Knihovna `requests` (nainstalujete ji pomocí `pip install requests`)

### Použití

```bash
python nazev_skriptu.py <URL_HLAVNI_STRANKY_KRAJE> <NAZEV_CSV_SOUBORU>