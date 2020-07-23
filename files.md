# Zarządzanie plikami i kolekcją

## Sprawdzanie kolekcji

Dobrze jest od czasu do czasu sprawdzić , czy plik kolekcji nie zawiera błedów. Możesz to zrobić poprzez menu "Narzędzia&gt;Sprawdź baze danych". Sprawdzanie bazy danych daje pewnośc, że plik nie jest uszkodzony. Funkcja również odubdowuje wewnętrzne struktury i optymalizuje plik .

Gdy sprawdzasz bazę danych, twoja lista etykiet równiez jest odbudowywana. Kiedy usuwasz pojedyńcze talie lub karty, Anki nie aktualizuje listy uzywanych etykiet, poniewaz byłoby to nieefektywne. Jesli chcesz usunąc stare, nieuzywane etykiety, użyj tej funkcji.

Pamiętaj, że Anki automatycznie optymalizuje twoją kolekcję co 2 tygodnie. Dzieki tej optymalizacji masz pewność, że kolekcja bedzie dobrze działać. Anki nie sprawdza jednak wtedy błędów, ani nie odbudowywuje listy etykiet.

## Lokalizacje plików

W systemie **Windows**, najnowsze wersje Anki przechowują pliki w folderze appdata. Możesz się do niego dostąc poprzez włączenie menadżera plików i wpisanie `%APPDATA%\Anki2` w polu wyszukiwania. Starsze wersje Anki przechowywały pliki w folderze nazwanym `Anki`, który znajdował sie w folderze `Dokumenty` .

Na komputerach **Mac**, najnowsze wersje Anki przechowują wszystkie pliki w folderze `~/Library/Application Support/Anki2`. Biblioteka jest domyślnie ukryta, ale można ją zobaczyć w Finderze poprzez przytrzymanie przycisku "Option" podczas wchodzenia do menu Go". Jeśli posiadasz zainstalowana starsza wersję anki, pliki znajdują sie w folderze `Documents/Anki`.  

Na systemie **Linux**, najnowsze wersje Anki przechowują twoje dane w `~/.local/share/Anki2` lub, jeśli ustawiłes własną ścieszkę w `$XDG_DATA_HOME/Anki2`. Starsze wersje Anki przechowywały pliki w `~/Documents/Anki` lub `~/Anki`

W folderze Anki znajdują się ustawienia programu jak i ustawienia profili. Znajdują się one w folderze prefs.db. 

Istnieje równiez osobny folder dla każdego profilu. Ten folder zawiera:

- Twoje notatki, talie, karty i tym podobne - w pliku nazwanym collection.anki2

- Twoje pliki audio i obrazy -  w folderze collection.media 

- Folder z kopiami zapasowymi

- Niektóre pliki systemowe

Nigdy nie powinieneś kopiować lub przenosić twojej kolekcji podczas, gdy Anki jest otwarte. Może to doprowadzić do uszkodzenia kolekcji. Nie przenoś ani nie modyfikuj równiez innych plików w tym folderze.

## Opcje uruchamiania

Jeśli dokonałeś krytycznej zmiany na jednym komputerze, a na drugim posiadasz nieuszkodzoną kopię, możesz chcieć włączyć Anki bez synchronizacji, aby uzyć pełnej sycnhronizacji bez uprzedniego pobierania zmian. Podobnie, jeśli natrafisz na problemy z Anki, możesz chcieć (lub możesz zostać poinstruktowany) wyłaczyć tymczasowo dodatki, aby sprawdzić, czy któryś z nich powoduje problem. Możesz zrobić obie te rzeczy przytrzymując Shift podczas uruchamiania Anki.

Jest możliwe ustawienie własnego folderu podczas uruchamiania. Jest to funkcja zaawansowana, stworzona głównie w celach instalacji na urządzeniu przenośnym i w wiekszości przypadków zalecamy używanie domyślnej lokacji.

Wzór, aby okreslić folder alternatywy wygląda nastepująco:

    anki -b /ścieżka/do/folderu/anki

- Jeśli istnieje kilka profili, moższ wpisać -p &lt;nazwa profilu&gt;, aby załadowac okreslony profil.

- Aby zmienić język interfejsu, użyj -l &lt;kod języka iso 639-1&gt;, na przykład "-l pl", aby ustawić język na polski. 

Jeśli zawsze chcesz uzywac własnego folderu, możesz zmodyfikowac twój skrót do Anki. na Windowsie, kliknij prawym przyciskiem na skrót, wybierz "Właściwości", zakładke "Skrót" i dodaj "-b
\\ścieżka\\do\\folderu\\anki, po ściezce do programu. Po wpisaniu tekst powinien wyglądać mniej więcej nastepująco:" 

    "C:\Program Files\Anki\anki.exe" -b "C:\AnkiDataFolder"

Możesz równiez uzywać tej techniki z wyzej opisana opcją "-l", aby łatwo uzywać Anki w róznych językach.

Na Windowsie powinieneś używać (\\), nie zaś (/).

Na Maku nie istnieje łatwa metoda na zmianę zachowania probramu poprzez nacisniecie na ikonę Anki. Jest za to możliwe uruchomienie anki z terminala z własnym folderem:

    open /Applications/Anki.app --args -b ~/myankifolder

Alternatywnie możesz okreslić zmienną srodowiska "ANKI_BASE".
Na Windowsie możesz okreslić zmienna środowiska poprzez:

    set "ANKI_BASE=C:/path/to/AnkiDataFolder"

Na systemach Linux i MacOS, możesz uzyć:

    export ANKI_BASE="/path/to/AnkiDataFolder"

## DropBox i synchronizacja plików 

Nie polecamy synchronizowanie folderu Anki bezpośrednio z usługami synchronizacji firm trzecich, ponieważ może to prowadzić do uszkodzenia bazy danych, gdy pliki są synchronizowane podczas użycia.

Jeśli chcesz tylko synchronizowac pliki, możesz podłączyć zewnętrzne foldery bezpośrednio do usług takich jak DropBox. Zobacz <http://www.dropboxwiki.com/tips-and-tricks/sync-other-folders>, aby dowiedzieć się więcej.

Jeśli chcesz także mieć w taki sposób synchronizowaną kolekcję, ostro zalecamy stworzenie skryptu, który kopiuje pliki z synchronizowanego folderu do folderu lokalnego, uruchamia anki, a nastepnie kopiuje pliki z powrotem, gdy Anki jest zamknięte. Daje to pewnosć, że pliki nigdy nie sa synchronizowane gdy są otwarte

## Sieciowe systemy plików

Bardzo zalecamy, pliki byłī przechowywane na lokalnym dysku twardym, ponieważ sieciowe systemy plików moga prowadzić do uszkoczenia bazy danych. Jeśli sieciowy system plików jest twoją jedyną, zalecane jest czeste uzywanie opcji Narzędzia&gt;Sprawdź baze danych

## Uruchamianie z pendrive'a

Na Windowsie anki może zostac zainstalowane na pendrive'ie / dysku przenośnym i być uruchamiane jako przenośna aplikacja. Poniższy przykład zakłada, że twój pendrive to dysk G.

- Skopiuj folder \\Program Files\\Anki  na pendrive'a, tak abyś miał folder taki jak G:\\Anki.

- Utwórz plik tekstowy nazwany  G:\\anki.bat, zawierający nastepujący tekst:

<!-- -->

    g:\anki\anki.exe -b g:\ankidata

Jesli chciałbyś, aby czarne okno konsoli nie było cały czas wyświetlane, możesz zamiast tego wpisać:

    start /b g:\anki\anki.exe -b g:\ankidata

- Podwójne klikniecie na anki.bat powinno uruchomić Anki z danymi użytkownika przechowywanymi w
  stored in G:\\ankidata.

Jest wymagana pełna ściezka, włącznie z literą dysku -  jesli spróbujesz wpisać `\anki\anki.exe`, synchronizacja przestanie działać.

Synchronizacja plików z AnkiWeb może nie działac, jesli twój dysk jest sformatowany jako system plików FAT32. Sformatuj dysk w systemie plików NTFS, aby miec pewnosc, że pliki synchronizują się prawidłowo.

## Kopie zapasowe

Each time your collection is closed (when closing Anki, switching
profiles, or synchronizing your deck), Anki exports your collection into
the backups folder. By default Anki will store up to 30 backups; you can
adjust this in the [preferences](preferences.md).

Automatic backups do not protect against disk or computer failure, and
do not extend to your media. To keep your collections safe, please
consider making manual backups too.

The easiest way to make a manual backup is to use the File&gt;Export
menu item to export all decks with scheduling and media information
included, which will save your data to a .colpkg file.

If you want to back up multiple profiles and your add-ons as well, you
can make a complete copy of your [Anki folder](files.md). Please make sure
you close Anki first, as backups may be corrupt if run while Anki is
open.

To restore from an automatic backup:

1.  From the File menu, select Switch Profile to show the Profiles
    window.

2.  Select the profile you wish to restore on the left.

3.  Click the Open Backup…​ button.

4.  Choose Yes and the available backups will appear.

5.  Open a backup based on the date you wish to restore to.

6.  Check that that the backup that was restored was the one you
    intended. If you wish to try a different backup, return to step 1.

7.  Anki has disabled automatic syncing and backups while you check the
    backup. When you’re happy with the backup you’ve selected, quit Anki
    and start it again to return to the normal behaviour.

Anki also logs deleted notes to a text file called deleted.txt in your
profile folder. These notes are in a text format that can be read by
File&gt;Import, though please note the import feature only supports a
single note type at one time, so if you have deleted notes from
different note types, you’ll need to split the file into separate files
for each note type first.

## Inaccessible Harddisk

If Anki can’t write to files in the [Anki folder](files.md), a message
will be displayed on startup saying that Anki can’t write to the
harddisk, and Anki will close. If you’re unsure how to fix the
permissions, please contact someone near you who is knowledgable about
computers and can help you out.

## Permissions of Temp Folder

Anki uses the system’s temporary folder to store temporary data. If the
permissions of this folder have been changed from the default settings
by a rogue app or buggy antivirus app, Anki will not function properly.

If you’re on a Windows 7 machine, the general steps to fix the problem
are listed below. As this is somewhat complicated, please ask someone
knowledgeable about Windows if you are not sure.

1.  Click on the start bar, and type in %temp% (including the percents),
    then hit enter.

2.  Go up one folder, and locate the temp folder. Right click on it, and
    choose Properties.

3.  In the security tab, click on Advanced.

4.  Click on the Owner tab. If you’re not listed as the owner, click the
    button to take ownership.

5.  On the permissions tab, ensure that you have full control. On a
    default W7 install the control will actually be inherited from
    c:\\users\\your-username.

## Corrupt Collections

Anki uses a file format that is robust against program and computer
crashes, but it’s still possible for your collection to become corrupt
if the files are modified while Anki is open, stored on a network drive,
or corrupted by a bug.

When you run Tools&gt;Check Database, you will receive a message if Anki
detects the file has been corrupted. **The best way to recover from this
is to restore from the most recent [automatic backup](preferences.md)**, but
if your backup is too old, then you can attempt to repair the corruption
instead.

On Linux, make sure sqlite3 is installed. On a Mac, it should be
installed already. On Windows, download
<http://www.sqlite.org/sqlite-3_6_23.zip>.

Next, create a backup of your collection.anki2 file, in case something
goes wrong with the steps below.

**Linux/OSX**

Open a terminal, change to the folder your collection is located in, and
type:

    sqlite3 collection.anki2 .dump > dump.txt

Open the resulting dump.txt file in a text editor, and look at the final
line. If it reads "rollback;", change it to "commit;"

Then run the following in a terminal:

    cat dump.txt | sqlite3 temp.file

Make sure you use temp.file - do not put collection.anki2 on the right,
or you will blank out the file. When you’re done, proceed to the final
step.

**Windows**

Copy the `sqlite3.exe` program and your deck to your desktop. Then go to
**Start&gt;Run** and type in `cmd.exe`.

If you’re on a recent Windows, the command prompt may not start on your
desktop. If you don’t see desktop displayed in the command prompt, type
something like the following, replacing 'administrator' with your login
name.

    cd C:\Users\Administrator\Desktop

Then type:

    sqlite3 collection.anki2 .dump > dump.txt

Open the resulting dump.txt file in a text editor, and look at the final
line. If it reads "rollback;", change it to "commit;"

Then run the following in a terminal:

    type dump.txt | sqlite3 temp.file

Make sure you use temp.file - do not put collection.anki2 on the right,
or you will blank out the file. When you’re done, proceed to the final
step.

**Final Step**

Check that you didn’t get an error message, and that temp.file is not
empty. The procedure optimizes the collection in the process, so it’s
normal for the new file to be somewhat smaller than the old one.

When you’ve confirmed the file is not empty:

- rename the original collection.anki2 file to something else

- rename temp.file to collection.anki2

- move collection.anki2 back into your collection folder, overwriting
  the old version

- start Anki and go to Tools&gt;Check Database to make sure the
  collection has been successfully restored.
