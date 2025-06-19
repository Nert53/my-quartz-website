---
aliases:
  - softwarové inženýrství
---
# Softwarový proces
- aktivity nutné k dokončení softwarového produktu
1) specifikace - jak to má vypadat?
	- zjistit - definovat - shodnout se na řešení
	- omezení vývoje (peníze, aktuální podmínky atd.)
	- **nejdůležitější část** (když to zkazím hned tady, tak se to potáhne všude dál)
	- nutné znát i problematiku zakázky
	- výstupem je formální definice = **dokument specifikace požadavků** (DSP)
	- studie proveditelnosti ->  zjištění a analýza požadavků -> soupis požadavků -> kontrola co jsme udělali
1) návrh + vývoj - ta technická část
2) validace - ověření, toho co se udělalo
3) evoluce - uprávy při tom, co sw už běží
# 1) Systémové inženýrství
- proč se tím vůbec zaobírat?
	- vývoj sw se děje opakovaně, je nutné to nějak zorganizovat (nejde o malou věc)
	- je to abstraktní => těžko uchopitelné pro člověka
- velký projekt = vysoká režie
- zpoždění znamnená vyšší náklady
- standardizuje postupy
- **software**
	- balík programu, dokumentace a konfigurační soubory (nutné pro bezproblémový běh)
1) **generický produkt** - výrobce vyvine a umístí na trh (např. OS, kancelářské balíky, photoshop)
2) **SW na míru** - zákazník se podílí i na specifikaci/vývoji (např. CMS, e-shop)
3) **obecné řešení přizpůsobené zákaníkovi** - ošetří se podoba jedné konkrétní instance
- **inženýrství** ... aplikace teorie v praxi
	- obsahuje prověřené metody pro splnění
	- různé podmínky pro splnění
- **softwarové inženýrství** ... aplikace metod na složky vývoje SW
	- specifikace, vývoj, testování, managment, údržba, interakce s ostním SW, ...
- informatika je teoretická, zatímco sw inženýrství řeší praxi (při vývoji SW)
- musíme mít mezioborovou znalost
- je to o nějakám kompromisu (může nás limitovat čas, prostředky)
- výhodou je umění komunikace se zákazníkem
# 2) Softwarový proces a jeho modely
- aktivity nutné k dokončení SW produkty
- složen ze 4 částí
	1) specifikace
	2) vývoj
	3) validace
	4) evoluce
	- různé projekty = různý důraz na každý krok
- architektura aplikací je srovnatelná jako architektura hmatatelných věcí (budova, auto)
1) **vodopádový model** - části se uzavřou a už se do nich nevracíme
2) **evoluční model** - fáze se překrývají, rychle prototyp, možná reimplementace
3) **formální transformace** - vychází z matematické specifikace, spíše se nepoužívá
4) **znovupoužitelní existujích komponent** - upravení zakoupeného softwaru, složení z již hotových komponent
5) **iterativní modely/spirálový** - každá aktivita několikrát
6) **agilní** - vodopád ve smyččce, každá část velmi krátce
7) **extrémní programování** - malé týmy a malé částí, rapidně rychle dodávají komponenty
8) **SCRUM**
- nejlepší se nedá určit => možná kombinace
#### Časové plány
- vývoj : údržba = 1 : 4
- **pareto principal** ... 80 % vývoje zabere 20 % času, zbylých 20 % pak 80 % času
#### Dobrý software
- nestačí, že dělá to co má nějak
- musí to dělat dobře
	- bezpečnost
	- efektivita
	- udržitelnost
	- znovupoužitelnost
	- spolehlivost

- dobrý programátor != dobrý SW inženýr
- nutná je pro ně znalost oboru, kde SW poběží
- **systém** ... kolekce komponent spolupracujících k dosažení cíle
- **systémové inženýrství** ... specifikace, design, implementace, ověřování, nasazování a údržba sociálně technických systémů
- častý problém - omezený rozpočet
# 3) UML a UML diagramy
- unified modeling language
	- standardizovaný jazyk pro modelování systémů
- k vizualizaci
- je intuitivní na čtení
- psaní je o něco náročnější (stanovená "gramatika")
- přesný model => usnadní nám konstrukci
	- případně naopak
	- pomůcky v IDE
- vyskytuje se v dokumentaci
#### Strukturální prvky (klasifikátory)
- podstatná jména (koncepty či fyzické věci)
1) **třída** - jako v OOP
2) **rozhraní** - taky jako v OOP
3) **spolupráce** - interakce mezi elementy
4) **případ užití** - akce co systém umožňuje
5) **komponenty** - součást systému skrývající funkcionalitu za rozhraní
6) **artefakty** - části s fyzickou informací (soubor, knihovna, ...)
![[Pasted image 20231221145625.png]]
#### Chování v UML
- dynamické části jazyka (slovesa popisující chování)
- propojuje strukturální prvky
1) **interakce** - šipka
2) **stavový stroj** - stav objektu, kterými může za život projít
3) **aktivita** - sekvence akcí, které systém provádí

- seskupení objektů možné do balíčků (čistě pro organizaci, nikoliv implementaci)
#### Vztahy
1) **závislosti** - sémantické vztahy
2) **asociace** - strukturální vztahy, popis vazby (1:N)
3) **agregace** - "has a"
4) **generalizace** - popis dědičnosti
5) **generalizace** - jeden vyžaduje, druhý zaručuje (funkcionalitu)
- n-ární vztahy (mezi vícero objekty)
![[Pasted image 20231221150316.png]]
#### Diagramy
- vizualizace z různých úhlů pohledu
	- jasné definice = **13 diagramů**
	- každý jiná část problematiky
	- při dodržení pravidel možno "vytvářet nové"
1) **class diagram**
2) **component diagram** - zapouzdřené třídy + jejich rozhraní
3) **object diagram** - objekty ze tříd v konkrétním čase (před/po interakci)
4) **artefact diagram** - vnitřní fyzická stránka systému (knihovny, soubory)
5) **diagram nasazení** - fyzická implementace, custom objekty (server, počítače, ...)
6) **diagram případů užití** - aktéři + co používají
7) **sekvenční diagram** - spolupráce objektů v čase
8) **komunikační diagram** - struktura objektů při zasílání zpráv (není časová osa => číslování)
9) **stavový diagram**  - změna stavu objektu při událostech
10) **diagram aktivit** - složitější případy užití (větvení atd.)
# 4) Specifikace požadavků a proces zjišťování
- zákazník musí přesně specifikovat cíle a vlastnosti celého systému
1) **Abstraktní popis funkčních požadavků**
	- základní funkce na abstraktní úrovni
	- např. telefon umožní uskutečnit hovor a poslat SMS
2) **Definice vlastností systému**
	- nefunkcionální emergnetní vlastnosti
	- jak má být bezpečný a spolehlivý
	- v každém subsytému
	- např. telefon vydrží 100 hodin v pohotovostním režimu
3) **Jak se systém nemá chovat**
	- občas nůže být vhodnější říct, co NEMÁ dělat
- jaká jsou fáze?
	1) rozdělení požadavků do skupin
	2) identifikace subsystémů
	3) přiřezení požadavek - subsytém
	4) specifikace funkcionality subsystémů
	5) definice rozhraní mezi subsystémy
	- fáze se ovlivňují navzájem (i zpětně) => možný i spirálový vývoj
#### Modelování systémlů
- abstraktní záležitost (v různé míře)
- **blokový diagram komponent**
	![[Pasted image 20231216113244.png]]
	- může být další i pro každý subsystém
- vhodné doplnit tabulkou
- ![[Pasted image 20231218163346.png]]
#### Studie providitelnosti
- levná, krátká
- výstupem je zpráva, která nám odpoví jestli se do toho vůbec máme pustit, případně co změnit aby to šlo
- zdroje: manažeři uživatelů, SW inženýři, technologičtí experti, koncoví uživatelé
- co má systém řešit? co by se dělalo pokud by nebyl implementován? můžeme použít info odjinud? musíme nasadit novou technologii?
#### Zjišťování požadavků
- zjistit požadavky a analyzovat je
- co nejvíce informací k fomrulaci uživatelských a systémových požadavků
- mnoho zúčastněných => problémy v porozumění
	- neví co chtějí
	- nejsou realistické
	- možné spory
	- různé pojmy
1) **objevování požadavků** - interakce s účastníky (nesmíme na nikoho zapomenout)
2) **klasifikace a organizace** - setřídení nasbíraných informací
3) **prioritizace a vyjednávání** - řešení sporů, co má přednost
4) **dokumentace** - bude sloužit jako podklad pro další fázi
- fáze možno opakovat, kvůli zpětné vazbě
- rozhovory
	- uzavřené vs otevřené otázky
	- získání vhledu do problematiky
	- pozor na moc nápadů
	- občas těžko porovant papír vs realita
	- vhodné demonstrovat na prototypu
	- použití konkrétních scénářů (pozor i na to co se může pokazit)
#### Validace požadavků
- běheme procesu
- oprávněnost, konzistence, úplnost, realizovatelnost, ověřitelnost
- revize od týmu nebo externího uživatele, prototyp produktu, testovací případy
#### Správa požadavků
- požadavky se v průběhu budou měnit
- koncepční vs konkrétní
- nutné udržovat historii verzí požadavků
- nutné je mít navzájem provázané
- verzovací systémy + jak evidovat změny
#### Proces změny požadavků
- změna by neměla proběhnout jen tak
- co je za problém, zda je validní, jak konkrétně změnit
- co jde ruku v ruce se změnou (cena, implementace, časová náročnost)
- rozchod DSP a reality při urgentní změna (může vést k lavinovému efektu)
# 5) Požadavky na SW (funkční, nefunkcionální, doménové, uživatelské, systémové)
- nutné služby popsat
- zjišťování, analýza, dokumentování ověření
- requirements engineering
- mohou být různé pohledy, různě abstraktní a celkově od různých pozic
- u těch požadavků zkusit uvést příklad (na slajdech LIBSYS)
1) **uživatelské požadavky**
	- v přirozeném jazyce + diagramy
	- co bude systém poskytovat
	- uživatel nepotřebuje technické znalosti, aby jim porozuměl
	- jednoduchost = cesta
	- přiřozený jazyk není dostatečně konkrétní => odprostit se od technických detailů
	- zdůvodnění, zdroj požadavku, míra nutnosti implementace
2) **systémové požadavky**
	- detailní popis funkcí systému
	- to co musíme implementovat
	- pro SW inženýry
	- běžně součástí smlouvy
	- přirozený jazyk, kterému dáme mantinely
	- funkce, vstup, výstup, závislosti, akce, vstupní a výstupní podmínky, vedlejší efekty
	- doplnění obrázkem, sekvenčním diagramem
1) **funkční požadavky**
	- co by měl systém poskytovat, případně co by NEMĚL dělat
	- reakce na vstupy
	- **uplná, konzistentní** (bývá problém, vznikají spory)
2) **nefunkcionuální požadavky**
	- požadavky na systém jako celek
	- běžně vágní formulace, což se dá těžko v praxi ověřit
	- zavést exaktní měřitelné věci (rychlost, paměť, velikost, spolehlivost, robustnost, snadnost, bezpečnost)
	1) na produkt - výkon, paměťová náročnost, spolehlivost
	2) organizační - co použít a jak (jazyk, dokumentace, standardy)
	3) externí - to co může interagovat s něčím na venek
3) **doménové požadavky**
	- přímo pro aplikační doménu (musím ji rozumět)
	- funkční i nefunkcionální
- nutné specifikovat rozhraní
- co nejdříve a přesně
- DSP ... dokument specifikace požadavků
#### DSP (dokument specifikace požadavků)
- oficiální dokument
- můžeme použít techničtějši detaily
- formát závislý na modelu SW procesu
- u měnších projektů ani neexistuje
- může být i velmi dlouhý
- velké společnosti vlastní standardy
# 6) Architektura SW a proces jejího návrhu
- rozdělení aplikace
	- subsystémy
	- hlavní komponenty
- spojuje požadavky a implementaci
- důsledná dokumentace => lepší systémová analýza, možnosti znovupoužití, poskytne "návod" pro implementaci
- ovlivní všechny aspekty systému
- architekturu vybíráme podle toho, co se dělá (měla by usnadit problémy, co mohou nastat)
#### Návrh shora dolů
- od abstraktních struktur ke konkrétním
- vhodné pokud dobře známe doménu
- oblíbené v korporátech (enterprise)
- **výhody**
	- systematické dělení funcionality
	- snadnější údržba (pro velké projekty)
	- delegování části práce na někoho jiného
- **nevýhody**
	- předesignování
	- neodhalení drobných problémů
	- těžko se dělají modifikace
	- více týmu => horší sdílení => větši redundance
#### Návrh zdola nahoru
- od nejnižších komponent až po abstrakci
- nepotřebujeme úplnou znalost domény (vždy se soustředíme jen na 1 věc)
- **výhody**
	- tým se focusuje na 1 věc
	- agilní vývoj
	- brzy programujeme
	- snazší použití kódu
- **nevýhody**
	- refaktorování kódu
	- architektura nemusí být tak dobrá (horší udržitelnost)
	- těžké něco naplánovat
- spíše menší projekty
- extrém je vždy špatný => možno udělat kombinaci
#### Co ovlivňuje architekturu?
1) učel návrhu
2) primární funkční požadavky
	- měla by být ovlivněna jen tím nejdůležitějším
3) požadavky na emergentní vlastnosti
	- vhodná architektura je vyřeší za nás
4) podmínky zákazníka
	- rozpočet, doba a způsob dodání, technologie, licence, znovupoužití toho co už mají

- jak architekturu navrhnout?
- nevymýšlet nic nového, ale využít návrhové vzory
- koncepty jsou již osvědčené
#### Referenční architektura
- šablona pro architekturu, která je nejlepší v dané doméně
- urychluje vývoj
- např. webový klient - API - mobilní aplikace pro e-shop
#### Nákup komponent
- existující subsystémy je možné koupit
- pokud nemáme lidi, tak outsourcing
- vlastní vývoj - na míru, můžeme znovu použít, zabere to čas i lidi, složité odladit
- nákup - ušetříme čas, je vyladěné, můžeme upravovat (aby nezastaralo), kompromisy, cena ?
#### Open source řešení
- zdarma, takže vypadá lákavě
- hodně alternativ (co je to nejlepší)
- pozor na licence
- GNU licence
- MIT licence

- bez dokumentace je jakákoliv architektura k ničemu
- takže dokumentovat a doplnit diagramy
	- může pomoct odhalit chyby
	- usnadní implementaci
- opět postupy jak architekturu navrhovat (držíme se jich)
#### Obecný model
1) analýza
2) syntéza
3) zhodnocení
- je to iterativní proces (nečekáme že napoprvé uspějeme)
#### ADD - atributive drive design
- krok za krokem popsáno co by se mělo dělat
- důraz na atributy kvality SW (funkční, emergentní vlastnosti, proces)
1) revize vstupů
2) cíl aktuální iterace
3) volba elementů pro konkretizaci
4) volba konceptu
5) stanovení elementů
6) rozkreslení a dokumentace
7) validace
8) pokračování v další iteraci
#### Technika Microsoftu
- podobné ADD
1) stnovení cílů architektury
2) klíčové scénáře použití
3) vytvoření náhledu aplikace - typ, podmínky nasazení, návrhový vzor, technologie
4) indentifikace klíčových problémů
5) návrh kandidáta řešení
#### ACDM - architecture centric design method
- iterativní metoda
- rovnováha mezi obchodními a technickými aspekty
1) odhalení faktorů
2) vymezení rozsahu projektu
3) nástřel architektury
4) revize současné architektury
5) je finální?
6) plán pokusů (jak zlepšit)
7) provedení pokusů
8) GOTO 4
# 7) Návrhové vzory architektur
- většinu problémů již někdo před námi řešil
- opravodvé problémy až při běhu aplikace
- ustálilo se několik osvědčených návrhových vzorů
- usnadní a urychlí návrh (ověřené, všichni to znají)
- aplikace možná na celý systém či jen částečně
#### Vrstvená architektura
- horizontální na sobě ležící vrstvy
- na vrstvách pod je závislá
- na vrstvách nad je nezásvislá
1) uzavřené vrstvy - implementace pouze pomocí nejbližší vrstvy, jako TCP/IP, kratší závislost
2) otevřené vrstvy - implementace pomocí kterékoliv nižší, horší údržba, nižšší režie => vyšší výkon
- specifikace problému obvykle definuje jen nejvyšší vrstvu
- nejnižší je logicky nejblíže HW/OS/knihovnám
- **výhody**
	- striktní rozdělení odpovědnosti
	- snadná testovatelnost
	- znovupoužitelnost
	- bezpečnost (přidání mezivrstev)
- **nevýhody**
	- nutné hlídat a dodržovat nezávislost
	- složitost komunikace
	- nižší výkon
#### Client-server
- vysokoúrovňová 2 vsrtvá architektura
- jsou úzce spjaté, komunikace je oboustranná
- klient - UI a UX, server - celá logika
- server musí vždy validovat získaná data od klienta
#### Event driven system
- události ... info o změně stavu
- může zajímat jiné části systému
- distribuovaný a asynchronní
- řídí dispečer a spouští callback
- publish-subsribe (vysílá se broadcast)
- např. GUI, sledování změn v DB, ...
- hodně možností jak události zpracovat
#### MVC - model view controller
- rozšířené pro GUI a webové appky
- striktní rozdělení odpovědností do 3 částí
- ![[Pasted image 20231218193810.png]]
#### MVP - model view presenter
- rozšíření MVC, zakazuje komunikace model-view
- ![[Pasted image 20231218193950.png]]
- každý view má vlastní presenter
#### MVVM - model view viewmodel
- viewmodel stojí mezi view a model
- view dostává notifikace od viewmodelu a na ty reaguje
- ![[Pasted image 20250223161844.png]]
#### SOA - service oriented architecture
- rozdělení na mírně nezávislé spolupracující služby
- služba zapouzdží funcionalitu a poskytne rozhraní
- bývají fyzicky odděleny
- např. webové služby, síťové služby
- bezstavovost
- klasicky výhody i nevýhody
#### Monolitická architektura
- SW je ucelený a pevně svázaný
- nízká režie => vyšší výkon
- vhodné pro malé projekty
- nedá se moc škálovat
- težká udržitelnost (technologie atd.)
#### Architektura mikroslužeb
- microservices
- velmi malé autonomní služby
- nezávislé (verze, technologie, umístění)
- fungují jako black boxy
- pro velké projekty (dobrá škálovatelnost)
- často komunikují pomocí HTTP
- trend dnešní doby
# 8) Návrhové vzory - vytvářecí vzory
- většinově OOP
- vychází z reálného pohledu na svět
- **dessign patter** (návrhový vzor) ... způsob řešení opakujícího se problému v OOP
	- nejde o konkrétní kód, ale popis struktury
	- jejich znalost urychlí návrh OOP programů
- různá "velikost vzorů" (celé problémy i malé komponenty)
- definován pomocí
	1) **název** - zapamatovatelné ,krátké, usnadní přemýšlení, ustáleno praxí, vice ekvivalentních
	2) **popis problému** - vysvětlí problém a kontext
	3) **popis řešení** - vzor řešení (detailní a ucelené)
	4) **možné důsledky** - kompromisy při použití
- jsou mezi třídami a vzroy architektur
- dělení podle abstrakce - třídní a objektové
- podle účelu - vytvářecí, strukturální a vzory chování
- konkurentní vzory (paralelizační problémy)

- řeší vytváření nových instancí
- skrývají konkrétnost třídy, jak jsou třídy vytvářeny
- v compiletime nemusíme vědět jaké třídy konkrétně dostaneme
#### Abstract factory
- využívá se hodně
- vytvaří instance vzájemně souvisejících tříd, ale nemusíme specifikovat konkrétní třídy těchto objektů
#### Builder
- tolik se nepoužívá
- odděluje konstrukci objektů od jejich prezentace
#### Factory method
- vysoké použití
- interface pro tvorbu objektů, jehož potomci rozhodnou co se vytvoří
- při tom když třída neví jaké třídy objektů má vytvářet
- má několik součástí
	- product
	- concrete product
	- creator
	- concrete factory
- příklad intel procesory
	![[Pasted image 20231219084619.png]]
	
#### Prototype
- střední
- specifická instance třídy
- nový objekt se vytvoří klonováním prototypu
#### Singleton
- dost se používá
- třída pouze s jedinou instancí (globálně dostupná)
- chceme, aby danou funkcionalitu měla pod kontrolou jen 1 instance
	- např. logger, přístup do DB, plánovač v OS
- konkrétní implementaci je nejlepší nechat přímo na třídě (globální proměnná není moc dobrá)
- `private konstruktor`
#  9) Návrhové vzory - strukturální vzory
- jak jsou třídy a objekty složeny do sebe
- využívají dědičnost
#### Adapter (Wrapper)
- vyšší použití
- konvertuje rozhraní navzájem nekompatabilních tříd
- příklad celkem triviální
- součásti
	- target - definice rozhraní v dané doméně
	- client - volá nekompatabilní rozhraní
	- adaptee - nekompatabilní rozhraní
	- adapter - překladač
- důsledky - kolik práce dělá? volá jen metody nebo i další práce?
#### Bridge
- střední
- odděluje rozhraní a implemetaci objektu
#### Composite
- vyšší
- uspořádá objekty do stromové struktury a s tou se pak dá pracovat jako s jediným objektem
#### Decorator
- střední
- dynamicky rozšiřuje funkcionalitu objektu
- znám z Pythonu
#### Facade
- vysoká
- třídá vytvářející rozhraní pro celý subsystém (rozhraní vyšší úrovně)
- taková rozhraní pro rozhraní
- proč? potřebujeme komunikovat se všemi třídami v subsystému
- důsledky - odstínění komponent subsystému (=> menší závislost)
#### Flyweight
- nízká
- efektivní správa více objektů s podobnou strukturou, sdílení dat
#### Proxy
- vyšší
- objekt zajišťující přístup k jinému objektu (deleguje to)
# 10) Návrhové vzory - vzory chování
- rozdělují zoodpovědnost
- řeší komunikaci mezi objekty
- tzv. control flow (téžké sledovat za běhu)
- třídní a objektové vzory
#### Chain of responsibility
- nízké
- předání požadavku do řetězce objektů
#### Interpreter
- nízká
- interpretace vět jednoduhcého jazyka
#### Mediator
- nižší
- komunikace mezi 2 třídami (komunikují přes prostředníka)
#### Observer (pozorovatel)
- objektový
- 1:N - při změně stavu 1 objektu informauje ostatní
- proč? systém se musí udržovat v konzistentním stavu
	- tabulka s daty -> změna dat -> nutné změnit zobrazení, o kterém data ale neví
1) **subject** - zná pozorovatele, rozhraní pro přihlášení a odhlášení odběru změn
2) **observer** - definuje rozhraní pro informování o změně
3) **concreteSubject** - uložení sledovaného stavu, inforamuje o změně
4) **concreteObserver** - zná pozorovaný objekt (a udržuje si jeho stav), reaguje na změny
		![[Pasted image 20231119205029.png]]
- funguje jako broadcast
- nevýhoda: pozorovatelé se neznají -> kaskáda změn
#### Iterator (cursor, enumerator)
- objektový
- poskytuje sekvenční procházení datové struktury
- vše pak můžeme procházet stejným způsobem a nemsuíme řešit zda jde o strom, list nebo tečkové páry
1) **concreteIterator** - implementace rozhraní, udržuje aktuální pozici
2) **aggregate** - rozhraní pro vytvoření objektu Iterator
3) **concreteAggregate** - konkrétní datová struktura, umožňuje sekvenční průchod
#### Strategy
- zapouzdří algoritmy a umožní uživateli libovolně rozhodovat, který vybere (jsou vzájemně zaměnitelné)
#### Command
- zapouzdří operaci, aby šla později zavolat a zároveň si pamatoval režijní informace
- odděluje zadání požadavku a jeho vykonání
#### Visitor
- definování nové operace třídě bez její úpravy
#### Memento
- řeší uchování vnitřního stavu objektu, tak abychom se do něj mohli později napříkald vrátit
- neporušuje zpouzdření
- např. pro operaci undo

# 11) Validace a verifikace SW
- měli bychom ověřovat běheme každé fáze (oprávněnost, konzistence, relizovatelnost atd.)
- **validace** ... vytváříme správný produkt? (co?)
- **verifikace** ... vytváříme ho správně? (jak?)
- produkt musí logicky splnit očekávání v obou ohledech
1) **inspekce a revize sw**
	- kontrola požadavků, diagramů
	- ruční kontrola kódu
	- korespondence s DSP
2) **testování softwaru** - spuštění SW na testovacích datech
- debuggování (velmi specifické, závisí na programátorovi)
	- výrazně zjednodušuje IDE
- **V-model**
	- ![[Pasted image 20231120112125.png]]
- nutné dobře naplánovat
	- nic by nemělo být úplně vynecháno
	- stanovení formalit (postup, jednotný formát, co dělat když?)
- struktura testovacího plánu
	1) testovací proces
	2) pokrytí požadavků
	3) testované elementy
	4) časový plán
	5) záznam výsledků
	6) HW a SW požadavky
	7) podmínky (ovlivňující start a průbeh testů)
### Kontrola a revize kódu
- statické (bez spuštění)
- týká se zdrojáku, specifikace a architektury
- odhalí více chyb než dynamické testování
- težko se měří
- proces je formalizován - **týmová revize**
	- 4 osoby (čtenář, autor, tester, moderátor)
	- pouze nachází chyby (neřeší je)
	- seznámení týmu -> individuální příprava -> revize
	- je časově náročná
- **automatická (statická) analýza kódu**
	- součást IDE
	- podezřelé části (kontrola typů, null pointery atd.)
# 12) Testování SW
- dynamický proces (musíme mít spustitelný kód)
- pro každý požadavek (uživatelský i systémový) alespoň 1 test
- defect testing ... úspešný test = nález chyby
- nedává 100% záruku, záleží na kvalitě a četnosti testů
- test case ... vstupy a očekávané výstup
	- jednotlivá funkcionalita a kombinovaná může (ne)fungovat rozdílně
- testovací data
	- vhodná - krajní případy, né moc velké množství
	- často pevně daná pravidla jak volit
- zprávy o testování (vyvodí závěr)
##### Integrační testy (při vývoji)
- k dispozici zdrojové kódy (white box)
- snaha najít původce chyb (debbuging) může být složitá
- inkrementální přístup
- nová funkcionalita -> testovat i předešlé případy -> důkaz že jsme nic "nerozbili"
- automatizace
##### Funkční testy (před vydáním)
- release candidate (testování kandidáta na vydání) = ověřujeme celý systém
- není k dispozici zdroják (black box) => odhalení chyby jen předáme dál (neřešíme ho)
- snaha systém rozbít (SQL injection, dostat se tam kam nemůžu, stack overflow) nebo vyvolat chybovou hlášku
- testujeme posloupnost funcionalit
##### Testy výkonu
- testuje hotový systém 
- ověřujeme emergentní vlastnosti
- ověření že systém zvládne očekávanou zátěž
- **bottle neck** ... úzké hrdlo systému
- **stress test** ... plně vytížení systému
	- jak reaguje na zahlcení (aby nenastaly problémy s daty)
- **profiler** - ukazuje kde v systému trávíme nejvíc času a co využívá nejvíce zdrojů
	- 2 režimy - vzorkování a instrumentace

- code coverage ... kolik % kódu je pokryto testy
	- ani 100 % nemusí znamenat bezchybnost
##### Testy komponent (unit)
- odhaluje chyby v samostatných komponentách
- fake data (i fake rozhraní)
- **code coverage** ... % řádků kódu pokrytá testy (100 % != bezchbyný kód)
##### Testy bezpečnosti
- co nás zajímá? bezpečnost dat, kdo má kam přístup, co se děje při přenosu dat
- penetrační testy (různé typy útoků, externí odborníci)
- **bug-bounty program** ... firmy platí nálezcům chyb
##### Alpha testy
- poslední krok před doručením
- nad reálnými daty
##### Beta testy
- testují už reální uživatelé
- pouze ladí drobnosti
#### Návrh testů
- každý požadavek by měl jít otestovat
- mezní případy podmínek
- path testing ... ověření všech podmínek (pokrytí všech větví diagramu aktivit)
##### Test driven developement
 - nejdříve testy, podle nich píšeme implementaci
	- refactoring - zjednodušení kódu po jeho napsání (a splnění daných testů)
# 13) Kvalitní kód a jeho čitelnost
- více metriky pro "kvalitní kód" (musí splňovat, ale nestačí)
	- dělá co má dělat
	- je naprogramován rychle/levně
	- splňuje emergentní vlastnosti
#### Vnější vlastnosti (od uživatele)
1) korektnost ... dělá co má
2) použitelnost ... jak rychle se uživatel naučí používat
3) spolehlivost ... jak často spadne
4) integrita ... zabránění neoprávněnému přístupu
5) robustnost ... chování při ztížených podmínkách
#### Vnitřní vlastnosti (od programátora)
1) udržovatelnost ... snadnost přidání nových funkcí
2) flexibilita ... úprava pro jiné než původně zamýšlené použití
3) přenositelnost ... běh v jiných prostředích
4) znovupoužitelnost ... kolik % můžeme použít i jinde
5) čitelnost ... čtení zdrojáků
6) testovatelnost ... nutné úsilí při tvorbě testů
7) srozumitelnost ... pochopení architektury
#### Formátování
- zkombinovat obojí je náročné (i drahé)
- vazba vlastností? vyžadují se navzájem? není nutné, požadavky se celkem doplňují
	- př. špatný srozumitelnost -> horší přidání funkcí -> větší pravděpodobnost chybovosti
- software by měl být flexibilní (měnící se požadavky uživatelů), zároveň ale musí mít rozumnou míru, aby programátorům nedal moc zabrat
- čitelnost se nedá exaktně měřit a je subjektivní
- existují pouze doporučení
- nejvíce bychom se měli držet konzistentnosti (tab vs mezerník, 2 vs 4, camelCase vs snake_case)
	- Coding conventions
	- celkově ovlivněno IDE
- zásadně ovlivňuje jazyk (jeho abstrakce atd.)
	- to obvykle programátor neovlivní (dostane zadání)
- rozdělění metod (ty co se volají navzájem blízko u sebe)
- dělení do více souborů (co třída to soubor)
- dělka řádku (do 80 dříve, do 120 dnes), kvůli řetězení metod
	- LINQ
#### Pojmenování
- jméno je nositelem informace
	- krátké a výstižné (logicky to není easy vymyslet)
	- dostatečně specifické
	- jednoznačný (němělo by jít vyložit 2 způsoby)
- mohou být i komplexní (pokud vyjádří přesně co mají)
- iterátory a zažitá jména (`i, j, k, it, iter`)
- pracujeme-li s jednotkami (sekundy, dny, ...) uvádíme je v názvu
	- `public void Delay (int delaySec)`
- vyhnout se magickým konstantám
- rozsahy - včetně obou, bez krajních hodnot, ...
	- `first, last`
	- `begin, end`
#### Složité výrazy
- rozdělit na podproblémy => najdeme obecnejší, abstrakci
- De Morganovy zákony využít ke zjednodušení podmínek
#### Komentáře
- dvousečné
- pokud je kód dobře napsaný nepotřebuje moc komentovat
- naopak může vysvětlit optimlizační úpravy či jiné hacky
- dočasné komentáře (@TODO, @FIXME atd.) zvýrazní IDE
#### Proměnné
- rozumné proměnné => zvýší čitelnost i udržitelnost
- rozsah platnosti
- oblast života (měla by být co nejkratší)
- každá deklarovaná by měla být použita
- do 16 znaků délky
- 1 proměnná = 1 účel
# 14) Techniky zvyšující kvalitu kódu
- doržování i základních technik by mělo zaručit určitou kvalitu kódu
- principy z PP
- dodržení i těch nejzákladnějších nese hodně ovoce
#### Defenzivní programování
- ochrana vstupu před špatnými daty
1) kontrola všechn vstupů z externích zdrojů (UI, soubory, síť)
2) kontrola vstupních hodnot funkcí (takže nevěřím ani vlastnímu kódu)
3) co dělat při špatných datech
- zvyšuje kvalitu kódu, ale snižuje čitelnost
- `assertion` ... makro
	- součástí pouze vývojového kódu
	- nevolat v nich kód
#### Ortogonální systém
- snažit se o nezávislost komponent systému
- ideál je, aby se modul dal vyměnit bez jakéhokoliv jiného zásahu
	- obvykle nedosažitelné
- zpřažení komponent ... jak moc jsou na sobě závislé (těžko přesně měřit)
	- čím více tím složitější prováděí změn i čehokoliv jiného
1) zpřažení obsahu (patologické zpřažení) - moduly odkazují na interní data z jiných
2) globální zpřažení - sdílení globálních dat mezi moduly
3) zpřažení řízení - jeden modul řídí jiný (pomocí flags)
4) zpřažení daty - komunikují spolu pomocí metod
5) zpřažení metodami - volají metody jiných bez argumentů
#### Minimalizování komplexnosti
- komplexní SW přináší problémy (opoždění, dražší, snadněji přehlédneme problém, ...)
- podstatné problémy ... nutné vyřešit
- vedlejší problémy ... vznikly ze samotno tvorby SW
- **KISS (keep it simple stupid)**
	- co je jednoduchá to funguje dobře
	- modul/komponenta by měl dělat 1 věc, ale pořádně
	- v GNU např. řetězen příkazů
- **DRY (don't repeat yourself)**
	- nemít redundantní kód
- **information hiding**
	- zavedeno v OOP
	- neprorazuji svu interní reprezentaci
	- i programátor může být v roli používajícího
- **YAGNI (you arent gona need it)**
	- nedělat to co nepotřebuji teď
- **separation of concerns**
	- rozdělí odpovědnost do menších celků (MVC, HTML/CSS/JS spolupracují)
- **SOLID**
	- pro srozumitelný a dobře udržovatelný kód
	1) single responsibility principle - každá třída 1 věc
	2) open/closed principle - otevřeno pro rozšíření, uzavřeno k modifikaci
	3) liskov substitution - pravidlo `is a`
	4) interface segregation - co nejmenší rozhraní
	5) dependency inversion - jak navrhovat volně zpřažené komponenty (to nejvýš by němělo záviset na tom nejníž)
# 15) Chyby v aplikacích, bezpečnostní chyby a jejich správa
- pár aktuálních věcí
- SW je komplexní => horší odhalení chyb
- používání hodně knihoven (jsou aktuální?)
- roste i kvalita podpůrných nástrojů
- ověření původu pomocí elektonického podpisu
- co může dělat "navíc"? vytežovat zdroje, nestabilita, pop-up windows
- jaká je toho příčina? záměr, špatná optimalizace, napadení
- **bezpečnostní chyba** ... umožní uživateli dělat, to na co nemá práva
- **arbitary code execution** ... spuštění libovolného kódu
- **remote code execution** ... vzdálené spuštění libovolného kódu
- **eskalace práv** ... triviální
- neoprávněný přístup do paměti
	- mohou tam být hesla, klíče, ...
- útěk z kontejneru
- **exploit** ... kód/data, která využívají zranitelnost aplikaci ve svůj prospěch
- něměly by se tutlat
- CVE informuje veřejnost a eviduje (přířazení čísla)
- CVSS - ohodnotí na stupniciu dle závažnosti
- oznámení že nějaká chyba je -> příprava na záplatování –> po čase odhalení detailů
- bug bounty programy
##### Buffer overflow
- program spadne nebo se dá přepsat/spustit jiný kód
- stack canaries, data execution prevention
##### Format string attack
- čtení/zápis kvůli špatnému formátování
##### Integer overflow attack
- celočíselná čísla omezená délka => může přetéct
##### Command injection attacks
- zavolání shellu se dá zneužít
##### XML attack
- čtení nečeho co nikdy neskončí
##### Přihlášení uživatele
- když odesíláme heslo provozovateli důvěřujeme, že s hesly pracuje rozumně
- co nejméně v otevřené podobně (hash + sůl)
- speciální hashovací funkce pro hesla
- rainbow tables
- slabá uživatelksá hesla - mít požadavky či nikoliv?
##### Session hijacking
- přihlášení -> generování session ID (má trvanlivost) -> proto se pak nemusí při každém požadavku přihlašovat
- co když session id ukradneme?
- šifrovat komunikaci
##### Zabezpečení souborů
- apache umožňuje defaultně zobrazit adresář
- `/uploads, /images, ...`
- získání  přes cestu v URL
##### Chybové hlášení
- při produktovém nasazení bychom neměli zobrazovat
- čím více toho útočník ví, tím snažší to má (struktura, jazyk, verze serveru, jazyka, ...)
##### Oddělit frontend a backend
- JS je veřejný, dá se upravovat -> validovat data na serveru
##### XSS (cross site scripting)
- zneužití nevalidování vstupu a interpretace jako HTML
- opět validace či překódování
#### Chyby v HW
- i tady se mohou vyskytnou (je velmi komplexní a rozsáhlý)
- problém jak opravit
- aktualizace mikrokódu
- např. floating point division bug intel pentium
#### Malware
- SW který dělá, co uživatel nechce
- oprávnění přebíra od uživatele, který jej spustí
- síťová komunikace, vytěžování zdrojů, úpravy na disku, odposlech, ...
1) vir - program modifikující osatní programy či i sám sebe
2) trojksý kůň - přidává ještě funkcionalitu "navíc"
3) backdoor 
4) červ - vir šířící svou kopii přes síť
5) spyware - špehující SW (klávesnice, kamera, ...)
6) adware - zobrazování nechtěné reklamy
7) ransomware - způsobí škodu a požaduje výkupné (zaplatit či nechat být)
8) jokeware
9) kombinace více typů

- Quine ... program vypisující svůj kód
#### Kvalitní virus
- obížně detekovatelný
- obtížně zneškodnšní
- rychle se šíří
- multiplatformní
- přinese něco tvůrci
#### Jak se šíří?
- přes internet a pirátský SW
- sociální inženýrství (člověk bývá nejslabší článek)
- chyby v síťových aplikacích
- přípona osuboru jiná než bychom čekali
- vir se nejdřív musí spustit, do té doby nic nedělá
	- připojí se k binárním usouboru jiná aplikace, uživatel nic nepozná

- boot sektor - pokud je nakažen, tak vir přejímá kompletní kontrolu
- resident routines ... funkce OS trvale načtené v paměti
- infiltrace přímo do jádra OS
#### Detekce
- vzor či signatura specifických virů => hledání na disku či v paměti
- těžké rozlišot od chtěné appky
- nutné zastavit všechny běžící instancea odstranit
	- v nouzovém režimu či před bootem OS
- může být triviální i velmi kompikované
- dobré přijít odkud se vir vzal
#### Prevence
- chovat se zodpovědně na síti
- používat důvěryhodný SW
- pokud něco není důvěryhodné testovat na odděleném PC
- kvalitní antivir je velmi komplexní program
- co když je antivir virem?

# 16) Verzování SW, verzovací systémy
- přidělíme jednoznačné ID pro aktuální stav projektu
- běžné dvojí značení
	1) marketingový název
	2) interní číslování
- mělo by dávat smysl (nikoliv náhodný řetězec)
- mělo by jít snadno zapamatovat
- hned určit co je starší a co novější
- občas se přidává i kódové jméno
- opět máme ustálené schéma
- obvykle zveřejněno i s **roadmap**
#### Sémantikcé verzování
- `major.minor.patch`
- pomáhá s problémy typu dependency hell
- deklarace veřejného API
- bez leading zeroes
- pokud `major` == 0, tak není stabilní
- patch se zvyšuje při opravách chyb
- minor při přidání nové funkcionality se zpětnou kompatabilitou
- major při nekompatabilních změnách ve veřejném API
- při zvýšením se vždy nižší verze nulují
- rozšíření pomocí pomlčky `1.0.0-aplha`
- pomocí + přidáme metadata `1.0.0-beta+exp.sha.511`
#### Verze odvozená od data
- vhodnější pro produkty měnící se často
- kombinace s sémantickým verzováním
- ihned poznáme stáří produktu
#### Další
- obyčejné číslo
- sudá-lichá vezre (sudá ... stabilní, lichá ... vývojová)
- zeroVer - major je pořád 0

- naše schéma by mělo být zveřejněno
- každé vydání musí obsahovat changelog
- zveřejnit roadmap
- včas ohlásit vydání nové major
- změna schématu (občas je nevyhnutelná, může přinést komplikace)
	- Java 1.8.0 -> Java 8
### Verzovací systémy
- nutné u projektů, kde pracuje více lidí
	- je nutné mít k dispozici i starší verzi
	- možnost synchronizovat přidané funkcionality od více lidí najednou
#### Git
- distribuovaný verzovací systém
- Linus Torvalds
- dnes nejpopiulárnější
##### Repozitář
- databáze obsahující všechny informace nutné ke správě verzí a sledování změn
- `.git`
- object store ... vše potřebné pro obnovení verze (logy, autoři, úložiště origo souborů)
- index ... dočasný binární soubor trackující změny
	- po commitu jsou zaznamenány natrvalo
- commit ... záznam o změně v repozitáři
	- ukládá pouze změněné soubory
	- vždy má předka
	- má unikátní jméno
- větvění ... rozdělení do více souběžných větví
	- spojení pomocí merge
	- proč? izolovanost jednotlivých funkcí, rozdělení podle vývojářů, oddělení pro různé verze
	- má vždy jméno (master, dev, testing, ...)
	- aktivní je vždy jen 1
- merge ... spojení
	- mohou nastat konflikty, jinak automatické
	- upravíme buď ručně nebo pomocí nějakého nástroje
- stash ... zásobník pro odležení rozpracované práce
	- pokud potřebujeme nutně jít dělat něco jiného
	- uložíme si jen pro sebe (není nikd epublikována)
- remote ... vzdálený repozitář
	- developement a bare
	- clone nebo fetch dat

- git má samozřejmě i alternativy, ale je nejpopiulárnější
	- mercurial
	- bazaar
#### Webové CVS
- slouží především pro prezentaci
- rychlo prohlížení kódu i nevývojáři
- vizualizace větví
- GitHub
- GitLab
- BitBucket
#### Continuous integration (CI)
- snaha o co největší míru automatizace sestavení a testování
- úzce spolupracuje s verzovacím systémem
	- commit sestaven, otestován unit testy (někdy i integrační)
- vývojáři vyvíjí a současně a průběžně se integruje
##### CI server
- SW kontrolujícíc repozitáíř a vykonávající různé akce
	- kompilace
	- spouštění testů (i výpočet code coverage)
	- checking coding conventions
	- CI pipeline
- podporují weboví klienti Gitu
#### Continuous delivery
- zahrnuje správu configurací a přístupových údajů
- automaticky synchronizuje testovací a produkční prostředí
- delivery je pouze doručení nikoliv nasazení (to si obvykle žádá manuální zásah)
#### Continuous deployment (CD)
- automatizace nasazení aktuální verze
- není žádoucí přímo na produkci, takže vhodné do testovacího prostředí
- v produkci dobré na jedno kliknutí (neboli potvrzení zákazníka)