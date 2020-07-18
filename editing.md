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

**Editing Font** allows you to customize the font and size used when
editing notes. This is useful if you want to make unimportant
information smaller, or increase the size of foreign characters which
are hard to read. The changes you make here do not affect how cards
appear when reviewing: to do that, please see the
[templates](templates/intro.md) section. If you have enabled the “type in the
answer” function, however, the text you type will use the font size
defined here. (For information about how to change the actual font face
when typing the answer, please see the [checking your
answer](templates/fields.md#checking-your-answer) section.)

**Sort by this field…​** tells Anki to show this field in the Sort Field
column of the browser. You can use this to sort cards by that field.
Only one field can be the sort field at once.

When **Remember last input…​** is checked, Anki will not clear out this
field’s content after a note is added. If you find yourself entering the
same content into multiple notes, you may find this useful.

**Reverse text direction** is useful if you are studying languages that
display text from right to left (RTL), such as Arabic or Hebrew. This
setting currently only controls editing; to make sure the text displays
correctly during review, you’ll need to adjust your
[template](templates/styling.md).

After you’ve added fields, you’ll probably want to add them to the front
or back of your cards. For more information on that, please see the
[templates](templates/intro.md) section.

Changing Deck / Note Type
-------------------------

While adding, you can click on the top left button to change note type,
and the top right button to change deck. The window that opens up will
not only allow you to select a deck or note type, but also to add new
decks or manage your note types.

Using Decks Appropriately
-------------------------

Decks are designed to divide your content up into broad categories that
you wish to study separately, such as English, Geography, and so on. You
may be tempted to create lots of little decks to keep your content
organized, such as “my geography book chapter 1”, or “food verbs”, but
this is not recommended, for the following reasons:

-   Lots of little decks mean you end up reviewing cards in a
    recognizable order. Whether it’s because you’re clicking on each
    deck in turn (which is slow) or you’ve added a number of decks under
    a single parent deck, you’ll end up seeing all the “chapter 1” or
    “food verb” cards together. This makes it easier to answer the
    cards, as you can guess them from the context, which leads to weaker
    memories. When you need to recall the word or phrase outside Anki,
    you won’t have the luxury of being shown related content first!

-   Anki was not designed to handle many decks (more than several
    dozen), and it will slow down as you add more – especially if you’re
    studying on a mobile client. A few extra decks is not going to make
    a noticeable difference, but if you have many decks the delays will
    start to add up.

Instead of creating lots of little decks, it’s a better idea to use tags
and/or fields to classify your content. Instead of creating a “food
verbs” decks for example, you could add those cards to your main
language study deck, and tag the cards with “food” and “verb”. Each card
can have multiple tags, which means you can do things like search for
all verbs, or all food-related vocabulary, or all verbs that are related
to food.

For those who like to stay very organized, you can add fields to your
notes to classify your content, such as “book”, “page”, and so on. Anki
supports searching in specific fields, which means you can do a search
for “book:'my book' page:63” and immediately find what you’re looking
for.

Anki’s [custom study and filtered deck](filtered-decks.md) features make this
especially powerful, as you can create temporary decks out of search
terms. This allows you to review your content mixed together in a single
deck most of the time (for optimum memory), but also create temporary
decks when you need to focus on particular material, such as before a
test. The general rule is that if you always want to be able to study
some content separately, it should be in a normal deck, and if you only
occasionally need to be able to study it separately (for a test, when
under a backlog, etc), tags/fields and filtered decks are better.

Features
--------

The editor is shown when [adding notes](editing.md), [editing a
note](studying.md) during reviews, or [browsing](browsing.md).

On the top left are two buttons, which open the [fields](editing.md#customizing-fields) and
[cards](templates/intro.md) windows.

On the right are buttons that control formatting. Bold, italic and
underline work like they do in a word processing program. The next two
buttons allow you to subscript or superscript text, which is useful for
chemical compounds like H<sub>2</sub>O or simple math equations like
x<sup>2</sup>.

The Fx button clears any formatting in the currently selected text. This
includes colours, bold, etc.

The next two buttons allow you to change text colour.

The \[…​\] button is visible when a cloze note type is selected.

You can use the paperclip button to select audio, images and videos from
your computer’s hard drive to attach to your notes. Alternatively, you
can copy the media onto your computer’s clipboard (for instance, by
right-clicking an image on the web and choosing 'Copy Image') and paste
it into the field that you want to place it in. For more information
about media, please see the [media](media.md) section.

The microphone icon allows you to record from your computer’s microphone
and attach the recording to the note.

The last button shows more advanced features, such as editing the
underlying HTML of a field, and shortcuts to add MathJax or
[LaTeX](math.md) to your notes.

Most of the buttons have shortcut keys. You can hover the mouse cursor
over a button to see its shortcut.

When pasting text, Anki will strip most formatting by default. If you
hold down the shift key while pasting, Anki will preserve more
formatting.

Cloze Deletion
--------------

'Cloze deletion' is the process of hiding one or more words in a
sentence. For example, if you have the sentence:

    Canberra was founded in 1913.

…​and you create a cloze deletion on “1913”, then the sentence would
become:

    Canberra was founded in [...].

Sometimes sections that have been removed in this fashion are said to be
'occluded'.

For more information on why you might want to use cloze deletion, see
rule number 5 [here](http://www.supermemo.com/articles/20rules.htm).

Anki provides a special cloze deletion type of note, to make creating
clozes easy. To create a cloze deletion note, select the Cloze note
type, and type some text into the "Text" field. Then drag the mouse over
the text you want to hide to select it, and click the \[…​\] button.
Anki will replace the text with:

    Canberra was founded in {{c1::1913}}.

The “c1” part means that you’ve created one cloze deletion on the
sentence. You can create more than one deletion if you’d like. For
example, if you select Canberra and click \[…​\] again, the text will
now look like:

    {{c2::Canberra}} was founded in {{c1::1913}}.

When you add the above note, Anki will create two cards. The first card
will show:

    Canberra was founded in [...].

…​on the question, with the full sentence on the answer. The other card
will have the following on the question:

    [...] was founded in 1913.

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
