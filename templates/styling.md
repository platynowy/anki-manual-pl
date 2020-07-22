Stylizowanie kart
------------

Możesz obejrzeć [film o stylizowaniu kart](http://www.youtube.com/watch?v=F1j1Zx0mXME&yt:cc=on)(w języku angielskim) na YouTube.
Ten film używa interfesju Anki 2.0, ale główne założenia pozostąły  takie same.

Pomiędzy obszarem edycji szablonu przodu i tyłu znajduje się obszar Styl. Możesz w nim zmieniać kolor tła karty, standardową czcionkę, wyrównanie tekstu i tak dalej.

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
Kolor tła karty,

Jakakolwiek komenda CSS może byc wpisana w oknie stylizacji - użytkownicy zaawansowani mogą dodać rzeczy takie jak tło lub gradient. Jeśli zastanawiasz się jak uzyskac określone formatowanie, poszukaj w internecie informacji jak wpisac je w CSS. W sieci znajduje się wiele informacji na ten temat.

Dany styl nadawany jest jednocześnie wszystkim kartom należącym do tego samego typu notatki. Możliwe jest jednak nadawanie wyjątków. Przykładowo poniższy kod nada wszystkim kartom tło koloru żółtego, z wyjątkiem pierwszej karty, która będzie miała tło niebieskie:

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

Możesz interaktywnie ekslorować stylizowanie kart używając Chrome:

<https://ankitects.github.io/addon-docs/#/porting2.0?id=webview-changes>

Stylizowanie pól
-------------

Domyślnie stylizowanie ustawione w szablonie obejmuje całą zawartość karty. Możliwe jest jednak nadanie poszczególnym polom ich własnych stylów czcionki, koloru itd. Funkcja ta jest szczególnie istotna podczas nauki języków obcych, kiedy dla danego tekstu musi zostać użyta specyficzna czcionka np. hebrajska lub arabska, gdyż w przeciwnym razie tekst nie zostanie poprawnie wyświetlony.

Powiedzmy, że masz w notatce pole o nazwie "Wyrażenie" i chcesz aby jego treść na karcie była wyświetlana przy pomocy tajskiej czcionki "Ayuthaya" (działa tylko na systemach Mac OSX). Twój szablon wygląda na razie w taki sposób:

    Co oznacza {{Wyrażenie}}?

    {{Notatki}}

Pierwszym krokiem będzie umieszczenie zawartości szablonu przodu w znacznikach HTML. Przed tekstem umieścimy:

    <div class=mojstyl1>

A po nim:

    </div>

Zastosowanie tych znaczników mówi Anki, żeby w stosunku do zawartego pomiędzy nimi tekstu został zastosowany jakiś styl, w tym przypadku o nazwie "mojstyl1". Styl ten utworzymy za chwilę.

Jeśli chcemy, żeby cały tekst Przodu posiadał dany styl to nasz szablon przodu będzie wyglądał następująco:

    <div class=mojstyl1>Co oznacza {{Wyrażenie}}?</div>

    {{Notatki}}

A jeśli chcemy, żeby tylko nasze pole "Wyrażenie" posiadało dany styl czy daną czcionkę to użyjemy takiego kodu:

    Co oznacza <div class=mojstyl>{{Wyrażenie}}</div>?

    {{Notatki}}

Po edycji Szablonu przodu musimy przejść teraz do środkowego obszaru Styl, zlokalizowanego pomiędzy obszarami Szablon przodu i Szablon tyłu. Standardowo zawartość obszaru Styl powinna wyglądąć tak:

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

Możliwa jest również wykorzystywanie zewnętrznych czcionek bez konieczności ich instalacji na komputerze czy urządzeniu mobilnym. Więcej informacji na ten temat znajduje się w rozdziale na temat instalacji czcionek.

Przyciski ponownego odtwarzania dźwieku
--------------------

Kiedy dźwięk lub tekst na mowę (TTS) znajduje sie w twoich kartach, Anki pokaże przyciski, na które możesz kliknąc, aby ponownie dotworzyć dźwięk. 

Jeśli wolisz nie widzieć tych przycisków, możesz je ukryć na ekranie ustawień.

Możesz zmienić ich wygląd w obsarze stylowania, na przykład jeśli chcesz, aby były one mniejsze i pokolorowane możesz wpisać nastepujący tekst:

```css
.replay-button svg { width: 20px; height: 20px; }
.replay-button svg circle { fill: blue; }
.replay-button svg path { stroke: white; fill: green; }
```

Kod HTML
----------

Szablony kart obsługują znaczniki języka HTML. Oznacza to, że wygląd kart może być dostosowany w ten sam sposób, w którym pisane są strony internetowe. Wspierane są tabele, listy, obrazy i odnośniki do zewnętrznych stron internetowych. Przykładowo, stosując odpowiedni układ tabeli możesz stworzyć szablon, w którym pytanie wyświetlane będzie po lewej stronie karty, zaś odpowiedź po prawej, zamiast standardowo na górze i na dole.

Nie ma sensu opisywać w tej instrukcji wszystkich możliwych zastosowań języka HTML, gdyż w internecie znaleźć możesz  wiele bardzo dobrych kursów na ten tema, jeśli chcesz dowiedzieć się więcej.

Wygląd w przeglądarce
------------------

Jeśli twoje szablony kart są skomplikowane, może być trudno odczytać kolumny "pytanie" i "odpowiedź" (nazwane "Przód" i "Tył") w [liście kart]. Opcja "wygląd w przeglądarce" pozwala określić własny szablon, uzywany tlyko w przeglądarce, więc jeśli chceszmożesz dodać tylko ważne pola i zmienić ich kolejność. Składnia jest taka sama jak w standardowych szablonach kart.

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
<div class=jp>{{Field}}</div>
```

Dla różnych urządzeń iOS możesz użyć "iphone" i ".ipad".

Możliwe jest również zastosowanie takich klas jak .gecko, .opera oraz .ie, które będą wyświetlane w zależności od użytej przeglądarki dla AnkiWeb. Więcej funkcji opisanych jest na stronie: <http://rafael.adm.br/css_browser_selector/>

Instalowanie czcionek
----------------

If you’re using Anki on a work or school computer where you don’t have
permission to install new fonts, or you’re using Anki on a mobile
device, it’s possible to add fonts directly to Anki.

To add a font to Anki, it must be in the TrueType format. TrueType fonts
have a filename ending in .ttf, such as "Arial.ttf". Once you’ve located
a TrueType font, we’ll need to add it to the media folder:

1.  Rename the file, adding an underscore at the start, so it becomes
    like "\_arial.ttf". Adding an underscore will tell Anki that this
    file will be used on a template, and should not be deleted when
    checking for unused media.

2.  In your computer’s file browser, go to your [Anki Folder](files.md),
    and then a folder called "User 1" (or your profile name if you’ve
    renamed/added profiles).

3.  Inside the folder, you should see a folder called collection.media.
    Drag the renamed file to that folder.

After that, we need to update the template:

1.  Click **Add** at the top of the main screen, and then select the
    note type you want to change with the top left button.

2.  Click **Cards**.

3.  In the styling section, add the following text to the bottom (after
    the last "}" character), replacing "\_arial.ttf" with the name of
    the file you copied into your media folder:

```css
@font-face { font-family: myfont; src: url('_arial.ttf'); }
```

Only change the "arial" part, not the "myfont" part.

After that, you can either change the font for the entire card, or for
individual fields. To change the font for the entire card, simply locate
the font-family: line in the .card section and change the font to
"myfont". To change the font for only certain fields, please see the
[Field Styling](templates/styling.md) instructions above.

Please make sure the filenames match exactly. If the file is called
arial.TTF and you write arial.ttf in your card templates, it will not
work.

Night Mode
----------

You can customize the way templates appear when night mode is enabled in
the preferences screen.

If you wanted a lighter grey background, you could use
something like:

```css
.card.nightMode { background-color: #555; }
```

If you have a 'myclass' style, the following would show the text in
yellow when night mode is enabled:

```css
.nightMode .myclass { color: yellow; }
```


Fading and Scrolling
--------------------

Anki will automatically scroll to the answer by default. It looks for a
HTML element with id=answer, and scrolls to that. You can place the id
on a different element to adjust the scrolling position, or remove the
id=answer to turn off scrolling.

The question side of a card fades in by default. If you wish to adjust
this delay, you can place the following at the top of your front card
template:

    <script>qFade=100; if (typeof anki !== 'undefined') anki.qFade=qFade;</script>

100 (milliseconds) is the default; set to 0 to disable fading.

Javascript
----------

As Anki cards are treated like webpages, it is possible to embed some
Javascript on your cards via the card template.

Because Javascript is an advanced feature and so many things can go
wrong, **Javascript functionality is provided without any support or
warranty**. We can not provide any assistance with writing Javascript,
and can not guarantee any code you have written will continue to work
without modification in future Anki updates. If you are not comfortable
addressing any issues you encounter on your own, then please avoid using
Javascript.

Each Anki client may implement card display differently, so you will
need to test the behaviour across platforms. A number of clients are
implemented by keeping a long running webpage and dynamically updating
parts of it as cards are reviewed, so your Javascript will need to
update sections of the document using things like
document.getElementById() rather than doing things like
document.write().

Functions like window.alert are also not available. Anki will write
javascript errors to the terminal, so if you’re running on a Mac or
Windows computer, you’ll need to manually catch the errors and write
them to the document to see them. There is no debugger available, so to
figure out problems you’ll need to break down your code until you
discover which parts are causing problems.
