# Nauka

Czas zacząć naukę pobranej lub samodzielnie stworzonej talii.

## Talie

W Anki można uczyć się jednocześnie tylko jednej talii oraz talii, które wchodzą w jej skład.

W oknie głównym talie wyświetlane są w formie listy. Są tam widoczne dwie kolumny Oczekujące oraz Nowe. W kolumnie Oczekujące pokazana jest liczba kart do nauki w poszczególnych taliach. W kolumnie Nowe wyświetlana jest liczba nowych kart oczekujących na naukę tego dnia.

Po kliknięciu na nazwę danej talii w oknie głównym pojawi się ekran nauki. Aby zmienić obecnie wybraną talię możesz powrócić do listy talii klikająć "Talie" u góry głównego okna (Mozesz również uzyć opcji Ucz się Talii w menu, aby wybrać nową talię uzywając klawiatury. Naciskając klawisz "s" włączysz naukę obecnie wybranej talii).

Aby zmienić nazwę talii, usunąć talię, dostosować jej ustawienia lub ją [wyeksportować](exporting.md), wybierz przycisk koła zębatego po prawej stronie nazwy talii w oknie Talie.

Jeśli talia posiada podtalie, karty będą wyświetlane [z każdej talii po kolei](studying.md#display-order).

## Powtórka

Po kliknięciu na nazwę talii, której chcesz się uczyć, wyświetli się ekran pokazujący liczbę kart oczekujących dzisiaj do nauki. Są ich trzy typy:

- **Nowe**, czyli karty pobrane lub samodzielnie wprowadzone, których jeszcze nigdy się nie uczyłeś.

- **Uczone** to karty, które widziałeś po raz pierwszy, ale jeszcze się ich nie nauczyłeś.

- **Do przejrzenia** to karty, których się już uczyłeś, a teraz będą powtarzane, abyś ich nie zapomniał.

Aby rozpocząć naukę kliknij przycisk Ucz się teraz. Anki rozpocznie wyświetlanie kart. Nauka będzie trwała do momentu wyczerpania się wszystkich kart przeznaczonych do nauki danego dnia.

Podczas nauki możesz cofnąć się do ekranu z liczbą kart naciskając klawisz "s" na klawiaturze.

## Pytania

W momencie wyświetlenia karty, jako pierwsze pokazywane jest pytanie. Po tym jak pomyślisz o odpowiedzi możesz albo kliknąć przycisk **Pokaż odpowiedź** albo nacisnąć spację. Zostanie wtedy wyświetlona odpowiedź. Normalną sytuacją jest, że przypomnienie sobie odpowiedzi na dane pytanie wymaga chwili namysłu, jeśli jednak po 10 sekundach dalej nie będziesz umiał podać prawidłowej odpowiedzi lepiej jest się poddać i wyświetlić odpowiedź niż w nieskończoność próbować ją wymyślić.

Po wyświetleniu odpowiedzi porównaj z nią swoją odpowiedź, a następnie oceń jak dobrze ci poszło. Jeśli nie jesteś pewien swoich odpowiedzi w myślach, możesz tak ustawić Anki, żeby odpowiedzi były przez ciebie [wpisywane](templates/fields.md#checking-your-answer), a nie tylko pokazywane.

Liczba przycisków do oceny twojej odpowiedzi zależna jest od tego czy karta była już wcześniej przeglądana.

## Nauka nowych kart

Podczas uczenia się nowych kart lub takich, które już wcześniej widziałeś, ale zapomniałeś ich odpowiedzi, Anki wyświetli je raz lub kilka razy, w pewnych odstępach czasu - tzw. interwałach. Standardowo dla takich kart są ustawione dwa interwały: 1 minuta oraz 10 minut. Możesz zmienić ich liczbę oraz wartości w  [Opcjach talii](deck-options.md).

Standardowo dla nowych kart w Anki wyświetlane są trzy przyciski oceny:

**Powtórz** cofa kartę do pierwszego kroku

**Dobra** przenosi kartę do nastepnego kroku. Jeżeli w poprzednim kroku karta została już wcześniej oceniona jako Dobra, to w tym kroku stanie się ona kartą powtórkową ("absolwentem"). By
default.Domyślnie zostanie ona wyświetlona następnego dnia, a potem co pewien narastający czas.
(zobacz nastepną sekcję)).

**Łatwa** natychmiast przekształca nową kartę w kartę powtórkową, nawet jeśli nie zostały dla niej wykonane inne kroki. Domyślnie karta ta zostanie wyświetlona za 4 dni, a potem co pewien narastający czas. Przycisk tej odpowiedzi nie będzie dostępny jeśli uczysz się kart, na które nie znałeś odpowiedzi lub odpowiedziałeś niepoprawnie, ponieważ przerwa byłaby taka sama jak przy odpowiedzi "Dobra".

Karta wyświetlana po raz pierwszy znajduje się w pierwszym kroku (1 minuta). Dla takiej karty odpowiedź **Dobra** będzie oznaczać, że zostanie ona wyświetlona za 10 minut, a początkowy krok - 1 minuta - zostanie pominięty.Jesli jednak przy drugim kroku (10 minut) naciśniesz "Powtórz", karta zostanie pokazana ponownie w ciągu jednej minuty.

Do oceny karty możesz również używać przycisków 1, 2 oraz 3 znajdujących się na klawiaturze, przy czym 1 = **Powtórz**. Wybranie spacji wybierze odpowiedź **Dobra**.

W sytuacji, gdy danego dnia nie ma już innych kart do nauki Anki domyślnie pokaże nowe karty, nawet wtedy, gdy nie upłynął jeszcze na nie czas oczekiwania. Jeśli jednak chciałbyś czekać pełen czas na kartę, to możesz zmienić ich zachowanie w [ustawieniach](preferences.md).

## Powtórka znanych kart

Jeżeli karta została już kiedyś wyświetlona w którejś z wcześniejszych powtórek będzie ona posiadała cztery przyciski oceny:

**Powtórz** oznacza, że podana odpowiedź była błędna, a w przyszłości Anki będzie częściej pokazywał tę kartę. Zobacz rozdział o [powtórkach](deck-options.md) aby dowiedzieć się wiecej na temat obsługi kart na które udzielono błędnej odpowiedzi.

**Trudna** karta zostanie wyświetlona po czasie niewiele dłuższym od tego przy ocenie Powtórz. W przyszłości Anki będzie ostrożniej harmonogramowało powtórki tej karty.

**Dobra** oznacza dla Anki, że ostatnio ustawiony interwał powtórki był bliski poprawnego i łatwość karty nie powinna być zmieniana ani w górę ani w dół. Przy standardowym, początkowym stopniu łatwości karta zostałaby pokazana po 2,5-krotnie dłuższym odstępie czasowym niż dotąd. Co dla karty z przerwą 10 dni oznacza kolejną powtórkę za około 25 dni.

**Łatwa** oznacza, karta jest dla użytkownika zbyt łatwa i należy zdecydowanie wydłużyć przerwę w  powtórkach. Karta otrzyma przerwę dłuższą niż w przypadku oceny Dobra, a Anki w przyszłym harmonogramowaniu karty będzie rzadziej ją pokazywał. Ponieważ ocena Łatwa gwałtownie wpływa na zwiększenie się odstepu czasowego powtórki najlepszym rozwiązaniem jest stosowanie jej tylko względem kart co do których jesteśmy w 100% pewni. W przypadku prawidłowej odpowiedzi najczęściej stosowaną oceną powinna być Dobra.

Tak samo jak przy nauce nowych kart, możesz użyć przycisków 1-4 na klawiaturze, aby wybrać odpowiedź. Naciśniecie spacji wybierze opcję "Dobra".

## Liczba oczekujących i czas nastepnej powtórki

W momencie pojawienia się karty z pytaniem na ekranie, u dołu wyświetlane są również trzy liczby np. 12 + 34 + 56. Reprezentują one: nowe karty, karty nienauczone oraz karty powtarzane. Jeśli chcesz, możesz ukryć te liczby w ustawieniach Anki.

W starym harmonogramie (wyznaczania powtórek), liczby pokazują liczbę _powtórek_ do ukończenia wszystkich kart w tej kolejce, a nie liczba samych _kart_. Jeśli ustawiłeś wielokrotną liczbę kroków, numer będzie się zwiekszał o więcej niż jeden, gdy odpowiesz "Powtórz", ponieważ ta karta musi być pokazana wiele razy.

W nowym harmonogramie (wyznaczania powtórek), liczby pokazują liczbę _kart_. Oznacza to, że liczby zawsze będą zwiększały się o jeden, niezależnie od liczby pozostałych kroków.

Po wyświetleniu odpowiedzi Anki pokaże również przybliżony, szacowany czas kolejnej powtórki danej karty. Jeśli chcesz, możesz ukryć ten wskaźnik w [ustawieniach](preferences.md) Anki.

Anki dodatkowo dodaje do czasu kolejnej powtórki pewną niewielką, losową liczbę, aby nowowprowadzone karty nie pojawiały się przy okazji kolejnych powtórek obok siebie. Ta losowość nie jest pokazywana w szacowanym czasie kolejnej powtórki danej karty, ale mimo tego algorytm Anki ją uwzględnia. 

## Przyciski Edytuj i Więcej

You can click the **Edit** button in the bottom left to edit the current
note. When you finish editing, you’ll be returned to study. The editing
screen works very similarly to the [add notes](editing.md) screen.

At the bottom right of the review screen is a button labeled **More**.
This button provides some other operations you can do on the current
card or note:

Flag Card  
Adds a colored marker to the card, or toggles it off. Flags will appear during
study, and you can search for flagged cards in the Browse screen. This is useful
when you want to take some action on the card at a later date, such as looking
up a word when you get home.

Mark Note  
Adds a “marked” tag to the current note, so it can be easily found in the
browser. This is similar to flagging individual cards, but works with a tag
instead, so if the note has multiple cards, all cards will appear in a search
for the marked tag. Most users will want to use flags instead - marking is
mainly left around for compatibility with older Anki versions.

Bury Card / Note  
Hides a card or all of the note’s cards from review until the next day.
(If you want to unbury cards before then, you can click the “unbury”
button on the [deck overview](studying.md#study-overview) screen.) This is useful if
you cannot answer the card at the moment or you want to come back to it
another time. Burying can also [happen automatically](studying.md#siblings-and-burying) for
cards of the same note. If cards were in learning when they are buried,
they are moved back to the new card queue or review queue prior to being
buried.

Suspend Card / Note  
Hides a card or all of the note’s cards from review until they are
manually unsuspended (by clicking the suspend button in the browser).
This is useful if you want to avoid reviewing the note for some time,
but don’t want to delete it. If cards were in learning when they are
suspended, they are moved back to the new card queue or review queue
prior to being suspended.

Delete Note  
Deletes the note and all of its cards.

Options  
Edit the options for the current deck.

Replay Audio  
If the card has audio on the front or back, play it again.

Record Own Voice  
Record from your microphone for the purposes of checking your
pronunciation. This recording is temporary and will go away when you
move to the next card. If you want to add audio to a card permanently,
you can do that in the edit window.

Replay Own Voice  
Replay the previous recording of your voice (presumably after showing
the answer).

## Display Order

Studying will show cards from the selected deck and any decks it
contains. Thus, if you select your “French” deck, the subdecks
“French::Vocab” and “French::My Textbook::Lesson 1” will be shown as
well.

For new cards and reviews, Anki fetches cards from the decks in
alphabetical order. So in the above example, you would get cards first
from “French”, then “My Textbook”, and finally “Vocab”. You can use this
to control the order cards appear in, placing high priority cards in
decks that appear higher in the list. When computers sort text
alphabetically, the “-” character comes before alphabetical characters,
and “\\~” comes after them. So you could call the deck “-Vocab” to make
them appear first, and you could call the other deck “~My Textbook” to
force it to appear after everything else.

New cards and reviews are fetched separately, and Anki won’t wait until
both queues are empty before moving on to the next deck, so it’s
possible you’ll be exposed to new cards from one deck while seeing
reviews from another deck, or vice versa. If you don’t want this, click
directly on the deck you want to study instead of one of the parent
decks.

Since cards in learning are somewhat time-critical, they are fetched
from all decks at once and shown in the order they are due.

To control the order reviews from a given deck appear in, or change new
cards from ordered to random order, please see the [deck
options](deck-options.md). For more fine-grained ordering of new cards, you
can change the order in the [browser](browsing.md).

## Siblings and Burying

Recall from [the basics](getting-started.md) that Anki can create more than one
card for each thing you input, such as a front→back card and a
back→front card, or two different cloze deletions from the same text.
These related cards are called 'siblings'.

When you answer a card that has siblings, Anki can prevent the card’s
siblings from being shown in the same session by automatically 'burying'
them. Buried cards are hidden from review until the clock rolls over to
a new day or you manually unbury them using the “Unbury” button that’s
visible at the bottom of the [deck overview](studying.md#study-overview) screen. Anki
will bury siblings even if the siblings are not in the same deck (for
instance, if you use the [deck override](templates/intro.md) feature).

You can enable burying from the [deck options](deck-options.md) screen -
there are separate settings for new cards and reviews.

Anki will only bury siblings that are new or review cards. It will not
hide cards in learning, as time is of the essence for those cards. On
the other hand, when you study a learning card, any new/review siblings
will be buried.

## Keyboard Shortcuts

Most of the common operations in Anki have keyboard shortcuts. Most of
them are discoverable in the interface: menu items list their shortcuts
next to them, and hovering the mouse cursor over a button will generally
show its shortcut in a tooltip.

When studying, either space or enter will show the answer. When the
answer is shown, you can use space or enter to select the Good button.
You can use the 1-4 keys to select a specific ease button. Many people
find it convenient to answer most cards with space and keep one finger
on 1 for when they forget.

The "Study Deck" item in the Tools menu allows you to quickly switch to
a deck with the keyboard. You can trigger it with the '/' key. When
opened, it will display all of your decks and show a filter area at the
top. As you type characters, Anki will display only decks matching the
characters you type. You can add a space to separate multiple search
terms, and Anki will show only decks that match all the terms. So “ja 1”
or “on1 ja” would both match a deck called “Japanese::Lesson1”.

## Falling Behind

If you fall behind in your reviews, Anki will prioritize cards that have
been waiting the longest. It does this by taking the the cards that have
been waiting the longest and showing them to you in a random order up
until your daily review limit. This ordering ensures that no cards will
be left waiting indefinitely, but it means that if you introduce new
cards, their reviews won’t appear until you’ve gotten through your
backlog.

If you wish to change the order of the overdue reviews, you can do so by
creating a [filtered deck](filtered-decks.md).

When you answer cards that have been waiting for a while, Anki factors
in that delay when determining the next time a card should be shown.
Please see the section on Anki’s spaced-repetition
[algorithm](faqs.md) for more information.
