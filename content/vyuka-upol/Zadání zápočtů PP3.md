## Úkol 4. Prototypy
- zadání úkolu naleznete v dokumentu 10_lecture.pdf k desáté přednášce v sekci Otázky a úkoly na cvičení. Z uvedených 15 úkolů si vyberte a vyřešte:
-   **6** z úkolů **1-9**,
-   **2** operace z úkolu **10**,
-   **1** z úkolů **11-15**.

## Úkol 3. Inspektor
 - Definujte třídu inspector-window, jejíž instance (nazývané prohlížeče) bu- dou okna, zobrazující informace o zvoleném objektu jiného (prohlíženého) okna. Informace o objektu by měla obsahovat název třídy objektu a dále názvy a hodnoty základních vlastností (např. color, thickness, radius, x,y, r, phi, closedp atd., podle třídy prohlíženého objektu). Prohlížená okna budou instancemi vámi definované třídy inspected-window.

**Základní funkčnost:**
1. Prohlížeč má nastavitelnou vlastnost inspected-window, která obsa- huje okno, jež má být prohlíženo.
2. Po nastavení prohlíženého okna prohlížeč zobrazí informace o tomto okně.
3. Po kliknutí do prohlíženého okna zobrazí prohlížeč informace o pevném objektu (tj. s vlastností solidp rovnou Pravda), na který uživatel klikl. Po kliknutí mimo všechny objekty se zobrazí opět informace o okně.
4. Prohlížený objekt je uložen ve vlastnosti inspected-object prohlížeče. Tato vlastnost nemusí být zapisovatelná.
5. Při změně aktuálně prohlíženého objektu prohlížeč automaticky aktua- lizuje zobrazenou informaci.
6. Po dvojkliku na hodnotu vlastnosti zobrazí prohlížeč dialog s dotazem na novou hodnotu. Po potvrzení vlastnost na tuto hodnotu změní.
7. Pro třídy grafických objektů, které definuje někdo jiný (třeba pro třídu bulls-eye), musí být specifikován (a v dokumentaci popsán) způsob, jakým prohlížeč zjistí a nastaví jejich nové vlastnosti. (Bez úpravy třídy inspector-window a inspected-window musí tedy autor třídy bulls- -eye být schopen zařídit, aby prohlížeč zobrazoval a nastavoval hodnotu vlastnosti squarep.)

## Úkol 2. Křižovatka
- Definujte třídu semaphore, která bude potomkem třídy abstract-picture a jejíž instance budou simulovat dopravní semafor. Dále definujte třídu crossroads, která bude rovněž potomkem třídy abstract-picture a jejíž instance budou představovat obrázky křižovatky.

Požadavky na třídu **semaphore**:
1.  Světla semaforu budou instancemi třídy light ze souboru 04_light.lisp.
2.  Semafor bude mít nastavitelnou vlastnost semaphore-type s možnými hodnotami (minimálně) :pedestrian a :vehicle.
3.  Instance třídy semaphore se budou vykreslovat jako jednoduchý obrázek semaforu (správný počet koleček v obdélníku).
4.  Semafor se může nacházet v jedné z několika fází, podle svého typu. Např. semafor pro vozidla bude mít čtyři fáze (červená, červená + oranžová, zelená, oranžová). Aktuální barvy světel semaforu musí odpovídat jeho fázi. Číslo fáze bude uložené v nastavitelné vlastnosti semaphore-phase. Počet fází bude uložen ve vlastnosti phase-count. Fáze se číslují od nuly.
5.  Pro přechod k následující fázi bude semafor implementovat metodu next-phase.

Požadavky na třídu **crossroads**:
1.  Vlastnost items bude nastavitelná uživatelem. Může obsahovat libovolné grafické objekty, z nichž některé mohou být semafory.
2.  Třída definuje vlastnost semaphores (jen ke čtení), která bude obsahovat seznam všech semaforů v křižovatce.
3.  Křižovatka se podobně jako semafor může nacházet v různých fázích. Jednotlivé fáze křižovatky se budou opět přepínat zprávou next-phase a budou uloženy ve vlastnosti crossroads-phase. Počet fází bude uložen ve vlastnosti phase-count.
4.  Fáze křižovatky určují, v jakých fázích jsou její semafory. To je zadáno nastavitelnou vlastností program, která obsahuje program semaforu. To je seznam seznamů. Jeho délka udává počet fází, i-tý podseznam programu určuje stav křižovatky v její i-té fázi. Každý podseznam má délku rovnou počtu semaforů v křižovatce a pro každý semafor obsahuje číslo jeho fáze. Příklad: pro křižovatku o třech semaforech a programem ((0 0 0) (0 1 0) (0 2 1)) platí, že je-li křižovatka ve fázi 2, je její první semafor ve fázi 0, druhý ve fázi 2 a třetí ve fázi 1.
5.  Pracujte s načtenou knihovnou micro-graphics a načtenými soubory 05.lisp a 04_light.lisp.

## Úkol 1. Halloween
- Naprogramujte funkce make-ghost a display-halloween-window (viz. přiložený obrázek), kde:

1. **make-ghost** _color scale-coeff_ => _picture_
	- Tato funkce vrátí instanci třídy picture, která vyobrazuje ducha z Pac-Mana dané barvy a zvětšeného o zadaný koeficient. Duch o velikosti 1 má 150x200 pixelů. Při vytváření ducha použijte Vámi implementovaou třídu _triangle_. Nově vytvořený duch bude mít střed na souřadnících [0,0].
2. **display-halloween-window** _ghost-count_ => _window_
- Tato funkce vytvoří okno, jehož pozadí je černé a slot shape obsahuje instanci picture se zadaným počtem duchů. Tito duchové:
	-   mají náhodnou barvu (např. z 5 různých),
	-   mají náhodné umístění v rámci okna,
	-   jsou otočení o náhodný úhel,
	-   jejich velikost je náhodně zvolená mezi 1/4 až 1/2.

Pozn. pro náhodný faktor použijte funkci _random_, kterou lze například použít i s konstantou pi pro získání double-float čísla z rozsahu [0,pi].