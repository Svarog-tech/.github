
# GitHub manuál

## Zakládání repozitáře [1]

Pro založení repozitáře se obraťte na `@ulaviceditestalozplnahrdlakricel`.

Po založení repozitáře je potřeba provést následující kroky:
- vytvořit `.gitignore` [1.1]
- vytvořit `.env` a `.env.example`
- vytvořit `README.md` [3]
- nastavit branche [2]

---

## `.gitignore` [1.1]

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

## README [3]

Soubor `README.md` slouží jako základní dokumentace projektu. Každý repozitář by měl obsahovat stručný, přehledný a aktuální popis projektu, aby i nový člověk v týmu rychle pochopil, co projekt dělá, jak ho spustit a co je k tomu potřeba.

### Co má README obsahovat
**1. Název projektu**

Uveď stručný a jasný název projektu.

**2. Popis projektu**

Krátce popiš:

co projekt dělá,
pro koho je určen,
jaký je jeho účel.

Například:
Projekt je moderní e-shop s modrým vizuálním stylem, jehož cílem je nabídnout přehledné a moderní prostředí pro prodej produktů.

#### DEV STACK [3.1]

Uveď použité technologie.

**Například:**

Backend: Django
Frontend: Tailwind CSS
Databáze: SQLite / PostgreSQL
Další technologie: JavaScript, Docker, GitHub Actions

#### Požadavky zadavatele [3.2]

Stručně vypiš hlavní požadavky na projekt.

**Například:**

e-shop,
modrý web,
moderní vzhled,
přehledné uživatelské rozhraní,
responzivní design.

#### Jaké jsou požadavky [3.3]

Uveď, co je potřeba mít nainstalované.

**Například:**

Python 3.x
pip
Git
Node.js, pokud je potřeba pro frontend
databáze, pokud projekt nepoužívá SQLite

#### Jak nastavit .env [3.4]

Je potřeba popsat práci s .env souborem.

Pravidla:

**.env nikdy necommitujeme do repozitáře**,
**.env.example musí obsahovat všechny potřebné proměnné bez citlivých údajů**,
pokud přidáš novou proměnnou do .env, musíš ji přidat i do .env.example.

**Například**:

zkopírovat .env.example do .env,
doplnit potřebné hodnoty podle lokálního prostředí.

#### Jak projekt spustit lokálně [3.5]

Popiš základní postup spuštění projektu na lokálním zařízení.

**Například:**

Naklonovat repozitář
Přesunout se do složky projektu
Nainstalovat závislosti
Nastavit .env
Spustit migrace
Spustit vývojový server

#### Základní příkazy [3.6]

Uveď nejdůležitější příkazy pro práci s projektem.

**Například:**

spuštění serveru,
migrace databáze,
vytvoření administrátora,
instalace závislostí.

#### Kontakt / odpovědná osoba [3.7]

Uveď, na koho se obrátit v případě dotazů.

**Například:**

projektový vedoucí: @jmeno
správce repozitáře: @jmeno
kontakt: email@example.com

#### Doporučení

README by mělo být:

stručné,
přehledné,
aktuální,
srozumitelné i pro člověka, který projekt vidí poprvé.

#### Důležité

README není jen formalita. Je to první místo, kam se člověk podívá, když s projektem začíná. Proto musí obsahovat všechny základní informace potřebné pro orientaci a spuštění projektu.

*
