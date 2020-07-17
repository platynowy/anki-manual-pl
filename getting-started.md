# Jak zacząć?

## Filmy instruktażowe

Aby szybko wejść do świata Anki obejrzyj te filmy instruktażowe. Zostały nagrane na poprzedniej wersji Anki, jednak podstawowe założenia dalej są aktualne. Filmy są dostępne w języku angielskim. 

-   [Udostępniane talie i podstawy powtórek
    ](http://www.youtube.com/watch?v=QS2G-k2hQyg&yt:cc=on)

-   [Zmiana kolejności kart
    ](http://www.youtube.com/watch?v=DnbKwHEQ1mA&yt:cc=on)

-   [Zmiana wyglądu kart](http://www.youtube.com/watch?v=F1j1Zx0mXME&yt:cc=on)

-   [Pisanie odpowiedzi w czasie powtórki](http://www.youtube.com/watch?v=5tYObQ3ocrw&yt:cc=on)

Możesz również [pobrać te filmy](https://apps.ankiweb.net/downloads/archive/screencasts/2.0/), jeśli Youtube nie jest dostępny w Twoim kraju.



## Podstawy

### Karty

Para odpowiedź - pytanie nazywa się kartą. Taka nazwa odnosi się do zwykłej, papierowej fiszki z pytaniem po jednej i odpowiedzią po drugiej stronie. W Anki karta nie ma wyglądu fizycznej kartki papieru, ale jeśli w czasie powtórki wyświetlisz pytanie i odpowiedź, to ich układ będzie przypominał właśnie taką papierową fiszkę. Przykładowo ucząc się podstaw chemii, możesz mieć następujące pytanie:

    Pytanie: Jaki jest symbol chemiczny tlenu?

Po namyśle, że prawidłową odpowiedzią jest O, klikniesz przycisk odpowiedzi a Anki wyświetli wtedy:

    Pytanie: Jaki jest symbol chemiczny tlenu?
    Odpowiedź: O

Po wyświetleniu odpowiedzi ocenisz jak dobrze ją pamiętałeś. Na tej podstawie Anki samo określi czas za jaki ma być ponownie wyświetlona ta fiszka.

### Talie

Talia to zbiór kart. Karty można  umieszczać  w różnych taliach, co pozwala uczyć się jedynie wybranej części kart ze swojej kolekcji, zamiast uczyć się wszystkiego na raz. Każda talia może posiadać swoje własne ustawienia np. liczbę nowych kart w danym dniu, albo czas oczekiwania na ponowne pojawienie się karty jeśli na przykład popełniłeś błąd

Talie mogą zawierać w sobie inne talie, pozwoli ci to stworzyć strukturę drzewa. Aby tworzyć różne poziomy talii Anki używa podwójnego dwukropka "::". Talia o nazwie "Chiński::Hanzi" odnosi się do talii "Hanzi", która jest częścią talii "Chiński". Wybierając "Hanzi" przejrzysz tylko te karty, które należą bezpośrednio do niej. Jeśli wybierzesz talię "Chiński", będziesz wtedy przeglądał wszystkie karty tej talii włącznie z kartami z talii "Hanzi" lekcje. 

Aby stworzyć strukturę drzewa, możesz nazywać talię z wykorzystaniem znaku "::" na każdym z poziomów lub po prostu przesuwając talie kursorem metodą "chwyć i upuść". Talie które zostały umieszczona pod inną talia (te które zawierają co najmniej jeden podwójny dwukropek "::" w swojej nazwie) są często nazywane "podtaliami", a talie na najwyższym poziomie nazywa się często taliami nadrzednymi.

Pierwszą talią dostępną po instalacji Anki jest talia "Domyślna"; wszystkie karty, które w jakiś sposób nie zostały zaszeregowane do innych talii będą domyślnie zapisywane właśnie w tej talii. W sytuacji, gdy dodasz do Anki nowe talie, a talia domyślna nie będzie zawierała żadnych kart, zostanie ona przez Anki ukryta. Możesz także dowolnie dostosować nazwę talii domyślnej do własnych potrzeb i używać ją do innych kart.

Talie służą do przechowywania jak najszerszego zakresu informacji, nie zaś po to, by przechowywać w nich specyficzne tematy np. "jedzenie rzeczowniki" lub "lekcja 1". Więcej informacji na ten temat znajduje się w rozdziale dotyczącym [prawidłowego używania talii](editing.md#using-decks-appropriately).

Jeśli chcesz się dowiedzieć jak talie oddziaływują na kolejność wyświetlania kart, proszę zapoznaj się z [odpowiednim rozdziałem](studying.md#display-order).

### Notatki i pola

Podczas tworzenia fiszek, często niezbędne jest stworzenie więcej niż jednej karty, która będzie odnosiła się do tej samej informacji. Przykładowo, ucząc się francuskiego poznasz słowo "bonjour" oznaczające "cześć". W tym przypadku możesz chcieć stworzyć jedną kartę, która pokaże ci słowo "bonjour" i zapyta o jego tłumaczenie, oraz drugą kartę, pokazującą słowo "cześć" pytającą o tłumaczenie na język francuski. Jedna karta ćwiczy twoją zdolność rozpoznawania obcych słów, zaś druga, przeciwnie, na przypisywanie polskim słowom ich obcego znaczenia.

Używając do nauki papierowych fiszek jedynym sensownym rozwiązaniem jest napisanie tych samych informacji na dwóch osobnych kartach, tak żeby móc podzielić twoją naukę na tę związaną z rozpoznawaniem i przypisywaniem. Niektóre programy komputerowe do obsługi fiszek ułatwiają ten proces poprzez funkcję odwrócenia karty. Tym samym tworzona jest karta standardowa i odwrotna. Jest to co prawda postęp w stosunku do papierowej wersji, ale takie rozwiązanie posiada dwie podstawowe wady:

-   Karta standardowa i odwrotna będą posiadały takie same interwały powtórki, ze względu na brak ich rozgraniczenia. Oznacza to, że karty nie będą powtarzane w optymalnym czasie, będziesz  łatwiej zapomniał informacje albo uczył się danej informacji więcej razy niż to konieczne.
-   Odwrócenie karty ma sens tylko, gdy na obu kartach- standardowej i odwrotnej, chcesz mieć dokładnie te same informacje. Oznacza to, że nie ma możliwości na dodanie jakichś dodatkowych informacji na którejś z kart.

Anki rozwiązuje te problemy poprzez podział informacji zawartych w karcie na kawałki informacji. Możesz określić Anki które z tych kawałków mają być wyświetlane na każdej karcie. Program wygeneruje wtedy dokładnie taką kartę jaką określiłeś , a także zaktualizuje ją w przypadku wprowadzenia jakichkolwiek poprawek w przyszłości.

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

Aby dodawać i edytować pola, kliknij przycisk “Pola...​”  podczas dodawania lub edytowania notatek. Aby dowieszieć się wiecej o polach, zobacz rozdział o [dostosowywaniu pól](editing.md#customizing-fields).

### Typy kart

Aby stworzyć karty, musimy zaprojektować pewien szablon, który wskaże jakie informacje mają być wyświetlane na przedniej i tylnej stronie każdej karty. Tym szablonem jest "typ karty". Każdy typ notatki może zawierać jedną lub więcej typów kart; kiedy dodajesz notatkę Anki stworzyjedną kartę dla każdego typu karty.

Każdy typ karty ma dwa "szablony", jeden dla pytania i drugi dla odpowiedzi. W powyższym przykładzie z językiem francuskim chcieliśmy aby karta standardowa wyglądała w ten sposób:

    Pytanie: Bonjour
    Odpowiedź: Cześć
       Strona 12

Aby to zrobić, musimy stworzyć szablon pytania i odpowiedzi:

    Pytanie: {{Francuski}}
    Odpowiedź: {{Polski}}<br>
       Strona {{Strona}}

Nazwa pola umieszczona w nawiasie klamrowym jest sygnałem dla Anki, że w tym miejscu ma zostać wyświetlona informacja, która jest przechowywana w tym polu. Tekst znajdujący się poza nawiasami klamrowymi będzie taki sam na każdej karcie.  (na przykład nie musimy wpisywać "Strona X" w polu "Strona" kiedy dodajemy materiał do nauki - to pole jest dodawane automatycznie do każdej karty.) &lt;br&gt; To specjalny znak, który daje znać  Anki aby przeszło ono  do następnej linii; więcej szczegółów znajduje się w sekcji [szablony](templates/intro.md).

Szablon karty odwrotnej tworzymy w bardzo podobny sposób co karty standardowej:

    Q: {{English}}
    A: {{French}}<br>
       Page #{{Page}}

Once a card type has been created, every time you add a new note, a card
will be created based on that card type. Card types make it easy to keep
the formatting of your cards consistent and can greatly reduce the
amount of effort involved in adding information. They also mean Anki can
ensure related cards don’t appear too close to each other, and they
allow you to fix a typing mistake or factual error once and have all the
related cards updated at once.

To add and edit card types, click the “Cards…​” button while adding or
editing notes. For more information on card types, please see the [Cards
and Templates](templates/intro.md) section.

### Typy notatek

Anki allows you to create different types of notes for different
material. Each type of note has its own set of fields and card types.
It’s a good idea to create a separate note type for each broad topic
you’re studying. In the above French example, we might create a note
type called “French” for that. If we wanted to learn capital cities, we
could create a separate note type for that as well, with fields such as
“Country” and “Capital City”.

When Anki checks for duplicates, it only compares other notes of the
same type. Thus if you add a capital city called “Orange” using the
capital city note type, you won’t see a duplicate message when it comes
time to learn how to say “orange” in French.

When you create a new collection, Anki automatically adds some standard
note types to it. These note types are provided to make Anki easier for
new users, but in the long run it’s recommended you define your own note
types for the content you are learning. The standard note types are as
follows:

Basic  
Has Front and Back fields, and will create one card. Text you enter in
Front will appear on the front of the card, and text you enter in Back
will appear on the back of the card.

Basic (and reversed card)  
Like Basic, but creates two cards for the text you enter: one from
front→back and one from back→front.

Basic (optional reversed card)  
This is a front→back card, and optionally a back→front card. To do this,
it has a third field called “Add Reverse.” If you enter any text into
that field, a reverse card will be created. More information about this
is available in the [Cards and Templates](templates/intro.md) section.

Cloze  
A note type which makes it easy to select text and turn it into a cloze
deletion (e.g., “Man landed on the moon in \[…​\]” → “Man landed on the
moon in 1969”). More information is available in the [cloze
deletion](editing.md#cloze-deletion) section.

To add your own note types and modify existing ones, you can use Tools →
Manage Note Types from the main Anki window.

Notes and note types are common to your whole collection rather than
limited to an individual deck. This means you can use many different
types of notes in a particular deck, or have different cards generated
from a particular note in different decks. When you add notes using the
Add window, you can select what note type to use and what deck to use,
and these choices are completely independent of each other. You can also
change the note type of some notes [after you’ve already created
them](browsing.md).

### Kolekcja

Twoja  'kolekcja' to cały materiał przechowywany w Anki all the material stored in Anki – twoje karty,
notatki, talie, typy notatek, opcje talii i tak dalej.

## Udostępnione talie

Możesz zobaczyć [film o udostępnianiu talii i podstawach powtórek](http://www.youtube.com/watch?v=QS2G-k2hQyg&yt:cc=on) na YouTube (w języku angielskim).

The easiest way to get started with Anki is to download a deck of cards
someone has shared:

1.  Click the “Get Shared” button at the bottom of the deck list.

2.  When you’ve found a deck you’re interested in, click the “Download”
    button to download a deck package.

3.  Double-click on the downloaded package to load it into Anki, or
    File→Import it.

Please note that it’s not currently possible to add shared decks
directly to your AnkiWeb account. You need to import them with the
desktop program, then synchronize to upload them to AnkiWeb.

Creating your own deck is the most effective way to learn a complex
subject. Subjects like languages and the sciences can’t be understood
simply by memorizing facts — they require explanation and context to
learn effectively. Furthermore, inputting the information yourself
forces you to decide what the key points are, leading to a better
understanding.

If you are a language learner, you may be tempted to download a long
list of words and their translations, but this won’t teach you a
language any more than memorizing scientific equations will teach you
astrophysics. To learn properly, you need textbooks, teachers, or
exposure to real-world sentences.

    Do not learn if you do not understand.
    --SuperMemo

Most shared decks are created by people who are learning material
outside of Anki – from textbooks, classes, TV, etc. They select the
interesting points from what they learn and put them into Anki. They
make no effort to add background information or explanations to the
cards, because they already understand the material. So when someone
else downloads their deck and tries to use it, they’ll find it very
difficult as the background information and explanations are missing.

That is not to say shared decks are useless – simply that for complex
subjects, they should be used as a 'supplement' to external material,
not as a 'replacement' for it. If you’re studying textbook ABC and
someone has shared a deck of ideas from ABC, that’s a great way to save
some time. And for simple subjects that are basically a list of facts,
such as capital city names or pub quiz trivia, you probably don’t need
external material. But if you attempt to study complex subjects without
external material, you will probably meet with disappointing results.

