# Szablony Kart

Szablony kart "mówią" Anki które pola powinny pojawić się z przodu, a które z tyłu karty i pozwala programowi kontrolować które karty zostaną wygenerowane gdy określone pola zawierają w sobie tekst. Poprzez dostosowanie swoich szablonów kart można zmienić wygląd wielu kart na raz.

O szablonach kart można dowiedizeć się z niektórych filmów wprowadzających (język angielski):

-   [Zmiana kolejności kart](http://www.youtube.com/watch?v=DnbKwHEQ1mA&yt:cc=on)

-   [Zmiana wygladu kart](http://www.youtube.com/watch?v=F1j1Zx0mXME&yt:cc=on)

-   [Pisanie odpowiedzi w czasie powtórki](http://www.youtube.com/watch?v=5tYObQ3ocrw&yt:cc=on)

## Okno szablonu {docsify-ignore}

Możesz modyfikować szablony kart klikając na przycisk "Karty..." wewnątrz okna edycji.

Na górze po lewej stronie znajduje się szablon przodu, pod nim sekcja stylizacji kart (pole "Styl"),a na samym dole znajduje się szablon tyłu.

Szablony w Anki są napisane w języku HTML, który jest jednym z podstawowych języków do tworzenia stron internetowych. Pole "Styl" korzysta z jezyka CSS, który służy do nadawania wyglądu treściom opisanym językiem HTML (czyli np stronom internetowym).

Po prawej stronie widoczny jest podgląd przodu i tyłu wybranej karty. Jeśli otworzyłeś okno w czasie dodawania notatek, podgląd zostanie wyświetlony na podstawie tekstu, który wpisałes w oknie Dodaj Notatki. Jeśli otworzyłeś okno podczas edytowania notatki, podgląd zostanie wyświetlony na podstawie zawartości tej notatki. Jeśli zaś otworzyłeś poprzez Narzędza → Zarządzaj typami notatek, Anki wyświetli nazwe każdego pola w nawiasach klamrowych.

U góry po prawej stronie znajduje się przycisk Opcji, po którego naciśnięciu można zmienić nazwę lub kolejność kart jak i również następujące opcje: 

-   The 'Deck Override' option allows you to change the deck that cards
    generated from the current card type will be placed into. By
    default, cards are placed into the deck you provide in the Add Notes
    window. If you set a deck here, that card type will be placed into
    the deck you specified, instead of the deck listed in the Add Notes
    window. This can be useful if you want to separate cards into
    different decks (for instance, when studying a language, to put
    production cards in one deck and recognition cards in another). You
    can check which deck the cards are currently going to by choosing
    Deck Override again.

-   The 'Browser Appearance' option allows you to set different (perhaps
    simplified) templates for display in the Question and Answer columns
    of the browser; see [browser appearance](templates/styling.md#browser-appearance) for more
    information.
