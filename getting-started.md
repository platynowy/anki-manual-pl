# Jak zacząć?

## Filmy instruktażowe

Aby szybko wejść do świata Anki, obejrzyj te filmy instruktażowe. Zostały nagrane na poprzedniej wersji Anki, jednak podstawowe założenia dalej są aktualne. Filmy są dostępne tylko w języku angielskim. 

-   [Udostępniane talie i podstawy powtórek
    ](http://www.youtube.com/watch?v=QS2G-k2hQyg&yt:cc=on)

-   [Zmiana kolejności kart
    ](http://www.youtube.com/watch?v=DnbKwHEQ1mA&yt:cc=on)

-   [Zmiana wyglądu kart](http://www.youtube.com/watch?v=F1j1Zx0mXME&yt:cc=on)

-   [Pisanie odpowiedzi w czasie powtórki](http://www.youtube.com/watch?v=5tYObQ3ocrw&yt:cc=on)

Możesz również [pobrać te filmy](https://apps.ankiweb.net/downloads/archive/screencasts/2.0/), jeśli Youtube nie jest dostępny w kraju, w którym przebywasz.



## Podstawy

### Karty

Para odpowiedź - pytanie nazywa się kartą. Taka nazwa odnosi się do zwykłej, papierowej fiszki z pytaniem po jednej i odpowiedzią po drugiej stronie. W Anki karta nie ma wyglądu fizycznej kartki papieru, ale jeśli w czasie powtórki wyświetlisz pytanie i odpowiedź, to ich układ będzie przypominał właśnie taką papierową fiszkę. Przykładowo, ucząc się podstaw chemii możesz mieć następujące pytanie:

    Pytanie: Jaki jest symbol chemiczny tlenu?

Po namyśle, że prawidłową odpowiedzią jest O, klikniesz przycisk odpowiedzi, a Anki wyświetli wtedy:

    Pytanie: Jaki jest symbol chemiczny tlenu?
    Odpowiedź: O

Po wyświetleniu odpowiedzi ocenisz, jak dobrze ją pamiętałeś. Na tej podstawie Anki samo określi czas, za jaki ma być ponownie wyświetlona ta fiszka.

### Talie

Talia to zbiór kart. Karty można  umieszczać  w różnych taliach, co pozwala uczyć się jedynie wybranej części kart ze swojej kolekcji, zamiast uczyć się wszystkiego na raz. Każda talia może posiadać swoje własne ustawienia np. liczbę nowych kart w danym dniu, albo czas oczekiwania na ponowne pojawienie się karty, jeśli na przykład popełniłeś błąd

Talie mogą zawierać w sobie inne talie, pozwoli Ci to stworzyć strukturę drzewa. Aby tworzyć różne poziomy talii Anki używa podwójnego dwukropka "::". Talia o nazwie "Chiński::Hanzi" odnosi się do talii "Hanzi", która jest częścią talii "Chiński". Wybierając "Hanzi" przejrzysz tylko te karty, które należą bezpośrednio do niej. Jeśli wybierzesz talię "Chiński", będziesz wtedy przeglądał wszystkie karty tej talii włącznie z kartami z talii "Hanzi". 

Aby stworzyć strukturę drzewa, możesz nazywać talie z wykorzystaniem znaku "::" na każdym z poziomów lub po prostu przesuwając talie kursorem metodą "chwyć i upuść". Talie, które zostały umieszczone pod inną talia (te, które zawierają co najmniej jeden podwójny dwukropek "::" w swojej nazwie) są często nazywane "podtaliami", a talie na najwyższym poziomie nazywa się często taliami nadrzednymi.

Pierwszą talią dostępną po instalacji Anki jest talia "Domyślna"; wszystkie karty, które w jakiś sposób nie zostały zaszeregowane do innych talii będą domyślnie zapisywane właśnie w tej talii. W sytuacji, gdy dodasz do Anki nowe talie, a talia domyślna nie będzie zawierała żadnych kart, zostanie ona przez Anki ukryta. Możesz także dowolnie dostosować nazwę talii domyślnej do własnych potrzeb i używać ją do innych kart.

Talie służą do przechowywania jak najszerszego zakresu informacji, nie zaś po to, by przechowywać w nich specyficzne tematy np. "jedzenie rzeczowniki" lub "lekcja 1". Więcej informacji na ten temat znajduje się w rozdziale dotyczącym [prawidłowego używania talii](editing.md#using-decks-appropriately).

Jeśli chcesz się dowiedzieć jak talie oddziaływują na kolejność wyświetlania kart, zapoznaj się z [odpowiednim rozdziałem](studying.md#display-order).

### Notatki i pola

Podczas tworzenia fiszek często niezbędne jest stworzenie więcej niż jednej karty, która będzie odnosiła się do tej samej informacji. Przykładowo, ucząc się francuskiego poznasz słowo "bonjour" oznaczające "cześć". W tym przypadku możesz chcieć stworzyć jedną kartę, która pokaże ci słowo "bonjour" i zapyta o jego tłumaczenie, oraz drugą kartę, pokazującą słowo "cześć" pytającą o tłumaczenie na język francuski. Jedna karta ćwiczy twoją zdolność rozpoznawania obcych słów, zaś druga przeciwnie, przypisywanie polskim słowom ich obcego znaczenia.

Używając do nauki papierowych fiszek jedynym sensownym rozwiązaniem jest napisanie tych samych informacji na dwóch osobnych kartach, tak żeby móc podzielić swoją naukę na tę związaną z rozpoznawaniem i przypisywaniem. Niektóre programy komputerowe do obsługi fiszek ułatwiają ten proces poprzez funkcję odwrócenia karty. Tym samym tworzona jest karta standardowa i odwrotna. Jest to co prawda postęp w stosunku do papierowej wersji, ale takie rozwiązanie posiada dwie podstawowe wady:

-   Karta standardowa i odwrotna będą posiadały takie same interwały powtórki, ze względu na brak ich rozgraniczenia. Oznacza to, że karty nie będą powtarzane w optymalnym czasie, będziesz  łatwiej zapomniał informacje albo uczył się danej informacji więcej razy niż to konieczne.
-   Odwrócenie karty ma sens tylko, gdy na obu kartach - standardowej i odwrotnej, chcesz mieć dokładnie te same informacje. Oznacza to, że nie ma możliwości na dodanie jakichś dodatkowych informacji na którejś z kart.

Anki rozwiązuje te problemy poprzez podział informacji zawartych w karcie na kawałki informacji. Możesz określić Anki, które z tych kawałków mają być wyświetlane na każdej karcie. Program wygeneruje wtedy dokładnie taką kartę jaką określiłeś, a także zaktualizuje ją w przypadku wprowadzenia jakichkolwiek poprawek w przyszłości.

Wyobraź sobie, że uczysz się francuskich słówek i na każdej tylnej stronie karty chcesz umieścić numer strony, z której pochodzi dane słówko. Karty standardowa i odwrotna będą wyglądały zatem w taki sposób:

    Pytanie: Bonjour
    Odpowiedź: Cześć
       Strona 12

oraz:

    Pytanie: Cześć
    Odpowiedź: Bonjour
       Strona 12

W tym przykładzie mamy trzy kawałki powiązanych ze sobą informacji: słówko francuskie, znaczenie polskie oraz numer strony. Jeśli złożymy je razem będą prezentowane w następujący sposób:

    Francuski: Bonjour
    Polski: Cześć
    Strona: 12

W Anki taki zbiór informacji nazywany jest notatką, a każdy z tych kawałków tworzących notatkę polem. Tak więc w tym typie notatki mamy utworzone trzy pola: Francuski, Polski i Strona.

Aby dodawać i edytować pola, kliknij przycisk “Pola...​”  podczas dodawania lub edytowania notatek. Jeśli chcesz dowiedzieć się wiecej o polach, zobacz rozdział o [dostosowywaniu pól](editing.md#customizing-fields).

### Typy kart

Aby stworzyć karty, musimy zaprojektować pewien szablon, który wskaże, jakie informacje mają być wyświetlane na przedniej i tylnej stronie każdej karty. Tym szablonem jest "typ karty". Każdy typ notatki może zawierać jedną lub więcej typów kart; kiedy dodajesz notatkę Anki stworzy jedną kartę dla każdego typu karty.

Każdy typ karty ma dwa "szablony", jeden dla pytania i drugi dla odpowiedzi. W powyższym przykładzie z językiem francuskim chcieliśmy, aby karta standardowa wyglądała w ten sposób:

    Pytanie: Bonjour
    Odpowiedź: Cześć
       Strona 12

Aby to zrobić, musimy stworzyć szablon pytania i odpowiedzi:

    Pytanie: {{Francuski}}
    Odpowiedź: {{Polski}}<br>
       Strona {{Strona}}

Nazwa pola umieszczona w nawiasie klamrowym jest sygnałem dla Anki, że w tym miejscu ma zostać wyświetlona informacja, która jest przechowywana w tym polu. Tekst znajdujący się poza nawiasami klamrowymi będzie taki sam na każdej karcie.  (na przykład nie musimy wpisywać "Strona X" w polu "Strona", kiedy dodajemy materiał do nauki - to pole jest dodawane automatycznie do każdej karty) &lt;br&gt; To specjalny znak, który daje znać  Anki, aby przeszło ono  do następnej linii; więcej szczegółów znajduje się w sekcji [szablony](templates/intro.md).

Szablon karty odwrotnej tworzymy w bardzo podobny sposób co karty standardowej:

    Pytanie: {{Angielski}}
    Odpowiedź: {{Polski}}<br>
       Strona #{{Strona}}

Gdy raz stworzymy szablon i zaczniemy dodawać notatki, to wszystkie powstałe na ich podstawie karty będą opierały się na tym samym typie karty. Dzięki typom kart nie trzeba formatować wyglądu każdej z kart, podejście to znacząco zmniejsza wysiłek związany z wprowadzaniem informacji. Taki sposób tworzenia kart sprawia, że Anki wie o ich spokrewnieniu i podczas powtórki odsuwa je od siebie w czasie. Jeśli przy wprowadzaniu informacji do pól w notatce popełnimy jakiś błąd, to wystarczy poprawić go tylko raz, aby wszystkie karty wygenerowane na podstawie tej notatki także zostały poprawione.

Aby dodać lub edytować typ karty kliknij przycisk “Karty…​” podczas edytowania lub dodawania notatki. Jeśli chcesz dowiedzieć się więcej o typach kart, zobacz rozdział o [kartach i szablonach](templates/intro.md).

### Typy notatek

Anki umożliwia tworzenie różnych typów notatek dla różnego rodzaju materiału do nauki. Każdy typ notatki posiada własne pola i typy kart. Najlepszym rozwiązaniem jest tworzenie nowego rodzaju notatki dla każdego z obszernych tematów do nauki. Na powyższym przykładzie moglibyśmy stworzyć typ notatki o nazwie "Francuski". Jeżeli chcielibyśmy uczyć się stolic państw świata stworzylibyśmy osobny typ notatki z polami o nazwie "Kraj" i "Stolica".

Anki posiada funkcje wyszukiwania duplikatów notatek. Są one jednak porównywane tylko w obrębie tego samego typu notatki. Oznacza to, że jeżeli dodałbyś notatkę ze stolicą o nazwie Pomarańcza (typ notatki Kraj-Stolica), to nie zostałby wykazany duplikat w stosunku do notatki odpytującej cię o słowo Pomarańcza w języku francuskim (typ notatki Francuski).

Przy tworzeniu nowej kolekcji Anki automatycznie połączy ją ze standardowymi typami notatek. Takie typy notatek mają na celu przede wszystkim łatwiejsze wprowadzenie do programu nowych użytkowników. Jeżeli jednak zaczniesz wykorzystywać Anki w bardziej intensywny sposób, najlepszym rozwiązaniem będzie zdefiniowanie nowych, własnych typów notatek dopasowanych do treści zawartych w taliach. Do standardowych typów notatek należą:

Podstawowy  
Posiada pola Przód oraz Tył i tworzy jedną kartę. Tekst wprowadzony do pola Przód (Front) pojawi się na przedniej stronie karty, zaś tekst z pola Tył na jego tylnej stronie.

Podstawowy (z odwrotną kartą)  
Tworzy dwie karty z wprowadzonym tekstem. Pierwszą jako Przód→Tył i drugą jako Tył→Przód.

Podstawowy (z opcjonalną odwrotną kartą)  
Tworzy kartę Przód→Tył i opcjonalnie kartę Tył→Przód. Aby włączyć kartę Tył→Przód należy wpisać jakikolwiek znak lub słowo do ostatniego pola "Dodaj rewers". Więcej informacji na ten temat znajdziesz w rozdziale o  [kartach i szablonach](templates/intro.md).

Luka
Typ notatki który ułatwia wybór tekstu i zamianę go na tekst z luką  (np. “Człowiek wylądował na księżycu w \[…​\]” roku → “Człowiek wylądował na księżycu w
1969 roku”). Wiecej informacji na ten temat znajdiesz w rozdziale [Wypełnianie luki](editing.md#cloze-deletion).

Aby dodać własny typ notatki lub zmodyfikować już istniejący wybierz w oknie głównym Anki menu Narzędzia>Zarządzaj typami notatek.

Notatki i typy notatek przechowywane są w całej kolekcji, nie w poszczególnych taliach. Oznacza to, że w jednej talii możesz używać wielu różnych typów notatek. Kiedy dodajesz notatki w oknie Dodaj, możesz wybrać typ notatki, którego chcesz użyć i talię, w której tę notatkę chcesz umieścić. Ustawienia te są od siebie całkowicie niezależne. Możesz również zmieniać typ notatek, które [dodałeś już wcześniej](browsing.md).

### Kolekcja

Twoja "kolekcja" to cały materiał przechowywany w Anki – twoje karty,
notatki, talie, typy notatek, opcje talii i tak dalej.

## Udostępnione talie

Możesz zobaczyć [film o udostępnianiu talii i podstawach powtórek](http://www.youtube.com/watch?v=QS2G-k2hQyg&yt:cc=on) na YouTube (w języku angielskim).

Najprostsza drogą, aby rozpocząć naukę z Anki, jest pobranie którejś z udostępnionych talii:

1.  Kliknij przycisk "Pobierz Gotową" na dole ekranu z listą talii.

2.  Jeśli chcesz pobrać którąś z talii naciśnij przycisk "Download", który znajduje się na stronie każdej z udostępnianych talii.

3.  Kliknij dwukrotnie na pobranym pliku aby załadować go do Anki lub wybierz Plik>Importuj w głównym oknie Anki.

Obecnie nie jest możliwe zaimportowanie udostępnionej talii bezpośrednio do konta na AnkiWeb. Talię należy najpierw importować do Anki, a następnie  zsynchronizować ją z AnkiWeb.

Tworzenie własnej talii jest najbardziej efektywnym sposobem nauki rozbudowanego materiału. Nie zrozumiemy obcego języka przez proste powtarzanie słówek - do tego wymagane są przede wszystkim objaśnienia i kontekst, które sprawią, że nauka będzie bardziej efektywna. Co więcej, wprowadzanie danych do programu sprawi, że będziesz musiał zdecydować co np. w danym zdaniu jest najistotniejsze, a to z kolei prowadzi do lepszego zrozumienia opanowywanego materiału.

Jeśli uczysz się języków możesz mieć ochotę pobrać długą listę słów wraz z ich tłumaczeniami, jednak tak samo jak ucząc się samych wzorów fizycznych nie staniesz się fizykiem, tak bezmyślne zakuwanie długiej listy słówek nie zrobi z Ciebie poligloty. Do prawidłowej nauki potrzebujesz podręczników, nauczycieli albo przebywania w danym obszarze językowym.

    Jeśli czegoś nie rozumiesz, nie ucz się tego.
    --SuperMemo

Większość udostępnionych talii została stworzona przez ludzi, którzy uczą się materiału poza Anki - z tekstów, na lekcjach, w telewizji itd. Z tych źródeł wybierają najbardziej interesujące ich fragmenty i dodają je do Anki. Nie dodają do notatek dodatkowych informacji na temat np. kontekstu danej sytuacji językowej, bo po prostu sami go znają. Opanowanie takiego materiału, z powodu między innymi  braku objaśnień, będzie sprawiało trudność komuś kto go pobrał.

Nie oznacza to oczywiście, że udostępniane talie są bezużyteczne - po prostu przy nauce pewnych obszernych zagadnień udostępniane talie nie powinny być traktowane jako główne źródło wiedzy, ale raczej jako dodatkowe narzędzie. Jeśli uczysz się z podręcznika ABC i ktoś udostępnił talię ze słowami z tego podręcznika, to użycie takiej talii jest świetnym sposobem na zaoszczędzenie czasu. Tak samo w sytuacji, gdy uczymy się podstawowej wiedzy np. z zakresu geografii - stolic państw świata. Nie jest tutaj potrzebny żaden dodatkowy, zewnętrzny materiał. Rozczarujesz się jednak, gdy będziesz chciał opanować jakiś obszerny zakres tematyczny. Tutaj będzie potrzebna też nauka materiału "z zewnątrz".
