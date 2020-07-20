# Wyszukiwanie

Zarówno przeglądarka jak i talie filtrowane używają w anki wspólnej metody wyszukiwania określonych kart/notatek.

## Proste wyszukiwania 

Gdy wpiszesz coś w wyszkiwarce Anki wyszukuje we wszystkich polach notatek, ale nie w atykietach (później w tej cześci nauczysz się jak wyszukiwać etykiety) Kilka przykładów:

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
wyszukuje notatki, które zawierają w sobie dokładnie takie wyrażenie -> "ten kot" funkcja wyszuka np. "tamten kot", jednak nie pojawią wyniki takie jak "kot tamten".

`-"ten kot"`  
wyszukuje notatki, które nie zawierają w sobie dokładnie takiego wyrażenua -> "ten kot".

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

- Kiedy podanych zostanie kilka warunków wyszukiwania, Anki bedzie szukać notatek, które spełniają wszystkie warunki (niewidoczne "and" pomiędzy każdym wyrażeniem). W Anki 2.1.24+ oraz AnkiMobile 2.0.60+ możesz te ukryte "and" wpisywać, jeśli chcesz - "lot and kot" jest tym samym co "lot kot". Starsze wersje anki traktują "and" jako normalne słowo do wyszukania. 

- Możesz używać "or" jeśli potrzebujesz, zeby tylko jedno z wyrażeń zostało znalezione.

- Możesz dodać przed wyrażeniem znak minus, aby znaleźć notatki, które nie spełniają kryteriów.

- Jeśli twoje wyszukiwanie zawiera spację lub nawias, zamknij je w cytatach. Możesz w nich umieścić
  `"całe:wyszukiwanie"`, lub tylko `część:"po dwókropku"`.

- You can group search terms by placing them in parentheses, as in the
  **dog (cat or mouse)** example. This becomes important when
  combining OR and AND searches — in the example, with the
  parentheses, it matches either 'dog cat' or 'dog mouse', whereas
  without them it would match either 'dog and cat' or 'mouse'.

- Anki is only able to search within formatting in the [sort
  field](editing.md#customizing-fields) you’ve configured. For example, if you add
  "**exa**mple" to one of your fields, this will not be matched when
  searching for "example" unless that field is the sort field. If a
  word is not formatted, or the formatting does not change in the
  middle of the word, then Anki will be able to find it in any field.

## Limiting to a field

You can also ask Anki to match only if a particular field contains some
text. Unlike the searches above, searching on fields requires an 'exact
match' by default.

`front:dog`  
find notes with a Front field of exactly "dog". A field that says "a
dog" will not match.

`front:*dog*`  
find notes with Front field containing dog somewhere

`front:`  
find notes that have an empty Front field

`front:_*`  
find notes that have a non-empty Front field

`front:*`  
find notes that have a Front field, empty or not

`fr*:text`
find notes in a field starting with "fr". Requires Anki 2.1.24+ or AnkiMobile 2.1.60+.

## Tags, decks, cards and notes

`tag:animal`  
find notes with the tag "animal"

`tag:none`  
find notes with no tags

`tag:ani*`  
find notes with tags starting with ani

`deck:french`  
find cards in a French deck, or subdecks like French::Vocab

`deck:french -deck:french::*`  
find cards in French, but not subdecks

`deck:"french vocab"`  
searching when a deck has a space

`"deck:french vocab"`  
also ok

`deck:filtered`  
filtered decks only

`-deck:filtered`  
normal decks only

`card:forward`  
search for Forward cards

`card:1`  
search for cards by template number - eg, to find the second cloze
deletion for a note, you’d use card:2

`note:basic`  
search for cards with a Basic note type

## Ignoring accents/combining characters

Requires Anki 2.1.24+ or AnkiMobile 2.0.60+.

You can use `nc:` to remove combining characters ("no combining"). For example:

`nc:uber`  
matches notes with "uber", "über", "Über" and so on.

`nc:は`  
matches "は", "ば", and "ぱ"

Searches that ignore combining characters are slower than regular searches.

## Regular expressions

Anki 2.1.24+ and AnkiMobile 2.0.60+ support searching in notes with "regular expressions",
a standard and powerful way of searching in text.

Start a search with `re:` to search by regular expression. Some examples:

`"re:(some|another).*thing"`  
find notes that have "some" or "another" on them, followed by 0 or more characters, and then "thing"

`re:\d{3}`  
find notes that have 3 digits in a row

Regular expressions can also be limited to a specific field. Please note that unlike the normal searches
in a specific field, regular expressions in fields don't require an exact match. Eg:

`front:re:[a-c]1`  
matches uppercase or lowercase a1, B1 or c1 that occurs anywhere in the "Front" field

`front:re:^[a-c]1$`  
like the above, but will not match if any other text falls before or after a1/b1/c1.

You can learn more about regular expressions here: https://regexone.com/lesson/introduction_abcs

Some things to be aware of:

- The search is case-insensitive by default; use (?-i) at the start to turn on case sensitivity.
- Some text like spaces and newlines may be represented differently in HTML - you can
  use the HTML editor in the editing screen to see the underlying HTML contents.
- For the specifics of Anki's regex support, please see the regex crate documentation: https://docs.rs/regex/1.3.9/regex/#syntax

## Card state

`is:due`  
review cards and learning cards waiting to be studied

`is:new`  
new cards

`is:learn`  
cards in learning

`is:review`  
reviews (both due and not due) and lapsed cards

`is:suspended`  
cards that have been manually suspended

`is:buried`  
cards that have been buried, either [automatically](studying.md#siblings-and-burying) or
manually

Cards that have lapsed fall into several of these categories, so it may
be useful to combine them to get more precise results:

`is:learn is:review`  
cards that have lapsed and are awaiting relearning

`-is:learn is:review`  
review cards, not including lapsed cards

`is:learn -is:review`  
cards that are in learning for the first time

## Card properties

`prop:ivl>=10`  
cards with interval of 10 days or more

`prop:due=1`  
cards due tomorrow

`prop:due=-1`  
cards due yesterday that haven’t been answered yet

`prop:due>-1 prop:due<1`  
cards due between yesterday and tomorrow

`prop:reps<10`  
cards that have been answered less than 10 times

`prop:lapses>3`  
cards that have moved into relearning more than 3 times

`prop:ease!=2.5`  
cards easier or harder than default

Note that due only matches review cards and learning cards with an
interval of a day or more: cards in learning with small intervals like
10 minutes are not included.

## Recently added

`added:1`  
cards added today

`added:7`  
cards added in last week

The check is made against card creation time rather than note creation
time, so cards that were generated within the time frame will be
included even if their notes were added a long time ago.

## Recently answered

`rated:1`  
cards answered today

`rated:1:2`  
cards answered Hard (2) today

`rated:7:1`  
cards answered Again (1) over the last 7 days

`rated:31:4`  
cards answered Easy (4) in the last month

For speed, rating searches are limited to 31 days.

## Object IDs

`nid:123`  
all cards of the note with note id 123

`cid:123`  
the card with card id 123

`mid:123`  
find note types with note type id 123

Note and card IDs can be found in the [card info](stats.md) dialog in the
browser. Note type IDs can be found by clicking on a note type in the
Browse screen. These searches may also be helpful when doing add-on
development or otherwise working closely with the database.

Object IDs will not work in the mobile clients, and are not intended to
be used in filtered decks at the moment.
