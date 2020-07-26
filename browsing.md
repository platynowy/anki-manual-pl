# Przeglądarka

Okno przeglądarki pozwala ci przeszukiwac twoje karty i notatki oraz je edytowac. JEst otwierane poprzez klikniecie *Przeglądaj* na ekranie głównym, lub naciśnięcie *b* na klawiaturze. Składa się ono z trzech sekcji: *pasku bocznego* po lewej, *listy kart* u góry po prawej, oraz *obecnej notatki*, na dole po prawje. Ustawiając myszkę pomiędzy dwoma sekcjami możliwe jest kliknięcie i przeciąganie, przez co można zmieniac wielkość każdej z sekcji.

Pasek boczny
-------

Pasek boczny po lewej pozwala na szybki dostęp do czesto szukanych terminów. Klikniecie na obiekcie wyszuka go.

Możesz przytrzymać Ctrl (Command na Maku) podczas klikania, aby dodac klikany przedmiot do obecnego wyszukiwania używając warunku AND, zamiast zaczynać nowe wyszukiwanie. Jeśli chciałbyś wyszukać karty uczone które byłyby równiez w talii Niemiecki, mógłbyś kliknąć na "Uczone", a następnie Ctrl+kliknąć na "Niemiecki".

Możesz przytrzymac Shift aby utworzyć wyszukiwanie OR zamiast AND. NA przykład, mógłbys kliknac na jedną talię, a potem kliknać z przytrzymanym shiftem na inną, aby pokazać karty z obu talii w jednym podglądzie.

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

This option (Notes→Find and Replace…​) allows you to replace text in the
notes you have selected. The regular expression option allows you to
perform complex replacements. For example, given the following text in a
field:

    <img src="pic.jpg" />

Searching for:

    <img src="(.+?)" />

and on Anki 2.1.28, replacing with:

     ${1}

 on older Anki versions, replacing with:

    \1

Will change the card to:

    pic.jpg

A full discussion on regular expressions is outside the scope of this
document. document. There are a number of tutorials available on the web. For a syntax guide, on Anki 2.1.28+ please see <https://docs.rs/regex/1.3.9/regex/#syntax>. For older Anki versions, please see <http://docs.python.org/library/re.html>.

Znajdowanie duplikatów
------------------

You can use the Notes→Find Duplicates option to search for notes that
have the same content. When you open the window, Anki will look at all
of your note types and present a list of all possible fields. If you
want to look for duplicates in the "Back" field, you’d select it from
the list and then click "Search".

Unlike the check that happens when you add cards manually, the duplicate
finding feature is not limited to a single note type. This means that by
default, it will search in all note types that have the field you
provided.

The *optional limit* text box allows you to narrow down where Anki will
look for duplicates. If you only want to search for duplicates in the
"French Vocab" and "French Verbs" note types, you would enter:

    note:'french vocab' or note:'french verbs'

Or you might want to look only for duplicates in a particular deck, so
you could use:

    deck:'myDeck'

The search syntax is the same as used when searching in the browser.
Please see the [searching](searching.md) section for more information.

You can click one of the links in the search results list to display the
duplicate notes in that set. If the search brings up a large number of
duplicates, you may wish to instead click the Tag Duplicates button,
which will tag all matching notes with "duplicate." You can then search
for this tag in the browser and handle them all from the same screen.

Inne elementy menu
----------------

Some other items in the menus:

*Reschedule* allows you to move cards to the end of the new card queue,
or reschedule them as a review card on a given date. The second option
is useful if you have imported already-learnt material, and you want to
start it off with higher initial intervals. For example, choosing 60 and
90 will give all the imported cards an initial interval of 2 to 3
months.

The card’s revision history is not cleared when rescheduling:
rescheduling changes the current state of a card, but not its history.
If you want to hide the history, you will need to export your notes as a
text file, delete the notes, and then import the text file again,
creating new notes.

*Reposition* allows you to change the order new cards will appear in.
You can find out the existing positions by enabling the *due* column, as
described in the card list section above. If you run the reposition
command when multiple cards are selected, it will apply increasing
numbers to each card in turn. By default the number increases by one for
each card, but this can be adjusted by changing the "step" setting. The
*Shift position of existing cards* option allows you to insert cards
between currently existing ones, pushing the currently existing ones
apart. For instance, if you have five cards and you want to move 3, 4,
and 5 between 1 and 2, selecting this setting would cause the cards to
end up in the order 1, 3, 4, 5, 2. By contrast, if you turn this option
off, 2 and 3 will get the same position number (and it will thus be
random which one comes up first).

*Change Note Type* allows you to convert the selected notes from one
type to another. For example, imagine you have a Russian note type and a
Computer note type, and you accidentally added some computer-related
text into a Russian note. You can use this option to fix that mistake.
The scheduling of cards is not affected.

*Select Notes* takes the currently selected cards, finds their notes,
and then selects all cards of those notes. If your notes have only one
card, this does nothing.

The *Go* menu exists to provide keyboard shortcuts to jump to various
parts of the browser, and to go up and down the card list.
