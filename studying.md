# Nauka

Czas zacząć naukę pobranej lub samodzielnie stworzonej talii.

## Talie

W Anki można uczyć się jednocześnie tylko jednej talii oraz talii, które wchodzą w jej skład.

W oknie głównym talie wyświetlane są w formie listy. Są tam widoczne dwie kolumny Oczekujące oraz Nowe. W kolumnie Oczekujące pokazana jest liczba kart do nauki w poszczególnych taliach. W kolumnie Nowe wyświetlana jest liczba nowych kart oczekujących na naukę tego dnia.

Po kliknięciu na nazwę danej talii w oknie głównym pojawi się ekran nauki. Aby zmienić obecnie wybraną talię możesz powrócić do listy talii klikająć "Talie" u góry głównego okna (Mozesz również uzyć opcji Ucz się Talii w menu, aby wybrać nową talię uzywając klawiatury. Naciskając klawisz "s" włączysz naukę obecnie wybranej talii).

Aby zmienić nazwę talii, usunąć talię, dostosować jej ustawienia lub ją [wyeksportować](exporting.md), wybierz przycisk koła zębatego po prawej stronie nazwy talii w oknie Talie.

Jeśli talia posiada podtalie, karty będą wyświetlane [z każdej talii po kolei](studying.md#display-order).

## Ekran główny talii

Po kliknięciu na nazwę talii, której chcesz się uczyć, wyświetli się ekran pokazujący liczbę kart oczekujących dzisiaj do nauki. Są ich trzy typy:

- **Nowe**, czyli karty pobrane lub samodzielnie wprowadzone, których jeszcze nigdy się nie uczyłeś.

- **Uczone** to karty, które widziałeś po raz pierwszy, ale jeszcze się ich nie nauczyłeś.

- **Do przejrzenia** to karty, których się już uczyłeś, a teraz będą powtarzane, abyś ich nie zapomniał.

Aby rozpocząć naukę kliknij przycisk Ucz się teraz. Anki rozpocznie wyświetlanie kart. Nauka będzie trwała do momentu wyczerpania się wszystkich kart przeznaczonych do nauki danego dnia.

Podczas nauki możesz cofnąć się do ekranu głównego talii naciskając klawisz "s" na klawiaturze.

## Pytania

W momencie wyświetlenia karty, jako pierwsze pokazywane jest pytanie. Po tym jak pomyślisz o odpowiedzi możesz albo kliknąć przycisk **Pokaż odpowiedź** albo nacisnąć spację. Zostanie wtedy wyświetlona odpowiedź. Normalną sytuacją jest, że przypomnienie sobie odpowiedzi na dane pytanie wymaga chwili namysłu, jeśli jednak po 10 sekundach dalej nie będziesz umiał podać prawidłowej odpowiedzi lepiej jest się poddać i wyświetlić odpowiedź niż w nieskończoność próbować ją wymyślić.

Po wyświetleniu odpowiedzi porównaj z nią swoją odpowiedź, a następnie oceń jak dobrze ci poszło. Jeśli nie jesteś pewien swoich odpowiedzi w myślach, możesz tak ustawić Anki, żeby odpowiedzi były przez ciebie [wpisywane](templates/fields.md#checking-your-answer), a nie tylko pokazywane.

Liczba przycisków do oceny twojej odpowiedzi zależna jest od tego czy karta była już wcześniej przeglądana.

## Nauka nowych kart

Podczas uczenia się nowych kart lub takich, które już wcześniej widziałeś, ale zapomniałeś ich odpowiedzi, Anki wyświetli je raz lub kilka razy, w pewnych odstępach czasu - tzw. interwałach. Standardowo dla takich kart są ustawione dwa interwały: 1 minuta oraz 10 minut. Możesz zmienić ich liczbę oraz wartości w  [Opcjach talii](deck-options.md).

Standardowo dla nowych kart w Anki wyświetlane są trzy przyciski oceny:

**Powtórz** cofa kartę do pierwszego kroku

**Dobra** przenosi kartę do nastepnego kroku. Jeżeli w poprzednim kroku karta została już wcześniej oceniona jako Dobra, to w tym kroku stanie się ona kartą powtórkową ("absolwentem"). By
default.Domyślnie zostanie ona wyświetlona następnego dnia, a potem co pewien narastający czas.
(zobacz nastepną sekcję)).

**Łatwa** natychmiast przekształca nową kartę w kartę powtórkową, nawet jeśli nie zostały dla niej wykonane inne kroki. Domyślnie karta ta zostanie wyświetlona za 4 dni, a potem co pewien narastający czas. Przycisk tej odpowiedzi nie będzie dostępny jeśli uczysz się kart, na które nie znałeś odpowiedzi lub odpowiedziałeś niepoprawnie, ponieważ przerwa byłaby taka sama jak przy odpowiedzi "Dobra".

Karta wyświetlana po raz pierwszy znajduje się w pierwszym kroku (1 minuta). Dla takiej karty odpowiedź **Dobra** będzie oznaczać, że zostanie ona wyświetlona za 10 minut, a początkowy krok - 1 minuta - zostanie pominięty.Jesli jednak przy drugim kroku (10 minut) naciśniesz "Powtórz", karta zostanie pokazana ponownie w ciągu jednej minuty.

Do oceny karty możesz również używać przycisków 1, 2 oraz 3 znajdujących się na klawiaturze, przy czym 1 = **Powtórz**. Wybranie spacji wybierze odpowiedź **Dobra**.

W sytuacji, gdy danego dnia nie ma już innych kart do nauki Anki domyślnie pokaże nowe karty, nawet wtedy, gdy nie upłynął jeszcze na nie czas oczekiwania. Jeśli jednak chciałbyś czekać pełen czas na kartę, to możesz zmienić ich zachowanie w [ustawieniach](preferences.md).

## Powtórka znanych kart

Jeżeli karta została już kiedyś wyświetlona w którejś z wcześniejszych powtórek będzie ona posiadała cztery przyciski oceny:

**Powtórz** oznacza, że podana odpowiedź była błędna, a w przyszłości Anki będzie częściej pokazywał tę kartę. Zobacz rozdział o [powtórkach](deck-options.md) aby dowiedzieć się wiecej na temat obsługi kart na które udzielono błędnej odpowiedzi.

**Trudna** karta zostanie wyświetlona po czasie niewiele dłuższym od tego przy ocenie Powtórz. W przyszłości Anki będzie ostrożniej harmonogramowało powtórki tej karty.

**Dobra** oznacza dla Anki, że ostatnio ustawiony interwał powtórki był bliski poprawnego i łatwość karty nie powinna być zmieniana ani w górę ani w dół. Przy standardowym, początkowym stopniu łatwości karta zostałaby pokazana po 2,5-krotnie dłuższym odstępie czasowym niż dotąd. Co dla karty z przerwą 10 dni oznacza kolejną powtórkę za około 25 dni.

**Łatwa** oznacza, karta jest dla użytkownika zbyt łatwa i należy zdecydowanie wydłużyć przerwę w  powtórkach. Karta otrzyma przerwę dłuższą niż w przypadku oceny Dobra, a Anki w przyszłym harmonogramowaniu karty będzie rzadziej ją pokazywał. Ponieważ ocena Łatwa gwałtownie wpływa na zwiększenie się odstepu czasowego powtórki najlepszym rozwiązaniem jest stosowanie jej tylko względem kart co do których jesteśmy w 100% pewni. W przypadku prawidłowej odpowiedzi najczęściej stosowaną oceną powinna być Dobra.

Tak samo jak przy nauce nowych kart, możesz użyć przycisków 1-4 na klawiaturze, aby wybrać odpowiedź. Naciśniecie spacji wybierze opcję "Dobra".

## Liczba oczekujących i czas nastepnej powtórki

W momencie pojawienia się karty z pytaniem na ekranie, u dołu wyświetlane są również trzy liczby np. 12 + 34 + 56. Reprezentują one: nowe karty, karty uczone oraz karty powtarzane. Jeśli chcesz, możesz ukryć te liczby w ustawieniach Anki.

W starym harmonogramie (wyznaczania powtórek), liczby pokazują liczbę _powtórek_ do ukończenia wszystkich kart w tej kolejce, a nie liczba samych _kart_. Jeśli ustawiłeś wielokrotną liczbę kroków, numer będzie się zwiekszał o więcej niż jeden, gdy odpowiesz "Powtórz", ponieważ ta karta musi być pokazana wiele razy.

W nowym harmonogramie (wyznaczania powtórek), liczby pokazują liczbę _kart_. Oznacza to, że liczby zawsze będą zwiększały się o jeden, niezależnie od liczby pozostałych kroków.

Po wyświetleniu odpowiedzi Anki pokaże również przybliżony, szacowany czas kolejnej powtórki danej karty. Jeśli chcesz, możesz ukryć ten wskaźnik w [ustawieniach](preferences.md) Anki.

Anki dodatkowo dodaje do czasu kolejnej powtórki pewną niewielką, losową liczbę, aby nowowprowadzone karty nie pojawiały się przy okazji kolejnych powtórek obok siebie. Ta losowość nie jest pokazywana w szacowanym czasie kolejnej powtórki danej karty, ale mimo tego algorytm Anki ją uwzględnia. 

## Przyciski Edytuj i Więcej

W czasie nauki, w celu edycji notatki możesz kliknąć przycisk **Edytuj**, który znajduje się po lewej stronie ekranu nauki. Po ukończeniu edycji powrócisz od razu do poprzedniego ekranu. Okno edytowania aktualnej karty jest bardzo podobne do standardowego okna [dodawania notatki](editing.md).

W prawym dolnym rogu ekranu nauki znajduje się przycisk **Więcej**, za pomocą którego możliwe jest wykonanie na danej karcie lub notatce dodatkowych operacji:

Dodaj flagę do karty 
Dodaje kolorowe wyróżnienie do karty lub je wyłącza. Flagi będa się pojawiały podczas nauki. Możesz szukać kart, do których dodano flagę w oknie przeglądania kart.  Opcja ta jest użyteczna jeśli chcesz w późniejszym czasie na tej szczególnej notatce wykonać jakąś czynność np. poszukanie danego słowa w słowniku kiedy wrócisz do domu.

Wyróżnij notatkę 
Dodaje etykietę "marked" do aktualnej notatki. Jest to opcja podobna do dodawania flag do kart, ale w przeciwieństwie do niej działa na podstawie etykiet, więc jeśli notatka ma kilka kart, wszystkie te karty pojawią się w poszukiwaniu etykiety "marked". Większość użytkowników bedzie preferowała używanie flag - wyróżnianie jest dalej dostępne głównie po to, aby zapewnić kompatybilność ze wcześniejszymi wersjami Anki.

Zakop kartę / notatkę  
Ukrywa kartę lub wszystkie karty danej notatki do momentu "odkopania" na [ekranie głównym talii](studying.md#study-overview) oraz automatycznie kolejnego dnia. Opcja ta jest użyteczna gdy nie możemy w danej chwili odpowiedzieć na kartę lub niedługo chcemy wrócić do niej wrócić. Zakopywanie może także odbywać się [automatycznie](studying.md#siblings-and-burying) podczas powtórki kart pochodzących z tej samej notatki. Jesli karty były kartami "Uczonymi", gdy zostały zakopane, są ustawiane do kolejki nowych lub powtarzanych kart przed zakopaniem.
buried.

Zawieś kartę / notatkę
Ukrywa kartę lub wszystkie karty danej notatki. Nie będą one wyświetlane aż do momentu ręcznego odwieszenia notatki przez użytkownika (poprzez wybranie notatki i klikniecie na przycisk Zawieś w oknie przeglądarki). Użyteczne, gdy chcesz wyłączyć na jakiś czas pokazywanie danej notatki, ale nie chcesz jej usuwać.
Jeśli karty były kartami "Uczonymi", gdy zostały zawieszone, są ustawiane do przed zakopaniem kolejki nowych lub powtarzanych kart.

Usuń notatkę
Usuwa notatkę i wszystkie jej karty.

Opcje 
Edycja ustawień obecnej talii

Odwtwórz dźwięk  
Odtwarza dźwięk, jeśli notatka posiada go na stronie tylnej lub przedniej.

Nagraj własny głos
Nagrywa swój głos w celu sprawdzenia wymowy. Nagranie to jest tymczasowe i zostanie skasowane po przejściu do kolejnej karty. Aby dodać do  karty nagranie na stałe musisz wykorzystać funkcję nagrywania w oknie Edycji.

Odtwórz swój głos  
Odtwórz swój nagrany głos (raczej użyjesz tej opcji po pokazaniu odpowiedzi).

## Kolejność wyświetlania

W czasie nauki zostaną wyświetlone karty z aktualnie wybranej talii oraz talii, które znajdują się pod nią. Jeżeli wybierzesz talię "Francuski", do której należą talie "Francuski::Słówka" oraz "Francuski::Mój Podręcznik::Lekcja 1" to także one zostaną wyświetlone w czasie nauki.

Jeżeli posiadasz talie zorganizowane w strukturze drzewa to powtórka i nauka zawartego w nich materiału będzie przebiegać w kolejności alfabetycznej według nazw tych talii. Dla powyższego przykładu w pierwszej kolejności pojawią się karty talii "Francuski", następnie "Mój podręcznik", a na końcu "Słówka". Opisana zasada może zostać wykorzystana do prioretyzowania poszczególnych talii, wstawiając karty o wysokim priorytecie do talii, które wyświetlane są wyżej. Do tego celu można również użyć symbolu myślnika "-", który interpretowany jest przed znakami liter oraz symboli “\\~” interpretowanych znakach liter. Jeśli zatem talię nazwiesz "-Słówka" to karty w niej zawarte zostaną wyświetlone jako pierwsze, zaś talia "~Mój Podręcznik" będzie w takim przypadku wyświetlona jako ostatnia. 

Nowe karty i karty powtarzane zużywane są niezależnie w trakcie powtórki. Oznacza to, że w jej trakcie możesz natrafić na nową kartę, która będzie pochodzić z kolejnej talii, gdy nowe karty z talii aktualnej zostały już wykorzystane. Sposobem na to aby karty nowe i powtarzane były wyświetlane jedynie w ramach powtórki tej samej talii jest nauka bezpośrednio tej szczególnej talii, zamiast wykorzystywania do tego celu rodzica (talii nadrzędnej).

Karty uczone, to znaczy takie które zostały wyświetlone po raz pierwszy i/lub oznaczone jako Powtórz, są wyświetlane niezależnie od aktualnie powtarzanej talii, zgodnie z przypisaną im przerwą.

Aby ustawić kolejność powtórek jaka wyświetla się z danej talii lub wyświetlać nowe karty losowo, zobacz [Opcje talii](deck-options.md). Aby uzyskać bardziej szczegółowe uporzadkowanie nowych kart, możesz zmienić ich kolejność w [przeglądarce kart](browsing.md).

## Bliźnięta i zakopywanie

Z [podstaw](getting-started.md) przypomnij sobie, że z jednej notatki Anki może stworzyć wiele kart, np. Przód→Tył i Tył-Przód, albo dwie różne luki w tym samym tekście. Karty, które powstają w ten sposób nazywają się bliźniętami. 

Aby zapobiec pokazaniu bliźniaka w czasie tej samej powtórki Anki automatycznie zakopuje bliźniaczą kartę. Zakopana karta nie będzie wyświetlana do kolejnego dnia lub do momentu kiedy sam ją ręcznie odblokujesz przy pomocy przycisku "Odkop", widocznego na dole okna po otwarciu [ekranu głównego](studying.md#study-overview) talii. Anki zakopuje bliźniaków, nawet jeśli znajdują się w innych taliach, na przykład gdy użyjesz [nadpisywania talii](templates/intro.md).

Jeżeli jednak w czasie powtórki chcesz widzieć więcej niż jedną kartę z danej notatki, możesz zatrzymać zakopywanie bliźniaczych kart w [opcjach talii](deck-options.md). Możesz ustawić osobne opcje dla nowych kart i dla powtórek.

Anki zakopie jedynie bliźnięta kart nowych i powtarzanych. Nie zakopie za to kart uczonych. Z drugiej strony, jeśli przeglądasz kartę nauczoną, wszelkie nowe/powtarzane bliźnięta zostaną zakopane.

## Skróty klawiszowe

Większość z operacji wykonywanych w Anki posiada przypisane do siebie skróty klawiszowe. Większość z tych skrótów widoczna jest bezpośrednio w oknie Anki np. w rozwijanych menu kontekstowych obok nazwy funkcji lub po najechaniu na dany przycisk kursorem myszy.

Najczęściej używanym skrótem klawiszowym w czasie powtórki jest przycisk spacji lub Enter, które wyświetlają odpowiedź na zadane pytanie. Kolejne kliknięcie spacji lub klawisza Enter spowoduje przypisanie do karty oceny Dobra. Wszystkie oceny dostępne są pod klawiszami 1-4, w kolejności rosnącej od Powtórz. Wiele osób używa jedynie dwóch klawiszy - spacji dla oceny Dobra i w celu wyświetlenia odpowiedzi oraz 1 jeżeli odpowiedź została zapomniana.

Przydatnym skrótem klawiszowym może okazać się też przycisk ukośnika "/", po wybraniu którego wyświetlane jest okno "Nauka tali…" dostępne standardowo w menu Narzędzia. W oknie tym pokazane są wszystkie talie w twojej kolekcji oraz pole filtrowania u góry. Po wpisaniu tekstu w polu filtrowania, poniżej wylistowane zostaną tylko te talie, które spełniają jego warunki. Co więcej, za pomocą spacji możesz nadawać kolejne warunki dla filtru. W ten sposób wyświetlą się tylko te talie, które spełniają wszystkie wstawione warunki. Przykładowo zarówno "ja 1" jak i "ad1 ja" wskażą na talię o nazwie "Japoński::Wykład1".

## Zaległości

Jeżeli z czasem zaczynasz zostawać w tyle z powtórkami, Anki będzie nadawał najwyższy priorytet tym kartom, które oczekują najdłużej na powtórkę. Karty te  w trakcie powtórki będą wyświetlane w sposób losowy do momentu wyczerpania dziennego limitu powtórek. Taka procedura gwarantuje, że żadna z kart nie będzie oczekiwała na wyświetlenie w nieskończoność. Jeśli jednak postanowisz wprowadzić nowe karty, ich powtórki nie będą one pokazywane do momentu, w którym nie powtórzysz wszystkich zaległych kart.

Jeśli chcesz zmienić kolejność długo oczekujących kart poprzez utworzenie [talii filtrowanej](filtered-decks.md).

Gdy przeglądasz karty, które oczekiwały już jakiś czas na powtórkę, Anki uwzględnia to oczekiwanie w przyszłym harmonogramowaniu powtórek karty.
Zobacz rozdział o [algorytmie](faqs.md) spaced-repetition, aby dowiedzieć się wiecej.
 
