
# GitHub manuál

## Zakládání repozitáře [1]

Pro založení repozitáře se obraťte na `@ulaviceditestalozplnahrdlakricel`.

Po založení repozitáře je potřeba provést následující kroky:
- vytvořit `.gitignore` [1.1]
- vytvořit `.env` a `.env.example`
- vytvořit `README.md` [3]
- nastavit branche [2]
- POKUD DELAS S PYTHONEM AT JE TAM REQUIREMENTS.TXT (https://boscacci.medium.com/why-and-how-to-make-a-requirements-txt-f329c685181e)
---

## `.gitignore` [1.1]
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
Dokumentace: https://git-scm.com/docs/gitignore

Do souboru `.gitignore` patří:
- cache soubory, např. `__pycache__`
- `.env`
- vše, co není nutné pro fungování projektu
- vše, co obsahuje citlivá data
- dočasné soubory editorů a IDE
- build a generované soubory, pokud nejsou potřeba verzovat

### Důležité
Do repozitáře nikdy nepatří:
- hesla
- API klíče
- tokeny
- přístupové údaje
- privátní konfigurační soubory

---

## branche [2]

### struktura branchů [2.1]

```
master
│
├── development
├── release/version-x.x   (volitelné)
└── hotfix
```

### master [2.1.1]
**obsahuje pouze stabilní, produkční kód připravený k nasazení**
**MUSI TO FUNGOVAT NA 100% NEZ TO MUZE DO MASTERU!!!**

je nastavena branch protekce na branch `master`<br>


#### co to znamená:
- nelze přímo pushovat do masteru
- lze mergovat pouze skrze pull request<br>
aby toto fungovalo musi se hlavní branch jmenovat `master`<br>
Pozor když vytvoříte repozitář skrze GitHub defaultně se bude jmenovat `main`  <br>
JE POTŘEBA HO PŘEJMENOVAT!!!!!! <br>

###  development [2.1.2]
**hlavní vývojová větev, kde se integrují nové funkce před vydáním**
**TOHLE JE TO KDE PRACUJETE**
- hlavní vývojová větev, kde se spojují všechny nové funkce
- slouží jako „pracovní verze“ projektu před vydáním
- po dokončení většího celku se merguje do masteru

### release/version-x.x [2.1.3]

Volitelná branch používaná při přípravě konkrétní verze vydání.

Použití:

finalizace verze před nasazením
poslední testování
drobné opravy před mergem do master

### hotfix [2.1.4]

Branch určená pro rychlé opravy kritických chyb v produkci.

Použití:

oprava závažných chyb
řešení problémů, které je potřeba nasadit okamžitě

### Pojmenování branchů [2.2]

Aby každý zakládal branche stejně.

Doporučený formát:

* feature/nazev-funkce
* fix/nazev-opravy
* hotfix/kriticka-oprava
* release/version-x.x

Příklady:

* feature/prihlaseni-uzivatele
* feature/kosik
* fix/oprava-validace
* hotfix/chyba-platby
* release/version-1.2

Pravidla:

* nepoužívat mezery
* nepoužívat diakritiku
* názvy psát stručně a výstižně
* branch musí být z názvu jasně rozpoznatelná

# Workflow práce [3]
Každá nová funkce nebo oprava by měla probíhat podle tohoto postupu:

1. stáhnout aktuální změny z development
2. vytvořit novou branch
3. udělat požadované změny
4. změny commitnout
5. branch pushnout na GitHub
6. otevřít Pull Request
7. počkat na review
8. po schválení provést merge

**Doporučený postup**

* nezačínej pracovat na staré branchi bez aktualizace
* nepracuj přímo v master
* běžnou práci dělej přes feature/* nebo fix/*

## Pull Request pravidla [3.1]

Každý merge do důležité branche musí probíhat přes Pull Request.

**Pull Request musí:**

* mít srozumitelný a stručný název
* obsahovat popis změn
* být zaměřený ideálně na jednu konkrétní věc
* být otevřený proti správné branchi

**Doporučení**

* nedělat zbytečně velké Pull Requesty
* velké změny rozdělit do menších částí
* do popisu uvést, co bylo změněno a proč
* pokud je potřeba, přidat screenshot nebo doplňující poznámku

### Commit message [3.2]

Commit message musí stručně a jasně popisovat, co bylo změněno.

**Doporučený formát**

* feat: přidání nové funkce
* fix: oprava chyby
* docs: úprava dokumentace
* refactor: úprava struktury kódu
* style: formátování nebo drobná vizuální úprava
* test: doplnění nebo úprava 

**Příklady**
* feat: přidání registrace uživatele
* fix: oprava validace formuláře
* docs: doplnění README
* refactor: úprava struktury views

**Nevhodné commit message**

* update
* oprava
* hotovo
* změny
* aaa

Commit message musí být užitečná i zpětně, když se někdo dívá do historie projektu.

## Kam se co merguje [3.3]

Pro přehlednost je potřeba dodržovat tento tok změn:

* `feature/*` → merge do `development`
* `fix/*` → merge do `development`
* `release/version-x.x` → merge do `master`
* `hotfix/*` → merge do `master` a následně i do development
* `development` → merge do `master` až po otestování

**Důležité**

* běžná práce nejde přímo do master
* master obsahuje pouze stabilní verzi
* development slouží jako hlavní pracovní větev

### Kontrola před pushnutím [3.3.1]

**Před pushnutím změn vždy zkontroluj:**

* projekt se spustí bez chyby
* změna funguje podle očekávání
* nic se nerozbilo
* nejsou v commitu citlivá data
* `.env` není součástí commitu
* `.env.example` je aktuální
* commit message dává smysl
* měníš správnou branch

Tento krok nepřeskakuj. Ušetří to čas tobě i ostatním.

## Code review [3.4]

Code review je povinná součást procesu před mergem.
REVIEW JE AUTOMOATIZOVANA PROVADI SE AUTOMATICKY KAZDYCH 5 MINUT!!!!!

**Reviewer kontroluje hlavně:**
* funkčnost
* čitelnost kódu
* bezpečnost
* logiku řešení
* zda změna neporušuje existující části projektu

**Důležité**
* bez schválení se nemerguje
* review není útok, ale kontrola kvality
* připomínky je potřeba brát věcně

---

# README [4]

Soubor `README.md` slouží jako základní dokumentace projektu. Každý repozitář by měl obsahovat stručný, přehledný a aktuální popis projektu, aby i nový člověk v týmu rychle pochopil, co projekt dělá, jak ho spustit a co je k tomu potřeba.

## Co má README obsahovat [4.1]

**1. Název projektu**

Uveď stručný a jasný název projektu.

**2. Popis projektu**

Krátce popiš:

co projekt dělá,
pro koho je určen,
jaký je jeho účel.

Například:
Projekt je moderní e-shop s modrým vizuálním stylem, jehož cílem je nabídnout přehledné a moderní prostředí pro prodej produktů.

#### DEV STACK [4.1.1]

Uveď použité technologie.

**Například:**

* Backend: Django
* Frontend: Tailwind CSS
* Databáze: SQLite / PostgreSQL
* Další technologie: JavaScript, Docker, GitHub Actions

#### Požadavky zadavatele [4.1.2]

Stručně vypiš hlavní požadavky na projekt.

**Například:**

* e-shop,
* modrý web,
* moderní vzhled,
* přehledné uživatelské rozhraní,
* responzivní design.

#### Jaké jsou požadavky [4.1.3]

Uveď, co je potřeba mít nainstalované.

**Například:**

* Python 3.x
* pip
* Git
* Node.js, pokud je potřeba pro frontend
* databáze, pokud projekt nepoužívá SQLite

#### Jak nastavit `.env` [4.1.4]
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
**.ENV PATRI DO GITIGNORU'!!!!!!!!**
Je potřeba popsat práci s `.env` souborem.

Pravidla:

**`.env` nikdy necommitujeme do repozitáře**,
**`.env.example` musí obsahovat všechny potřebné proměnné bez citlivých údajů**,
pokud přidáš novou proměnnou do `.env`, musíš ji přidat i do `.env.example`.

**Například**:

zkopírovat .env.example do .env,
doplnit potřebné hodnoty podle lokálního prostředí.

#### Jak projekt spustit lokálně [4.1.5]

Popiš základní postup spuštění projektu na lokálním zařízení.

**Například:**

Naklonovat repozitář
Přesunout se do složky projektu
Nainstalovat závislosti
Nastavit `.env`
Spustit migrace
Spustit vývojový server

#### Základní příkazy [4.1.6]

Uveď nejdůležitější příkazy pro práci s projektem.

**Například:**

spuštění serveru,
migrace databáze,
vytvoření administrátora,
instalace závislostí.

#### Kontakt / odpovědná osoba [4.1.7]

Uveď, na koho se obrátit v případě dotazů.

**Například:**

DEJ TAM SVOJE DISCORD JMENO

#### Doporučení
I KDYZ TO DELA AI PRECTI TO PO NEM AT SE V TOM VYZNA CLOVEK A AT TO SPLNUJE VSECHNY BODY KDO TAK NEUCINI NEDOSTANE DAREK OD JEZISKA
README by mělo být:

stručné,
přehledné,
aktuální,
srozumitelné i pro člověka, který projekt vidí poprvé.

#### Důležité

README není jen formalita. Je to první místo, kam se člověk podívá, když s projektem začíná. Proto musí obsahovat všechny základní informace potřebné pro orientaci a spuštění projektu. !!!

---

## První spuštění projektu [5]

Tato sekce slouží hlavně pro nováčky, kteří projekt spouští poprvé.

**Doporučený postup**
1. naklonovat repozitář
2. přepnout se na `development`
3. vytvořit `.env` podle `.env.example`
4. nainstalovat všechny závislosti
5. spustit databázové migrace
6. spustit projekt lokálně
7. ověřit, že vše funguje

**Cíl**

Než začneš programovat, musíš mít jistotu, že:

* projekt funguje lokálně
* máš správně nastavené prostředí
* rozumíš základní struktuře projektu

---

## Co dělat a nedělat [6]

**Dělat**

* pracovat přes vlastní branch
* pravidelně stahovat aktuální změny
* psát srozumitelné commit messages
* otevírat Pull Requesty s popisem
* reagovat na review
* udržovat README a `.env.example` aktuální

**Nedělat**

* nepushovat přímo do `master`
* necommitovat `.env` !!!
* necommitovat hesla, tokeny nebo API klíče
* nedělat obří Pull Requesty bez důvodu
* neobcházet code review
* nezačínat práci bez aktualizace branche
* nevytvářet nejasně pojmenované branche a commity

**Důležité**

Cílem těchto pravidel není zbytečně komplikovat práci, ale udržet repozitář přehledný, bezpečný a snadno pochopitelný pro celý týmprojektový vedoucí: `@jmeno`
správce repozitáře: `@jmeno`
kontakt: `email@example.com`
‘‘‘
EPGmooky, KrAsync
‘‘‘
