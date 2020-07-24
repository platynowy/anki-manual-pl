# Ustawienia

W ustawienia możesz wejsć poprzez menu Narzędzia na systemach Windows/Linux lub poprzez menu Anki na Maku.

## Ogólne

Gdy wklejasz obrazki ze schowka są one wklejane jako pliki JPG aby, zaoszczędzić miejsce na dysku. Możesz użyć opcji **Wklej zdjęcia ze schowka jako PNG**, aby zamiast tego wklejać zdjęcia w formacie PNG. Obrazy PNG obsługują przezroczyste tła i nie tracą na jakości, jednak często ich waga jest o wiele wyższa.

Jeśli **tryb nocny** jest włączony, Anki pokazuje karty jako biały tekst na czarnym tle. Niektóre szablony kart muszą zostać zmodyfikowane, żeby działały poprawnie z trybem nocnym - zobacz [stylizowanie w trybie nocnym](templates/styling.md#night-mode), aby dowiedzieć się więcej.

Podczas korzystenia z trybu nocnego w systemie macOS, najnowsze wersje Anki automatycznie przełączą sie na tryb nocny. Jeśli chcesz wymusić używanie trybu jasnego mając włączony tryb nocny w systemie, zainstaluj wersję anki 2.1.21beta3 lub nowszą i zainstaluj  wersję -alternate zamiast -standard.

O **Planiście Anki 2.1** możesz poczytać tutaj:
<https://anki.tenderapp.com/kb/anki-ecosystem/experiment-scheduling-changes-in-anki-21>

Pierwsze wysuwane menu kontroluje jak typy notatek i talie współgrają ze sobą. Domyślna opcja "Dodawaj domyślnie do aktualnej talii" oznacza, że Anki zapisuje ostatnia użyty typ notatki dla każdej talii i wybiera ją ponownie nastepnym razem, gdy wybierasz określoną talię (Anki sprawi również, że ta talia będzie wybrana   podczas naciśnięcia przycisku "Dodaj", nieważne, gdzie w programie wybierzesz ten przycisk). Druga opcja "Zmień talię na podstawie typu notatki" zapisuje ostatnią użytą talię dla każdego typu notatki (oraz sprawi, że ostatnio użyta  notatka będzie automatycznie wybrana, gdy klikniesz "Dodaj"). Opcja ta może być przydatna, gdy używasz zawsze jednego typu notatki dla każdej talii.

Drugie wysuwane menu kontroluje, kiedy pokazywane są nowe karty: albo losowo albo przed, podczas lub po wszystkich powtórkach.

Opcja **Nowy dzień zaczyna się..**  określa, kiedy Anki powinno pokazywać karty z nastepnego dnia. Domyślna opcja o 4 rano pozwala być pewnym, że jeśli uczysz się około północy, nie będziesz miał kart z dwóch dni do przejrzenia podczas jednej sesji. Jeśli siedzisz do późna lub budzisz się bardzo wcześnie, warto dostosować tę opcję do swojego rytmu dobowego.

Opcja **Limit nauki z wyprzedzeniem** ustala, jak Anki ma się zachowywać, gdy w talii nie zostały żadne karty do nauki oprócz kart uczonych. Domyślna opcja ustawiona jest na 20 minut, co oznacza, że karty są pokazywane wcześniej, jeśli ich czas do nastepnej powtórki wynosi mniej niż 20 minut i nie ma innych kart do nauki. Jeśli 
ustawisz w tej opcji 0, Anki pokaże kartę dopiero, gdy nadejdzie jej czas, pokazując w miedzyczasie stronę z gratulacjami, aż do momentu  gotowości na powtórkę pozostałych kart.  

Opcja **Limit czasowy na sesję** bazuje na technice, która pozwala na podzielenie dłuższej aktywności (np. 30 minutowej sesji nauki) na krótsze sesje. Jeśli wpisesz w tej opcji liczbę inną niż 0, Anki będzie co jakiś czas pokazywało Ci ile kart udało Ci się przejrzeć w ciągu ustalonego czasu.

## Sieć

Zakładka "Sieć" zawiera opcje dotyczące synchronizacji z AnkiWeb.

- Gdy jesteś zalogowany, opcja **deautoryzuj**, sprawi że zostaniesz wylogowany.
- Jeśli opcja "wymuś zmiany" jest włączona, następna synchronizacja zapyta Cię, czy chcesz przesłać, czy pobrać swoją kolekcję. Opcja ta jest przydatna, gdy przez przypadek dokonasz zmian i będziesz chciał je nadpisać starszą wersją kolekcji z AnkiWeb.

