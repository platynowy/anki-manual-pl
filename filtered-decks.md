Talie filtrowane i zakuwanie
=========================

Gdy uczysz się w Anki normalnej talii, tylko określona liczba kart jest pokazywana: karty, które według Anki właśnie masz zapomnieć oraz nowe karty według dziennego limitu. Jest to przydatne, poniewaz daje to  pewnosć, że nie będziesz się uczył dłużej, niż to konieczne. Ale czasami może okazać się przydatne uczenie się pokza domyślnymi limitami, na przykład jak musisz powtórzyć materiał na egzamin, skupić się na określonych terminach i tak dalej. Aby było to możliwe, w Anki istnieje inny typ talii nazywający się "talia filtrowana" 

Talie filtrowane oferują wiele możliwości. Mogą być używane do podglądania kart, zakuwania ich przed testem, nauki okreslonych etykiet, nadrrabiania zaległości z okresloną kolejnością, nauki z wyprzedzeniem planowania, przeglądnięcia kart, na które odpowiedziano "Powtórz" oraz do wielu innych zastosowań.

Nauka własna
------------

Najłatwiejszym sposobem na stworzenie talii filtrowanej jest uzycia przycisku Nauka własna, który pojawia sie na dole ekranu, gdy naciśniesz na talię. Oferujeon   wygodne ustawienia wstępne dla częstych zadań typu powtarzanie kart, na które odpowiedziano "Powtórz". Stworzy on talię filtrowaną nazwaną "Sesja nauki własnej" i automatycznie ją otworzy. 

Jeśli istnieje już talia "Sesja nauki własnej", zostanie ona opróżniona przed utworzeniem nowej. Jeśli chcesz zachować talię nauki własnej, możesz zmienić jej nazwę na liście talii. 

Oto podsumowanie działania każdej z opcji:Here is a summary of each of the options:

**Zwiększenie dzisiejszego limitu nowych kart**  
Dodaj więcej nowych kart do talii, której aktualnie się uczysz. Zauważ, że w przceciwieństwie do innych opcji, nie jest tutaj tworzona talia filtrowana, tylko jest modyfikowana jest już istniejącatalia .

**Zwiększenie dzisiejszego limitu przejrzanych kart**  
Jesli nie zostały pokazane wsyzetkie powtórki ze względu na limity ustawione na dzienny limit powtórek, ta opcja umozliwia ci pokazac większą liczbę tych powtórek. Jak z opcją dotyczącą nowych kart, opcja ta modyfikuje istniejącą talię

**Powtórka zapomnianych kart**  
Pokaż wszystkie karty, na które odpowiedziałeś "Powtórz" (1) (możesz okreslić liczbę ostatnich dni, z których chcesz powtórzyć zapomniane karty).

**Powtórka z wyprzedzeniem**  
Pokaż karty, które oczekują na powtórkę w najbliższej przyszłości (określasz liczbę dni). Opcja ta jest przydatna do przejrzenia niektórych ze starszych kart przed wakacjami, ale nie pomoże ci zapamiętać kart kart, które nauczyłeś się niedawno. Zobacz rozdział o [nauce z wyprzedzeniem](#reviewing-ahead) poniżej, aby dowiedzieć się więcej.

**Podgląd nowych kart**  
Pokaż karty, które ostatnio dodałeś, bez zmiany ich typu na karty powtarzane po odpowiedzi.

**Powtórka według stanu karty lub etykiety**  
Wybierz określoną liczbe kart do nauki z  obecnej talii. Możesz uczyć sie tylko nowych kart, tylko oczekujących, lub wszystkich kart; po kliknieciu "Wybierz etykiety" możesz także zawęzić naukę do kart z okreslonymi etykietami. Jesli chcesz zobaczyć wszystkie karty znajdujace się w talii (na przykład, aby pouczyć się przed egzaminem z dużą ilością materiału), możesz ustawić liczbę kart większą, niż całkowita liczba kart znajdująca sie w tej talii.

Talie początkowe
----------

When a card is moved to a filtered deck, it retains a link to the deck
it was in previously. That previous deck is said to be the card’s 'home
deck'.

Cards automatically return to their home deck after they are studied in
the filtered deck. This can be after a single review, or after multiple
reviews, depending on your settings.

It is also possible to move all cards back to their home decks at once:

-   The "Empty" button in the study overview moves all cards in the
    filtered deck back to their home deck, but does not delete the empty
    filtered deck. This can be useful if you want to fill it again later
    (using the Rebuild button).

-   Deleting a filtered deck does the same thing as "Empty" does, but
    also removes the emptied deck from the deck list. No cards are
    deleted when you delete a filtered deck.

In the current implementation, if you create, rebuild, empty or delete a
filtered deck while cards are still in learning, they will be turned
back into new cards. In the case of failed reviews in relearning, any
remaining relearning steps will be skipped. This has been fixed in the
[experimental
scheduler](https://anki.tenderapp.com/kb/anki-ecosystem/experiment-scheduling-changes-in-anki-21).

Tworzenie ręczne
-----------------

Advanced users can create filtered decks with arbitrary search strings,
instead of relying on set presets. To create a filtered deck manually,
choose Create Filtered Deck from the Tools menu.

When you click the Build button, Anki finds cards that match the
settings you specified, and temporarily moves them from their existing
decks into your new filtered deck for study.

If you wish to fetch cards again using the same filter options (for
instance, if you want to study all cards with a particular tag every
day), you can use the Rebuild button at the bottom of the deck’s
overview screen.

The **search** area controls what cards Anki will gather. All of the
searches possible in the browser are also possible for filtered decks,
such as limiting to tags, finding cards forgotten a certain number of
times, and so on. Please see the [searching](searching.md) section of the
manual for more information on the different possibilities.

Filtered decks can not pull in cards that are suspended, buried, or
already in a different filtered deck. And unless you are using the
experimental scheduler, they can not pull in cards that are in
(re)learning. For this reason, a search in the browser may reveal cards
that don’t end up in the filtered deck.

The **limit** option controls how many cards will be gathered into the
deck. The order you select controls both the order cards are gathered
in, and the order they will be reviewed in. If you select "most lapses"
and a limit of 20 for example, then Anki will show you only the 20 most
lapsed cards.

For efficiency reasons, if your cram deck contains more than 1000 cards,
only 1000 cards will be shown as due on the deck list and study screens.

Kolejność
-----

The "cards selected by" option controls the order that cards will appear
in. If the maximum number of cards you select is lower than the number
of cards that match the filter criteria, Anki will exclude the cards at
the end of this sorted list first.

**Oldest seen first**  
Display cards that you haven’t seen in reviews for the longest time
first.

**Random**  
Randomize the order of all cards that match the filter criteria (use no
set order).

**Increasing intervals**  
Display cards that have the smallest interval first.

**Decreasing intervals**  
Display cards that have the largest interval first.

**Most lapses**  
Display cards that you have failed the most times first.

**Order added**  
Display cards that you added first (have the earliest creation date)
first.

**Order due**  
Display cards with the earliest due date first.

**Latest added first**  
Display cards that you’ve most recently added to the deck first. (This
is the opposite of 'Order added'.)

**Relative overdueness**  
Display cards that are most overdue in relation to their current
interval first (for instance, a card with a current interval of 5 days
overdue by 2 days displays before a card with a current interval of 5
years overdue by a week). This is useful if you have a large backlog
that may take some time to get through and want to review the cards
you’re most in danger of forgetting first.

Kroki i powrót
-----------------

Please see the section on [learning](studying.md#learning) as a reminder of how
steps work.

By default, Anki will use the steps of a card’s home deck. If a new card
would normally be reviewed twice when being learnt, the same thing will
happen when you study it in a filtered deck.

Cards return to their home deck when (re)learning is complete. Thus if
you have 3 learning steps, a new card will return to its home deck upon
three presses of "Good" or a single press of "Easy".

The **custom steps** option allows you to override the home deck’s steps
and provide your own steps instead. The provided steps apply to both
cards being learnt, lapsed reviews, and reviews ahead of time.

Liczby
------

In a filtered deck, reviews that were already due are displayed in the
review count as normal. Learning cards and non-due reviews are counted
in the new card count, due to how the underlying implementation works.
Reviews that were not due are not scheduled like new cards however -
Anki uses a special algorithm that takes into account how close they
were to their normal due time when reviewed.

Powtórki oczekujące
-----------

If the filtered deck includes cards that were due for review, they will
be shown like they would have been in their original deck - they appear
in the review card count at the bottom of the screen, and there are four
choices for how well you remembered. Upon a correct answer, the card
will be moved back to its home deck, and its next delay adjusted using
the home deck’s settings. If you forget the card, it will be shown
according to the relearning steps defined in the home deck.

Nauka z wyprzedzeniem
---------------

If your search included cards that are not due, Anki will show the
reviews ahead of time.

Anki uses a special algorithm for these reviews that takes into account
how early you are reviewing. If the cards were almost due to be shown,
they will be given a new delay similar to what they would have received
if you had reviewed them on time. If the cards are reviewed soon after
they were scheduled however, their new delay will be similar to their
previous delay. This calculation works on a sliding scale.

Because reviewing a card shortly after it is scheduled has little impact
on scheduling (eg, a card due tomorrow with a one day interval will
remain due tomorrow if reviewed early), **the "review ahead" custom
study setting is not appropriate for repeated use**. If used to go
through a week’s worth of cards before a trip, the mature cards will be
rescheduled into the future and the new cards will remain at small
intervals, because you don’t know them well enough for them to be
rescheduled further. If you review ahead again the next day, all you’ll
end up doing is going through those same new cards again, to little
benefit.

Early reviews are included in the new card count rather than the review
count, and will be shown according to the number of relearning steps
defined in the home deck (unless you have provided custom steps). This
means that if you have customized the number of relearning steps in the
home deck, the non-due card may be shown more than once.

If you have multiple steps, Anki will only consider the first answer
when deciding the next delay, and like relearning in normal decks,
"Good" and "Easy" differ only in the step change and not the resulting
delay.

Zmiana planu
------------

By default, Anki will return cards to their home decks with altered
scheduling based on your performance in the filtered deck. If you
disable the **reschedule cards based on my answers** option, Anki will
return the cards in the same state they were in when they were moved
into the filtered deck. This is useful for quickly flipping through
material.

If you have disabled rescheduling, the "Good" and "Easy" buttons will
display no time above them when pressing them would cause the card to
return to its home deck with its original scheduling.

Please note that new cards are returned to the end of the new card
queue, rather than the start of it.

Nadrabianie zaległości
-----------

Filtered decks can be useful for catching up when you’ve fallen behind
in your reviews. One Anki user describes the way they use the filtered
decks to catch up as follows:

    I did this for a backlog of 800 cards with filtered subdecks. Worked
    very well for me.
    
    Just Due filter with: "is:due prop:due>-7"
    
    Over Due filter with: "is:due prop:due<=-7"
        
    The Just Due deck will then contain cards that became due in the past
    week. That's the deck you should study every day as it gets the cards
    that become due regularly. With this you can study as if there wasn't
    any backlog.
    
    The Over Due deck will contain your backlog, cards which you didn't
    study in time. You can study them the same way you would study new
    cards. They go back into the regular cards, so the number of overdue
    will never grow as long as you keep your Just Due deck in check.
    
    How long it takes depends on how many overdue cards you study each day
    in addition to the ones that become due regularly. You can still motor
    through them when you feel like it - or you can do a specific number per
    day like you would for new cards. Up to you.
