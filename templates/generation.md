# Generowanie kart

Karty odwrotne
-------------

Możesz obejrzeć [film o odwracaniu kart](http://www.youtube.com/watch?v=DnbKwHEQ1mA&yt:cc=on) na YouTube.

Jeżeli chcesz stworzyć notatkę, która będzie cię odpytywać w dwóch kierunkach (np. zarówno "ookii"→"duży" oraz "duży"→"ookii") masz kilka możliwości, by to zrobić. Najprostszym sposobem jest wykorzystanie wbudowanego typu notatki Podstawowy (z odwrotną kartą). Typ ten automatycznie wygeneruje dwie karty, każdą w jednym kierunku.

Jeśli chcesz wygenerować karty odwrotne tylko dla części notatek (np. chcesz uczyć się najważniejszych informacji tylko z kart odwrotnych lub, gdy dla niektórych notatek karta podwójna po prostu nie ma sensu), możesz użyć do tego celu typu notatki Podstawowy (z opcjonalną odwrotną kartą). Ten typ notatki stworzy standardową kartę jeśli wypełnisz tylko dwa pierwsze pola. Aby uzyskać również kartę odwrotną wystarczyć wpisać dowolny znak do trzeciego pola o nazwie Dodaj rewers. Należy podkreślić, że zawartość ostatniego pola nie będzie wyświetlana na kartach podczas powtórki.

Generowanie i usuwanie kart
--------------------------

Anki nie wygeneruje żadnej karty jeżeli jej przód będzie pusty. Przykładowo jeżeli w podstawowym typie notatki pole Przód będzie puste, a szablon przodu będzie zawierał tylko to pole, to karta nie zostanie wygenerowana.

W takim przypadku w oknie Dodaj pojawi się ostrzeżenie, o tym, że karta nie powstanie dopóki pole to nie zostanie wypełnione informacją.

Po edycji wcześniej dodanej notatki Anki utworzy automatycznie dodatkowe karty, jeśli były one wcześniej puste, ale już nie są. Jesli twoje zmiany sprawiły, że karty, które wczesniej nie były puste takie się stałym Anki nie usunie ich od razu ponieważ mogłoby to prowadzić do utraty danych. Aby usunąć puste karty, wejdź w oknie głównym do Narzędzia → Puste karty. Zostanie pokazana lista pustych kart z opcją ich usunięcia.

Nie ma możliwości usuwania ręcznie pojedynczych kart, ponieważ i tak zostałyby one odtworzone w momencie kolejnej edycji notatki. Zamiast tego, możesz usunąć informacje z pól warunkowego zastępowania (niektórych pól), a następnie użyć opcji "Puste Karty".


Anki przy generowaniu kart nie uwzględnia pól specjalnych oraz zwykłego tekstu, który nie jest odnośnikiem do pola, to znaczy, że na ich podstawie nie zostaną stworzone żadne nowe karty. Przykładowo jeżeli pole "Kraj" w szablonie przodu w poniższym przykładzie będzie puste, to karta nie powstanie, pomimo tego, że szablon zawiera jeszcze zwykły tekst "Gdzie na mapie znajduje się":

    Gdzie na mapie znajduje się {{Kraj}}?

Generowanie kart opcjonalnych
-------------------------

W niektórych sytuacjach możesz mieć potrzebę wygenerowania dodatkowych kart w celu nauki obcych znaczeń polski słów, ale tylko niektórych, tych przez ciebie wybranych. Aby móc stworzyć takie  opcjonalne, dla niektórych notatek, karty musisz w pierwszej kolejności dla danego typu notatki utworzyć nowe pole. Jeżeli w polu tym będzie znajdował się jakikolwiek tekst - wystarczy jedna litera lub cyfra, to zostanie wygenerowania dodatkowa karta. Następnym krokiem jest dokonanie odpowiednich zmian w szablonie notatki. Więcej informacji na ten temat znajduje się w rozdziale poświęconym poleceniom warunkowym poniżej.


Polecenia warunkowe
-----------------------

W Anki istnieje możliwość dodawania do karty określonego tekstu w zależności czy w danym polu znajduje się tekst lub zxy jest puste. Przykład:

    Ten tekst będzie zawsze widoczny

    {{#NazwaPola}}
        Ten tekst będzie widoczny tylko, gdy w polu NazwaPola będzie tekst.
    {{/NazwaPola}}

    {{^NazwaPola}}
        Ten tekst będzie widoczny tylko, gdy pole NazwaPola będzie puste.
    {{/NazwaPola}}

Przykład poniżej pokazuje etykiety, gdy pole etykiet zawiera jakąś treść:

    {{#Tags}}
        Etykiety: {{Tags}}
    {{/Tags}}

Lub założmy, że chcesz wyświetlać okreslone okręslone pole w kolorze niebieskiem na przodzie karty, jesli istnieją dodatkowe notatki na tyle (fakt, ze istnieja dodatkowe notatki może słuzyć jako przypomnienie, ze powinienes spędzić wiecej czasu nad zastanowieniem się nad powiedzią). Możesz wystylizować pole w następujący sposób:

    {{#Notatki}}
        <span style="color:blue;">
    {{/Notatki}}
    
    {{Pole do sformatowania}}
    
    {{#Notatki}}
        </span>
    {{/Notatki}}

Poleceń warunkowych możesz równiez używać, aby kontrolowac, które karty są generowane. To zadziało, jako że Anki nie generuje kart, które miałyby pustą przednia stronę. Na przykład, karta z dwoma polami na przodzie:

    {{Wyrażenie}}
    {{Notatki}}

Zwykle karty zostałaby wygenerowane jesli którekolwiek pole "wyrażenia" lub "notatki" miałoby w sobie tekst. Jesli chciałbyś, żeby karta się generowała tylko jesli "Wyrażenie" nie byłoby puste, możesz zmienić szablon na nastepujący:

    {{#Wyrażenie}}
        {{Wyrażenie}}
        {{Notatki}}
    {{/Wyrażenie}}

Jesli chciałbyś, aby oba pola były wymagane, mógłbys użyć zastępowania warunkowego:

    {{#Wyrażenie}}
        {{#Notatki}}
            {{Wyrażenie}}
            {{Notatki}}
        {{/Notatki}}
    {{/Wyrażenie}}

Pamiętaj, że działa to tylko, gdy umiescisz kod zastepowania warunkowego na *przodzie* karty. Jesli zrobisz to w tylnej części, karty beda w niej po prostu puste. Podobnie, jako ze to działa poprzez sprawdznie, czy pole przodu jest puste, ważne jest aby upewnić się, że cała częśc przednia zostanie objęta przez kod zastepowania warunkowego. NA przykład poiniższyt przykład nie zadziałałby, jak byśmy tego oczekiwali:

    {{#Wyrażenie}}
        {{Wyrażenie}}
    {{/Wyrażenie}}
    {{Notatki}}

## Ograniczenia w starszych wersjach Anki

Poniższe ograniczenia nie mają zastosowania Anki 2.1.28+ i AnkiMobile 2.0.64+.

Wcześniejsze wersje Anki nie mogą używać negacji (negatywnych poleceń warunkowych) do wygenerowania karty.
 Na przykład, na Anki 2.1.28, poniższy tekst dodałby kartę, jesli pole nazwane "DodajJeśliPuste" byłoby puste, a "Przód" zawierałoby jakiś tekst:

     {{^DodajJeśliPuste}}
         {{Przód}}
     {{/DodajJeśliPuste}}

Na wczesniejszych wersjach Anki negacja jest ignorowane, a generowanie kart w tym przypadku zależałoby tylko od tego, czy pole "Przód" nie byłoby puste.

 Mieszanie warunków  **I** i **LUB** również może spowodowac problemy w starszych wersjach. Na przykład, poniższy tekst ("dodaj karte, jeśli A **LUB** B **LUB** C nie jest puste) jest prawidłowy:

     {{A}}
     {{B}}
     {{C}}

 Również następny tekst("dodaj kartę jeśli A **I** B **I** C nie są puste") jest prawidłowy:

     {{#A}}
         {{#B}}
             {{#C}}
                 {{A}}
             {{/C}}
         {{/B}}
     {{/A}}

Jednak poniższy ("dodaj kartę, jeśli A **LUB** (B **I** C) nie są puste") nie będzie działał poprawnie:

     {{A}}
     {{#B}}
         {{#C}}
             {{B}}
         {{/C}}
     {{/B}}

Szablon luki
---------------

Zobacz rozdział o [wypełnianiu luki](editing.md#cloze-deletion), aby dowiedzieć się podstaw.

Budowa notatki typu luka różni się od budowy notatki standardowego typu. Zamiast pewnej liczby kart generowanych na podstawie notatki mamy tutaj do czynienia z tylko jedną kartą. Co więcej, wszystkie karty z luką generowane są na podstawie tego samego szablonu notatki.

Jak zostało to wspomniane w rozdziale dotyczącym generowania kart, standardowe karty tworzone są na podstawie jednego lub więcej pól, przy czym pole znajdujące się w pytaniu nie może być puste. Generowanie kart wygląda trochę inaczej w przypadku notatki typu luka:

-  Anki najpierw przeszukuje szablon przodu pod kątem polecenia {{cloze:NazwaPola}}.

-  Następnie w polu NazwaPola wyszukuje luki w postaci {{c1::tekst}}.

-  Na końcu dla każdej luki tworzona jest osobna karta.

JAko, że generowanie kart działa inaczej dla kart typu luka, tagi {{cloze:…​}} nie moga bhyć używane ze standardowym typem notatki - bea one działały poprawnie tylko z typem notatki "luka".

W kartach typu luka możliwe jest również używanie poleceń warunkowych. Przykładowo dla, każdej luki możemy wstawić niezależne podpowiedzi. Aby to zrobić, w szablonie przodu powinien znaleźć się następujący kod:

    {{cloze:Tekst}}

    {{#c1}}
    {{Podpowiedź1}}
    {{/c1}}

    {{#c2}}
    {{Podpowiedź2}}
    {{/c2}}
