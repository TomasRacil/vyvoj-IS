# Vývoj IS - Úvodní hodina

## 1. Cíle předmětu

V rámci tohoto předmětu se společně ponoříme do světa moderního vývoje informačních systémů. Cílem je:

* Seznámit vás se základními principy, architekturami a technologiemi, které stojí za dnešními informačními systémy.
* Poskytnout vám praktické dovednosti v oblasti návrhu, implementace a správy databázových systémů, jak relačních (SQL), tak vybraných NoSQL řešení.
* Naučit vás vytvářet dynamické webové aplikace, od klientské části (frontend – HTML, CSS, JavaScript) až po serverovou logiku (backend – PHP/Python) a její propojení s databází.
* Představit a procvičit si klíčové nástroje a postupy pro efektivní týmový vývoj, zejména verzovací systém Git a kontejnerizační platformu Docker.

Po absolvování kurzu byste měli být schopni navrhnout, vyvinout a spravovat jednodušší informační systém.

## 2. Organizační informace

* **Způsob zakončení:** Zápočet bude udělen za odevzdání projektu, který bude definován v první části předmětu.
* **Hodnocení:** Podmínkou udělení zápočtu jsou pravidelné prezentace vyvíjeného informačního systému, termíny budou upřesněny v průběhu předmětu.
* **Materiály:** Veškeré podklady, zadání úkolů a další informace budou dostupné v tomto repozitáři nebo na MS Teams.

## 3. Předpoklady

Pro úspěšné zvládnutí praktických částí předmětu je nezbytná základní orientace v následujících nástrojích. Pokud si nejste jisti, využijte prosím připravené materiály pro samostudium:

* **Git:** Základy verzování, práce s lokálním a vzdáleným repozitářem, větvení a slučování.
    * Materiály pro osvěžení znalostí [zde](../00-predpoklady/git/README.md).
* **Docker:** Principy kontejnerizace, práce s Docker image a kontejnery, základy Docker Compose pro správu vícekontejnerových aplikací.
    * Materiály pro osvěžení znalostí [zde](../00-predpoklady/docker/README.md).

Důrazně doporučujeme si tyto technologie osvěžit nebo doučit ještě před začátkem výuky témat, kde budou aktivně využívány (zejména při práci s databázemi a webovými aplikacemi).

## 4. Harmonogram předmětu

Aktuální plán výuky je dostupný online v [této tabulce](https://docs.google.com/spreadsheets/d/1unlghcFp0WomZLNOnwnwKmU65gzm9eoSRz6vJdFNR1A/edit?usp=sharing).

*Poznámka: Harmonogram je orientační a může dojít k drobným úpravám v průběhu semestru.*

## 5. Úvod do problematiky vývoje IS

* **Co je to informační systém (IS)?**
    * V nejširším slova smyslu je informační systém jakýkoli **organizovaný systém pro sběr, uchovávání, zpracování, analýzu a šíření informací**. Nemusí nutně zahrnovat počítače!
    * Jeho základními složkami jsou typicky:
        * **Lidé:** Uživatelé, správci, vývojáři.
        * **Data/Informace:** Fakta, čísla, texty, obrazy, které systém zpracovává.
        * **Procesy/Metody:** Pravidla a postupy, jak se s daty pracuje.
        * **Technologie (volitelně):** Nástroje používané pro podporu procesů (papír, tužka, kartotéka, ale i počítače).
    * **Příklady nepočítačových IS:** Lístkový katalog v knihovně, systém papírového účetnictví, Kanbanová tabule s úkoly na papírcích, jízdní řád na zastávce, neformální rozhovor (např. "pokec v hospodě" o tom, kdo má jaké pivo nebo jak dopadl fotbal - i zde dochází ke sběru informací [ptáme se], jejich uchovávání [pamatujeme si], zpracování [porovnáváme, kdo co řekl], a šíření [odpovídáme, sdílíme názory] mezi lidmi [účastníky] pomocí neformálních procesů [konverzace]).
    * **Počítačový IS (Computerized IS - CIS):** V kontextu tohoto kurzu a moderní doby budeme pod pojmem "informační systém" rozumět primárně **počítačový informační systém**. Ten rozšiřuje obecnou definici o specifické technologické komponenty:
        * **Hardware:** Počítače, servery, sítě, periferie.
        * **Software:** Operační systémy, databázové systémy, aplikační software (náš hlavní fokus).
        * **Data:** Digitálně uložená data v databázích.
        * **Lidé:** Uživatelé interagující se systémem přes rozhraní, správci, vývojáři.
        * **Procesy:** Definované workflow a postupy implementované v softwaru.
        * **Rozhraní:** Způsoby, jak lidé a jiné systémy interagují s IS (grafické uživatelské rozhraní - GUI, aplikační programovací rozhraní - API).

* **Proč je vývoj IS důležitý?**
    * **Efektivita a automatizace:** IS umožňují zrychlit a zautomatizovat rutinní úkoly, snížit chybovost a uvolnit lidské zdroje pro komplexnější činnosti.
    * **Podpora rozhodování:** Poskytují relevantní, včasné a přesné informace pro lepší strategické i operativní rozhodování.
    * **Konkurenční výhoda:** Inovativní IS mohou firmě přinést významnou výhodu na trhu.
    * **Komunikace a spolupráce:** Usnadňují sdílení informací a spolupráci uvnitř organizace i navenek.
    * **Nové obchodní modely:** Moderní IS umožňují vznik zcela nových služeb a obchodních modelů (např. e-commerce, sdílená ekonomika).
    * **Správa znalostí:** Pomáhají uchovávat a sdílet znalosti v rámci organizace.
    * **Klíčová infrastruktura:** V dnešním světě jsou IS páteří fungování téměř všech organizací, od malých firem po globální korporace a státní správu. Schopnost je efektivně navrhovat, vyvíjet a spravovat je proto kriticky důležitá.

* **Klíčové komponenty IS (z našeho pohledu - fokus na vývoj):**
    * **Data:** Srdce každého IS. Budeme se zabývat jejich modelováním (jak strukturovat data), ukládáním (persistence v databázích – relačních i NoSQL), zajištěním jejich kvality (integrita, konzistence) a bezpečnosti. Naučíme se s nimi efektivně manipulovat pomocí SQL a dalších nástrojů.
    * **Aplikace (Logika):** Software, který s daty pracuje a poskytuje funkcionalitu uživatelům. Typicky se dělí na:
        * **Frontend (Klient):** Část, se kterou přímo interaguje uživatel, obvykle v prostředí webového prohlížeče. Zodpovídá za prezentaci dat a sběr uživatelských vstupů (HTML, CSS, JavaScript).
        * **Backend (Server):** Logika běžící na serveru. Zpracovává požadavky od frontendu, komunikuje s databází, provádí výpočty, zajišťuje bezpečnost a obchodní logiku aplikace (PHP/Python s využitím MVC frameworků). Frontend a backend spolu komunikují (často přes API).
    * **Infrastruktura (Nástroje a Prostředí):** Technologie a nástroje, které podporují vývoj, testování, nasazení a provoz IS. V tomto kurzu se zaměříme na:
        * **Git:** Verzovací systém pro správu změn v kódu a týmovou spolupráci.
        * **Docker:** Kontejnerizační platforma pro snadné vytváření, nasazování a správu izolovaných aplikačních prostředí (databáze, web server, aplikace).
        * (Implicitně sem patří i operační systémy, sítě, webové servery, databázové servery, které Docker pomáhá spravovat).

## 6. Motivace a Nástroje

* **Motivační příklad:** Jako motivační příklad si ukážeme jednoduchý informačního systém. Jedná se o aplikaci s REST API backendem v Pythonu, frontendem vytvořeným v Reactu a databází PostgreSQL. Celá aplikace spustitelná pomocí Dockeru. Tento příklad demonstruje použití všech klíčových technologii (databáze, backend, frontend, kontejnerizace) do funkčního celku. K nalezení [zde](./motivacni-priklad/README.md).
* **Primární nástroje:**
    * **PostgreSQL:** Výkonný open-source relační databázový systém.
    * **Python (s frameworkem Flask nebo FastAPI):** Pro vývoj backendu a REST API.
    * **React (pro frontend), HTML, CSS:** Standardní technologie pro moderní frontend.
    * **Git & GitHub/GitLab:** Pro verzování a sdílení kódu.
    * **Docker & Docker Compose:** Pro správu vývojového a produkčního prostředí.
    * **IDE/Editor:** VS Code, PhpStorm, PyCharm nebo jiný dle vaší preference.

## 7. Co dál?

* **Osvěžte si Git a Docker:** Projděte si materiály v sekci "Předpoklady". Zkuste si základní příkazy.
* **Nainstalujte si software:** Ujistěte se, že máte nainstalovaný Git a Docker Desktop (nebo ekvivalent pro váš OS).
* **Připravte se na příští hodinu:** Podíváme se na základy relačních databází a představíme si PostgreSQL.
