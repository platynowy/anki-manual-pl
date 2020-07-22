# Generowanie kart

Karty odwrotne
-------------

Możesz obejrzeć [film o odwracaniu kart](http://www.youtube.com/watch?v=DnbKwHEQ1mA&yt:cc=on) na YouTube.

Jeżeli chcesz stworzyć notatkę, która będzie cię odpytywać w dwóch kierunkach (np. zarówno "ookii"→"duży" oraz "duży"→"ookii") masz kilka możliwości, by to zrobić. Najprostszym sposobem jest wykorzystanie wbudowanego typu notatki Podstawowy (z odwrotną kartą). Typ ten automatycznie wygeneruje dwie karty, każdą w jednym kierunku.

Jeśli chcesz wygenerować karty odwrotne tylko dla części notatek (np. chcesz uczyć się najważniejszych informacji tylko z kart odwrotnych lub, gdy dla niektórych notatek karta podwójna po prostu nie ma sensu), możesz użyć do tego celu typu notatki Podstawowy (z opcjonalną odwrotną kartą). Ten typ notatki stworzy standardową kartę jeśli wypełnisz tylko dwa pierwsze pola. Aby uzyskać również kartę odwrotną wystarczyć wpisać dowolny znak do trzeciego pola o nazwie Dodaj rewers. Należy podkreślić, że zawartość ostatniego pola nie będzie wyświetlana na kartach podczas powtórki.

Generowanie i usuwanie kart
--------------------------

Anki nie wygeneruje żadnej karty jeżeli jej przód będzie pusty. Przykładowo jeżeli w podstawowym typie notatki pole Przód będzie puste, a szablon przodu będzie zawierał tylko to pole, to karta nie zostanie wygenerowana.

W takim przypadku w oknie Dodaj pojawi się ostrzeżenie, o tym, że karta nie powstanie dopóki pole to nie zostanie wypełnione informacją.

Po edycji wcześniej dodanej notatki Anki utworzy automatycznie dodatkowe karty, jeśli były one wcześniej puste, ale już nie są. Jesli twoje zmiany sprawiły, że karty, które wczesniej nie były puste takie się stałym Anki nie usunie ich od razu ponieważ mogłoby to prowadzić do utraty danych. Aby usunąć puste karty, wejdź w oknie głównym do Narzędzia → Puste karty. Zostanie pokazana lista pustych kart z opcją ich usunięcia.

Nie ma możliwości usuwania ręcznie pojedynczych kart, ponieważ i tak zostałyby one odtworzone w momencie kolejnej edycji notatki. Zamiast tego, możesz usunąć informacje z pól warunkowego zastępowania (niektórych pól), a następnie użyć opcji "Puste Karty".


Anki przy generowaniu kart nie uwzględnia pól specjalnych oraz zwykłego tekstu, który nie jest odnośnikiem do pola, to znaczy, że na ich podstawie nie zostaną stworzone żadne nowe karty. Przykładowo jeżeli pole "Kraj" w szablonie przodu w poniższym przykładzie będzie puste, to karta nie powstanie, pomimo tego, że szablon zawiera jeszcze zwykły tekst "Gdzie na mapie znajduje się":

    Gdzie na mapie znajduje się {{Kraj}}?

Selektywne generowanie kart
-------------------------

Sometimes you may want to generate extra cards for only some of your
material, such as testing your ability to recall the most important
words of a set. You can accomplish this by adding an extra field to your
note, and adding some text into it (such as "1") on the notes you want
the extra card. Then in the card template, you can make the card’s
creation depend on that field being non-empty. For more information on
this, please see the conditional replacement section below.


Conditional Replacement
-----------------------

It is possible to include certain text, fields, or HTML on your cards
only if a field is empty or not empty. An example:

    This text is always shown.

    {{#FieldName}}
        This text is only shown if FieldName has text in it
    {{/FieldName}}

    {{^FieldName}}
        This text is only shown if FieldName is empty
    {{/FieldName}}

A real life example is only showing a label if the field is not empty:

    {{#Tags}}
        Tags: {{Tags}}
    {{/Tags}}

Or say you want to display a specific field in blue on the front of your
card if there are extra notes on the back (perhaps the fact that there
are notes serves as a reminder that you should spend more time thinking
about the answer). You can style the field as follows:

    {{#Notes}}
        <span style="color:blue;">
    {{/Notes}}
    
    {{FieldToFormat}}
    
    {{#Notes}}
        </span>
    {{/Notes}}

You can also use conditional replacement to control which cards are
generated. This works since Anki will not generate
cards which would have a blank front side. For
example, consider a card with two fields on the front:

    {{Expression}}
    {{Notes}}

Normally a card would be generated if either the expression or notes
field had text in it. If you only wanted a card generated if expression
was not empty, then you could change the template to this:

    {{#Expression}}
        {{Expression}}
        {{Notes}}
    {{/Expression}}

And if you wanted to require both fields, you could use two conditional
replacements:

    {{#Expression}}
        {{#Notes}}
            {{Expression}}
            {{Notes}}
        {{/Notes}}
    {{/Expression}}

Keep in mind that this only works when you place the
conditional replacement code on the *front* of the card; if you do this
on the back, you will simply end up with cards with a blank back side.
Similarly, since this works by checking if the front field would be
empty, it is important to make sure you wrap the 'entire' front side in
the conditional replacement; for instance, the following would not work
as expected:

    {{#Expression}}
        {{Expression}}
    {{/Expression}}
    {{Notes}}

## Limitations in older Anki versions

The following limitations do not apply to Anki 2.1.28+ and AnkiMobile 2.0.64+.

Older Anki versions can not used negated conditionals for card generation.
 For example, on Anki 2.1.28, the following would add a card if a field
 called AddIfEmpty is empty, and Front is non-empty:

     {{^AddIfEmpty}}
         {{Front}}
     {{/AddIfEmpty}}

 On earlier Anki versions, the negated conditional is ignored, and card
 generation will depend only on Front being non-empty.

 Mixing **AND** and **OR** conditions can also cause problems on older versions.
 For example, the following ("add the card if A **OR** B **OR** C is non-empty)
 is fine:

     {{A}}
     {{B}}
     {{C}}

 And the following ("add the card if A **AND** B **AND** C are non-empty") is fine:

     {{#A}}
         {{#B}}
             {{#C}}
                 {{A}}
             {{/C}}
         {{/B}}
     {{/A}}

But the following ("add the card if A **OR** (B **AND** C) are non-empty") will not work properly:

     {{A}}
     {{#B}}
         {{#C}}
             {{B}}
         {{/C}}
     {{/B}}

Cloze Templates
---------------

Please see the [cloze deletion](editing.md#cloze-deletion) section for background info.

The cloze note type functions differently from regular note types.
Instead of a customizable number of card types, it has a single type
which is shared by all cloze deletions on a note.

As mentioned in the card generation section above, generation of regular
cards depends on one or more fields on the question being non-empty.
Cloze deletion note types are generated differently:

-  Anki looks on the front template for one or more cloze replacements,
    like {{cloze:FieldName}}.

-  It then looks in the FieldName field for all cloze references, like
    {{c1::text}}.

-  For each separate number, a card will be generated.

Because card generation functions differently for cloze deletion cards,
{{cloze:…​}} tags can not be used with a regular note type - they
will only function properly when used with a cloze note type.

Conditional generation provides a special field so you can check which
card you are rendering. If you wanted to display the "hint1" field on
the first cloze, and "hint2" field on the second cloze for example, you
could use the following template:

    {{cloze:Text}}

    {{#c1}}
    {{Hint1}}
    {{/c1}}

    {{#c2}}
    {{Hint2}}
    {{/c2}}
