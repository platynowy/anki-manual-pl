Stylizowanie kart
------------

Możesz obejrzeć [film o stylizowaniu kart](http://www.youtube.com/watch?v=F1j1Zx0mXME&yt:cc=on) (w języku angielskim) na YouTube.
Ten film używa interfesju Anki 2.0, ale główne założenia pozostały takie same.

Na końcu, po prawej stranie, za obszarem edycji szablonu przodu i tyłu znajduje  przycisk do pokazania się obszaru Styl. Możesz w nim zmieniać kolor tła karty, standardową czcionkę, wyrównanie tekstu i tak dalej.

Podstawowe dostępne polecenia to:

**font-family**  
Nazwa czcionki, którą będą wyświetlane informacje na karcie podczas powtórki. Jeżeli czcionka w nazwie posiada spację np. "MS Unicode", jej nazwę należy ująć w cudzysłów. Możliwe jest także użycie wielu różnych czcionek na jednej karcie. Informacje na ten temat znajdują się poniżej.

**font-size**  
Rozmiar czcionki określany w liczbie pikseli. Zmieniając rozmiar upewnij się, że po liczbie określiłeś jednostkę "px".

**text-align**  
Wyrównanie tekstu: wycentrowanie (center), do lewej (left), do prawej (right).

**color**  
Kolor tekstu. Może być określony po prostu przez wpisanie angielskich nazw kolorów podstawowych np. blue (niebieski), lightyellow (jasno żółty) itd. Możliwe jest także użycie kodów kolorów wedłóg modelu RGB. Kody kolorów zapisane w tej postaci odnaleźć można na [tej stronie](http://htmlcolorcodes.org/).

**background-color**  
Kolor tła karty.

Jakakolwiek komenda CSS może byc wpisana w oknie stylizacji - użytkownicy zaawansowani mogą dodać rzeczy takie jak tło lub gradient. Jeśli zastanawiasz się, jak uzyskać określone formatowanie, poszukaj w internecie informacji jak wpisac je w CSS. W sieci znajduje się wiele informacji na ten temat.

Dany styl nadawany jest jednocześnie wszystkim kartom należącym do tego samego typu notatki. Możliwe jest jednak nadawanie wyjątków. Przykładowo, poniższy kod nada wszystkim kartom tło koloru żółtego, z wyjątkiem pierwszej karty, która będzie miała tło niebieskie:

```css
.card { background-color: yellow; }
.card1 { background-color: blue; }
```
    
## Zmiana wielkości obrazów

Anki domyslnie zmniejsza obrazy, aby pasowały one do ekranu. Możesz to zmienić dodając następujący tekst do okna stylizacji (poza domyślnym `.card { ... }`): 

```css
img { max-width: none; max-height: none; }
```

AnkiDroid czasami ma [problemy ze skalowaniem obrazów, aby dopasowały się do ekranu](https://github.com/ankidroid/Anki-Android/issues/3612). Ustawienie maksymalnych wymiarów obrazu używając CSS powinno to naprawić, ale jest to ignorowane w wersji AnkiDroid 2.9. Naprawić to można dodając `!important` do każdej dyrektywy stylu, na przykład:

```css
img { max-width: 300px !important; max-height: 300px !important; }
```

Jeśli spróbujesz zmienić styl obrazów i zobaczysz, że gwiazdka, która pojawia się przy wyróżnionych kartach nie wyświetla się poprawnie (np. jest zbyt duża), to możesz to naprawić nastepującym tekstem:

```css
img#star { ... }
```

Możesz interaktywnie eksplorować stylizowanie kart używając Chrome:

<https://ankitects.github.io/addon-docs/#/porting2.0?id=webview-changes>

Stylizowanie pól
-------------

Domyślnie stylizowanie ustawione w szablonie obejmuje całą zawartość karty. Możliwe jest jednak nadanie poszczególnym polom ich własnych stylów czcionki, koloru itd. Funkcja ta jest szczególnie istotna podczas nauki języków obcych, kiedy dla danego tekstu musi zostać użyta specyficzna czcionka np. hebrajska lub arabska, gdyż w przeciwnym razie tekst nie zostanie poprawnie wyświetlony.

Powiedzmy, że masz w notatce pole o nazwie "Wyrażenie" i chcesz, aby jego treść na karcie była wyświetlana przy pomocy tajskiej czcionki "Ayuthaya" (działa tylko na systemach Mac OSX). Twój szablon wygląda na razie w taki sposób:

    Co oznacza {{Wyrażenie}}?

    {{Notatki}}

Pierwszym krokiem będzie umieszczenie zawartości, której wygląd chcemy zmienić w znacznikach HTML. Przed tekstem umieścimy:

    <div class=mojstyl1>

A po nim:

    </div>

Zastosowanie tych znaczników mówi Anki, żeby w stosunku do zawartego pomiędzy nimi tekstu został zastosowany jakiś styl, w tym przypadku o nazwie "mojstyl1". Styl ten utworzymy za chwilę.

Jeśli chcemy, żeby całe wyrażenie "Co oznacza...?" posiadało dany styl, to nasz szablon przodu będzie wyglądał następująco:

    <div class=mojstyl1>Co oznacza {{Wyrażenie}}?</div>

    {{Notatki}}

A jeśli chcemy, żeby tylko nasze pole "Wyrażenie" posiadało dany styl, czy daną czcionkę to użyjemy takiego kodu:

    Co oznacza <div class=mojstyl1>{{Wyrażenie}}</div>?

    {{Notatki}}

Po edycji szablonu przodu musimy przejść teraz do  obszaru Styl, który można wybrać po prwej stroniu szablonu przodu i szablonu tyłu. Standardowo zawartość obszaru Styl powinna wyglądąć tak:

```css
.card {
 font-family: arial;
 font-size: 20px;
 text-align: center;
 color: black;
 background-color: white;
}
```

Na dole tego kodu dodaj trzy linijki twojego stylu, jak poniżej:

```css
.card {
 font-family: arial;
 font-size: 20px;
 text-align: center;
 color: black;
 background-color: white;
}

.mojstyl1 {
 font-family: ayuthaya;
}
```

Do stylu możesz oczywiście dodawać dowolny kod zgodny z językiem CSS. Jeśli chciałbyś np. zwiększyć rozmiar czcionki w nowo powstałym stylu, dodaj kolejna linijkę kodu:

```css
.mojstyl1 {
 font-family: ayuthaya;
 font-size: 30px;
}
```

Możliwe jest również wykorzystywanie zewnętrznych czcionek bez konieczności ich instalacji na komputerze, czy urządzeniu mobilnym. Więcej informacji na ten temat znajduje się w rozdziale na temat instalacji czcionek.

Przyciski ponownego odtwarzania dźwieku
--------------------

Kiedy dźwięk lub tekst na mowę (TTS) znajduje się w twoich kartach, Anki pokaże przyciski, na które możesz kliknąć, aby ponownie dotworzyć dźwięk. 

Jeśli wolisz nie widzieć tych przycisków, możesz je ukryć w ustawieniach.

Możesz zmienić ich wygląd w obsarze stylizowania, na przykład jeśli chcesz, aby były one mniejsze i pokolorowane możesz wpisać nastepujący tekst:

```css
.replay-button svg { width: 20px; height: 20px; }
.replay-button svg circle { fill: blue; }
.replay-button svg path { stroke: white; fill: green; }
```

Kod HTML
----------

Szablony kart obsługują znaczniki języka HTML. Oznacza to, że wygląd kart może być dostosowany w ten sam sposób, w którym pisane są strony internetowe. Wspierane są tabele, listy, obrazy i odnośniki do zewnętrznych stron internetowych. Przykładowo, stosując odpowiedni układ tabeli możesz stworzyć szablon, w którym pytanie wyświetlane będzie po lewej stronie karty, zaś odpowiedź po prawej, zamiast standardowo na górze i na dole.

Nie ma sensu opisywać w tej instrukcji wszystkich możliwych zastosowań języka HTML, gdyż w internecie znaleźć możesz wiele bardzo dobrych kursów na ten temat, jeśli chcesz dowiedzieć się więcej.

Wygląd w przeglądarce
------------------

Jeśli twoje szablony kart są skomplikowane, może być trudno odczytać kolumny "pytanie" i "odpowiedź" (nazwane "Przód" i "Tył") w [liście kart](browsing.md). Opcja "wygląd w przeglądarce" pozwala określić własny szablon, używany tylko w przeglądarce, więć jeśli chcesz, możesz dodać tylko ważne pola i zmienić ich kolejność. Składnia jest taka sama jak w standardowych szablonach kart.

CSS dla określonych platform
---------------------

Anki posiada wbudowane klasy CSS, które pozwalają na różne wyświetlanie symboli japońskich w zależności od systemu operacyjnego. Przykład poniżej pokazuje jak uzależnić czcionkę od systemu w oknie nauki:

```css
.win .jp { font-family: "MS Mincho"; }
.mac .jp { font-family: "Hiragino Mincho Pro"; }
.linux .jp { font-family: "Kochi Mincho"; }
.mobile .jp { font-family: "Hiragino Mincho ProN"; }
```

A w szablonie karty należy wpisać:

```
<div class=jp>{{Pole}}</div>
```

Dla różnych urządzeń iOS możesz użyć ".iphone" i ".ipad".

Możliwe jest również zastosowanie takich klas jak .gecko, .opera oraz .ie, które będą wyświetlane w zależności od użytej przeglądarki w AnkiWeb. Więcej funkcji opisanych jest na stronie: <http://rafael.adm.br/css_browser_selector/>

Instalowanie czcionek
----------------

Jeżeli używasz Anki  na komuterze w pracy lub w szkole, albo na urządzeniu mobilnym, gdzie nie masz możliwości bezpośredniej instalacji czcionki w systemie, istnieje możliwość dodania czciocnki tylko do Anki, bez jej instalacji w systemie komputera czy komórki.

Aby czcionka mogła zostać użyta przez Anki, musi ona być zapisana w formacie TrueType. Nazwa pliku czcionki w formacie TrueType powinna posiadać końcówkę .ttf, przykładowo: "Arial.ttf". Plik ten powinien zostać umieszczony w folderze z plikami multimedialnymi:

1.  Zmień nazwę pliku, tak żeby na jej początku znajdował się znak podkreślnika, przykładowo "\_arial.ttf". Podkreślnik sygnalizuje Anki, że plik ten będzie używany w szablonie i nie powinien zostać usunięty w przypadku wyszukiwania nieużywanych plików (multimedialnych).

2.  W swoim systemie przejdź do [folderu Anki](files.md), a w nim znajdź folder o nazwie "Użytkownik 1" (lub folder o nazwie zgodnej z nazwą twojego profilu w Anki).

3.  Wewnątrz tego folderu znajduje się kolejny, o nazwie collection.media. Tam umieść swój plik z czcionką (pamiętaj o podkreślniku na początku nazwy pliku).

Następnie zaktualizuj szablon notatki:

1.  Kliknij **Dodaj** w oknie głównym Anki, a następnie wybierz typ notatki, w którym zamierzasz zmienić czcionkę.

2.  Kliknij **Karty**.

3.  W polu Styl, na dole (po ostatnim "}"), dodaj następujący kod, zastępując "\_arial.ttf" nazwą czcionki, którą skopiowałeś wcześniej do folderu z plikami:

```css
@font-face { font-family: myfont; src: url('_arial.ttf'); }
```

Zmień tylko część "arial", a nie "myfont".

Nastepnie możesz albo zmienić czcionkę całej karty, albo pojedynczych pól. Aby zmienić czcionke całej karty, znajdź linię "font-family" w sekcji .card i zmień nazwę czcionki na "myfont". Aby zmienić czcionkę pojedynczych pól, zobacz rozdział u góry o [stylizowaniu pól](templates/styling.md).

Upewnij się, że nazwa czcionki dokładnie zgadza się z tym co wpisałeś w kodzie. Jeżeli plik czcionki nosi nazwę arial.TTF, a w kodzie wpiszesz arial.ttf, czcionka ta nie zadziała w Anki.

Tryb nocny 
----------

Możesz dostosować sposób wyświetlania szablonów, gdy tryb nocny jest włączony w ustawieniach.

Jeśli chcesz jasno-szare tło, możesz wpisać:

```css
.card.nightMode { background-color: #555; }
```

Jeśli posiadasz własny styl "myclass", poniższy kod pokaże tekst na żółto, gdy tryb nocny będzie włączony:
```css
.nightMode .myclass { color: yellow; }
```


Zanikanie i przewijanie
--------------------

Domyślnie Anki automatycznie przewija do odpowiedzi. Program szuka elementu HTML zawierającego "id=answer" i przewija do miejsca, w którym się znajduje. Możesz umieścić "id" w innym elemencie, aby dostosować miejsce przewijania lub usunąć "id=answer", aby je wyłączyć. 

Strona z pytaniem domyślnie zanika. Jeśli chcesz dostosować opóźnienie tego zanikania, możesz umieścić następujący kod na samej górze przedniego szablonu karty:

    <script>qFade=100; if (typeof anki !== 'undefined') anki.qFade=qFade;</script>

100 (milisekund) to wartość domyślna; ustaw na 0, aby wyłączyć zanikanie.

Javascript
----------

Jako, że karty Anki są traktowane jak strony internetowe, możliwe jest załączonie kodu Javascript do kart poprzez szablon karty.

Javascript jest zaawansowana funkcją i wiele rzeczy może nie działać. **Funkcjonalność ta jest dostępna bez żadnego wsparcia ani gwarancji**. Nie zapewniamy żadnego wsparcia w pisaniu Javascript, ani nie gwarantujemy, że twój kod będzie działał w przyszłych wersjach Anki bez konieczności jego modyfikacji. Jeśli nie masz ochoty na zajmowanie się samemu problemami, które napotkasz, unikaj używania Javascript.

Każdy klient Anki może implementować pokazywanie kart inaczej, więc będziesz musiał przetestować, zachowanie kodu na różnych platformach. Wielu klienów jest zaimplementowanych poprzez utrzymywanie długo działającej strony internetowej i dynamiczne jej uaktualnianie w czasie, gdy karty są powtarzane, więc twój kod Javascript będzie musiał aktualizować sekcje dokumentu używając komend takich jak document.getElementById(), zamiast document.write()

Funkcje takie jak window.alert również nie są dostepne. Anki zapisze błedy Javascript w terminalu, więc jeśli korzystasz z Maka lub Windowsa, będziesz musiał ręcznie wyłapać błędy i zapisać je do dokumentu, aby je zobaczyć. Nie ma dostepnego debuggera, więc aby rozwiązać problemy. będziesz musiał rozbijać twój kod, aż nie odnajdziesz, które części powodują problemy.
