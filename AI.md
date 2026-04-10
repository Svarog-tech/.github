# AI MANUÁL

## AI není náhrada za programátora
AI tě nenahradí. Je to zesilovač tvých schopností.
Pokud máš dobré návyky, výrazně ti zrychlí práci. Pokud máš špatné návyky, jen je znásobí.

## Logiku musí řídit člověk

AI tě nenahradí. Je to zesilovač tvých schopností.
Pokud máš dobré návyky, výrazně ti zrychlí práci. Pokud máš špatné návyky, jen je znásobí.

## AI funguje lépe u menších úkolů

Čím větší a obecnější zadání, tím větší šance na chyby.
Proto úkoly rozděluj na malé, konkrétní a snadno ověřitelné části.

## Kvalita výstupu závisí na kvalitě promptu

Co AI nenapíšeš, to často neudělá správně.
Nejasné nebo moc obecné zadání vede ke slabému výsledku.

## Jak AI správně úkolovat

1. Zadávej malé a testovatelné úkoly.
2. Buď konkrétní.
3. Řekni i to, co AI dělat nemá.
4. Vždy chtěj kontrolu a ověření výstupu.

**S příchodem AI nejsou základy vývoje méně důležité. Naopak. Architektura, čitelnost, testování, bezpečnost, dokumentace a audit výstupu jsou dnes důležitější než dřív.**
**AI ti může ušetřit čas, ale odpovědnost za kvalitu je pořád na tobě!!!!!!**

## Vždy dělej audit

Nikdy neber výstup AI jako automaticky správný.
I dobrý kód může obsahovat chyby, bezpečnostní problémy nebo špatnou logiku. Audit je povinná součást práce.


## Doporučené skills.sh 
https://skills.sh/

Co je skills.sh?

skills.sh je otevřený ekosystém pro tzv. AI skills — tedy znovupoužitelné schopnosti pro AI agenty.
Můžeš si je představit jako pluginy, rozšíření nebo hotové workflow, které AI dávají lepší postupy, pravidla, specializované know-how a strukturu pro konkrétní úkoly. Místo obecného odpovídání tak AI pracuje podle ověřeného postupu pro audit, SEO, UI/UX, testování, security nebo brainstorming.

Proč to používat

Bez skills AI často:

* moc domýšlí
* přeskakuje důležité kroky
* jde rovnou do kódu bez návrhu
* dělá slabší audit nebo příliš obecné výstupy

Se správným skillem dostane AI lepší rámec práce. To znamená lepší výstup, méně chaosu a větší šanci, že bude postupovat rozumně a systematicky.

**Jak to funguje**

Skills se instalují přes skills CLI, typicky jedním příkazem jako:
npx skills add owner/skill-name

CLI slouží k instalaci a správě skillů pro AI agenty. Některé skills fungují napříč populárními coding agenty jako Claude Code, Cursor nebo Windsurf, ale vždy je dobré zkontrolovat kompatibilitu konkrétního skillu.

**Jak o skills přemýšlet v praxi**

Neber je jako magii navíc.
Ber je jako předpřipravené expert workflow, které AI nutí postupovat kvalitněji. Jeden skill může řešit audit webu, jiný SEO, další UI/UX návrh a jiný třeba brainstorming před samotným kódováním.

**Tyhle jsou fakt OP**

1. audit-website
https://skills.sh/squirrelscan/skills/audit-website
Tohle je za mě jeden z nejsilnějších skillů vůbec, pokud chceš reálný audit webu. Umí audit přes 230+ pravidel ve 21 kategoriích, řeší SEO, technické chyby, výkon, bezpečnost, accessibility, mobilní použitelnost, structured data a další oblasti. Navíc má režimy quick / surface / full a umí i porovnávat regrese mezi skeny. Jediný háček je, že vyžaduje lokálně nainstalovaný squirrel CLI.

2. ui-ux-pro-max
https://skills.sh/nextlevelbuilder/ui-ux-pro-max-skill/ui-ux-pro-max
Tohle je extrémně silné pro frontend, landing pages, dashboardy a obecně vizuální kvalitu. Má pokrytí pro 10 stacků, obsahuje 50+ stylů, 161 barevných palet, 57 font pairingů, 99 UX pravidel a guideliney pro accessibility, touch interaction, performance i responsive layout. Na UI review, redesign a návrh komponent je to velmi silný skill.

3. seo-audit
https://skills.sh/coreyhaines31/marketingskills/seo-audit
Na čistě SEO věci je to mnohem lepší než generické „zkontroluj SEO“. Má jasný framework: crawlability, indexace, technické základy, on-page optimalizace, kvalita obsahu a autorita, plus guidance podle typu webu jako SaaS, e-commerce nebo content web. Líbí se mi i to, že výslovně upozorňuje na omezení statické kontroly schema markup a doporučuje validaci přes browser/rendered testy.

4. brainstorming
https://skills.sh/obra/superpowers/brainstorming
Tohle není audit skill, ale je brutálně užitečný pro to, aby AI nezačala bezhlavě kódovat. Vynucuje proces: nejdřív kontext, pak otázky, návrh přístupů, design, spec a až potom implementace. Dokonce má „hard gate“, že se nemá jít do kódu bez prezentace návrhu a schválení. Na větší feature nebo nový web je to přesně ten typ skillu, který zlepší kvalitu zadání.

**Další skills.sh**

1. vercel-labs/react-best-practices
   Must-have, pokud děláš React nebo Next. Pomáhá s výkonem, bundle size, re-rendery, data fetchingem a architekturou komponent.
2. vercel-labs/web-design-guidelines
   Skvělé na UI audit. Řeší accessibility, UX, formuláře, obrázky, performance, dark mode, interakce a další web best practices. Na frontend manuál téměř povinnost.
3. vercel-labs/next-best-practices
   Pokud jedeš Next.js, tohle bych přidal hned. Je vedené jako oficiální Vercel skill na doporučené Next patterns.
4. openai/security-best-practices
   Na review bezpečnostních průserů v kódu. Hodí se jako základní security vrstva při každém větším tasku nebo auditu.
5. trailofbits/static-analysis
   Velmi dobrý skill na hlubší technický audit, protože cílí na statickou analýzu s CodeQL, Semgrep a SARIF. To už je víc „seriózní audit“ než jen povrchní review.
6. trailofbits/testing-handbook-skills
   Výborné, pokud chceš AI tlačit do testování, fuzzingu, sanitizerů a ověřování edge cases. Přesně pasuje k tomu, co píšeš v manuálu o malých taskách a verifikaci.
7. getsentry/code-review a getsentry/find-bugs
   Praktické skills na průběžné code review a hledání bugů. Dobré jako „každodenní pracovní dvojice“.
8. openai/playwright-interactive
   Super pro UI debug, testování chování webu a ověřování, že věci opravdu fungují v browseru, ne jen „vypadají správně v kódu“.
9. openai/frontend-skill
   Když chceš, aby AI nedělala generický hnusný layout, ale uměla stavět vizuálně silnější landing pages a rozumné UI.
10.cloudflare/web-perf
   Hodně dobré, pokud chceš audit výkonu webu a Core Web Vitals. Pro SEO/performance workflow velmi užitečné.

**Když to seřadím**

Pro weby a reálnou práci bych to teď seřadil takhle:

* audit-website
* ui-ux-pro-max
* seo-audit
* brainstorming

**Když stavíš nový web**

Použil bych:

* brainstorming
* ui-ux-pro-max

Nejdřív si vynutíš správný návrh a pak řešíš kvalitu UI/UX.

**Když chceš zlepšit hotový web**

Použil bych:

* audit-website
* seo-audit
* ui-ux-pro-max

Tohle je velmi silná kombinace, protože jeden skill řeší široký health check, druhý jde víc do SEO hloubky a třetí dorovná UX a vizuální kvalitu.

**Když chceš workflow pro tým**

Použil bych:

brainstorming jako povinný začátek
audit-website jako povinný konec



## Detailní promty: 
**Ukázka promptu pro základ webu:**

Vytvoř základ moderního responzivního webu pro [typ projektu].

Technologie:
- HTML, CSS, JavaScript
- bez backendu
- čistý a přehledný kód
- rozděl strukturu logicky

Požadavky:
- vytvoř úvodní hero sekci
- navigaci
- sekci služby / features
- referenční sekci
- kontaktní sekci
- footer
- web musí být responzivní pro desktop i mobil

Design:
- moderní, čistý, profesionální
- dostatek mezer
- důraz na čitelnost
- používej srozumitelné názvy tříd

Důležité:
- nevymýšlej zbytečné funkce navíc
- nepoužívej knihovny ani frameworky
- kód piš tak, aby se dal snadno rozšířit
- ke každé části stručně napiš, co dělá

Nakonec:
- zkontroluj HTML strukturu
- ověř responzivitu
- napiš, na co si dát pozor při dalším rozšiřování

**Přiklad pro menší task:**

Uprav pouze navigační lištu na mém webu.

Cíl:
- navbar má být horizontálně vycentrovaný
- logo vlevo
- tlačítko Přihlášení vpravo
- menu musí fungovat i na mobilu

Omezení:
- neupravuj ostatní sekce webu
- neměň barvy mimo navbar
- nepřepisuj celý projekt, uprav jen potřebné části

Výstup:
- pošli pouze relevantní HTML a CSS úpravy
- vysvětli, co jsi změnil
- zkontroluj, že se layout nerozbíjí na menších obrazovkách

Prompt pro audit kódu, security, SEO a kvality

**Univerzální audit prompt:**

**Proveď důkladný audit tohoto projektu.**

Zaměř se na:
1. Kvalitu kódu
- čitelnost
- duplicity
- špatná struktura
- zbytečně složitý kód
- porušení best practices
- možnosti refaktoringu

2. Security
- potenciální XSS
- špatná validace vstupů
- nebezpečné zacházení s daty
- citlivé informace v kódu
- špatně řešená autentizace nebo autorizace
- riziková místa v API voláních

3. SEO
- struktura headingů
- title a meta description
- sémantické HTML
- alt atributy u obrázků
- interní struktura obsahu
- indexovatelnost
- technické SEO problémy

4. Performance
- zbytečné rendery
- příliš velké assety
- neefektivní načítání
- problémy s lazy loadingem
- špatná optimalizace frontendu

5. UX / frontend kvalita
- responzivita
- přístupnost
- konzistence komponent
- čitelnost
- problematická místa pro uživatele

Chci výstup v tomto formátu:
- Kategorie
- Problém
- Proč je to problém
- Dopad
- Návrh opravy
- Priorita: nízká / střední / vysoká

Důležité:
- nevypisuj obecné fráze bez konkrétního důvodu
- buď konkrétní a technický
- pokud je něco v pořádku, napiš to
- pokud si nejsi jistý, uveď to
- na konci udělej stručné shrnutí nejkritičtějších problémů

Nakonec:
- vytvoř seznam top 5 nejdůležitějších oprav
- navrhni pořadí, v jakém je řešit


**Jestli chceš audit spíš pro web jako celek:**

Udělej kompletní audit webu z pohledu kódu, bezpečnosti, SEO, výkonu a UX.

Chci, abys zkontroloval:
- strukturu HTML
- kvalitu CSS
- čistotu JavaScriptu
- responzivitu
- přístupnost
- SEO základy
- technické SEO chyby
- performance problémy
- bezpečnostní rizika
- nekonzistentní nebo slabá místa v UI

Postup:
- nejdřív stručně popiš celkový stav
- potom rozděl problémy do kategorií
- u každého problému napiš konkrétní návrh opravy
- označ kritické chyby
- upozorni na části, kterým nelze plně věřit bez ruční kontroly

Na konci dej:
- top 10 problémů
- quick wins, které jdou opravit hned
- věci, které jsou rizikové do budoucna
