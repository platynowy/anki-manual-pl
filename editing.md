Dodawanie/Edytowanie
===============

Dodawanie kart i notatek
----------------------

Jak zostało to opisane w rozdziale na temat [podstaw](getting-started.md), w Anki użytkownik tworzy notatki, a na ich podstawie program generuje automatycznie karty. Aby dodać nową notatkę  naciśnij przycisk "Dodaj" w oknie głównym. Pojawi się wtedy nowe okno "Dodaj Notatki.

W lewym górnym rogu okna "Dodaj" znajduje się informacja o aktualnie używanym typie notatki. Jeśli widnieje tam inna nazwa niż "Podstawowy" (czyli podstawowy typ notatki) to prawdopodobnie poprzez import którejś z udostępnionych talii dodałeś nowy typ notatki. W dalszej części tego opisu będziemy omawiać tylko typ "Podstawowy".

W prawym górnym rogu okna "Dodaj" wyświetlana jest nazwa talii do której zostanie dodana notatka. Żeby dodać notatkę do innej tali, wystarczy kliknąć przycisk z nazwą obecnej talii a następnie wybrać "Dodaj".

Poniżej przycisku z typem notatki znajdują się dwa pola tekstowe o nazwie "Przód" oraz "Tył". Przód i Tył to właśnie pola notatki, możesz dodawać nowe pola, usuwać je i zmieniać ich nazwy. Aby wykonać, którąś z tych czynności wybierz przycisk “Pola…​”, który znajduje się pod przyciskiem z typem notatki.

Poniżej pól notatki znajduje się pole tekstowe oznaczone jako "Etykiety" są to tzw. tagi. Etykiety to słowa, które będą charakteryzowały notatki w celu ich lepszej organizacji lub po to by ułatwić ich wyszukiwanie. Dana notatka może być scharakteryzowana przez więcej niż jedną etykietę. Nadawanie etykiet notatkom nie jest obowiązkowe, to pole może pozostać puste. Etykiety oddzielane są znakiem spacji. Przykładowo jeśli nadamy notatce etykiety:

    słownictwo do_sprawdzenia

…​wtedy notatka będzie posiadałą dwie etykiety

Aby dodać notatkę do kolekcji wypełnij najpierw pola Przód i Tył, a następnie wybierz przycisk Dodaj (u dołu okna) lub naciśnij Ctrl + Enter (Command + Enter na komputerach Mac). Razem z notatką wygeneruje się karta, która zostanie umieszczona we wcześniej wybranej przez ciebie talii. Aby edytować wcześniej dodaną kartę, wystarczy że klikniesz przycisk Historia, co otworzy [przeglądarkę](browsing.md).

Pamiętaj, pierwsze pole notatki nigdy nie może pozostać puste, a jego treść musi być niepowtarzalna - nie można na przykład stworzyć dwóch notatek, które w polu Przód będą zawierały słowo "jabłko". Ta niepowtarzalność treści jest jednak ograniczona tylko do jednego typu notatki, przykładowo: jeśli uczysz się wielu języków i dla każdego z nich stworzony jest inny typ notatki, to dane słowo w polu Przód może się powtarzać o ile notatki z tym słowem należą do różnych typów. 

Anki w czasie dodawania notatki, ze względu na wydajność programu, nie sprawdza innych pól pod kątem niepowtarzalności. Jednakże w przeglądarce kart znajduje się przycisk "Znajdź duplikaty…" (Przeglądaj>Notatki>Znajdź duplikaty…). Funkcja ta przeszukuje wszystkie pola wszystkich notatek pod względem duplikatów. Warto jest od czasu do czasu takie przeszukanie wykonać.

Aby dowiedzieć się więcej na temat przycisków, które znajdują się pomiędzy polami notatki a przyciskiem typu notatki zajrzyj do rozdziału na temat [edytora](editing.md).

Kart można się uczyć w różny sposób, jednak  zawsze należy pamiętać o pewnych ogólnych zasadach. Dobre wprowadzenie stanowi [artykuł](http://www.supermemo.com/articles/20rules.htm) na stronie SuperMemo. Zasadniczo:

-   **Pamiętaj o prostocie**: Im prostsze są karty tym łatwiej jest się ich uczyć. Czasami może cię kusić, żeby dodać więcej treści do jednej karty, tak na wszelki wypadek, jednak w takim przypadku bardzo szybko nauka stanie się męczarnią.

-   **Nie ucz się rzeczy których nie rozumiesz**: Jeśli uczysz się języka obcego unikaj tworzenia długich list wyrazów w jednej karcie. Najlepszym sposobem nauki języka obcego jest wstawienie wyrazów w pewien kontekst, który pokaże słowa w ich prawidłowym zastosowaniu (np. w zdaniu). Jeśli będziesz starał się zapamiętać całą górę znaczeń różnych skrótów, bardzo szybko zauważysz jak trudno jest zrobić jakikolwiek postęp przy takim sposobie nauki. Ale jeśli włożysz trochę więcej pracy i postarasz się zrozumieć co tak naprawdę stoi za tymi skrótami, nauka będzie wtedy dużo prostsza i efektywniejsza.

Dodawanie typu notatki
------------------

Podstawowy typ notatki w zupełności wystarcza do tworzenia prostych kart z jednym słowem lub zdaniem po każdej ze stron karty. Jednak jeśli stwierdzisz, że chciałbyś umieścić w notatce więcej niż jedną informację na przodzie i tyle karty, to najlepszym wyjściem jest podzielenie takiej informacji na więcej pól.

Możesz sobie jednak pomyśleć "przecież ja chcę tylko jedną kartę, umieszczę obrazek, podpowiedź i wymowę słowa na przodzie karty, a na tylnej stronie odpowiedź". Oczywiście bez problemu możesz stworzyć taką kartę. Jednak takie podejście ma jedną główną wadę, wszystkie informacje są zbite w jedno pole. W takiej sytuacji nie ma możliwości np. posortowania kart pod kątem treści podpowiedzi albo treści pytania. Nie da się wtedy przenieść np. pliku audio z przodu karty na jej tył, no chyba że ręcznie kopiując go w każdej notatce. Trzymanie informacji w osobnych polach sprawia, że zmiana układu karty w przyszłośco będzie znacznie prostsza.

Aby utworzyć nowy typ notatki wybierz Narzędzia → Zarządzaj typami notatek z okna głównego Anki. Kliknij "Dodaj" aby dodać nowy typ notatki. Pojawi się teraz następne okno, które pokaże Ci typy notatek na podstawie których możesz stworzyć nowy typ notatki. "Dodaj" tworzy nowy typ notatki na podstawie, któregoś ze standardowych typów Anki. "Klonuj" odnosi się do typów notatek stworzonych wcześniej przez użytkownika. Przykładowo na tym samym typie notatki możesz uczyć się zarówno francuskiego jak i niemieckiego.

Po wybraniu przycisku "OK" Anki poprosi o podanie nazwy dla nowego typu notatki. Dobrze wybrać nazwę, która wprost odnosi się do materiału, do nauki którego będzie wykorzystywany dany typ notatki np. japoński lub geografia. Po nadaniu nazwy nowemu typowi notatki można zamknąć okno Typy notatek i powrócić do okna dodawania notatki. 

Dostosowywanie pól
------------------

Aby dostosować pola do własnych potrzeb kliknij przycisk “Pola…​” podczas dodawania lub edycji notatki lub gdy typ notatki jest wybrany w oknie "Zarządzaj typami notatek".

Możesz dodawać, usuwać lub zmieniać nazwy pól po klikając odpowiednie przyciski po prawej stronie okna. Aby zmienić kolejność, w której pola pokazywane są w oknie dodawania notatki użyj przycisku "Zmień pozycję". Pojawi się okno, w którym zostaniesz poproszony o podanie kolejności w formie numerów. Przykładowo, jeśli chcesz aby dane pole w oknie dodawania notatki wyświetlane było jako pierwsze wpisujesz po prostu "1".

Nie używaj "Tags", "Type", "Deck", "Card", lub 'FrontSide' jako nazw pól, ponieważ są to [pola specjalne](templates/fields.md#special-fields) i nie będą działać poprawnie.

Opcje zlokalizowane w dolnej części okna "Pola…" pozwalają na dodatkową edycję ustawień pól, ale tylko w oknie dodawania notatki. *Nie jest* to miejsce, w którym dostosujesz sposób wyświetlania pól na karcie podczas nauki. Te ustawienia opisane sa w sekcji [szablony](templates/intro.md).

**Czcionka edycji** pozwala na wybranie czcionki, która będzie wykorzystywana w polu podczas dodawania i edycji notatki. W ten sposób mniej istotne informacje w notatce mogą być pisane mniejszą czcionką, a te ważniejsze jak np. trudne do odczytania znaki języka japońskiego - większą. Zauważ, że nie mówimy tutaj o rozmiarze tekstu w karcie, tylko o rozmiarze tekstu podczas wprowadzania informacji do notatki w oknie "Dodaj" (to znaczy, że nie zauważysz zmian na karcie podczas nauki). Aby zmienić rozmiar tekstu w karcie, zobacz rozdział [Szablony](templates/intro.md) .Jeśli jednak włączyłeś funkcję pisanie w odpowiedzi, to odpowiedź zostanie wyświetlona właśnie przy pomocy ustawionej tutaj czcionki. (Aby dowiedzieć się więcej jak zmienić czcionkę używaną podczas pisania odpowiedzi, zobacz rozdział [sprawdzanie odpowiedzi](templates/fields.md#checking-your-answer)).

**Sortuj w przeglądarce według tego pola​** mówi Anki, że to pole powinno znajdować się w kolumnie Pole sortowania w przeglądarce. Karty w przeglądarce mogą być sortowane jednocześnie tylko według jednego pola.

Zaznaczając opcję  **Zapamiętuj ostatnią wartość przy dodawaniu​** przy dodawaniu kolejnej notatki Anki pozostawi w polach informacje z poprzednio dodanej notatki. Jest to funkcja użyteczna przy dodawaniu wielu notatek, które w którymś z pól posiadają tę samą informację.

Opcja **Odwrotny kierunek tekstu** służy do wprowadzania tekstu pisanego z prawej do lewej strony (np. w językach arabskim lub hebrajskim). Jak zostało to wspomniane powyżej, opisywane tutaj ustawienia służą jedynie do kontroli wyświetlanego tekstu podczas edycji lub dodawania nowej notatki. W celu ustawienia czcionki wyświetlanej w kartach, należy edytować ustawienia [szablonów](templates/styling.md).

Po dodaniu wszystkich pól będziesz chciał najpewniej dodać te pola do przedniej lub tylnej strony karty. Więcej informacji na ten temat znajduje się w sekcji dotyczącej [szablonów](templates/intro.md).

Zmiana talii/typu notatki
-------------------------

Aby zmienić talię lub typ notatki podczas dodawania notatki kliknij w oknie "Dodaj" odpowiednio prawy górny lub lewy górny przycisk. Okno zmiany talii i zmiany typu notatki pozwalają również na utworzenie nowej talii lub nowego typu notatki, a także na zarządzanie już istniejącymi.

Prawidłowe używanie talii
-------------------------

Celem talii jest przede wszystkim oddzielenie od siebie dużych zakresów tematycznych np. języka angielskiego, geografii itd. Tworząc talie możesz stwierdzić, że chciałbyś mieć każdy z mniejszych tematów w osobnej talii, dla lepszej organizacji np. "mój podręcznik geografii rozdział 1" albo "angielski zwierzęta", wbrew pozorom taki układ kolekcji nie jest dobrym rozwiązaniem, przynajmniej z trzech powodów:

-   Wiele małych talii oznacza, że nauka będzie odbywała się w pewnej kolejności. Choćby ze względu na to, że będziesz klikał po kolei poszczególne talie, albo nawet, gdy talie będą uporządkowane w strukturze drzewa to talie prezentowane będą w całości tzn. wszystkie karty z talii "angielski zwierzęta", a następnie z talii "…rozdział 1". Takie przeglądanie kart znacząco ułatwia naukę, co z kolei ma wpływ na jakość zapamiętanych informacji. W sytuacji, w której będziesz zmuszony przypomnieć sobie daną informację nie będziesz miał przecież możliwości przywołania w głowie kolejności, w której ta karta pojawiła się podczas nauki.

-   Anki nie jest zaprojektowane do obsługi bardzo wielu talii (więcej niż kilku tuzinów) i może dojść do spowolnienia całego programu - szczególnie jeśli uczysz się na kliencie mobilnym. Kilka dodatkowych talii nie sprawi wielkiej różnicy, jednak jeżeli stworzysz ich zbyt dużo opóźnienie może stać się odczuwalne.

Lepszym pomysłem od tworzenia wielu małych talii jest użycie Etykiet czyli tzw. tagów i/lub pól do klasyfikacji zawartości kolekcji. Przykładowo zamiast tworzyć talię "angielski zwierzęta", możesz dodać te notatki do głównej talii "angielski" i otagować je jako "zwierzęta" i "rzeczowniki". Notatki mogą posiadać wiele różnych tagów, co w przyszłości, po szybkim przefiltrowaniu zwartości talii lub nawet całej kolekcji umożliwi ci np. naukę tylko rzeczowników albo tylko nazw zwierząt lub rzeczowników związanych ze zwierzętami.

Dla tych którzy chcą mieć wszystko naprawdę dobrze zorganizowane - do tego celu przeznaczyć można również pola notatek. Stwórz pole o nazwie "książka" lub "strona" i dodawaj w nich tytuły książek i numery stron z których pochodzą dane informacje. Takie działanie jest możliwe bo Anki w pełni wspiera przeszukiwanie pól, co oznacza że możesz przeszukiwać talię na przykład w taki sposób: "książka:"moja książka" strona:63" i natychmiast znajdziesz to czego szukasz.

Szczególnie użyteczne są funkcje ["Nauka własna" oraz "talia filtrowana"](filtered-decks.md), przy użyciu których możesz tworzyć tymczasowe talie na podstawie określonych kryteriów przeszukiwania. Funkcje te pozwalają na naukę różnego rodzaju informacji wymieszanych ze sobą w jedną talię, ale mogą również tworzyć bardzo szczegółowe talie, kiedy musisz przygotować się z jakiegoś konkretnego zakresu materiału, np. przed egazminem. Ogólna zasada jest taka, że jeżeli danych informacji chcesz zawsze uczyć się oddzielnie, powinny one być zebrane w jednej talii. Jeżeli jednak tych informacji chcesz uczyć się tylko od czasu do czasu oddzielnie (np. mając zaległości z jakiegoś materiału do testu) to do tego celu powienieneś wykorzystać etykiety/pola i talie filtrowane.

Funkcje
--------

Okno edycji jest wyświetlane podczas [dodawania notatek](editing.md), [edytowania notatek](studying.md) w czasie powtórki lub w [przeglądarce](browsing.md).

W jego górnym lewym rogu znajdują się dwa przyciski, które otwierają okna [pola](editing.md#customizing-fields) oraz [karty](templates/intro.md).

Po prawej stronie umieszczone są przyciski edycji (formatowania) tekstu. Pogrubienie, kursywa oraz podkreślenie działają dokładnie w ten sam sposób co w standardowych edytorach tekstu. Kolejne dwa przyciski pozwalają na dodanie przypisu dolnego i górnego, które są szczególnie przydatne w czasie wpisywania wzorów chemicznych w postaci sumarycznej np. H<sub>2</sub>O lub prostych wzorów matematycznych np. x<sup>2</sup>.

Przycisk Fx jest odpowiedzialny za czyszczenie formatowania aktualnie zaznaczonego tekstu, włącznie z kolorem, pogrubieniem itd.

Następne dwa przyciski pozwalają na zmiane koloru tekstu.

Przycisk \[…​\] jest widoczny gdy wybrana jest notatka typu "Luka".

Spinacz służy do dodawania nagrań audio, obrazów oraz plików wideo do notatek z dysku twardego. Możesz również skopiować pliki multimedialne do schowka twojego komputera (na przykład poprzez kliknięcie prawym przyciskiem na obrazku w przeglądarce  internetowej i wybierając "Kopiuj obraz") i wkleić je do wybranego przez Ciebie pola. Aby dowiedzieć się więcej o plikach, zobacz rozdział [pliki](media.md).

Ikona mikrofonu pozwala nagranie dźwieku z mikrofonu i dodanie go do notatki.

Ostatni przycisk umożliwia dodanie do notatki zaawansowanych równań matematycznych (oraz ich edycję) przy użyciu języka znaczników [LaTeX](math.md) lub MathJax oraz edycję kodu HTML danego pola.

Większość z opisanych tutaj przycisków posiada własne skróty klawiszowe. Aby je zobaczyć wystarczy, że najdziesz kursorem myszy na dany przycisk. 

Wklejając tekst Anki domyślnie usunie większość formatowania. Jesli podczas tej czynności przytrzymasz przycisk shift, Anki postara się zatrzymać wiecej formatowania.

Wypełnianie luki
--------------

Wypełnianie luki polega na ukryciu jednego lub większej liczby słów w zdaniu. Przykładowe zdanie:

    Mieszko I przyjął chrzest Polski w 966 roku.

…​Teraz tworzymy lukę dla roku 966. Zdanie będzie wyglądało następująco:

    Mieszko I przyjał chrzest Polski w [...] roku.

Aby dowiedzieć się więcej o tym dlaczego warto używać wypełniana luki, zobacz zasadę numer 5 [tutaj](http://www.supermemo.com/articles/20rules.htm).

Anki posiada wbudowany typ notatki o nawie Luka, dzięki któremu możliwe jest łatwe tworzenie luki w notatce. Aby stworzyć taką właśnie notatkę, w oknie Dodaj wybierz typ notatki Luka i w polu Tekst wpisz jakieś zdanie. Następnie zaznacz myszą słowo lub słowa, które chcesz ukryć i naciśnij przycisk \[…​\]  znajdujący się na belce edycji tekstu. Anki zastąpi tym samym zaznaczony tekst w następującą formułą:
Anki will replace the text with:

    Mieszko I przyjął chrzest Polski w {{c1::966}} roku.

Symbol "c1" oznacza, że stworzyłeś w tym zdaniu jedną lukę. Możesz oczywiście stworzyć ich więcej. Przykładowo jeśli wybierzesz słowo "Mieszko" i znowu naciśniesz \[…​\], zdanie to będzie wyglądało tak:

    {{c2::Mieszko I}} przyjął chrzest Polski w {{c1::966}} roku.

Jeśli dodasz powyższą notatkę do talii, Anki wygeneruje dwie karty. Pierwsza z nich to:

    Mieszko I przyjął chrzest Polski w [...] roku

…​jako pytanie, a jako odpowiedź - pełne zdanie z uzupełnionym rokiem. Pytanie drugiej karty będzie wyglądało tak:

    [...] przyjął chrzest Polski w 966 roku.

You can also elide multiple sections on the same card. In the above
example, if you change c2 to c1, only one card would be created, with
both Canberra and 1913 hidden. If you hold down alt (option on a Mac)
while creating a cloze, Anki will automatically use the same number
instead of incrementing it.

Cloze deletions don’t need to fall on word boundaries, so if you select
“anberra” rather than “Canberra” in the above example, the question
would appear as “C\[…​\] was founded in 1913”, giving you a hint.

You can also give yourself hints that don’t match the text. If you
replace the original sentence with:

    Canberra::city was founded in 1913

…​and then press \[…​\] after selecting "Canberra::city", Anki will
treat the text after the two colons as a hint, changing the text into:

    {{c1::Canberra::city}} was founded in 1913

When the card comes up for review, it will appear as:

    [city] was founded in 1913.

For information on testing your ability to type in a cloze deletion
correctly, please see the section on [typing answers](templates/fields.md#checking-your-answer).

Please note that overlapping clozes are not supported. For example, the
following field is invalid:

    {{c1::Canberra was {{c2::founded}}}} in 1913

If you need to create clozes from overlapping text, add another Text
field to your cloze, add it to the [template](templates/intro.md), and then when
creating notes, paste the text into two separate fields, like so:

    Text1 field: {{c1::Canberra was founded}} in 1913

    Text2 field: {{c2::Canberra}} was founded in 1913

The default cloze note type has a second field called Extra, that is
shown on the answer side of each card. It can be used for adding some
usage notes or extra information.

The cloze note type is treated specially by Anki, and cannot be created
based on a regular note type. If you wish to customize it, please make
sure to clone the existing Cloze type instead of another type of note.
Things like formatting can be customized, but it is not possible to add
extra card templates to the cloze note type.


Inputting Foreign Characters and Accents
----------------------------------------

All modern computers have built in support for typing accents and
foreign characters, and multiple ways to go about it. The method we
recommend is using a keyboard layout for the language you want to learn.

Languages with a separate script like Japanese, Chinese, Thai and so on
have their own layouts specifically for that language.

European languages that use accents may have their own layout, but can
often by typed on a generic "international keyboard" layout. These work
by typing the accent, then the character you want accented - eg an
apostrophe (') then the letter a (a) gives á.

To add the international keyboard on Windows machines, please see
<https://support.microsoft.com/en-au/kb/306560>

To add it on Macs, please see
<http://www.macworld.com/article/1147039/os-x/accentinput.html>

Keyboards for a specific language are added in a similar way, but we can
not cover them all here. For more information, please try searching
Google for "input Japanese on a mac", "type Chinese on Windows 10", and
so on.

If you’re learning a right to left language, there are lots of other
things to consider. Please see [this
page](http://dotancohen.com/howto/rtl_right_to_left.html) for more
information.

The toolkit Anki is built on has trouble dealing with a few input
methods, such as holding down keys to select accented characters on Mac
OS X, and typing characters by holding down the alt key and typing a
numeric code on Windows.
