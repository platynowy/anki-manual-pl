# Przeglądarka

Okno przeglądarki pozwala Ci przeszukiwac twoje karty i notatki oraz je edytować. Jest otwierane poprzez kliknięcie *Przeglądaj* na ekranie głównym, lub naciśnięcie *b* na klawiaturze. Składa się ono z trzech sekcji: *pasku bocznego* po lewej, *listy kart* u góry po prawej, oraz *obecnej notatki*, na dole po prawej. Ustawiając myszkę pomiędzy dwoma sekcjami możliwe jest kliknięcie i przeciąganie, przez co można zmieniac wielkość każdej z sekcji.

Pasek boczny
-------

Pasek boczny po lewej pozwala na szybki dostęp do często szukanych informacji. Kliknięcie na obiekcie wyszuka go.

Możesz przytrzymać Ctrl (Command na Maku) podczas klikania, aby dodać klikany przedmiot do obecnego wyszukiwania używając warunku AND, zamiast wyszukiwać od nowa. Jeśli chciałbyś wyszukać karty uczone, które byłyby równiez w talii Niemiecki, mógłbyś kliknąć na "Uczone", a następnie Ctrl+kliknąć na "Niemiecki".

Możesz przytrzymać Shift, aby utworzyć wyszukiwanie OR zamiast AND. Na przykład, mógłbys kliknać na jedną talię, a potem kliknać z przytrzymanym shiftem na inną, aby pokazać karty z obu talii w jednym podglądzie.

Możesz przytrzymac Alt (Option na Maku), aby odwrócić wyszukiwanie (dodać *-*) - na przykład, aby pokazać wszystkie karty w obecnej talii, które *nie* mają określonej etykiety. Alt/Option moga być łączone z Ctrl lub Shift (np. Ctrl-Alt i kliknięcie spowoduje dodanie nowego wyszukiwanego terminu, który jest negowany). 

Aby usunąć etykiety, które nie są używane przez żadne notatki, wybierz z ekranu głównego Narzedzia&gt;Sprawdź bazę danych.

Wyszukiwanie
---------

Nad listą kart znajduje się pole do wyszukiwania. Możesz wpisywać tam różne rzeczy, aby wyszukiwać karty. Aby dowiedzieć się więcej informacji, zobacz [rozdział o wyszukiwaniu](searching.md).

Lista kart
---------

Lista kart wyświetla wyniki obecnego wyszukiwania.

Kolumny można dostosować: kliknij prawym przyciskiem na jednej z nich (lub używjąc ctrl i kliknięcie na Maku), aby wybrać, które kolumny mają być widoczne. Możesz przeciągać kolumny, aby je uporządkować. Kliknięcie na kolumnie spowoduje sortowanie na podstawie tej kolumny; klikniecie ponowne odwróci kolejność sortowania. Wyników wyszukiwania nie można sortować na podstawie niektórych kolumn.

Kolumna "oczekujące" zachowuje się inaczej dla każdego typu kart. Przy Nowych kartach zamiast daty znajduje się numer, który wskazuje kolejność prezentowania nowych kart. Karty uczone (ponownie) oraz powtórki mają przypisaną datę, jednak podczas sortowania są grupowane najpierw ze względu na typ, a nastepnie ze względu na datę.

Kolumny "notatka zmodyfikowana" i "karta zmodyfikowana" brzmią podobnie, ale są odpowiedzialne za inne funkcje. "Notatka zmodyfikowana" śledzi ostatni czas, kiedy w *notatce* dokonano zmian (np. gdy zwawartość pola została zedytowana), podczas gdy "karta zmodyfikowana" śledzi ostatni czas, kiedy w *karcie* dokonano zmian (np. gdy powtarzałeś kartę i historia powtórek oraz przerwa zostały zaktualizowane).

Gdy klikasz na karte, jej notatka zostanie pokazana w dolnej części ekranu. Jeśli przeciagniesz myszą lub przytrzymasz ctrl (command), aby wybrać kilka kart, edytor będzie czasowo ukryty. Różne operajce (jak zmiana talii) można wykonywać na wielu kartach na raz.

Kolor tła zmienia się w zależności od karty. Karty wyróznione są w kolorze fioletowym, karty zawieszone w kolorze żółtym. Aby dowiedzieć się więcej o kartach wyróznionych i zawieszonych, zobacz rozdział [edytowanie i więcej](studying.md).

Jedną z dostępnych kolumn jest *sortuj pole*. Anki umożliwia na wybranie jednego pola do sortowania z każdego typu notatki. Możesz zmienić pole sortowania klikając na "Pola…​" w sekcji wybranej notatki.

Kolumny pytania i odpowiedzi pokazują to, co zobaczyłbyś w  pytaniu i odpowiedzi podczas nauki, z wyjatkiem tego, że kolumna "odpowiedź" usunie cześć z pytaniem, aby była ona czytelniejsza. Możesz równiez wybrać [własny format](templates/styling.md#browser-appearance) w edytorze typów kart, zamiast pokazywać to, co zobaczyłbyś w czasie nauki

Wybrana notatka
------------

Na dole po prawej stronie znajduje się notatka obecnie wybranej karty. Aby dowiedzieć się więcej o kartach i notatkach, zobacz [podstawy](getting-started.md). Jeśli chcesz dowiedzieć się więcej o przyciskach formatowania, zobacz rozdział o [edytowaniu](editing.md).

Możesz zobaczyć podgląd tego, jak obecnie wybrana karta wyglądałby podczas powtórki, klikając na przycisk "podgląd" obok pola wyszukiwania. Zauważ, że nie wyświetli na twoich kartach żadnych pól zawierających pisanie odpowiedzi, co sprawia, że podgląd kart jest łatwiejszy.

Menu
----

U góry okna znajduje się menu. Możesz szybko uzyskać do niego dostęp poprzez kliknięcie prawym klawiszem myszy (lub command + klikniecie prawym klawiszem myszy na Maku) na obszarze z listą kart.

*Informacje* pokazuje różne informacje o obecnie wybranej karcie, włącznie z historią powtórek. Aby dowiedzieć się więcej, zobacz rozdział o [statystykach](stats.md).

*Przełącz wyróżnienie* i *Przełącz Zawieszenie* zostały opisane w rozdziale [edytowanie i więcej](studying.md).

*Zmień talię* umożliwia przenoszenie kart do innej talii. Karty mogą być umieszczone w różnych taliach, więc jeśli chcesz przenieść wszystkie karty w notatce, powinieneś najpierw uzyć opcji Edytuj &gt; Wybierz notatki.

*Dodaj etykiety* oraz *Usuń etykiety* umożliwia masowe dodawanie lub usuwanie etykiet z notatek.

*Usuń* usuwa wybraną kartę (lub karty) i ich notatki. Nie jest możliwe usuwanie pojedynczych kart, jako, że są one pod kontrolą [szablonów](templates/intro.md). 

Znajdź i zamień
----------------

Ta opcja (Notatki→Znajdź i zamień…​) umożliwia zamienić tekst w notatkach, które zaznaczyłeś. Dzięki wyażeniom regularnym można przeprowadzać zaawansowane zamienianie tekstu. Na przykład, jeśli w polu znajduje się tekst: 

    <img src="pic.jpg" />

Wyszukując:

    <img src="(.+?)" />

i w Anki 2.1.28 zamieniając na:

     ${1}

 w starszych wersjach Anki, zamieniając na:

    \1

Zmieni tekst w karcie na:

    pic.jpg

Pełny opis wyrażeń regularnych nie jest cześcią tej instrukcji. W sieci znajduje się wiele poradników. 
Aby dowiedzieć się o składni w 2.1.28+, zobacz:  <https://docs.rs/regex/1.3.9/regex/#syntax>. 
Dla starszych wersji Anki zobacz: <http://docs.python.org/library/re.html>.

Znajdowanie duplikatów
------------------

Możesz używać opcji Notatki→Znajdź Duplikaty, aby wyszukiwać notatki, które maja w sobie tę samą zawartość. Gdy otwierasz okno, Anki przejrzy wszystkie twoje typy notatkek i wyświetli listę wszystkich możliwych pól. Jeśli chcesz szukać duplikatów w polu "Tył", wybierz je z listy, a następnie naciśnij "Szukaj".

W przeciwieństwie do sprawdzania odbywającego się przy ręcznym dodawaniu kart, opcja znajdowania duplikatów nie jest ograniczana do jednego typu notatki. To oznacza, że domyślnie będzie przszukiwać wszystkie typy notatek, które posiadają pole, które wybrałeś.

Opcja *opcjonalny filtr* pozwala na zawężenie, gdzie Anki ma szukać duplikatów. Jeśli chcesz szukać duplikatów w typach notatek "Francuski Słownictwo" i "Francuski czasowniki", wpisałbyś: 

    note:'francuski słownictwo' or note:'french czasowniki'

Lub jeśli chcesz szukac duplikatów tylko w określonej talii, wpisz (mojaTalia = nazwa twojej talii):

    deck:'mojaTalia'

Sposoby wyszukiwania są takie same jak w przeglądarce. Zobacz rozdział o [wyszukiwaniu](searching.md), aby dowiedzieć się więcej.

Możesz kliknąć na jednym z linków, które pojawiły się w wynikasz wyszukiwania, aby wyświetlić zduplikowane notatki w tym zestawie. Jeśli podczas wyszukiwania znaleziono duża liczbę duplikatów, możesz kliknć przycisk "Nadaj etykiety duplikatom", który doda etykiety "duplicate" do wszystkich znalezionych notatek. Możesz wyszukiwać za pomoca tej etykiety w przegladarce, aby zająć wszystkimi duplikatami na jednym ekranie.

Inne elementy menu
----------------

Inne elementy menu, to:

*Zmień plan*, umożliwia przenoszenie kart na koniec kolejki nowych kart, lub ustawienie nowej daty powtórki. Druga opcja jest przydatna, gdy zaimportowałeś już uczony materiał i chcesz zacząć się go uczyć z wyższymi początkowymi przerwami. Na przykład, wybierając 60 i 90 nada wszystkim zaimportowanym kartą poczatkową przerwę w wysokości 2 do 3 miesiecy

Historia zmian karty nie jest usuwana podczas zmiany planu: zmiana planu zmienia obecny stan karty, ale nie jej historię. Jeśli chcesz ukryć historię, będziesz musiał wyeksportować twoje notatki jako plik tekstowy, usunąć notatki, a nastepnie zaimportować ten plik tekstowy ponownie, tworząc nowe notatki.

*Zmień pozycję* umozliwia zmienić kolejność nowych kart. Możesz dowiedzieć się obecnej pozycji włączając kolumnę *oczekujące*, jak to zostało opisane w sekcji "lista kart". Jeśli uruchomisz tę opcję podczas, gdy wybranych jest wiele kart, nada ona każdej karcie po kolei rosnące numery. Domyślnie numer zwiększa się o jeden dla każdej karty ale może to zostać zmienione, zmieniając opcję "krok". 

Opcja *Zmień pozycję istniejacych kart* umożliwia wstawianie kart miedzy juz istniejące, wypychając już istniejace z dala od siebie. Na przykład, jeśli masz 5 kart i chcesz przenieść karty numer  3,4 i 5 między 1 i 2, wybranie tej opcji sprawi, że kolejność kart wygladałaby tak: 1, 3, 4, 5, 2. Jeśli za to wyłączysz tę opcje, 1 i 2 otrzymają taki sam numer pozycji (przez co nie będzie można przewidzieć, która karta z tym samym numerem pojawi się pierwsza).

*Zmień typ notatki* umożliwia przekonwertowanie wybranej notatki z jednej do drugiej. Na przykład, masz typ notatki "Rosyjski" oraz "Komputer" i przypadkowo dodałeś tekst dodyczący komputerów do notatki "Rosyjski". Możesz to naprawić używając tej opcji. Nie ma ona wpływu na planowanie kart.

*Wybierz notatki* na podstawie wybranych kart, znajduje ich notatki, a nastepnie wybiera wszystkie karty tych notatek. Jeśli twoje notatki mają tylko jedną kartę, opcja ta nie zadziała.

Menu *Idź* umożliwia używanie skrótów klawiszowych, aby przechodzić do róznych części przeglądarki oraz, żeby poruszac się w górę i w dół na liście kart.
