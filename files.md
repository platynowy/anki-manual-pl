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

    open /Applications/Anki.app --args -b ~/mojfolderanki

Alternatywnie możesz okreslić zmienną srodowiska "ANKI_BASE".

Na Windowsie możesz okreslić zmienną środowiska poprzez:

    set "ANKI_BASE=C:/ścieżka/do/FolderuZDanymiAnki"

Na systemach Linux i MacOS, możesz uzyć:

    export ANKI_BASE="/ścieżka/do/FolderuZDanymiAnki"

## DropBox i synchronizacja plików 

Nie polecamy synchronizowanie folderu Anki bezpośrednio z usługami synchronizacji firm trzecich, ponieważ może to prowadzić do uszkodzenia bazy danych, gdy pliki są synchronizowane podczas użycia.

Jeśli chcesz tylko synchronizowac pliki, możesz podłączyć zewnętrzne foldery bezpośrednio do usług takich jak DropBox. Zobacz <http://www.dropboxwiki.com/tips-and-tricks/sync-other-folders>, aby dowiedzieć się więcej.

Jeśli chcesz także mieć w taki sposób synchronizowaną kolekcję, ostro zalecamy stworzenie skryptu, który kopiuje pliki z synchronizowanego folderu do folderu lokalnego, uruchamia anki, a nastepnie kopiuje pliki z powrotem, gdy Anki jest zamknięte. Daje to pewnosć, że pliki nigdy nie sa synchronizowane gdy są otwarte

## Sieciowe systemy plików

Bardzo zalecamy, pliki byłī przechowywane na lokalnym dysku twardym, ponieważ sieciowe systemy plików moga prowadzić do uszkoczenia bazy danych. Jeśli sieciowy system plików jest twoją jedyną, zalecane jest czeste uzywanie opcji Narzędzia&gt;Sprawdź baze danych

## Uruchamianie z pendrive'a

Na Windowsie anki może zostac zainstalowane na pendrive'ie / dysku przenośnym i być uruchamiane jako przenośna aplikacja. Poniższy przykład zakłada, że twój pendrive to dysk G.

- Skopiuj folder \\Program Files\\Anki na pendrive'a, tak abyś miał folder taki jak G:\\Anki.

- Utwórz plik tekstowy nazwany G:\\anki.bat, zawierający nastepujący tekst:

<!-- -->

    g:\anki\anki.exe -b g:\ankidata

Jesli chciałbyś, aby czarne okno konsoli nie było cały czas wyświetlane, możesz zamiast tego wpisać:

    start /b g:\anki\anki.exe -b g:\ankidata

- Podwójne kliknięcie na anki.bat powinno uruchomić Anki z danymi użytkownika przechowywanymi w G:\\ankidata.

Jest wymagana pełna ściezka, włącznie z literą dysku -  jesli spróbujesz wpisać `\anki\anki.exe`, synchronizacja przestanie działać.

Synchronizacja plików z AnkiWeb może nie działac, jesli twój dysk jest sformatowany jako system plików FAT32. Sformatuj dysk w systemie plików NTFS, aby miec pewnosc, że pliki synchronizują się prawidłowo.

## Kopie zapasowe

Za każdym razem, gdy twoja kolekcja jest zamykana (podczas zamykania Anki, przełączania profili lub synchronizacji talii), Anki exportuje twoją kolekcję do folderu z kopiami zapasowymi (backups). Domyslnie anki przechowuje do 30 kopii zapasowych. Możesz zmienić tę liczbe w [ustawieniach](preferences.md)

Automatyczne kopie zapasowe nie chronią przed awarią dysku lub komputera i nie przechowują plików multimedialnych. Aby chronić swoją kolekcję, rozważ tworzenie ręcznych  kopii zapasowych.

Najłatwiejszym sposobem utworzenia ręcznej kopii zapasowej jest wejście w menu Plik&gt;Eksportuj, aby wyeksportować wszystkie talie włącznie z  planowaniem i plikami. Plik zawierający twoje dane będzie plikiem .colpkg.

Jesli chcesz utworzyć kopie zapasowe kilku profili oraz dodatków, możesz zrobić kopię [folderu Anki](files.md). Upewnij się najpierw, że Anki jest zamknięte, jako, że kopie zapasowe mogą być uszkodzone, jesli się je uruchomi, gdy Anki jest otwarte (?) If you want to back up multiple profiles and your add-ons as well, you
can make a complete copy of your [Anki folder](files.md). Please make sure
you close Anki first, as backups may be corrupt if run while Anki is
open.

Aby przywrócić z automatycznej kopii zapasowej:

1.  Z menu "Plik", wybierz "Przełącz Profil", aby pokazać ekran z profilami

2.  Wybierz po lewej profil, w którym chcesz przywrócić kopię zapasową.

3.  Klknij na "Otwórz kopię zapasową…​".

4.  Wybierz "Tak", pojawią się dostepne kopie zapasowe.

5.  Otwórz kopię zapasową z dnia, do którego chcesz przywrócić kolekcję.

6.  Sprawdź, czy kopia zapasowa, do której przywróciłeś swoją kolekcję na pewno była tą, do której chciałeś przywrócić. Jeśli chcesz spróbować z inną kopią zapasową, powróć do kroku 1.

7.  Anki wyłączyło automatyczną synchronizację i kopie zapasowe podczas, gdy sprawdzasz kopię zapasową. Jeśli wybrałeś odpowiednią kopię zapasową, zamknij Anki i uruchom ponownie, aby przywrócić normane zachowanie.

Anki równiez prowadzi dziennik usuniętych notatek, zapisuje go w pliku tekstowym nazwanym deleted.txt w folderze profili. Te notatki sa w formacie, który może zostać odczytany przez Plik&gt;Importuj. Jednak pamiętaj, że funkcja "Import"uj obsługuje tylko jeden typ notatki na raz, więc jeśli masz usunięte notatki z różnych typów notatek, bedziesz musiał najpierw rozdzielic plik na kilka innych plików,po jednym dla każdego typu notatki. 

## Niedostępny dysk twardy

Jeśli Anki nie może zapisywać plików w [folderze Anki](files.md), przy starcue pojawi się wiadomość, że Anki nie może zapisywać plików na dysku twardym, po czym program się wyłączy. Jeśli nie jesteś pewien jak naprawić pozwolenia, skontaktuj się z kimś z twojego otoczenia, kto dysponuje wiedzą komputerową i będzie mógł Ci pomóc.

## Uprawnienia do folderu tymczasowego

Anki używa systemowego folderu tymczasowego, aby przechowywać tymaczaowe dane. Jeśli pozwolanie na ten folder zostały zmienione z domyślnych przez jakas aplikację lub błędnie aplikację antywirusową, Anki nie bedzie w stanie działać poprawnie.

Na dole znajduje się opis naprawienia tego problemu dla systemów Windows 7. Jako, ze jest to dość skomplikowane, poproś o pomoc kogoś znającego się na Windowsie, jeśli czegoś nie jesteś pewien.

1.  Kliknij na pasku Start i wpisz %temp% (razem z procentami), a nastepnie naciśnij enter.

2.  Cofnij się jeden folder wstecz oraz znajdź folder "temp". Kliknij na niego prawym przyciskiem i wybierz Właściwości.

3.  W zakładce bezpieczeństwo, kliknij Zaawansowane

4.  Kliknij na zakładkę Właściciel. Jesli nie jesteś wymieniony jako właściciel, kliknij na przycisk, aby się nim stać.

5.  W zakładce pozwolenia, upewnij się, że posiadasz pełną kontrolę On the permissions tab, ensure that you have full control. W domyślnie zainstalowanym Windows 7 kontrola będzie automatycznie nadawana dla c:\\users\\twoja-nazwa-użytkownika. 

## Uszkodzone kolekcje

Anki używa formatu plików, który jest odporny na nieoczekiwane wyłączenia programu i komputera, jednak nadal istnieje możliwość uszkoczenia kolekcji, jesli pliki są modyfikowane, gdy Anki jest otwarte, przechowywane na dysku sieciowym lub uszkodzone przez błąd.

Gdy używasz opcji Narzedzia&gt;Sprawdź bazę danych, otrzymasz wiadomość, czy Anki wykryje plik, który jest uszkodzony. **Najlepszym sposobem, aby uporać się z tym problemem jest przywrócenie  najnowszej [automatycznej kopii zapasowej](preferences.md)**, jednak jesli twoja kopia zapasowa jest zbyt stara, możesz spróbować zamiast tego naprawić kolekcję.

Na systemie Linux, upewnij się, że zainstalowany jest sqlite3. Na Maku powinien się on już znajdować. Na Windowsie pobierz <http://www.sqlite.org/sqlite-3_6_23.zip>.

Nastepnie utwórz kopię zapasową pliku collection.anki2, w razie gdyby coś poszło nie tak.

**Linux/OSX**

Otwórz terminal, zmień na folder, w którym znajduje się twoja kolekcja i wpisz:

    sqlite3 collection.anki2 .dump > dump.txt

Otwórz plik dump.txt w edytorze tekstu i zobacz na ostatnią linię. Jeśli jest w niej napisane "rollback;", zmień ten tekst na "commit;".

Nastepnie uruchom nastepujący kod w terminalu:

    cat dump.txt | sqlite3 temp.file

Upewnij się, ze używasz pliku temp.file - nie wpisuj collection.anki2 po prawej, bo opróżnisz ten plik. Gdy już skończyłeś, przejdż do ostatniego kroku.

**Windows**

Skopiuj program `sqlite3.exe` i twoją talię na pulpit. Następnie włącz Then go to
**Start&gt;Rozpocznij** i wpisz `cmd.exe`.

Jeśli znajdujesz się na jednej z ostatnich wersji systemu Windows, okno komend może nie wyświetlic się na pulpicie. W przypadku, gdy nie widzisz okna komend na pulpicie, wpisz tekst poniższy, zamieniając "administrator" na nazwę użytkownika.
    
    cd C:\Users\Administrator\Desktop
    
Następnie wpisz:

    sqlite3 collection.anki2 .dump > dump.txt

Otwórz plik dump.txt i edytorze tekstu i zobacz ostatnią linię. Jeśli jest w niej napisane "rollback;", zmień ten tekst na "commit;".

Następnie uruchom następujący kod w terminalu:

    type dump.txt | sqlite3 temp.file

Upewnij się, ze używasz pliku temp.file - nie wpisuj collection.anki2 po prawej, bo opróżnisz ten plik. Gdy już skończyłeś, przejdż do ostatniego kroku.

**Ostatni krok**

Sprawdź, czy nie wyskoczyłą żadna wiadomosc z błędem i plik temp.file nie jest pusty. Procedura ta optymalizuje kolekcję, dlatego normalne jest, że nowy plik może mieć  mniejszą wagę od starszego.

Jeśli upewniłeś się, ze plik nie jest pusty:

- zmień nazwe  oryginalnego pliku collection.anki2 na coś innego.

- zmień nazwę temp.file na collection.anki2

- przenieś plik collection.anki2 z powrotem do folderu kolekcji, nadpisując starszą wersję.

- Uruchom Anki i idź do Narzędzia&gt;Sprawdź baze danych, aby upewnić się, że kolekcja została prawidłowo naprawiona.
