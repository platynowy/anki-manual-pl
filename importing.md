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

Anki can treat text imported from text files as HTML (the language used
for web pages). This means that text with bold, italics and other
formatting can be exported to a text file and imported again. If you
want to include HTML formatting, you can check the "allow HTML in
fields" checkbox when importing. You may wish to turn this off if you’re
trying to import cards whose content contains angle brackets or other
HTML syntax.

If you wish to use HTML for formatting your file but also wish to
include angle brackets, you may write them differently:

-   For "&lt;", use "&lt;"

-   For "&gt;", use "&gt;"

### Importowanie plików multimedialnych

If you want to include audio and pictures from a text file import, copy
the files into the [collection.media folder](files.md). **Do not put
subdirectories in the media folder, or some features will not work.**

After you’ve copied the files, change one of the fields in your text
file as follows.

    <img src="myimage.jpg">

or

    [sound:myaudio.mp3]

Alternatively, you can use the [find and replace](browsing.md) feature
in the browse screen to update all the fields at once. If each field
contains text like "myaudio", and you wish to make it play a sound,
you’d search for (.\*) and replace it with "\[sound:\\1.mp3\]", with the
'regular expressions' option enabled.

When importing a text file with these references, you must make sure to
enable the "Allow HTML" option.

You might be tempted to do this in a template, like:

    <img src="{{field name}}">

Anki doesn’t support this for two reasons: searching for used media is
expensive, as each card has to be rendered, and such functionality isn’t
obvious to shared deck users. Please use the find & replace technique
instead.

### Masowe dodawanie plików multimedialnych

Another option for importing large amounts of media at once is to use
the [media import add-on](https://ankiweb.net/shared/info/1531997860).
This add-on will automatically create notes for all files in a folder
you select, with the filenames on the front (minus the file extension,
so if you have a file named apple.jpg, the front would say 'apple') and
the images or audio on the back. If you would like a different
arrangement of media and filenames, you can [change the note
type](browsing.md) of the created cards afterwards.

### Dodawanie etykiet

If you want to add 'tag1' and 'tag2' to every line you’re importing, add
the following to the top of the text file:

    tags:tag1 tag2

### Duplikaty i aktualizowanie

When importing text files, Anki uses the first field to determine if a
note is unique. By default, if the file you are importing has a first
field that matches one of the existing notes in your collection and that
existing note is the same type as the type you’re importing, the
existing note’s other fields will be updated based on content of the
imported file. A drop-down box in the import screen allows you to change
this behaviour, to either ignore duplicates completely, or import them
as new notes instead of updating existing ones.

The duplicate check is done for your 'entire collection', not just in
the current deck. If Anki is indicating that notes have not changed when
you expected them to be imported, please check that the notes are not
already in your collection somewhere.

If you have updating turned on and older versions of the notes you’re
importing are already in your collection, they will be updated in place
(in their current decks) rather than being moved to the deck you have
set in the import dialog. If notes are updated in place, the existing
scheduling information on all their cards will be preserved.

For info on how duplicates are handled in .apkg files, please see the
[Deck Packages](exporting.md) section below.
