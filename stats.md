Wykresy i statystyki
=====================

Informacje o karcie
---------

Możesz wyświetlić informację o karcie klikając na przycisk "Informacje" w pasku narzędzi podczas przeglądania. Większość pokazywanych informacji nie wymaga wytłumaczenia, oprócz:

**Pozycja**  
Pokazywana tylko, gdy karta jest nowa. Pokazuje miejsce w kolejce,  do wyświetlenia karty w stosunku do innych nowych kart. Może zostać zmieniona w przeglądarce.

**Przerwa**  
Różnica między jedną powtórką, a nastepną. The delay from one review to the next. Nazwy są skrócone; "0s, 1m,
3g, 4d, 5mc, 6r" oznacza kolejno: sekundy, minuty, godziny, dni, miesiące, lata.

**Łatwość**  
Przybliżona ilość, o jaką wzrośnie przerwa po odpowiedzi "Dobra" na kartę.

Statystyki
----------

Okno statystyk dostępne jest pod przyciskiem "Statystyki" znajdującym się u góry okna głównego Anki lub za pomocą klawisza T. . Okno statystyk pokaże statystki z aktualnie wybranej talii i talii podrzędnych. Dane dotyczące całej kolekcji dostępne są po wybraniu "kolekcja" u góry okna statystyk. W Anki 2.1.28+ można również wyświetlać wykresy dla dowolnych wyszukiwań poprzez dodawanie filtrów w polu wyszukiwania.

Anki 2.1.28+ wprowadza nowe, przeprojektowane wykresy. Stare wykresy dalej są dostępne, poprzez przytrzymanie przycisku Shift podczas podczas otewierania statystyk (klikniecia na przycisk "Statystyki").i

W Anki 2.1.28+, anki będzie domyślnie pokazywać statystyki z ostatniego roku. Możesz zmienić tę opcję na klikając na "cała historia" lub "czas życia talii" u góry. (Nie wpływa to na wygląd statystyk w sekcji "Dzisiaj") 

W starszych wersjach Anki będzie domyślnie pokazywać statystyki dla ostatniego miesiąca. Możesz zmienić to do okresu ostatniego roku lub czasu życia talii  klikając odpowiedni przycisk na dole ekranu. (Nie wpływa to na wygląd statystyk w sekcji "Dzisiaj") 

Kliknięcie na "Zapisz jako PDF" zapisze dokument pdf ze statystykami jako plik na twoim pulpicie, aby łatwież można było udostępniać swoje statystyki z innymi.

Gdy usuwasz notatki, ich historia powtórek jest zatrzymywana w Anki. Nie będa one załączone  podczas przeglądania  statystyk określonej talii (jako, że Anki nie może sprawdzić do jakiej talii należała usunięta karta), jednak ich historia będzie pokazywana podczas przeglądania statystyk dla całej kolekcji.

Typy kart
--------------

W oknie Statystki czasami mogą być użyte terminy i nazwy, których jeszcze nie znasz:

**Dojrzałe**  
Karty, których przerwa wynosi 21 dni lub więcej.

**Młode**  
Karta młoda to taka, której przerwa jest krótsza niż 21 dni i nie uczysz się jej, a jedynie powtarzasz.

**Uczone**  
Karty nowe, których jeszcze się nie nauczyłeś

**Uczone ponownie**  
Karty dojrzałe lub młode, które w czasie powtórki otrzymały ocenę Powtórz i będziesz się ich uczył ponownie.

**Niewidziane**  
Karty, które zostały niedawno dodane do twojej kolekcji, ale nie zostały ci jeszcze wyświetlone do nauki. Można je nazywać również kartami nowymi, zwłaszcza gdy są w kolejce nowych kart do pokazania pierwszy raz.

Dzisiaj
-----

Na górze okna statystyk znajduje się krótka lista statystyk tekstowych powtórek, które ukończono dzisiaj. "Powtórka" w tym kontekście oznacza "jedną odpowiedź dla karty", więc karta może liczyć się jako kilka powtórek, jeśli była pokazana kilka razy, a karty uczone równiez sa liczone jako "powtórka". Kilka terminów, które mogą na pierwszy rzut oka być niezrozumiałe:

**Liczba pomyłek**  
Liczba powtórek, na które odopwiedziano błędnie (to znaczy naciśnięto przycisk "Powtórz"). Pokazywany procent to liczba kart, na które nie odpowiedziano "Powtórz" podzielona przez całkowitą liczbę kart, których się uczono.

**Uczone, Powtarzane, Uczone ponownie, Filtrowane**  
Liczba powtórek, które były kartami uczonymi, powtarzanymi, uczonymi ponownie lub, które nie oczekiwały, a były uczone w talii filtrowanej.

Statystyki z danego dnia nie są dobrym wskaźnikiem postepów w nauce. Każdy ma lepsze i gorsze dni, a widzac, że procent poprawnych odpowiedzi jest mniejszy w danym dniu nie powinien niepokoić. Pozostałe statystyki, które biorą pod uwagę dłuższy okres czasu, będa dawały bardziej prawdziwy obraz postpępów w nauce, i będą bardziej przydatne,jeśli chciałbyś zmienic nawyki nauki lub opcje planowania bazując na twojej wydajności.

Na statystyki "dzisiaj" nie ma wpływu wybrany okres czasu u góry ekranu.

Wykresy
----------

**Prognoza**  
Wykres wyświetla przybliżoną liczbę kart, które będą powtarzane w przyszłości, bez uwzględnienia kart nowych i uczonych na nowo. Do osi pionowej z lewej strony odnosi się wykres słupkowy. Kolumny oznaczają liczbę kart, które zostaną wyświetlone do powtórki w kolejnych dniach. Do osi pionowej z prawej strony odnosi się wykres ciągły, na którym przedstawiona jest skumulowana liczba powtórek. Wykres prognozy nie uwzględnia kart zaległych, które nagromadziły się w wyniku np. kilkudniowej przerwy w pracy z Anki. Te karty nie są widoczne na wykresie. Aby karty zaległe były widoczne, kliknij przycisk "Zaległości".

**Liczba powtórek**  
Wykres przedstawia liczbę kart powtórzonych w przeszłości. Słupki mogą odpowiadać dniom, tygodniom lub miesiącom, w zależności od okresu jaki wybrałeś na u góry ekranu statystyk. Poszczególne kolory pokazują ile z kart, na które udzieliłeś odpowiedzi było [dojrzałe](stats.md#types-of-cards), młode, uczone i uczone ponownie. Jest także oddzielna grupa kart, na które udzieliłeś odpowiedzi w ramach talii filtrowanej. Prawa pionowa oś, do której przypisany jest wykres liniowy wskazuje skumulowaną liczbę odpowiedzi na karty od daty początku wykresu.


**Review Time**  
Wykres ten należy interpretować w ten sam sposób co "Liczba powtórek", jednakże jednostką jest tutaj czas spędzony na powtórce.

**Przerwy**  
Wykres pokazuje liczbę kart o określonym interwale (czyli przerwie, odsunięciu w czasie pomiędzy dwoma powtórkami). Na prawej osi wyrażono procentowo liczbę kart, które mają interwał równy lub mniejszy od wartości na tej osi. Zauważ, że pozioma oś czasu w przypadku tego wykresu okresla on, w jakim okresie czasowym w przyszłości mają byc wyświetlane przerwy, a nie jak w innych wykresach, jaki okres czaus nauki jest uwzględniany. Innymi słowy, na tym wykresie nie są przedstawione dane historyczne, ale dane o przyszłości. Wybrany okres czasu określa, jak dalekie przerwy są wyświetlane (a więc przerwa 14-sto miesięczna nie bedzie wyświetlona na wykresie obejmującym jeden rok)

**Podział godzinowy**  
Wykres przedstawia odsetek poprawnych odpowiedzi na powtarzane karty w różnych porach dnia. Większe, ciemniejsze słupki i lewa oś określają liczbę poprawnie odpowiedzianych kart w danej godzinie, zaś cieńszy, szary słupek i prawa oś odpowiadają za ogólną liczbę powtórek w danej godzinie (wiesz tym samym na ile wydajne są powtórki w poszczególnych godzinach dnia).

**Przyciski odpowiedzi**  
Wykres pokazuje ile razy wybrałeś Powtórz, Trudna, Dobra i Łatwa w stosunku do kart uczonych, młodych i [dojrzałych](stats.md#types-of-cards). Anki wyświetla również procent poprawnych odpowiedzi dla każdego typu kart.

**Typy kart**  
Ten Wykres przedstawia udział procentowy kart dojrzałych, niewidzianych, młodych/uczonych i zawieszonych w twojej talii. Po najechaniu  myszką na wykres widoczna jest dokładna liczba kart każdego z typów, jeżeli chciałbyś dokładniej policzyć te wartości. Liczba wszystkich kart w talii dostępna jest równiez po najechaniu myszą na wykres.

Analiza ręczna
---------------

Jeśli chciałbys uzyskać więcej informacji o statystykach, niż zapewnia Anki, można to zrobić poprzez bezpośredni dostęp do danych. JAko, że jest to skomplikowane, nie możemy zapewnić żadnego wsparcia dla tej czynności.

Jedną z opcji jest [napisanie dodatku](addons.md), który dodaje kolejny wykres lub wiecej szczegółów w oknie statystyk. Istnieje kilka dodatków tegotypu na AnkiWeb. Możesz je przejrzeć, żeby zobaczyć, jak one działają.

Bardziej skutecznym i skomplikowanym sposobem jest wyodrębnienie dziennika powtórek bezpośrednio z dany bazych Anki i jego analiza przez zewnętrzny program. Anki używa bazy danych nazwanej "SQLite". Istnieje wiele nażędzi do pracy z bazami danych SQLite; jednym z najłatwiejszych na poczatek jest [SQLite Browser](http://sqlitebrowser.org/), który pozwoli ci przemieszczać się po bazie danych oraz eksportować wersję CSV tabeli, aby zaimportować je do innego pogramu. 

Najważniejszą tabelą dla statystyk jest tabela "revlog", która przechowuje wpis każdej wykonanej powtórki. Opis zawartych kolumn:

**id**  
The time at which the review was conducted, as the number of
milliseconds that had passed since midnight UTC on January 1, 1970.
(This is sometimes known as 'Unix epoch time', especially when in
straight seconds instead of milliseconds.)

**cid**  
The ID of the card that was reviewed. You can look up this value in the
id field of the 'cards' table to get more information about the card,
although note that the card could have changed between when the revlog
entry was recorded and when you are looking it up. It is also the
millisecond timestamp of the card’s creation time.

**usn**  
This column is used to keep track of the sync state of reviews and
provides no useful information for analysis.

**ease**  
Which button you pressed at the end of the review (1 for Again, 4 for
Easy).

**ivl**  
The new interval that the card was pushed to after the review. Positive
values are in days; negative values are in seconds (for learning cards).

**lastIvl**  
The interval the card had before the review. Cards introduced for the
first time have a last interval equal to the Again delay.

**factor**  
The new ease factor of the card in permille (parts per thousand). If the
ease factor is 2500, the card’s interval will be multiplied by 2.5 the
next time you press Good.

**time**  
The amount of time (in milliseconds) you spent on the question and
answer sides of the card before selecting an ease button.

**type**  
This is 0 for learning cards, 1 for review cards, 2 for relearn cards,
and 3 for early "cram" cards (cards being studied in a filtered deck when they
are not due).
