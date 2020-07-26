# Zastępowanie pól

## Podstawy zastępowania pól

Podstawowy szablon wygląda w następujący sposób:

    {{Przód}}

Gdy w nawiasy klamrowe wpiszesz jakiś tekst, Anki uzna to za odniesienie do któregoś z istniejących pól o tej samej nazwie. Przy wyświetlaniu danej karty zastąpi ten tekst zawartością danego pola.

W nazwach pól brana jest pod uwagę wielkość liter. Jeśli masz pole nazwane `Przód`, wpisanie `{{przód}}` nie zadziała.

W szablonach możesz umieścić odwołania do dowolnej liczby pól. Możesz w nich również umieszczać możesz dowolny tekst. Na przykład, jeźli uczysz się stolic państw i utworzyłeś typ notatki z polem "Kraj", możesz zmodyfikować szablon przodu, aby wyglądał w nastepujący sposób:

    Jaka jest stolica {{Kraj}}?

Standardowy szablon tyłu karty wygląda tak:

    {{FrontSide}}

    <hr id=answer>

    {{Tył}}

Kod ten należy interpretować w następujący sposób: "pokaż mi pytanie, narysuj linię i pokaż pole Tył".

Kod "id=answer" daje znać Anki, gdzie znajduje się granica miedzy pytaniem i odpowiedzią. Umożliwia to Anki na automatyczne przewijanie do miejsca, gdzie znajduje się odpowiedź, gdy naciśniej przycisk "pokaż odpowiedź" na długiej karcie (szczególnie przydatne na urządzeniach mobilnych z małymi ekranami). Jeśli nie chcesz, aby pozioma linia wyświetlała się na początku odpowiedzi, możesz użyć innego elementu HTML takiego jak akapit lub komenda "div".

## Nowy wiersz

Szablony kart zachowują się jak strony internetowe, co oznacza, że wymagana jest specjalna komenda, aby stworzyć nowy wiersz. Na przykład, jeśli w szablonie napiszesz poniższy tekst:

    jeden
    dwa

W podglądzie karty zobaczysz:

    jeden dwa

Aby dodać nową linię, wystarczy, że pomiędzy dwoma słowami wstawiamy znacznik &lt;br&gt;, jak poniżej:

    jeden<br>
    dwa

Znacznik ten pochodzi z języka HTML i jest skrótem od angielskiego wyrażenia "(line) br(eak)" czyli "łamanie wiersza".

W ten sam sposób można wyświetlać pola notatki. Jeżeli chciałbyś, żeby jedno pole znajdowało sie zaraz pod drugim:

    {{Pole 1}}<br>
    {{Pole 2}}

## Tekst na mowę (Text to Speech - TTS)

Ta funkcjonalność wymaga Anki 2.1.20, lub AnkiMobile 2.0.56. AnkiDroid obecnie nie obsługuje tej metody.

Aby Anki czytało pole Przód przykładowo w języku angielskim amerykańskim, możesz umiescić poniższy tekst w szablonie karty.

    {{tts en_US:Przód}}

Na systemach Windows, MacOS i iOS Anki użyje wbudowanych plików głosowych. Na Linux'ie nie ma wbudowanych głosów, ale moga one być udostępnione przez dodatki takie [jak ten](https://ankiweb.net/shared/info/391644525).

Aby zobaczyć listę dostepnych języków/głosów, umieść poniższy tekst na szablonie karty:

    {{tts-voices:}}

Jeśli jest kilka dostępnych głosów dla danego języka możesz doprecyzować w liście, których głosów chcesz używać, a Anki odtworzy pierwszy dostępny głos. Przykład: 

    {{tts ja_JP voices=Apple_Otoya,Microsoft_Haruka:Pole}}

Ta komenda sprawi, że Anki użyje głosu Otoya na urządzeniu Apple, a głosu Haruka na urządzeniu Windows PC. 

Ustawienie innej szybkości odtwarzania jest możliwe w niektórych wersjach TTS:

    {{tts fr_FR speed=0.8:JakieśPole}}

Umieszczanie informacji o szybkości i głosach nie jest wymagane, jednak trzeba umieścić kod języka.

Na Makach możesz dostosować dostepne głosy

- Otwórz "Preferencje systemowe"

- Kliknij na "Dostępność"

- Kliknij na "Mowa"

- Kliknij na oknienko przy "Głos systemowy" i wybierz "Dostosuj".

Niektóre głosy brzmią lepiej od innych, wiec możesz poeksperymentować, aby znaleźć ten, który ci odpowiada. Pamiętaj o tym, ze głos Siri moze być używany tylko przez aplikacje Apple. Po zainstalowaniu nowych głosów musisz uruchomić Anki ponownie, aby nowe głowy stały się dostępne.

Na urządzeniach z systemem Windows, niektóre głosy takie jak Cortana nie mogą zostać wybrane, ponieważ Microsoft nie udostępnia ich innym aplikacjom.

## Pola specjalne

Istnieje kilka rodzajów pól specjalnych, których możesz użyć w szablonie:

    Znacznik etykiety: {{Tags}}

    Znacznik typu notatki: {{Type}}

    Znacznik nazwy talii: {{Deck}}

    Znacznik podtalii karty: {{Subdeck}}

    Znacznik typu karty ("Przód", itp.): {{Card}}

    Znacznik zawartości przodu karty (poprawna tylko 2 szablonie tyłu): {{FrontSide}}

Znacznik zawartości przodu karty FrontSide nie skopiuje na jej tył nagrania audio. Jeśli chcesz mieć to samo nagranie na przodzie i tyle karty musisz je tam ręcznie dodać.

Tak jak z innymi polami, w polach specjalnych ważna jest wielkosć liter - musisz używać np. `{{Tags}}` zamiast `{{tags}}`.

## Podpowiedzi

Anki umożliwia dodanie do przodu lub tyłu karty własnej podpowiedzi, która wyświetlana będzie tylko po kliknięciu na nią przez użytkownika. Przed dodaniem takiej podpowiedzi należy najpierw rozważyć czy ma ona sens, gdyż takie rozwiązanie znacząco ułatwia naukę. Może się ona stać mało efektywna i trudniej będzie ci zapamiętać w przyszłości daną informację np. jeśli nie przypomnisz sobie podpowiedzi. Przed użyciem podpowiedzi zapoznaj się z podstawowymi zasadami znajdującymi się na stronie: <http://www.supermemo.com/articles/20rules.htm>.

Aby utworzyć podpowiedź, w pierwszej kolejności musisz dodać do notatki nowe pole, w którym podpowiedź będzie przechowywana. Jego nazwa nie ma znaczenia. Jeżeli nie umiesz jeszcze dodawać nowych [pól](editing.md#customizing-fields), zapoznaj się z rozdziałem na ich temat.

Jeśli stworzyłeś już pole podpowiedzi (zakładamy, że nazywa się "Podpowiedź"), możesz teraz nakazać Anki aby pole to zostało automatycznie zakryte. Do szablonu przodu dodaj następujący kod:

    {{hint:Podpowiedź}}

Kod ten pokaże link pokazujacy sie jako "pokaż podpowiedź". Kiedy na niego naciśniesz, zawartość tego pola zostanie pokazana na karcie. (Jeżeli pole Podpowiedź jest puste, nic nie zostanie wyświetlone.)

Jeśli odsłonisz podpowiedź, a następnie wyświetlisz odpowiedź, to podpowiedź zostanie ponownie zakryta. Jeżeli chcesz aby mimo wszystko podpowiedź cały czas pozostawała widoczna, musisz usunąć `{{FrontSide}}` z szablonu tyłu i ręcznie dodać pola, które mają się pojawiać.

Nie jest obecnie możliwe używanie dźwięku w polu podpowiedzi - dźwięk będzie się odtwarzał niezaleznie, czy odsłonięto odpowiedź.

Jeśli chcesz zmienić wygląd, lub zachowanie tego pola, będziesz musiał sam je zaimplementować. W tym miejscu nasza pomoc sie kończy, ale poniższy kod może być dobrym punktem wyjscia:

    {{#Back}}
    ﻿<a class=hint href="#"
    onclick="this.style.display='none';document.getElementById('hint4753594160').style.display='inline-block';return false;">
    Show Back</a><div id="hint4753594160" class=hint style="display: none">{{Back}}</div>
    {{/Back}}

## Linki do słowników

Możesz używac zastepowania pól do tworzenia linków do słowników. Jeśli na przykład uczysz się języka, a twój ulubiony słownik umożliwia szuaknie tekstu przy uzyciu linku, takiego jak:

    http://przyklad.com/search?q=mojeslowo

Dzięki takiej standardowej formie i przy użyciu nazwy pola możesz stworzyć odnośnik do słowa w danym słowniku, który będzie automatycznie uzupełniany o zawartość pola:

    {{Wyrażenie}}

    <a href="http://przyklad.com/search?q={{Wyrażenie}}">sprawdź w słowniku</a>

Powyższa linijka kodu umożliwi ci sprawdzenie znaczenia danego wyrazu w słowniku podczas powtórki. W tej metodzie jest jednak pewien haczyk. Został on opisany poniżej.

## Pomijanie HTML

Podobnie jak w szablonach, w Polach również możliwe jest używanie znaczników HTML. W przykładzie powyższym, gdyby wyrażenie zawierało "mojeslowo" bez żadnego formatowania, wtedy HTML byłoby takie same - "mojeslowo". Ale gdy dodasz formatowanie do pól, dodatkowe HTML jest dołączane. Jeśli "mojeslowo" zostało na przykład pogrubione, HTML wyglądałoby tak "&lt;b&gt;mojeslowo&lt;/b&gt;".

Może to być problemem dla linków takich jak linki do słowników. W powyższym przykładzie, link do słownika byłby taki:

    <a href="http://przyklad.com/search?q=<b>mojeslowo</b>">sprawdź w słowniku</a>

W ten sposób odnośnik najpewniej nie wyświetli żadnej strony, gdyż kod HTML nie jest stosowany w adresach URL.

Aby rozwiązać ten problem, Anki posiada funkcję pomijania kodu HTML znajdującego się w polach notatki. Jeżeli nazwę pola użytą w szablonie poprzedzisz prefiksem text:, Anki w momencie podstawiania zawartości pola do karty, pominie całkowicie jego formatowanie określone przy pomocy HTML. Kod HTML przycisku zawarty w szablonie notatki będzie zatem wyglądał w następujący sposób:

    <a href="http://przyklad.com/search?q={{text:Wyrażenie}}">sprawdź w słowniku</a>

## Pisanie z prawej do lewej

Do nauki języków pisanych z prawej do lewej niezbędne jest stosowanie w szablonie następującego formatowania pól:

    <div dir=rtl>{{PolezTekstemzPrawejdoLewej}}</div>

## Pliki & LaTeX

Anki nie przegląda szablonów w poszukiwaniu odnośników do plików multimedialnych oraz plików LateXa, ze względu na powolność takiego procesu. Ma to pewne następstwa przy załączaniu plików do szablonu.

### Stałe pliki audio i obrazy {docsify-ignore}

Aby dodać plik audio lub obraz, który będzie taki sam na każdej karcie (np. logo firmy w rogu każdej karty):

1.  Zmień nazwę pliku, tak żeby rozpoczynała się od znaku podkreślenia np. "\_logo.jpg". Znak ten informuje program, że plik używany jest przez szablon i powinien być eksportowany i synchronizowany podczas udostępniania talii.

2.  Dodaj odnośnik do pliku w szablonie przodu lub tyłu, przykładowo:

<!-- -->

    <img src="_logo.jpg">

### Odnośniki do pól w nazwach plików{docsify-ignore}

Anki nie obsługuje odnośników do plików w polach. Takie pliki prawdopodobnie nie będą wyświetlane na karcie ani importowane/eksportowane do Ankiweb. Przykład błędnego zastosowania pola w nazwach plików wstawianych do kart:

    <img src="{{Wyrażenie}}.jpg">

    [sound:{{Słowo}}]

    [latex]{{Pole 1}}[/latex]

Jedyną możliwością jest bezpośrednie wstawienie pliku w danym polu. Plik ten powinien posiadać stałą i niezmienną nazwę. Więcej informacji na ten temat znajduje się w rozdziale dotyczącym importowania.

## Pisanie odpowiedzi

Możesz obejrzeć [film dotyczący tej funkcji](http://www.youtube.com/watch?v=5tYObQ3ocrw&yt:cc=on) na
YouTube.

Najłatwiejszym sposobem, aby umożliwić wpisanie odpowiedzi, jest klikniecie "Podstawowa" w górnym lewym rogu na oknie dodawania karty, a następnie wybranie "Podstawowy (wpisywanie odpowiedzi)".

Jeśli pobrałeś udostępnioną talie i chciałbyś wpisywać w niej odpowiedź, możesz zmodyfikować szablon jej kart. Gdy ten szablon wygląda przykładowo tak:

    {{Polskie słowo}}

    {{FrontSide}}

    <hr id=answer>

    {{Obce słowo}}

Żeby mieć możliwość pisania w odpowiedzi musisz dokonać edycji szablonu przodu i tyłu, tak by wyglądały w ten sposób:

    {{Polskie słowo}}
    {{type:Obce słowo}}

Zauważ, ze dodaliśmy `type:` z przodu pola, w którym chcemy wpisywać odpowiedź. Jako, że FrontSide znajduje się na tyle karty, pole wpisywania równiez sie tam pojawi.

Podczas powtórki, pod pytaniem Anki wyświetli puste pole tekstowe, które służy właśnie do wpisania twojej odpowiedzi. Następnie wystarczy, że zatwierdzisz swoją odpowiedź przyciskiem Enter na klawiaturze lub Pokaż odpowiedź na ekranie nauki. Anki wskaże, które części odpowiedzi są błędne. Rozmiar czcionki w pustym polu przeznaczonym do podania odpowiedzi jest zgodnym z tym, który ustawiony jest dla tego pola w oknie "Pole…".

Zauważ, że choć w twojej odpowiedzi mogą pojawić się błędy, to nie wpływają one na ocenę karty. W dalszym ciągu sam oceniasz swoją odpowiedź. Anki nie zrobi tego automatycznie za ciebie na podstawie wpisanego tekstu.

Na karcie może być użyte tylko jedno pole tekstowe służące do wpisywania odpowiedzi. Jeżeli umieścisz ich więcej, wpisywanie odpowiedzi nie zadziała poprawnie. Ponadto odpowiedź może zostać podana w polu tekstowym o wysokości tylko jednej linii, co oznacza, że nie ma sensu porównywanie odpowiedzi z kartami posiadającymi pytanie w wielu liniach.

Zarówno pytanie i jak i odpowiedź wyświetlane są przy użyciu czcionki o stałej szerokości znaków, dzięki czemu możliwe jest czytelne porównywanie wprowadzonych w odpowiedzi znaków z tym co jest napisane w pytaniu. Możesz również zmienić tę czcionkę. Wystarczy, że w oknie Karty…→Styl umieścisz następujący kod:

    code#typeans { font-family: "nazwa_mojej_czcionki"; }

Co wpłynie na nastepujący kod HTML do porównania odpowiedzi:

    <code id=typeans>...</code>

Bardziej zaawansowani użytkownicy mogą również zmienić kolor prostokątów oznaczających błędne i poprawne znaki. Klasy CSS odpowiedzialne za nie to "typeGood", "typeBad" i "typeMissed". Z tych komend AnkiMobile rozpoznaje "typeGood", i "typeBad", ale nie "typeMissed".'.

Jeśli chcesz nadpisać wielkosć pola do wpisywania, ale nie chcesz zmieniać czcionki w oknie Pole, możesz nadpisac domyślny styl używając `!important`, jak poniżej: 

    #typeans { font-size: 50px !important; }

Możliwe jest również pisanie odpowiedzi w kartach z lukami. Aby to zrobić dodaj `{{type:cloze:Text}}` do obu stron szablonu. Szablon tyłu powinien wyglądać następująco:

    {{cloze:Tekst}}
    {{type:cloze:Tekstt}}
    {{Dodatkowe}}

Zauważ, że kod ten, w przeciwieństwie do standardowych kart, musi zostać dodany po obu stronach notatki (typu Luka).

Jeśli jest wiele luk do uzupełnienia, możesz oddzielić odpowiedzi w polu tekstowym używając przecinka

Pola tekstowe do wpisywania odpowiedzi nie pojawią się na [podglądzie](templates/intro.md) w przeglądarce. Pojawią sie za to, gdy uczysz się lub wciśniesz "podgląd" na ekranie z typem kart.
