# Importowanie

Anki może importować pliki tekstowe, spakowasne talie Anki (stworzone poprzez wyeksporotwanie talii w Anki), pliki Mnemosyne 2.0 .db oraz pliki SuperMemo .xml. Aby zaimportować plik, opcje Plik w menu, a nastepnie "Importuj".

## Pliki tekstowe

Każdy **czysty plik tekstowy**, w którym pola oddzielone są od siebie przecinkami, średnikami lub tabulatorami może zostać zaimportowany do Anki. Aby import tych danych przebiegł prawidłowo należy spełnić następujące warunki:

-   Plik musi być zapisany w formacie tekstowym .txt . Inne formaty plików jak .xls, .rtf, .doc muszą najpierw zostać zapisane jako plik tekstowy. (.txt)

-   Plik tekstowy musi być zakodowany w UTF-8 (patrz niżej).

-   Anki określa liczę pól w pliku na podstawie pierwszego wiersza pliku (nie będącego komentarzem). Wszystkie pozostałe linie, które nie posiadają tej samej liczby pól są ignorowane.

-   Pierwszy wiersz definiuje również rodzaj sepratora - jeżeli Anki odnajdzie ; w pierwszym wierszu, w kolejnych również będzie poszukiwał tego sepratora, nawet jeśli wystąpi w nim przecinek lub tabulator.

Pola znajdujące się w pliku tekstowym mogą zostać przekształcone w dowolne pole notatki, także w tagi. Możesz wybrać, które pole w pliku odpowiada któremu polu w notatce.

Podczas importu pliku tekstowego możesz oczywiście określić, do której talii zostaną zaimportowane notatki. Pamiętaj jednak, że jeśli masz włączoną opcję nadpisywania talii dla jednego lub więcej szablonów, karty zostaną dodane do talii wymuszonej przez tę opcje, a nie do tej, która wybrałeś.

Przykład prawidłowego pliku:

    foo bar; bar baz; baz quux
    jabłko; banan; winogron

Są dwa sposob, aby uwzgledniać nowe linie w polach.

**Unikaj wielu linii poprzez wplatanie zawartości pola w podwójne cudzysłowy**:

    cześć; "to jest
    odpowiedź w dwóch liniach"
    dwa; to jest odpowiedź w jednej linii

Ponieważ cudzysłowy są używane do kreslenie gdzie pole się kończy, a gdzie zaczyna, jeśli chciałbyś te cudzysłowy umieścić w polu, musisz zamienić pojedyńczy podwójny cudzysłów dwoma pojedyńczymi cudzysłowami, aby "uniknąć" traktowanie ich w zwykły sposób

    pole pierwsze;"pole drugie z ""podwójnymi cudzysłowami"" w środku"

Gdy używasz programów z arkuszami kalkulacyjnymi takimi jak Libreoffice, aby utworzyć plik CSV, prgoram automatycznie zajmie się powyższą sprawą.

**Używaj nowych linii HTML**:

    cześć; to jest<br>odpowiedź w dwóch liniach
    dwa; to jest odpowiedź w jednej linii

Musisz włączyć opcję "zezwól na HTML w polach" w oknie importowania, aby nowe linie HTML zadziałały.

Podwójne cudzysłowy nie będa działac poprawnie, jeśli używasz wypełniania luk, które obejmuje wiele wierszy. W tym przypadku, używaj nowych linii HTML. 

Możesz równiez dołączyć etykiety w innym polu i wybrac je jako pole z etykietami w oknie importowania:

    pierwsze pole; drugie pole; etykiety

To przykład poprawnego pliku, gdzie pierwsza linia jest ignorowana (\#)):

    # to komentarz, który jest ignorowany
    foo bar; bar baz; baz quux
    pole1; pole2; pole3

### Arkusze kalkulacyjne i UTF-8

Jeśli w twoim pliku znajdują się znaki z innego alfabetu niż łaciński (np. akcenty, język japoński i tym podobne). Anki oczekuje plików zapisanych w kodowaniu UTF-8. Najłatwiejszym sposobem, aby zrobić taki plik to użycie programu arkuszy kalkulacyjnych LibreOffice zamiast Excela, aby wyedytowac plik, jako ze wspiera on łatwo UTF-8 oraz eksportuje poprawnie wieloliniową zawartość, w przeciwieństwie do Excela. Jeśli jednak chcesz użyć Excela, zobacz [ten post na forum](https://docs.google.com/document/d/12YE_FS6A9ANLTESJNtPP116ti4nNmCBghyoJBRtno_k/edit?usp=sharing)
 
Aby zapisać w LibreOffice arkusz kalkulacyjny do pliku, który Anki będzie w stanie odczytać idź do Plik&gt;Zapisz jako, a nastepnie wybierz CSV jako typ pliku. Po akceptacji ustawień domyslnych, LibreOffice zapisze plik, który będziesz mógł zaimportować do Anki

### HTML

Anki może traktować teksrt zaimportowany z plików tekstowych jako HTML (język uzywany do tworzenia stron internetowych). Oznacza to, że tekst z pogrubieniem, kursywą i innym formatowaniem może zostać wyeksporrtowany ponownie do pliku tekstowego, a następnie ponownie zaimportowany. Jesli chcesz załączyć formatowanie HTML, możesz zaznaczyć "dołącz HTML do plików" podczas importowania. Możesz to wyłączyć, jeśli importujesz karty, w których znajdują się nawiasy ostry lub inna składnię HTML.

Jeśli chcesz użyć formatowania HTML do formatowania pliku, ale również chcesz załączyć nawiasy ostre, możesz je zapisać inaczej:

-   Dla "&lt;", użyj "&lt;"

-   Dla "&gt;", użyj "&gt;"

### Importowanie plików multimedialnych

Jeśli chcesz załączyć dźwięk i obrazy z importowanego pliku tekstowego, skopiuj pliki do [folderu collection.media](files.md) **Nie kopiuj podkatalogów do folderu plików, niektóre funkcje mogą nie działać, jeśli to zrobisz**

Po skopiowaniu plików, zmień jedno z pól w pliku tekstowym. jak niżej:

    <img src="mojobraz.jpg">

lub

    [sound:mojdzwiek.mp3]

Możesz też użyć opcji [znajdź i zamień](browsing.md) w oknie przeglądarki, aby zaktualizować wszystkie pola na raz. Jeśli pole zawiera tekst taki jak "mojeaudio", i chciałbyś, żeby odtwarzało ono dźwięk, szukałbyś (.\*), i zamieniłbyś to na "\[sound:\\1.mp3\]", z włączonączonymi wyrażeniami regularnymi. 

Podczas impotowania pliku tekstowego z tym sposobem, musisz się upewnić, aby włączyć opcję "zezwól na HTML".

Możesz chcieć wstawić poniższy, lub podobny  tekst w szablon:

    <img src="{{nazwa pola}}">

W Anki taka komenda nie zadziałą z dwóch powodów: wyszukiwanie używanych plików jesy wymagające, jako, że każda karta musi być wyrenderowana oraz taka funkcjonalność nie ejst jesna dla użytkowników udostępnionych talii. Zamiast tego żżyj techniki znajdź i zamień Anki doesn’t support this for two reasons: searching for used media is
expensive, as each card has to be rendered, and such functionality isn’t
obvious to shared deck users. Please use the find & replace technique
instead.

### Masowe dodawanie plików multimedialnych

Inną opcją importowania dużej ilości plików na raz jest [dodatek media import](https://ankiweb.net/shared/info/1531997860). Automatycznie tworzy on notatki dla wszystkich plików w folderze, z nazwami plików na przodzie (odejmując rozszerzenie, więc plik nazwany cytryna.jpg na przodzie wyglądalby jak "cytryna") oraz obrazy i dźwięk na tyle. Jeśli chciałbyś innne ułożenie plików multimedialnych oraz nazw plików, możesz [zmienić typ notatki](browsing.md) stworzonych kart po zakończonej operacji.

### Dodawanie etykiet

Jeśli chcesz dodać "etykieta1" i "etykieta2" do każdej linii, którą importujesz, dodaj poniższy tekst na górze pliku tekstowego:

    tags:etykieta1 etykieta2

### Duplikaty i aktualizowanie

Podczas importowania plików tekstowych, Anki używa pierwszego pola aby ustalić, czy notatka jest unikalna. Domyślnie, jeśli plik, który importujesz posiada pierwsze pole, które zgadza się z jedna z isniejacych notastek w twojej kolekcji i ta istniejaca notatka jest tym samym typem jak ta, która importujesz, Anki zaktualizuje reszte pól istniejącej notatki  bazujac na zaimportowanym pliku. Wysuwane menu w oknie importu pozwala zmienic to zachowanie na kompletne ignorowanie duplikatów lub importowanie ich jako nowe notatki zamaist aktualizacji już istniejących.

Duplikaty są sprawdzane dla całej kolekcji, nie tylko w obecnej talii. Jeśli Anki wskazuje, że notatki nie zostały zmienione (podczas gdy oczekiwałeś, ze zostana zaimportowane) sprawdź, czy notatki nie znajdują się już gdzieś w kolekcji.

Jesli masz włączone aktualizowanie notatek i starsze wersje tych notatek, które importujesz znajdują się już w twojej kolekcji, beda one aktualizowane w miejscu (w ich taliach) zamiast być przesuwane do talii, do której importujesz nowe karty. Jeśli notatki śa aktualizowane w miejscu, istniejace informacje o planowaniu w ich wszystkich kartach zostaną zachowane.

Aby dowiedzieć się, jak Anki radzi sobie z duplikatami w plikach .apkg, zobacz rozdział o [spakowanej talii](exporting.md).
