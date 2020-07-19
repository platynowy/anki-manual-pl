# Ustawienia

W ustawienia możesz wejsć poprzez menu Narzędzia na systemach Windows/Linux lub poprzez menu Anki na Maku.

## Ogólne

Gdy wklejasz obrazki ze schowka są one wklejane jako pliki JPG aby oszczędzić miejsce na dysku. Możesz użyć opcji **Wklej zdjęcia ze schowka jako PNG** aby zamiast tego wklejać zdjęcia w formacie PNG. Obrazy PNG obsługują przezroczyste tła i nie tracą na jakości, jednak często ich waga jest o wiele wyższa.

Jeśli **tryb nocny** jest włączony, Anki pokazuje karty jako biały tekst na czarnym tle. Niektóre szablony kart muszą zostać zmodyfikowane żeby działały poprawnie z trybem nocnym - zobacz [stylowanie w trybie nocnym], aby dowiedzieć się więcej.

Podczas korzystenie z trybu nocnego w systemie macOS najnowsze wersje anki automatycznie. Jesli chcesz wymusić używanie trybu jasnego mając włączony tryb nocny w systemie, zainstaluje wersję anki 2.1.21beta3 lub nowszą i zainstaluj  wersję -alternate zamiast -standard.

O **Harmonogramie Anki 2.1** możesz poczytać tutaj:
<https://anki.tenderapp.com/kb/anki-ecosystem/experiment-scheduling-changes-in-anki-21>

Pierwsze wysuwane menu kontroluje jak typy notatek i talie współgrają ze sobą. Domyślna opcja "Dodawaj domyślnie do aktualnej talii" oznacza, że Anki zapisuje ostatnia użyty typ notatki dla każdej talii i wybiera ją ponownie nastepnym razem gdy wybierasz określoną talię (oraz otworzy okno z wybraną talią  podczas wybrania opcji "Dodaj", nieważne, gdzie w programie wybierzesz tę opcję). Druga opcja "Zmień talię na podstawie typu notatki" zapisuje ostatnia użytą talię  dla każdego typu notatki (oraz otworzy okno z wybraną ostatnio użyta notatką gdy użyjesz opcji "Dodaj"). Opcja ta może być przydatna, gdy używasz zawsze jednego typu notatki dla każdej talii.

Drugie wysuwane menu kontroluje kiedy pokazywane są nowe karty: albo losowo albo przed,podczas lub po wszystkich powtórakch.

Opcja **Nowy dzień zaczyna się..**  określa kiedy Anki powinno pokazywać karty z nastepnego dnia. Domyślna opcja o 4 rano pozwala być pewnym, że jeśli uczysz się około północy, nie będziesz miał kart z dwóch dni do przejrzenia podczas jednej sesji. Jeśli siedzisz do późnia lub budzisz się bardzo wcześnie dostosować tę opcję do swojego rytmu dobowego.

Opcja **Limit nauki z wyprzedzeniem** ustala, jak Anki ma się zachowywać gdy talii nie zostały żadne karty do nauki oprócz kart uczonych. Domyślna opcja ustawiona jest na 20 minut, co oznacza, że karty są pokazywane wcześniej jeśli ich czas do nastepnej powtórki wynosi mniej niż 20 minut i nie ma innych kart do nauki. Jeśli 
ustawisz w tej opcji 0, Anki pokaże kartę dopiero, gdy nadejdzie jej czas,pokazując w miedzyczasie stronę z gratulacjami aż do momentu powtórki pozostałych kart.  

Opcja **timebox time limit** bazuje na technice, która pozwala na podzielenie dłuższej aktywności (np 30 minutowa sesję nauki) na krótsze sesje. Jeśli wpisesz w tej opcji liczbę inną niż 0, Anki będzie co jakiś czas pokazywało Ci ile kart udało Ci się przejrzeć w ciagu ustalonego czasu.

## Sieć

Zakładka "Sieć" zawiera opcje dotyczące synchronizacji z AnkiWeb.

- Gdy jesteś zalogowany opcja **deautoryzuj**, sprawi że zostaniesz wylogowany.
- Jeśli opcja "wymuś zmiany" jest włączona, następna synchronizacja zapyta Cię czy chcesz przesłać, czy pobrać swoją kolekcję. Opcja ta jest przydatna gdy przez przypadek dokonasz zmian i będziesz chciał je nadpisać starszą wersją z AnkiWeb.

