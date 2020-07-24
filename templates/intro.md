# Szablony kart

Szablony kart informują Anki, które pola powinny pojawić się z przodu, a które z tyłu karty i pozwala programowi kontrolować, które karty zostaną wygenerowane, gdy określone pola zawierają w sobie tekst. Poprzez dostosowanie swoich szablonów kart można zmienić wygląd wielu kart na raz.

O szablonach kart można dowiedzieć się z niektórych filmów wprowadzających (język angielski):

-   [Zmiana kolejności kart](http://www.youtube.com/watch?v=DnbKwHEQ1mA&yt:cc=on)

-   [Zmiana wygladu kart](http://www.youtube.com/watch?v=F1j1Zx0mXME&yt:cc=on)

-   [Pisanie odpowiedzi w czasie powtórki](http://www.youtube.com/watch?v=5tYObQ3ocrw&yt:cc=on)

## Okno szablonu {docsify-ignore}

Możesz modyfikować szablony kart klikając na przycisk "Karty..." wewnątrz okna edycji.

W starszych wersjach Anki, na górze po lewej stronie znajduje się szablon przodu, pod nim sekcja stylizacji kart (pole "Styl"), a na samym dole znajduje się szablon tyłu. W wersjach Anki  2.1.28+, przód, tył oraz pole "Styl" nie są pokazywane w tym samym czasie. Możesz przełączać się pomiedzy nimi, używając ctrl+1/2/3 lub cmd+1/2/3 na systemach MacOS.

Szablony w Anki są napisane w języku HTML, który jest jednym z podstawowych języków do tworzenia stron internetowych. Pole "Styl" korzysta z jezyka CSS, który służy do nadawania wyglądu treściom opisanym językiem HTML (czyli np. stronom internetowym).

Po prawej stronie widoczny jest podgląd przodu i tyłu wybranej karty. Jeśli otworzyłeś okno w czasie dodawania notatek, podgląd zostanie wyświetlony na podstawie tekstu, który wpisałes w oknie "Dodaj Notatki". Jeśli otworzyłeś okno podczas edytowania notatki, podgląd zostanie wyświetlony na podstawie zawartości tej notatki. Jeśli zaś otworzyłeś poprzez Narzędza → Zarządzaj typami notatek, Anki wyświetli nazwe każdego pola w nawiasach klamrowych.

U góry po prawej stronie znajduje się przycisk "Opcje", po którego naciśnięciu można zmienić nazwę lub kolejność kart jak i również następujące opcje: 

-   Opcja "Nadpisz talię" pozwala na zmianę talii, do której trafią karty generowane z wybranego typu karty. Domyślnie karty trafiają do talii, którą podajesz w oknie "Dodaj Notatki". Jeśli ustawisz talię tutaj, ten typ karty trafi do talii, którą podałeś, zamiast do talii podanej w oknie "Dodaj Notatki". Może się to przydać, jeśli będziesz chciał oddzielić karty do różnych talii (na przykład gdy podczas nauki języka będziesz chciał dodać karty z nauką pasywną do jednej talii, a z aktywną do drugiej). Możesz sprawdzić do której talii trafiają karty wybierając "Nadpisz Talię" ponownie.

-   Opcja "Wygląd w przeglądarce" pozwola ci ustawić inne (np. mniej skomplikowane) szablony, które wyświetlają się w przeglądarce w kolumnach Pytanie i Odpowiedź. Zobacz [wygląd w przegladarce](templates/styling.md#browser-appearance), aby dowiedzieć się więcej. 
