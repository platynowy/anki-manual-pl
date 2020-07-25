# Synchronizacja z AnkiWeb

Ankiweb to usługa, która pozwala na synchronizację twojej kolekcji pomiędzy wieloma urządzeniami, a tym samym umożliwia posiadanie zawsze aktualnej talii na każdym z tych urządzeń. Założ [darmowe konto](https://ankiweb.net/), zanim przejdziesz do dalszej lektury tego rozdziału.

## Konfiguracja

Aby rozpocząć synchronizację kolekcji, naciśnij przycisk Synchronizuj znajdujący się u góry w  głownym oknie Anki lub naciśnij klawisz "y" na klawiaturze. Zostaniesz poproszony o swoj identyfikator AnkiWeb ID oraz hasło, które określiłeś w procesie rejestracji.

Podczas pierwszej synchronizacji kolekcji, Anki nie będzie w stanie połączyć danych znajdujących się w AnkiWeb z tymi, które masz na swoim komputerze, dlatego zostaniesz poproszony o wybranie,  czyc hcesz pobrać, czy przesłać dane. Jeśli posiadasz karty z innego urządzenia w AnkiWeb, a na komputerze nie masz żadnych kart wybierz "pobierz", aby zastąpić lokalną, pustą  kolekcję kartami pobranymi z AnkiWeb. Jeśli masz różne karty na obu urządzeniach, [wymagane jest wiecej pracy](#merging-conflicts), aby uniknąć utraty danych. Po tym kroku Anki bez problemu będzie mogło łączyć zmiany w talii pochodzące z różnych lokalizacji (z kilkoma wyjątkami).

Po pierwszej synchronizacji Anki będzie w stanie łączyć zmiany z różnych urządzeń (z kilkoma wyjątkami).

Jeśli kilka osób używa Anki na jednym urządzeniu i dla każdej z tych osób został utworzony profil, wszyscy będą musieli utworzyć swoje własne konto AnkiWeb, aby móc synchronizować kolekcję. Zsynchronizowanie różnych profili z jednym kontem AnkiWeb doprowadzi do do utraty danych. 

## Automatyczna synchronizacja

Po pierwszej synchronizacji, każda kolejna wykonywana będzie automatycznie po otwarciu lub zamknięciu kolekcji. Jeżeli jednak chcesz synchronizować kolekcję ręcznie, wyłącz opcję automatycznego sychronizowania w ustawieniach Anki.

## Pliki

Anki synchronizuje dźwieki i obrazy używane przez twoje notatki. Zauważy, gdy pliki zostana dodane lub usunięte z folderu plików. Nie zauważy jednak  edycji istniejacych plików bez dodawania lub usuwania żadnych innych. Jesli chcesz, Aby Anki zauwazyło zmiany, musisz dodać lub usunąć co najmniej jeden plik.

Jeśli uruchamiasz anki z pamięci USB, powinieneś używać systemu plików NTFS, ponieważ Anki może nie wykryć zmian plików w systemie plików FAT32.


## Konflikty

W normalnych okolicznosciach powtórki i edycje notatek mogą zostać złączone, więc jeśli powtarzasz lub edytujesz na dwóch róznych urządzeniach przed synchronizacją, Anki zachowa twoje zmiany z obu lokacji. Jeśli taka sama karta zostanie powtórzona w dwóch różnych lokacjach, obie powtórki zostaną zaznaczone w historii powtórek, a przerwa karty będzie ustalona na podstawie najnowszej powtórki.

Istnieją pewne zmiany, których Anki nie jest w stanie połączyć. Są to głównie zmiany powiązane z formatem notatek. Jeśli zrobisz coś, czego nie można połączyć, dostaniesz ostrzeżenie, a Anki umożliwi ci opcje przerwania operacji. Jeśli będziesz ją kontynuował, podczas następnej synchronizacji zostaniesz zapytany, czy zatrzymać lokalną kolekcję, czy kopię na AnkiWeb.

Jeśli pewne problemy zostaną wykryte podczas synchronizacji, Anki wymusi synchronizację jednokierunkową. Jeśli zauważysz, ze dzieje sie to często, daj nam znać na stronie wsparcia Anki.

Gdy wymagana jest jednokierunkowa synchronizacja, musisz wybrać, czy chcesz zachowac kolekcję na urządzeniu, czy w Ankiweb. Jeśli zmiany zostały dokonane w obu miejscach, tylko po jednej stronie bedzie można zachować zmiany.

Jeśli wybierzesz "Prześlij", zawartość na twoim urządzeniu zostanie wysłana do AnkiWeb. Nastepnie musisz zsynchronizować pozostałe urządzenia i wybrać "Pobierz", aby również i na nich była dostepna ta zawartość.

Jeśli wybierzesz "Pobierz", Anki zastapi twoją lokalną kolekcję danymi z AnkiWeb.

Po tym, jak wszystkie urządzenia zostały zsynchronizowane, przyszłe synchronizacje będą zachoywały się normalnie, łącząc zmiany z obu miejsc.

Jeśli chcesz wymusić pełne przesłanie lub pobieranie (na przykład ponieważ przez przypadek usunąłeś talię po jednej stronie i chcesz ją odzyskać, zamiast synchronizować jego usunięcie), możesz zaznaczyć opcję "podczas następnej synchronizacji wymuś zmiany w jednym kierunku", znajdujacą sie w Narzędzia&gt;Ustawienia&gt;Sieć, a następnie zsynchronizuj jak zawsze (pojawi się opcja, aby wybrać stronę, po której zachować zmiany).

Wymuszanie synchronizacji jednokierunkowej ma wpływ tylko na synchronizację kart - pliki sa synchronizowane normalnie. Jeśli posiadasz pliki, które chcesz usunąć z AnkiWeb, upewnij się najpierw, że twoja kolekcja jest w pełni zsynchronizowana. Gdy kolekcja jest aktualna, jakiekolwiek pliki, które zostaną usunięte (np. poprzez funkcję "Sprawdz pliki"), zostaną również usunięte z AnkiWeb podczas nastepnej synchronizacji.

## Konflikty łączenia 

Jako, że [pierwsza synchronizacja](#setup) może synchronizować zmiany tylko w jednym kierunku, jeśli dodałeś inną zawartość do innych urządzeń lub profili przed synchronizacją, zawartość na jednym z urządzeń zostanie utracona, gdy nadpiszesz ją zawartością z innego urządzenia. Jest możliwe również ręczne dodanie danych do pojedyńczej kolekcji. 

Najpierw utwórz kopię zapasową na każdym urządzeniu/profilu w razie, gdyby coś poszło nie tak. Na wersji komputerowej możesz to zrobić używając Plik&gt;Eksportuj , aby wyeksportować "wszystkie talie" razem z informacją o planowaniu oraz plikami. Plik zapisz gdzieś w bezpiecznym miejscu. W AnkiMobile, plik Dodaj/Eksportuj na ekranie z listą talii pozwoli ci wyeksportować wszystkie talie razem z plikami.

Nastepnie, jeśli jedno z twoich urządzeń jest urządzeniem mobilnym, zsynchronizuj je. W wypadku, gdy powstanie konflikt, wybierz "prześlij", aby nadpisać dane na AnkiWeb danymi z twojego urządzenia. Jeśli oba urządzenia/profile znajdują się na kompueterze, najpierw zsynchronizuj urządzenie/profil z większą ilością talii.

Teraz powróć do pierwszego profilu/urządzenia. Jeśli automatyczna synchronizacja jest włączona, może pojawić się okno, które zapyta, czy chcesz pobrać, czy przesłać dane. Kliknij przycisk anuluj - jeszcze nie pora na synchronizację.

Na ekranie z listą talii naciśnij ikonę koła zębatego przy pierwszej talii, a nastepnie naciśnij "eksportuj". Wyeksportuj zawartość z informacją o planowaniu oraz plikami i zapisz gdzieś jako plik .apkg. Teraz musisz powtórzyć tę czynność dla każdej talii (oprócz talii podrzędnych).

Po tym jak wszystkie główne talie zostały wyeksportowane, naciśnij przycisk "synchronizuj" na ekranie głównym (u góry po prawej) i wybierz "pobierz", co nadpisze lokalną zawartość zawartością, którą zsynchronizowałeś z drugiego urządzenia.

Możesz teraz użyć opcji Plik&gt;Importuj, aby zaimportować pliki .apkg, które wyeksportowałeś wcześniej, co złączy wyeksportowaną zawartosć z istniejącą. Dzieki temu wszystko znajduje się w jednym miejscu.

## Firewall

Anki musi mieć możliwość tworzenia wychodzących połączeń HTTPS, aby móc synchronizować. Musi móc połączyć się co najmniej z ankiweb.net, sync.ankiweb.net i
syncN.ankiweb.net. W tym ostatnim N jest numerem między 2, a 6. Te domeny mogą zmienić się z czasem tak samo jak ich adresy IP, więc zalecamy dostęp z użyciem symboli wieloznacznych z \*.ankiweb.net, aby obniżyć szansę na konieczność aktualizowania firewalla w przyszłości.

Jeśli posiadasz firewall na twoim sprzecie, powinieneś dodać wyjątek dla Anki. W przypadku, gdy korzystasz z internetu w pracy/w szkole, skontaktuj się z administratorem twojej sieci i poproś o wsparcie - tutaj nasza możliwość pomocy się kończy.

## Połączenie przez proxy

Jeśli potrzebujesz proxy, aby mięć dostęp do internetu, Anki na systemach Windows lub OS X powinno automatycznie użyć twoich ustawień systemowych oraz będzie uznawać środowisko HTTP_PROXY, jeśli korzystasz z Anki na innej platformie. 

Anki będzie w stanie użyć ustawień systemowych, jeśli proxy jest skonfigurowana ręcznie i nie wymaga hasła. Gdy twój system ma automatycznie skonfigurowane proxy lub proxy wymaga nazwy użytkownika i hasła, będziesz musiał sam poprowadzić w Anki konfigurację proxy.

Aby ustawić twoje ustawienia proxy w Anki, zdefiniuj zmienne środowisko HTTPS_PROXY, które wskazuje na serwer proxy. Bedzie to wyglądało w ten sposób: 

    http://user:pass@proxy.company.com:8080

Jeśli nazwa użytkownika i hasło zawierają małpę (@) (np. <user@workdomain.com>), musisz zamiast niej wpisać %40, jak poniżej:

    http://user%40workdomain.com:pass@proxy.company.com:8080

Anki 2.0 szuka HTTP_PROXY, zamiast HTTPS_PROXY.

Aby ustawić zmienne środowiska na systemie Windows, zobacz:
<https://www.google.com/search?q=windows+set+environmental+variable>

Jeśli za to korzystasz z Maka, zobacz:
<http://stackoverflow.com/questions/135688/setting-environment-variables-in-os-x>

Bardzo zamknięte sieci, które przechwycują bezpieczne połączenia i okazują swój własny certyfikat, mogą powodować, że w Anki pojawią się błędy SSL. W takich środowiskach możesz spróbować obejść te błędy, używając <https://ankiweb.net/shared/info/878367706>.

Alternatywnym sposobem jest instalacja lokalnego serwera proxy i skierowanie go do twojego zwykłego serwera proxy. Nzstępnie możesz ustawić w Anki, aby używało lokalnego proxy, które skieruje połączenie do proxy, którego zwykle używasz.
