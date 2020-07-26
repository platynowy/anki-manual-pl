# Przeglądarka

Okno przeglądarki pozwala ci przeszukiwac twoje karty i notatki oraz je edytowac. JEst otwierane poprzez klikniecie *Przeglądaj* na ekranie głównym, lub naciśnięcie *b* na klawiaturze. Składa się ono z trzech sekcji: *pasku bocznego* po lewej, *listy kart* u góry po prawej, oraz *obecnej notatki*, na dole po prawje. Ustawiając myszkę pomiędzy dwoma sekcjami możliwe jest kliknięcie i przeciąganie, przez co można zmieniac wielkość każdej z sekcji.

Pasek boczny
-------

Pasek boczny po lewej pozwala na szybki dostęp do czesto szukanych terminów. Klikniecie na obiekcie wyszuka go.

Możesz przytrzymać Ctrl (Command na Maku) podczas klikania, aby dodac klikany przedmiot do obecnego wyszukiwania używając warunku AND, zamiast zaczynać nowe wyszukiwanie. Jeśli chciałbyś wyszukać karty uczone które byłyby równiez w talii Niemiecki, mógłbyś kliknąć na "Uczone", a następnie Ctrl+kliknąć na "Niemiecki".

Możesz przytrzymac Shift aby utworzyć wyszukiwanie OR zamiast AND. Na przykład, mógłbys kliknać na jedną talię, a potem kliknać z przytrzymanym shiftem na inną, aby pokazać karty z obu talii w jednym podglądzie.

Możesz przytrzymac Alt (Option na Maku), aby odwrócić wyszukiwanie (dodać *-*) - na przykład, abhy pokazać wszystkie karty w obecnej talii, które *nie* mają określonej etykiety. Alt/option moga być łączone z Ctrl lub shift (np. Ctrl-Alt i klikniecie spowoduje dodanie nowego wyszukiwanego terminu, który jest negowany). 

Aby usunąć talie, które nie są używane przez żadne notatki, wybierz z ekranu głównego  Narzedzia&gt;Sprawdź bazę danych.

Wyszukiwanie
---------

Nad listą kart znajduje się pole do wyszukiwania. Możesz wpisywać tam różne rzeczy, aby wyszukiwać karty. Aby dowiedzieć się więcej informacji, zobacz [rozdział o wyszukiwaniu] 

Lista kart
---------

Lista kart wyświetla wyniki obecnego wyszukiwania,

Kolumny można dostosować: kliknij prawym przyciskiem na jednej z nich ( lub używjaąc ctrl i kliknięcie na Maku), aby wybrać, które kolumny mają być widoczne. Możesz przeciągać kolumny, aby je uporzadkować. Kliknięcie na kolumnie spowoduje sortowanie na podstawie tej kolumny; klikniecie ponowne odwróci kolejność sortowanie. Wyników wyszukiwania nie mozna sortować na podstawie niektórych kolumn.

Kolumna "oczekujące" zachowuje się inaczej dla każdego typu kart. Nowe karty pokazuja numer zamiast daty, który wskazuje kolejność prezentowania nowych kart. Karty uczone (ponownie) oraz powtórki pokazują  date, jednak podczas sortowania są grupowane najpierw ze względu na typ, a nastepnie ze względu na datę.

Kolumny "notatka zmodyfikowana" i "karta zmodyfikowana" brzmią podobnie, ale śledzą inne rzeczy. "Notatka zmodyfikowana" śledzi ostatni czas, kiedy w *notatce* dokonano zmian (np. gdy zwawartość pola została zedytowana) podczas gdy "karta zmodyfikowana" śledzi ostatni czas, kiedy w *karcie* dokonano zmian (np. gdy powtarzałeś kartę i historia powtó®ek oraz przerwa zostały zaktualizowane).

Gdy klikasz na karte, jej notatka zostanie pokazana w dolnej części ekranu. Jeśli przeciagniesz mysz lub przytrzymasz ctrl lub command, aby wybrac kilka kart, edytor będzie czasowo ukryty. Różne operajce (jak zmiana talii) można wykonywać na wielu kartach na raz.

Kolor tła zmienia się w zależności od karty. Karty wyróznione są w kolorze fioletowym, karty zawieszone w koloerze żółtym. Aby dowiedzieć się więcej o kartach wyróznionych i zawieszonych, zobacz [edytowanie i więcej].(studying.md)

Jedną z dostępnych kolumn jest *sortuj pole*. Anki umożliwia na wybranie jednego pola z kazdego typu notatki do sortowania. Możesz zmienić pole sortowania klikając na "Pola…​" w sekcji wybranej notatki.

Kolumny pytania i odpowiedzi pokazują to, co zobaczyłbyś w  pytaniu i odpowiedzi podczas nauki, z wyjatkiem tego, że kolumna "odpowiedź" usunie cześć z. pytaniem, aby była ona czytelniejsza. Możesz równiez wybrać [własny format](templates/styling.md#browser-appearance) w edytorze typów kart, zamiast pokazywać to, zobaczyłbys w czasie nauki

Obecna notatka
------------

Na dole po prawej stronie znajduje się notatka obecnie wybranej karty. Aby dowiedzieć się więcej o kartach i notatkach, zobacz [podstawy](getting-started.md). Jeśli chcesz dowiedzieć się więcej o przyciskach formatowania, zobacz rozdział o [edytowaniu](editing.md).

Możesz zobaczyć podgląd tego, jak obecnie wybrana karta wyglądałby podczas powtórki, klikając na przycisk "podgląd" obok pola wyszukiwania. Zauważ, że nie wyświetli na twoich kartach żadnych pól zawierających pisanie odpowiedzi, co sprawia, że podgląd kart jest łatwiejszy.

Menu
----

U góry okna znajduje się menu. Możesz szybko uzyskac do niego dostęp poprzez kliknięcie prawym klawiszem myszy (lub command+ klikniecie prawym klawiszem myszy na Maku) na obszarze z listą kart.

*Informacje* pokazuje różne informacje o obecnie wybranej karcie, włącznie z historią powtórek. Aby dowiedzieć się więcej, zobacz rozdział o [statystykach].

*Przełącz wyróżnienie* i *Przełącz Zawieszenie* zostały opisane w rozdziale [edytowanie i więcej](studying.md).

*Zmień talię* umożliwia przenoszenie kart do innej talii. Karty mogą być umieszczone w różnych taliach, więc jesli chcesz przenieść wszystkie karty w notatce, powinieneś najpierw uzyć opcji Edytuj &gt; Wybierz notatki.

*Dodaj etykiety* oraz *Usuń etykiety* umożliwia masowe dodawanie lub usuwanie etykiet z notatek.

*Usuń* usuwa wybraną kartę (lub karty) i ich notatki. Nie jest możliwe usuwanie pojedyńczych kart, jako, że są one pod kontrolą [szablonów](templates/intro.md). 

Znajdź i zamień
----------------

Ta opcja (Notatki→Znajdź i zamień…​) umożliwia zamienić tekst w notatkach, które zaznaczyłeś. Dzięki Wyażeniu regularnemi można przeprowadzać zaawansowane zamienianie tekstu. Na przykład, jeśli w polu znajduje się tekst: 

    <img src="pic.jpg" />

Wyszukując:

    <img src="(.+?)" />

i w Anki 2.1.28 zamieniając na:

     ${1}

 w starszych wersjach Anki , zamieniając na:

    \1

Zmieni tekst w karcie na:

    pic.jpg

Pełny opis wyrażeń regularnych nie jest cześcią tej instrukcji. W sieci znajduje się wiele poradników. Aby dowiedzieć się o składni w 2.1.28+, zobacz:  <https://docs.rs/regex/1.3.9/regex/#syntax>. Dla starszych wersji Anki zobacz: <http://docs.python.org/library/re.html>.

Znajdowanie duplikatów
------------------

Możesz używać opcji Notatki→Znajdź Duplikaty, aby wyszukiwac notatki, które maja w sobie tę sma zawartość. Gdy otwierasz okno, Anki przejrzy wszystkie twoje typy notatki i wyświetli listę wszystkich możliwych pól. Jeśli chcesz szukać duplikatów w polu "Tył", wybierz je z listy, a następnie naciśnij "Szukaj".

W przeciwieństwie do sprawdzania odbywającego się przy ręcznym dodawaniu kart, opcja znajdowania duplikatów nie jest ograniczana do jednego typu notatki. to oznacza, że domyslnie będzie przszukiwać wszystkie typy notatek, które posiadają pole, które wybrałeś.

Opcja *opcjonalny filtr* pozwala na zawężenie, gdzie Anki ma szukać duplikatów. Jesli chcesz szukać duplikatów w typach notatek "Francuski Słownictwo" i "Francuski czasowniki", wpisałbyś: 

    note:'francuski słownictwo' or note:'french czasowniki'

Lub jesli chcesz szukac duplikatów tylko w określonej talii wpisz (mojaTalia = nazwa twojej talii):

    deck:'mojaTalia'

Sposoby wyszukiwania są takie same jak w przeglądarce. Zobacz rozdział o [wyszukiwaniu](searching.md), aby dowiedzieć się więcej.

Możesz kliknąc na jednym z linków, które pojawiły się w wynikasz wyszukiwania, aby wyświetlić zduplikowane notatki w tym zestawie. Jeśli podczas wyszukiwania znaleziono duża liczbę duplikatów, możesz kliknć przycisk "Nadaj etykiety duplikatom", który doda etykiety "duplicate" do wszystkich znalezionych notatek. Możesz wyszukiwać za pomoca tej etykiety w przegladarce, aby zając  wszystkimi dyplikatami na jednym ekranie.

Inne elementy menu
----------------

Inne elementy menu to:

*Zmień plan*, umożliwia przenoszenie kart na koniec kolejki nowych kart, lub ustawienie nowej daty powtórki. Druga opcja jest przydatna, gdy zaimportowałeś  już uczony materiał i chcesz zacząć się go uczyć go z wyższymi początkowymi przerwami. Na przykład, wybierając 60 i 90 nada wszystkim zaimportowanym kartą poczatkową przerwę w wysokości 2 do 3 miesiecy

Historia zmian karty nie jest usuwana podczas zmiany planu: zmiana planu zmienia obecny stan karty, ale nie jej historię. Jeśli chcesz ukryć historię, będziesz musiał wyeksportować twoje notatki jako plik tekstowy, usunąć notatki, a nastepnie zaimportować ten plik tekstowy ponownie, tworzac nowe notatki.


*Zmień pozycję* umozliwia zmienić kolejność nowych kart. Możesz dowiedzieć się obecnych pokzycji włączając kolumnę *oczekujące*, jak to zostało opisane w sekcji "lista kart". Jeśli uruchomisz tę opcję podczas gdy wybranych jest wiele kart, nada ona każdej karcie po kolei rosnące numery. Domyslnie numer zwiększa się o jeden dla każdej karty w turze, ale może to zostać zmienione zmieniając opcję "krok". 

Opcja *Zmień pozycję istniejacych kart* umożliwia wstawianie kart miedzy juz istniejące, wypychając już istniejace z dala od siebie. Na przykład jeśli masz 5 karti chcesz przenieść 3,4 i 5 między 1 i 2, wybranie tej opcji sprawi, że kolejnośc kart wygladałaby tak: 1, 3, 4, 5, 2. Jeśli za to wyłączyć tę opcje, 2 i 3 otrzymają taki sam numer pozycji (i ich kolejnosć pojawienia będzie losowa).

*Zmień typ notatki* umożliwia przekonwertowanie wybrane notatki z jednej do drugiej. Na przykład, masz typ notatki "Rosyjski" oraz "Komputer" i przypadkowo dodałeś  tekst dodyczący komputerów do notatki "Rosyjski". Możesz to naprawić używając tej opcji. Nie ma ona wpływu na planowanie krt.

*Wybierz notatki* na podstawie wybranych kart, znajduje ich notatki, a nastepnie wybiera wszystkie karty tych notatek. Jesli twoje notatki mają tylko jedną kartę, opcja ta nie zadziała.

Menu *Idź* umożliwia używanie skrótów klawiszowych, aby przechodzić do róznych cześci przeglądarki, oraz żeby poruszac się w górę i w dół w liście kart.
