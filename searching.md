# Wyszukiwanie

Zarówno przeglądarka jak i talie filtrowane używają w Anki wspólnej metody wyszukiwania określonych kart/notatek.

## Proste wyszukiwania 

Gdy wpiszesz coś w wyszkiwarce, Anki wyszukuje we wszystkich polach notatek, ale nie w dtykietach (później w tej cześci nauczysz się jak wyszukiwać etykiety) Kilka przykładów:

`lot`  
wyszukuje słowa "lot" - wyniki wyświetlą również słówka takie jak "lotem" oraz "nalot".

`lot kot`  
wyszukuje notatki, w których znajdują się zarówno słowa "lot" i "kot" np. "Kot udaje się w daleki lot".

`lot or kot`  
wyszukuje notatki ze słowem "lot" lub "kot".

`lot (kot or mysz)`  
wyszukuje notatki ze słowami "lot" i "kot" lub "lot" i "mysz".

`-kot`  
wyszukuje notatki nie zawierające słowa "kot".

`-kot -mysz`  
wyszukuje notatki bez słów "kot" oraz "mysz".

`-(kot or mysz)`  
jak wyżej.

`"ten kot"`  
wyszukuje notatki, które zawierają w sobie dokładnie takie wyrażenie -> "ten kot". Funkcja wyszuka np. "tamten kot", jednak nie pojawią wyniki takie jak "kot tamten".

`-"ten kot"`  
wyszukuje notatki, które nie zawierają w sobie dokładnie takiego wyrażenia -> "ten kot".

`k_t`  
wyszukuje notatki z k, &lt;dowolną literą&gt;, t, takie jak kit, kat, kot, i tak dalej.

`k*t`  
wyszukuje notatki ze słowami rozpoczynającymi się od litery k i kończącymi się literą t, takie jak koloryt lub kapitanat.

`w:lot`  
wyszukuje "lot" tylko w granicach słowa - wyszuka "lot", ale nie "lotem" ani "nalot". Wymaga Anki 2.1.24+ lub AnkiMobile 2.1.61+. 

`w:lot*`  
wyszukuje "lot" oraz "lotem", ale nie "nalot".

`w:*lot`  
wyszukuje "lot" oraz "nalot", ale nie "lotem".

Z powyższych przykładów wynika, że:

- Szukane słowa zawsze są oddzielone spacją

- Kiedy podanych zostanie kilka warunków wyszukiwania, Anki bedzie szukać notatek, które spełniają wszystkie warunki (niewidoczne "and" pomiędzy każdym wyrażeniem). Jeśli chcesz,W Anki 2.1.24+ oraz AnkiMobile 2.0.60+ możesz te ukryte "and" wpisywać - "lot and kot" jest tym samym co "lot kot". Starsze wersje Anki traktują "and" jako normalne słowo do wyszukania. 

- Możesz używać "or" jeśli chcesz, żeby tylko jedno z wyrażeń zostało znalezione.

- Możesz dodać przed wyrażeniem znak minus, aby znaleźć notatki, które nie spełniają kryteriów.

- Jeśli twoje wyszukiwanie zawiera spację lub nawias, zamknij je w cytatach. Możesz w nich umieścić
  `"całe:wyszukiwanie"`, lub tylko `część:"po dwókropku"`.

- Możesz grupować pojęcia, które wyszukujesz, poprzez wstawianie ich do nawiasów, tak jak w przykładzie **lot (kot or mysz)**. Jest to dosyć istotne podczas łączenia wyszukiwań OR oraz AND - w przykładzie z nawiasami zostaną wyszukane "lot kot" lub "lot mysz", podczas gdy bez nich Anki szukałoby "lot and kot" lub "mysz". 

- Anki jest w stanie wyszukiwać uwzględniając formatowanie tylko w skonfigurowanym [polu sortowania](editing.md#customizing-fields). Jeśli na przykład dodasz "**przy**kład" do jednego z twoich pól, nie zostanie ono znalezione podczas wyszukiwania "przykład", chyba, że to pole jest polem sortowania. Gdy słowo nie jest sformatowane lub formatowanie nie zmienia się w środku, słowa Anki będzie w stanie je znaleźć niezaleznie od pola. 

## Zawężanie wyszukiwania do pola

Możesz równiez wyszukać tak, aby wyniki zostały znalezione tylko jeśli określone pole zawiera jakiś tekst. W przeciwieństwie do wyszukiwań u góry, szukanie po polu domyślnie wymaga "ścisłego dopasowania".

`przód:kot`  
wyszukuje notatki z polem Przód, w którym znajduje się dokładnie "kot". Pole, w którym znajduje się "ten kot" nie zostanie znalezione.

`przód:*kot*`  
wyszukuje notatki z polem Przód, które zawiera gdzieś słowo "kot".

`przód:`  
wyszukuje notatki, które zawierają puste pole Przód.

`przód:_*`  
wyszukuje notatki, które zawierają pole Przód, które nie jest puste.

`przód:*`  
wyszukuje notatki, które zawierają Pole przód, niezależnie czy jest coś w nim napisane 

`pr*:text`
wyszukuje notatki w polu zaczynającym sie na "pr". Wymaga Anki 2.1.24+ lub AnkiMobile 2.1.60+.

## Etykiety, talie, karty i notatki

`tag:zwierze`  
wyszukuje notatki z etykietą "zwierze"

`tag:none`  
wyszukuje notatki bez etykiet

`tag:zwi*`  
wyszukuje notatki z etykietami, które zaczynają się na zwi-.

`deck:francuski`  
wyszukuje karty w talii Francuski lub jej podtaliach np. Francuski::Słownictwo.

`deck:francuski -deck:francuski::*`  
znajduje karty w talii Francuski, ale nie wyszukuje w podtaliach.

`deck:"francuski słownictwo"`  
używane, gdy w nazwie talii jest spacja

`"deck:francuski słownictwo"`  
też działa

`deck:filtered`  
tylko talie filtrowane

`-deck:filtered`  
tylko talie niefiltrowane

`card:forward`  
wyszukuje kart przednich

`card:1`  
wyszukuje karty po numerze szablonu np. aby znaleźć drugie wypełnianie luki dla karty, wpisałbyś card:2

`note:basic`  
wyszukuje kart z podstawowym typem notatki

## Ignorowanie akcentów i łączenia znaków

Wymaga Anki 2.1.24+ lub AnkiMobile 2.0.60+.

Możesz użyć `nc:` aby ignorować akcenty i łączenie znaków. Przykładowo:

`nc:uber`  
wyszukuje notatki  "uber", "über", "Über" i tak dalej.

`nc:は`  
wyszukuje "は", "ば", oraz "ぱ"

Wyszukiwania, które ignorują łączenie znaków i akcenty są wolniejsze niż standardowe wyszukiwania.

## Wyrażenia regularne

Anki 2.1.24+ oraz AnkiMobile 2.0.60+ umozliwiają wyszukiwanie w notatkach za pomocą "wyrazeń regularnych". Jest to standardowy i skuteczny sposób wyszukiwania informacji w tekście.

Zaczanij wyszukiwanie od `re:`, aby wyszukać przy pomocy wyrażenia regularnego. Kilka przykładów:

`"re:(niektóre|inne).*rzecz"`  
wyszukuje notatki zawierające "niektóre" lub "inne", po nich znajdujące się 0 lub więcej znaków, a nastepnie "rzecz".

`re:\d{3}`  
wyszukuje notatki, które są złożone z 3 cyfr w rzędzie.

Wyrażenia regularne mogą  być również limitowane do określonego pola. Zauważ, że w odróżnieniu od normalnych wyszukiwań w określonym polu, wyrażenia regularne nie wymagają w polach ścisłego dopasowania. Przykładowo:

`przód:re:[a-c]1`  
wyszukuje duże jak i małe litery a1, B1 lub c1, które pojawiają sie gdziekolwiek w polu "Przód".

`przód:re:^[a-c]1$`  
jak wyżej, ale nie wyszukają, jeśli przed a1/b1/c1 pojawi się jakikolwiek tekst.
Możesz dowiedzieć się więcej o wyrażeniach regularnych tutaj: https://regexone.com/lesson/introduction_abcs.

Kilka rzeczy, na które trzeba zwrócić uwagę:

- Wyszukiwanie domyślnie nie bierze pod uwagę wielkość liter; wpisz (?-i) na początku, aby brać pod uwagę wielkość liter w wyszukiwaniach.
- Niektóry tekst jak spacje albo nowe linie mogą być pokazane inaczej w HTML - możesz użyć edytora HTML w oknie edycji, aby zobaczyć niewidoczną zawartość HTML
- Aby dowiedzieć się szczegółów o wsparciu Anki dla wyrażeń regularnych, zobacz następującą dokumentację: https://docs.rs/regex/1.3.9/regex/#syntax

## Stan karty

`is:due`  
karty powtórkowe i karty uczone oczekujące na naukę

`is:new`  
karty nowe

`is:learn`  
karty uczone

`is:review`  
powtórki (zarówno oczekujące jak i nieoczekujące) oraz pomyłki

`is:suspended`  
karty, które zostały ręcznie zawieszone

`is:buried`  
karty, które zostały zakopane [automatycznie](studying.md#siblings-and-burying) lub ręcznie.

Karty - pomyłki zliczają się do kilku z tych kategorii, więc może okazać się przydatne połączenie tych wyszukiwań, aby otrzymać bardziej precyzyjne wyniki:

`is:learn is:review`  
pomyłki oraz karty oczekujące na ponowną naukę 

`-is:learn is:review`  
powtórki bez pomyłek

`is:learn -is:review`  
karty, które są uczone po raz pierwszy.

`edited:n`
karty, których tekst notatki został zmieniony w ciągu ostatnich "n" dni. Wymaga Anki 2.1.28+ lub AnkiMobile 2.0.64+.

## Własciwości karty

`prop:ivl>=10`  
karty z przerwą 10 dni lub więcej

`prop:due=1`  
karty na jutro

`prop:due=-1`  
karty wczorajsze, na które jeszcze nie odpowiedziano

`prop:due>-1 prop:due<1`  
karty oczekujące pomiedzy dniem wczorajszym a jutrzejszym

`prop:reps<10`  
karty, na które odpowiedziano mniej niż 10 razy

`prop:lapses>3`  
karty, które były uczone ponownie więcej niż 3 razy.

`prop:ease!=2.5`  
karty łatwiejsze lub trudniejsze niż domyślna wartość

Miej na uwadzę, że "due" wyszukuje tylko karty powtórkowe i karty uczone z przerwą wynosząca jeden dzień lub więcej: karty uczone z mniejszymi przerwami takimi jak 10 minut nie są uwzgledniane.

## Ostatnio dodane

`added:1`  
karty dodane dzisiaj

`added:7`  
karty dodane w ciągu ostatniego tygodnia

Data dodania jest sprawdzana na podstawie daty utworzenia karty a nie daty utworzenia notatki, więc karty, które zostały wygenerowane w określonym czasie będa brane pod uwagę nawet, jeśli ich notatki zostały dodane dawno temu

## Ostatnio powtarzane

`rated:1`  
karty, nak tóre odpowiedziano dzisiaj

`rated:1:2`  
karty, na które odpowiedziano dzisiaj Trudna (2) 

`rated:7:1`  
karty, na które odpowiedziano Powtórz (1) w ciągu ostatnich 7 dni

`rated:31:4`  
karty, na które odpowiedziano Łatwa (4) w ciągu ostatniego miesiąca

Ze względu na wydajnosć, wyszukiwania ze względu na ocene są limitowane do 31 dni.

## Numery ID objektu

`nid:123`  
wszystkie karty notatki z numerem ID notatki 123

`cid:123`  
karta z numerem ID karty 123

`mid:123`  
wyszukuje typy notatek z numerem ID typeu notatki 123.

numery ID notatek i kart możesz znaleźć w oknie [informacji o karcie](stats.md) w przeglądarce. Numery ID typu notatki możesz znaleźć klikając na typ notatki w oknie przeglądarki. Te wyszukiwania mogą być przydatne podczas tworzenia dodatku lub innej czynności wymagającej ścisłej pracy z bazą danych.

numery ID objektu nie działają w aplikacjach mobilnych i nie są obecnie stworzone do używania z taliami filtrowanymi. 
