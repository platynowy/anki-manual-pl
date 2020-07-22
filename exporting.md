# Eksportowanie

Eksportowanie umożliwia zapisane części kolekcji jako pliku tekstowego lub w formacie "packaged Anki deck". Aby wyeksportować, naciśnij w menu "Plik" i wybierz "Eksportuj".

## Pliki tekstowe

Jeśli wybierzesz "Notes in Plan Text" Anki zapisze zawatość notatek w pliku tekstowym. Każde pole jest od siebie odseparowane tabulatorem. Jeśli zedytujesz wyeksportowany plik, ale nie zmienisz pierwszego pola, będziesz mógł później zaimportować ten plik spowrotem do Anki, a Anki zaktualizuje twoje notatki na podstawie twoich zmian. Zadziała to jeśli zaimportujesz z powrotem do tego samego typu notatki

Jeśli stwierdzisz, ze musisz zedytować również pierwsze pole, będziesz musiał zmienic format twojego typu notatki tak, aby pierwszym polem było numer ID, a nie tekst (możesz zainstalować dodatek "Add note id", aby zrobić to łatwiej)

Tekst jest eksportowany z osadzonym w nim całym formatowaniem HTML po to, abyformatowanie zostało zachowane gdy importujesz tekst z powrotem.

## Spakowane talie

"Spakowana talia" składa się z kart, notatek, typów notatek oraz wszelkich dźwięków lub obrazów osadzonych w jednym pliku o końcówce .apkg lub .colpkg. Możesz używać spakowanych talii, aby przenosić karty pomiędzy różnymi osobami. Moga one też służyć jako kopie zapasowe cześci twojej kolekcji.

Sa dwa różne typy spakowanych talii.

### Kolekcja (.colpkg)

Kiedy eksportujesz wszystkie talie razem z planowaniem, to nazywa się to "pakietem kolekcji (collection package)". Anki skopiuje całą twoją kolekcję do pliku z koncówką .colpkg.i umieści go na twoim pulpicie. Pakiet kolekcji jest używany jako kopia zapasowa, lub aby skopiować dane na inne urządzenie.

Pakiety kolekcji utworzone na poprzednich wersjach Anki były nazywane w ten sposób: collection.apkg.

Kiedy ten plik jest później zaimportowany, Anki usuwa wszystkie obecne karty w kolekcji i zastępuje je treścią z pliku. Jesto to przydatne do kopiowania twojej kolekcji miedzy urządzeniami.

Istniejące pliki w twojej kolekcji nie zostaną usuniete, kiedy importujesz pakiet kolekcji. Aby usunać nieuzywane pliki, użyj Narzędzia&gt;Sprawdź pliki

### Talia (.apkg)

Pakiety talii zawierają pojedyńczą talię (oraz każdą z jej podtalii, jeśli jakąś posiada). Końcówka ich pliku to .apkg, a sama nazwa pliku jest inna niż collection.apkg. Kiedy importujesz pakiet talii, Anki doda zawartość do twojej kolekcji zamiast ja nadpisywać

Jeśli niektóre notatki w pakiecie talii zostały wcześniej zaimportowane, Anki zostawi najnowsza wersję. Więc jesli pobierzesz zaktualizowana talię, modyfikacje poczynione w zaktualizowanej wersji przeniosa się do twojej kolekcji, ale jeśli zaimportujesz niezmienioną talię po dokonaniu zmian w twojej kolekcji, zmiany w twojej kolekcji zostaną zachowane.

Jeśli zdecydujesz nie zawierrac informacji o planowaniu, Anki założy, że udostepniasz talię innym osobom i usunie etykiety "marked (wyróżniona)" i "leech (pijawka)" tak, aby osoby uczące się posiadały "czystą" talię.
