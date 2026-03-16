# Vývoj IS - Materiály k předmětu

Tento repozitář obsahuje výukové materiály a příklady pro předmět zaměřený na **Vývoj informačních systémů (IS)**.

Tento kurz pokrývá široké spektrum témat nezbytných pro moderní vývoj aplikací, včetně:

* Práce s **databázemi**: Relační databáze (PostgreSQL, SQL), úvod do NoSQL.
* **Vývoj webových aplikací**: Frontend (HTML, CSS, JavaScript, React) i backend (Python - Flask/FastAPI, MVC).
* **Databázové programování**: Uložené procedury, triggery.
* **Správa databází**: Základy administrace, ladění, zálohování.
* **Nástroje a technologie**: Git, Docker, REST API.

## Předpoklady

Pro úspěšné absolvování praktických částí předmětu se očekává základní znalost následujících nástrojů. Materiály pro samostudium naleznete v příslušné sekci:

* **Git:** Základy verzování. ([Viz 00-predpoklady/git](./00-predpoklady/git/README.md))
* **Docker:** Základy kontejnerizace a Docker Compose. ([Viz 00-predpoklady/docker](./00-predpoklady/docker/README.md))

Dále se předpokládá základní algoritmické myšlení a znalost základů programování (ideálně v Pythonu nebo JavaScriptu, ale není striktní podmínkou).

## Struktura repozitáře

Materiály jsou organizovány do číslovaných adresářů podle témat probíraných na přednáškách a cvičeních:

* [`00-predpoklady/`](./00-predpoklady/): Materiály a příklady k Gitu a Dockeru.
* [`01-uvodni-hodina/`](./01-uvodni-hodina/README.md): Úvodní informace k předmětu, cíle, hodnocení, harmonogram. **Začněte zde!**
* [`02-relacni-db-sql/`](./02-relacni-db-sql/README.md): Materiály k relačnímu modelu, databázím PostgreSQL a jazyku SQL (DDL, DML, DQL...).
    * Obsahuje vlastní `docker-compose.yml` pro spuštění PostgreSQL a pgAdminu pro tuto sekci.
* [`03-vyvoj-web-server/`](./03-vyvoj-web-server/README.md): Materiály k vývoji serverové části webových aplikací (Python, Flask/FastAPI, MVC, REST API...).
* [`04-vyvoj-web-client/`](./04-vyvoj-web-client/README.md): Materiály k vývoji klientské části webových aplikací (HTML, CSS, JS, React...).
* [`05-vyvoj-db-server/`](./05-vyvoj-db-server/README.md): Materiály k uloženým procedurám, triggerům v PostgreSQL.
* [`06-sprava-db/`](./06-sprava-databaze/): Materiály k administraci databází.
* [`07-nosql-newsql/`](https://github.com/TomasRacil/analyza-IS-NoSQL): Materiály k NoSQL a NewSQL databázím.

*(Struktura se může v průběhu semestru mírně upravovat)*

## Jak začít?

1.  Projděte si informace v adresáři [`01-uvodni-hodina/`](./01-uvodni-hodina/README.md).
2.  Osvěžte si znalosti Gitu a Dockeru v sekci [`00-predpoklady/`](./00-predpoklady/README.md). Ujistěte se, že máte Docker a Docker Compose nainstalované a funkční.
3.  Postupujte podle materiálů v jednotlivých číslovaných adresářích dle aktuálního harmonogramu výuky.
4.  Pro praktické ukázky v jednotlivých sekcích (např. SQL, motivační příklad) naleznete specifické `docker-compose.yml` soubory a instrukce ke spuštění v příslušných `README.md` souborech dané sekce.

## Používané nástroje (shrnutí)

* **Verzování:** Git
* **Kontejnerizace:** Docker, Docker Compose
* **Databáze:** PostgreSQL
* **Správa DB:** pgAdmin 4, SQLTools (VS Code), DBeaver, psql
* **Backend:** Python (Flask/FastAPI)
* **Frontend:** React, HTML, CSS, JavaScript
* **IDE/Editor:** Doporučeno VS Code, PyCharm, WebStorm, nebo dle vaší preference.

## Dotazy a problémy

Pokud narazíte na problém s materiály nebo budete mít dotaz, využijte prosím kontakt emailem. Pokud máte návrh na vylepšení nebo opravu materiálů, budu rád, pokud navrhnete změnu přímo v tomto repozitáři formou Pull Requestu.
