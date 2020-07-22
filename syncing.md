# Synchronizacja z AnkiWeb

Ankiweb to usługa, która pozwala na synchronizację twojej kolekcji pomiędzy wieloma urządzeniami, a tym samym umożliwia posiadanie zawsze aktualnej talii na każdym z tych urządzeń. Założ [darmowe konto](https://ankiweb.net/)  zanim przejdziesz do dalszej lektury tego rozdziału.

## Konfiguracja

Aby rozpocząć synchronizację kolekcji, naciśnij przycisk Synchronizuj znajdujący się w prawym górnym rogu głownego okna Anki lub naciśnij klawisz "y" na klawiaturze. Zostaniesz poproszony o swoj identyfikator AnkiWeb ID oraz hasło, które określiłeś w procesie rejestracji.

Podczas pierwszej synchronizacji kolekcji, Anki nie będzie w stanie połączyć danych znajdujących się na Ankiweb z tymi, które masz na swoim komputerze, dlatego zostaniesz poproszony o wybranie czychcesz pobrać, czy przesłać dane. Jeśli posiadasz karty z innego urządzenia w AnkiWeb, a na komputerze nie masz żadnych kart wybierz "pobierz", aby zastąpić pustą lokalną kolekcję kartami pobranymi z AnkiWeb. Jeśli masz różne karty na obu urządzeniach, [wymagane jest wiecej pracy](#merging-conflicts), aby uniknąć utraty danych
avoid losing data.  Po tym kroku Anki bez problemu będzie mogło łączyć zmiany w talii pochodzące z różnych lokalizacji, z kilkoma wyjątkami.

Po pierwszej synchronizacji Anki będzie w stanie łączyć zmiany z różnych urządzeń (z kilkoma wyjątkami).

Jeśli kilka osób używa Anki na jednym urządzeniu, i dla każdej z tych osób został utworzony profil, wszyscy beda musieli utworzyć swoje własne konto AnkiWeb, aby móc synchronizować. Zsynchronizowanie różnych profili z jednym kontem AnkiWeb doprowadzi do do utraty danych. 

## Automatyczna synchronizacja

Po pierwszej synchronizacji, każda kolejna wykonywana będzie automatycznie po otwarciu lub zamknięciu kolekcji. Jeżeli jednak chcesz synchronizować kolekcję ręcznie, wyłącz opcję automatycznego sychronizowania w ustawieniach Anki.

## Pliki

Anki synchronizuje dźwieki i obrazy używane przez twoje notatki. Zauważy, gdy pliki zostana dodane lub usunięte z folderu plików., jednak nie zauważy edycji istniejacych plików bez dodawania lub usuwania żadnych innych. Jesli chcesz, Aby anki zauwazyło zmiano, musisz dodać lub usunąć co najmniej jeden plik.

Jesli uruchamiasz anki z pamieci USB, powinieneś uzywać systemu plików NTFS poniewaz Anki może nie wykryć zmian plików w systemie plików FAT32.


## Konflikty

W normalnych okolicznosciach powtórki i edycje notatek mogą zostać złączone, więc jeśli powtarzasz lub edytujesz na dwóch róznych urządzeniach przed synchronizacją, Anki zachowa twoje zmiany z obu lokacji. Jesli taka sama karta zostanie powtórzona w dwóch różnych lokacjach, obie powtórki zostaną zaznaczone w historce powtórek, a przerwą karty będzie najnowsza powtórka.

Są pewne zmiany, których Anki nie jest w stanie połączyć. Są to głównie zmiany powiązane z formatem notatek. Jeśli zrobisz coś, co nie można połączyć dostaniesz ostrzeżenie, a Anki umożliwi ci opcje przerwania operacji. Jeśli będziesz ją kontynuował, podczas następnej synchronizacji zostaniesz zapytany czy zatrzymać lokalną kolekcję, czy kopię na AnkiWeb.

Jeśli podczas synchronizacji zostaną wykryte określone problemy, anki wymusi synchronizację jednokierunkową. Jeśli zauwazysz, ze dzieje sie to często, daj nam znac na stronie wsparcia Anki.

Gdy wymagana jest jednokierunkowa synchronizacja, musisz wybrać, czy chcesz zachowac kolekcję na urządzeniu, czy w Ankiweb. Jeśli zmiany zostały dokonane w obu miejscach, tylko po jednej stronie bedzie można zachować zmiany.

Jeśli wybierzesz "Prześlij", zawartość na twoim urządzeniu zostanie wysłana do AnkiWeb. Nastepnie musisz zsynchronizować pozostałe urządzenia i wybrać "Pobierz", aby również i na nich była dostepna ta zawartość.

Jeśli wybierzesz "Pobierz", Anki zastapi twoja lokalną kolekcję danymi z AnkiWeb.

Po tym jak wszystkie urządzenia zostały zsynchronizowane, przyszłe synchronizację będą zachoywały sie normalnie, łącząc zmiany z obu miejsc.

Jeśli chcesz wymusić pełne przesłanie lub pobieranie ( na przykład ponieważ przez przypadek usunąłeś talię po jednej stronie i chcesz go odzyskac zamiast synchronizować jego usunięcie), możesz zaznaczyć opcję "podczas następnej synchronizacji wymuś zmiany w jednym kierunku", znajdujaca sie w Narzędzia&gt;Ustawienia&gt;Sieć, a następnie zsynchronizuj jak zawsze (pojawi się opcja, aby wybrać stornę, po której zachowac zmiany).

Wymuszanie synchronizacji jednokierunkowej ma wpływ tylko na synchronizację kart - pliki sa synchronizowane normalnie. Jeśli posiadasz pliki, które chcesz usunąć z AnkiWeb upewnij się, najpierw, że twoja kolekcja jest w pełni zsynchronizowana. Gdy kolekcja jest aktualna, jakiekolwiek pliki, które zostaną usunięte (np poprzez funkcję "Sprawdz pliki"), zostaną również usunięte z AnkiWeb podczas nastepnej synchronizacji.

## Konflikty łącznia 

Jako, że [pierwsza synchronizacja](#setup) może synchronizować zmiany tylko w jednym kierunku, jeśli dodałeś inną zawartość do innych urządzeń lub profili przed synchronizacją, zawartość na jednym z urządzeń zostanie utracona, jeśli nadpiszesz ją zawartością z innego urządzenia. Jest możliwe również ręczne dodanie danych do pojedyńczej kolekcji. 

Start by taking a backup on each device/profile, in case something goes
wrong. With the computer version you can use File&gt;Export to export
"all decks" with scheduling information and media files included, and
save the file somewhere safe. In AnkiMobile, the Add/Export button on
the decks list screen will let you export all decks with media.

Next, if one of your devices is a mobile device, synchronize it first.
If there’s a conflict, choose "upload" to overwrite any existing data on
AnkiWeb with the data from your mobile device. If both devices/profiles
are on your computer, synchronize the device/profile with the most
number of decks first.

Now return to the other device/profile. If automatic syncing is enabled,
a message may pop up asking if you want to upload or download. Click the
cancel button - we don’t want to sync yet.

Once you’re looking at the deck list, click the cog icon next to the
first deck, and choose "export". Export the content with scheduling
information and media included, and save the .apkg file somewhere. Now
you’ll need to repeat this for each top-level deck.

Once all top-level decks have been exported, click the sync button at
the top right, and choose "download", which will overwrite the local
content with the content you synced from your other device.

You can now use File&gt;Import to import the .apkg files you exported
earlier, which will merge the exported content with the existing
content, so everything will be in one place.

## Firewall (język angielski)

Anki needs to be able to make outbound HTTPS connections to sync. At a
minimum it must be able to connect to ankiweb.net, sync.ankiweb.net and
syncN.ankiweb.net, where N is number between 2 and 6. These domains may
change over time, and the IP addresses they point to may also change, so
we recommend you allow wildcard access to \*.ankiweb.net to reduce the
chance of the firewall rules needing to be updated in the future.

If you have a firewall on your machine, you should add an exception for
Anki. If you are on a work or school network, please contact your
network administrator for assistance - it is not something we can help
you with.

## Połączenie przez proxy

If you need a proxy to access the internet, Anki should automatically
pick up your system proxy settings if you’re on Windows or OS X, and
will honour the HTTP_PROXY environment variable if you’re on another
platform.

Anki will only be able to pick up your system settings if a proxy is
manually configured, and does not require a password. If your system
uses automatic proxy setup, or uses a proxy that requires a username and
password, you will need to manually tell Anki the proxy configuration.

To tell Anki your proxy settings, define a HTTPS_PROXY environmental
variable that points to the proxy server. It will look like:

    http://user:pass@proxy.company.com:8080

If your username or password contains an @ (eg <user@workdomain.com>),
you need to change it to %40, like so:

    http://user%40workdomain.com:pass@proxy.company.com:8080

Anki 2.0 expects to find HTTP_PROXY instead of HTTPS_PROXY.

To set environmental variables on Windows, please see
<https://www.google.com/search?q=windows+set+environmental+variable>

If you’re on a Mac, please see
<http://stackoverflow.com/questions/135688/setting-environment-variables-in-os-x>

Heavily locked down networks that intercept secure connections and
present their own certificate instead may cause Anki to throw up SSL
errors. In such environments, you may be able to work around the errors
with <https://ankiweb.net/shared/info/878367706>

An alternative solution is to install a local proxy server, and point
that proxy server at your normal proxy server. You can then tell Anki to
use the local proxy, which will redirect requests to the proxy you
normally use.
