Opcje talii
============

Opcje talii dostępne są po wybraniu odpowiedniej talii w oknie głównym, pod przyciskiem Opcje na dole ekranu.

Anki umożliwia na wspóldzielenie tych samych opcji pomiędzy różnymi taliami. Dzięki temu możliwa jest zmiana ustawień wielu talii poprzez jednokrotnę zmianę opcji. Aby to zrobić, opcje umieszczone są w grupach opcji. Domyślnie, wszystkie nowopowstałe talie używają tej samej grupy opcji, zaś talie zaimportowane z poprzedniej wersji Anki będą posiadały oddzielne grupy opcji. Aby zmienić ustawienia tylko jednej talii, ale nie innych, kliknij ikonę koła zębatego w prawnym górnym rogu okna i dodaj nową grupę opcji.

Pamiętaj, żeby dokonywać zmian tylko w ustawieniach, których działanie w pełni rozumiesz. Nieodpowiednie ustawienia mogą doprowadzić do zmniejszenia efektywności nauki.

Opcje programu nie działają wstecz. Jeśli zmienisz opcję, która określa po jakim czasie karta ma być wyświetlona po błędnej odpowiedzi, a następnie powrócisz do poczatkowych ustawień, to karty z poprzednim ustawieniem zachowają nadany im już wcześniej czas oczekiwania.

Nowe karty
---------

**Kroki** kontrolują liczbę wyświetleń nauki nowej karty i opóźnienie pomiędzy tymi wyświetleniami. Aby dowiedzieć się więcej o tym, jak działają kroki, zajrzyj do rozdziału o [nauce](studying.md#learning).

Domyślnie jednostką kroków jest minuta, możliwe jest jednak ustawienie kroków wyrażonych w dniach, a więc nie tylko: 10 minut, ale również 1 dzień (1440 minut), trzy dni (4320 minut) lub 7 dni itd.

Jeśli nie ma nic innego do nauki, Anki pokazuje karty z wyprzedzeniem (domyślnie limit nauki z wyprzedzeniem ustawiony jest na 20 minut). Czas nauki z wyprzedzeniem można zmienić w [ustawieniach](preferences.md). Warto być świadomym tego, że w tym przypadku liczba kart oczekujacych będzie się różnić między ekranem talii a ekranem nauki. Ekran talii nie będzie liczył kart, które nie będą jeszcze gotowe, podczas gdy ekran nauki będzie brał je pod uwagę. Zostało to zrobione w ten sposób abyś wiedział, która talia wymaga twojej uwagi.

Anki traktuje inaczej małe kroki oraz kroki, które przekraczają granice jednego dnia. Jeśli chodzi o małe kroki, karty są pokazywane tak szybko jak nadejdzie ich pora, faworyzując inne czekające karty jak powtórki. Jest to zrobione w taki sposób abyś mógł odpowiedzieć na karty jak najbliżej chwili, kiedy powinny one zostać planowo pokazane. Inaczej sytuacja wygląda w przypadku kart przekraczających jeden dzień. Ich pokazanie jest planowane na zasadzie dni (tak samo jak jest to z powtórkami). Gdy powrócisz do nauki w dniu nastepnym, karty uczone, które są planowane na zasadzie dni, nie bedą pokazane jako pierwsze. Zostało to zrobione w ten sposób, aby pierwsza połowa sesji powtórek nie była z byt frustrująca. Zamiast tego karty są pokazywane po tym jak powtórki zostaną przejrzane. Ze względu na sposób w jaki kroki przekraczające granice jednego dnia są traktowane przez program, są one uwzględniane w liczniku powtórek, a nie uczonych kart.

**Kolejność** to funkcja, która kontroluje sposób wyświetlania nowych kart w trakcie powtórki. Mogą być one pokazywane w losowej kolejności lub według kolejności ich dodania do talii. Gdy zmienisz tę opcję nowe karty zostaną "przetasowane" przy użyciu aktualnej grupy opcji. W przypadku kiedy wybierzesz opcję "Pokaż nowe karty w kolejności losowej", a do swoich talii dodajesz dużo nowych kart, to karty najnowsze, będą wyświetlane trochę częściej niż te wcześniej dodane. Wyjściem z tej sytuacji jest zmiana ustawienia na "Pokaż nowe karty w kolejności dodania", a następnie powrót do opcji "Pokaż nowe karty w kolejności losowej". Nastąpi wtedy ponowne "przetasowanie" nowych kart.

Gdy wybierasz kolejność losową, Anki przesortuje twoje notatki, zachowując karty danej notatki blisko siebie. Karty danej notatki są pokazywane w kolejności, w jakiej wyświetlane są jej typy kart, aby bliźnięta były wprowadzane konsekwentnie. W przeciwnym przypadku karty niektórych notatek byłyby już pokazane, podczas gdy inne notatki miałyby pokazane tylko jedną lub dwie karty. Zobacz na dole opcję "zakop powiazane", aby dowiedzieć się więcej.

**Nowe karty/dzień** określa, ile nowych kart będzie pokazywanych każdego dnia, kiedy otwierasz program. Jeżeli któregoś dnia ominiesz powtórkę, liczba nowych kart do nauki nie wzrośnie, codziennie pozostając na tym samym poziomie. Limit odnosi się do talii i podtalii. To oznacza, że jeżeli talia "Francuski" posiada limit 20 nowych kart dziennie, zaś "Francuski::Lekcja 1" oraz "Francuski::Lekcja 2" limit 15 nowych kart dziennie to ucząc się talii "Francuski" otrzymasz 15 kart z lekcji pierwszej i 5 kart z lekcji drugiej.

Nauka nowych kart spowoduje tymczasowy wzrost liczby kart w dziennej powtórce. Świeży materiał musi być powtarzany częściej, w późniejszym okresie odstępy czasowe staną się dłuższe. Jeżeli każdego dnia uczysz się 20 nowych kart, możesz oczekiwać, że do codziennej powtórki będzie ok 200 kart. Liczbę tę możesz zmniejszyć wprowadzając mniejszą liczbę nowych kart lub w ogóle wyłączyć wprowadzanie nowych kart do momentu gdy spadnie liczba kart powtarzanych. Niektórzy użytkownicy Anki próbowali uczyć się setek nowych kart podczas pierwszych ich dni nauki z programem, przez co zostali przytłoczeni przez nadchodzące powtórki.

**Przerwa kart absolwentów** to czas do następnego pokazania karty po odpowiedzi "Dobra" na karcie, która wykonała wszystkie kroki.

**Przerwa dla Łatwych** to czas do pierwszego pokazania karty jako powtórki po odpowiedzi "Łatwa" na uczonej karcie.

**Początkowa łatwość**  kontroluje łatwość z jaką karty są tworzone. Jest ona ustalana gdy karta uczona po raz pierwszy przechodzi do puli powtórek. Domyślnie jest ustawiona na 250% co oznacza, że gdy skończyłeś uczyć się karty, odpowiedź "Dobra" na kolejne powtórki zwiększy odstęp czasowy o około 2,5 razy (np. jeśli ostatnia przerwa wynosiła 10 dni, następna będzie wynosić już 25 dni). Łatwość może wzrosnąć lub zmniejszyć się na podstawie tego jak ocenisz karte w następnych powtórkach.  

Wyłączając opcje **zakop powiązane…​**, sprawisz że [bliźnięta nie będą zakopywane](studying.md#siblings-and-burying). Zamiast tego Anki będzie starało się odsuwać pokazywanie bliźniaczych kart w czasie, ale jeszcze w czasie tej samej powtórki. Aby ta funkcja zadziałała, liczba nowych kart na dzień musi być odpowiednio duża, tak żeby możliwe było odpowiednie rozsunięcie kart.

Powtórki
-------

**Maksymalnie powtórek/dzień** pozwala na ustawienie dziennego limitu powtarzanych kart. Kiedy limit zostanie osiągnięty, Anki nie pokaże następnych kart do powtórki tego dnia, nawet jeśli są karty oczekujące. Funkcja ta jest przydatna przy systematycznej nauce, gdyż pomaga uniknąć tzw. górek, czyli nagromadzenia się dużej liczby kart do powtórki jednego dnia. Dzięki tej funkcji również po powrocie z wakacji nie zaczynasz od odkopywania się z ogromnej liczby zaległych kart. Jeżeli po ukończeniu powtórki pozostają jakieś karty oczekujące, to informacja o tym zostanie wyświetlona na ekranie z gratulacjami po skończonej powtórce, gdzie pojawi się sugestia zwiekszenia limitu, jeśli starczy nam jeszcze czasu na powtórki. 

**Premia odpowiedzi Łatwa** pozwala na ustalenie różnicy w przerwie pomiędzy odpowiedziami "Dobra" i "Łatwa". Na przykład w domyślnej wartości 130% odpowiedź "Łatwa" nada przerwę wynosząca 1,3 raza odpowiedzi "Dobra"(czyli Łatwa = 1,3xDobra)

**Modyfikator przerw** pozwala na ustawienie mnożnika przerw. Domyślnie ustawiona jest wartość 100%, która nie modyfikuje w żaden sposób długości przerwy. Jeżeli modyfikator będzie miał wartość 80% to przerwa będzie wynosiła 80% czasu standardowej (zamiast 10 dni przerwy będzie to 8 dni). Zmieniając to ustawienie żonglujemy odstępami w pokazywaniu kart np. pokazując je cześciej w zamian za lepsze zapamiętywanie i dłuższy czas nauki.

Przeciętny użytkownik uczący się materiału o umiarkowanej trudności powinien zapamiętywać około 90% dojrzałych kart. Swój własny wynik w powtórce dojrzałych kart możesz znaleźć w statystykach danej talii na wykresie Przyciski odpowiedzi - procentowa skuteczność odpowiedzi udzielonych do potwórki kart dojrzałych pokazana jest na czterech kolumnach po prawej stronie. Jeżeli nie uczysz się danej talii dostatecznie długo, możesz jeszcze nie mieć żadnych dojrzałych kart. Analizę wyników warto jednak odłożyć na czas, gdy uzbiera się już odpowiednia liczba wyników, które będą w reprezentatywny sposób określały stan twojej wiedzy.

Twórcy SuperMemo sugerują użycie wzoru do obliczenia oczekiwanego przez użytkownika poziomu zapamiętywania. Wzór sprowadza się do:

    log(docelowe zapamiętanie%) / log(obecne zapamiętanie%)

Załóżmy, że obecne zapamiętanie to 85% i chcemy je zwiększyć do 90%. Policzmy zatem modyfikator:

    log(90%) / log(85%) = 0.65

Do obliczeń możesz [użyć Google](https://www.google.com/search?q=log(90%25)+%2F+log(85%25)).

Zatem, jeśli ustawisz modyfikator przerw na poziomie 65%, po pewnym czasie twoje zapamiętywanie powinno zbliżyć się do zakładanego, docelowego poziomu.

Zauważ, że zależność pomiędzy czasem spędzonym przy nauce a poprawą zapamiętania jest nieliniowa: zapamiętanie poprawiasz o 5%, zaś wzrost częstotliwości nauki to aż 35%. Jeżeli uczysz się czegoś ważnego, to dodatkowy wysiłek rzeczywiście może się opłacić - sam musisz zdecydować. Jeżeli jednak jesteś po prostu niezadowolony z faktu, że dużo zapominasz, to będzie dla ciebie lepiej jeśli spędzisz więcej czasu nad początkowym etapem nauki i/lub do nauki wykorystasz mnemotechniki.

Ostatnią rzecza wartą wspomnienia jest fakt, że Anki wymusza nową przerwę, która jest co najmniej o 1 dzień dłuższa niż poprzednia, abyś nie utknął powtarzając kart w kółko z tą samą przerwą. Jeśli twoim celem jest powtarzanie karty raz dziennie przez kilka dni, możesz to zrobić ustawiając więcej kroków. zamiast zmieniać modyfikator przerw.

**Maksymalna przerwa** określa górny limit czasu między powtórkami w danej talii. Wartość domyślna to 100 lat. Możesz go jednak zmniejszyć, aby dodać więcej powtórek i uzyskać tym samym lepsze zapamiętywanie kosztem dłuższego czasu nauki.

**Przerwa dla Trudnych** określa, jak długa bedzie następna przerwa po naciśnieciu przycisku "Trudna". Procent jest zależny od poprzedniej przerwy, np. w przypadku domyślnej opcji 120%, karta, której przerwa wynosi 10 dni otrzyma przerwę wynoszącą 12 dni. Ta opcja jest dostepna tylko wtedy, gdy w ustawieniach włączony jest eksperymentalny planista.

Wyłączając opcje **zakop powiązane…​** spowoduje, że [bliźnięta nie będa zakopywane](studying.md#siblings-and-burying), a Anki postara się nie pokazywać bliźniaków po sobie w tej samej sesji nauki.

Kartry powtórkowe są zawsze pokazywane w losowej kolejności. Jeśli chcesz je przejrzeć w innej kolejności, możesz uzyć [talii filtrowanej](filtered-decks.md). W szczegółach - Anki losuje powtórki poprzez zbieranie pakietów po 50 kart w kolejności w jakiej występują w bazie danych, mieszając każdy pakiet, a następnie wszystkie je łączy. Oznacza to, że istnieja lekka skłonność do pokazywania najpierw starszych kart, jednak dzięki temu karty nie są pokazywane w przewidywanej kolejności.

Pomyłki
------

Jeżeli podczas powtórki nie będziesz potrafił odpowiedź na zadane pytanie i ocenisz kartę jako "Powtórz", zostanie ona określona jako pomyłka. Domyślnym zachowaniem pomyłek jest zresetowanie ich interwału powtórki do 1 i wrzucenie ich do kolejki kart do ponownej nauki za 10 minut. To zachowanie może zostać zmodyfikowane poprzez zastosowanie opisanych poniżej opcji.

Jeśli pozostawisz pole z krokami puste, Anki nie umieści karty z powrotem w kolejce ponownie uczonych kart i będzie rozplanowana jako powtórka według ustawień znajdujących się poniżej.

Nowa przerwa jest ustalana, gdy odpowiadasz "Powtórz" na kartę powtórkową, a nie, kiedy karta ukończy kroki ponownej nauki. Z tego powodu odpowiedzi "Dobra" i "Łatwa" nie są mają wpływu na przerwę podczas gdy karty są uczone ponownie - kontrolują tylko ile zostało ci kroków. Jeśli jest tylko jeden krok (domyślna opcja), przycisk "Łatwa" zostanie ukryty, jako że pełniłby taką samą funkcję jak odpowiedź "Dobra". W przypadku, gdy masz ustawionych 2 lub więcej kroków, odpowiedź "Łatwa" nie jest ukryta, aby umożliwić ci ukończenie nauki kart przed przejściem przez wszystkie kroki. 

"Przerwa nowej karty" kontroluje jak bardzo Anki powinno zmniejszyć poprzednią przerwę. Robi to wykorzystując, procent, który został w tej opcji ustawiony. Jeśli karta miała przerwę w ilości 200 dni, domyślna opcja 0% sprawi, że przerwa będzie wynosić 0 (ale spójrz na akapit poniżej). Jeśli za to ustawisz tę opcję na 50%, wtedy przerwa karty zostałaby obniżona do 100 dni.

"Minimalna przerwa" pozwala ustawić minimalny limit dla opcji powyżej. Domyślna opcja ustala, że pomyłki powinny być powtarzane jeden dzień później. Przrerwa musi wynosiź co najmniej 1 dzień.

Opcja "Pijawki" ustala, co Anki ma zrobić z wykrytymi pijawkami. Zobacz rozdział o [pijawkach](leeches.md), aby dowiedzieć się wiecej.

Ogólne
-------

Anki monitoruje czas twojej odpowiedzi, pozwala to między innymi na obliczenie czasu, jaki spędzasz powtarzając i ucząc się kart każdego dnia. Czas ten nie wpływa na harmonogram powtórek. Jeżeli nie udzielisz odpowiedzi na kartę w ciągu 60 sekund, Anki przyjmuje, że odszedłeś od komputera lub rozproszyłeś się na tyle, że nie jesteś w stanie udzielić poprawnej odpowiedzi. Twoja ocena w takim przypadku nie zostaje uznana i nie wpłynie niekorzystanie na statystki powtórki. "Ignoruj odpowiedzi z czasem dłuższym niż…​" pozwala na kontrolę czasu po którym odpowiedzi nie będa brane pod uwagę do statystyki powtórki. Minimalnie wynosi ona 30 sekund.

Jeżeli zaznaczona jest opcja Pokaż czas odpowiedzi, Anki będzie wyświetlał aktualny czas spędzony na danej karcie.

Domyślanie Anki automatycznie odtwarza pliki audio zarówno na przodzie jaki i tyle karty. Jeżeli odznaczysz "Automatycznie odtwórz pliki audio", Anki odtworzy plik audio dopiero w przypadku, kiedy naciśniesz przycisk powtórz dźwiek, `r` lub `F5`.

"Zawsze dołączaj stronę pytania przy odtwarzaniu nagrania" - opcja ta określa, co dzieje się kiedy naciśniesz przycisk powtórz dźwięk, gdy pokazana jest odpowiedź. Opcja ta nie kontroluje tego, co dzieje się po pokazaniu odpowiedzi; więcej informacji na ten temat znajduje się [tym rozdziale](templates/fields.md#special-fields).

Opis
-----------

Możesz tu edytować opis talii, który będzie pokazywany po wejściu do danej talii w oknie głównym Anki. Opis pobierany jest automatycznie z taliami udostępnionymi przez społeczność Anki. Można go w każdej chwili dowolnie edytować lub usunąć, również w przypadku talii udostępnionych.

W opisie możesz również używać HTML - wszystko co działa w notatce powinno działać również i tutaj.
