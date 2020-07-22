# Zastępowanie pól

## Podstawy zastępowania pól

Podstawowy szablon wygląda w następujący sposób:

    {{Przód}}

Gdy w nawiasy klamrowe wpiszesz jakiś tekst, Anki uzna to za odniesienie do któregoś z istniejących pól o tej samej nazwie. Przy wyświetlaniu danej karty zastąpi ten tekst zawartością danego pola.

W nazwach pól brana jest pod uwagę wielkość liter. Jeśli masz pole nazwane `Przód`, wpisanie `{{przód}}` nie zadziała.

W szablonach możesz umieścić odwołania do dowolnej liczby pól. Możesz w nich również umieszczać możesz dowolny tekst. Na przykład, jesli uczysz się stolic państw i utworzyłeś typ notatki z polem "Kraj", możesz zmodyfikować szablon przodu, aby wyglądał w nastepujący sposób:

    Jaka jest stolica {{Kraj}}?

Standardowy szablon tyłu karty wygląda w następujący sposób:

    {{FrontSide}}

    <hr id=answer>

    {{Tył}}

Kod ten należy interpretować w następujący sposób: "pokaż mi pytanie, narysuj linię i pokaż pole Tył.

Kod "id=answer" daje znać Anki, gdzie znajduje się granica miedzy pytaniem i odpowiedzią. Umożliwia to Anki na automatyczne przewijanie do miejsca, gdzie znajduje się odpowiedź, gdy naciśniej przycisk "pokaż odpowiedź" na długiej karcie (szczególnie przydatne na urządzeniach mobilnych z małymi ekranami). Jeśli nie chcesz, aby pozioma linia wyświetlała się na początku odpowiedzi, możesz użyć innego elementu HTML takiego jak akapit lub komenda "div".

## Nowy wiersz

Szablony kart zachowują się jak strony internetowe, co oznaczą, że wymagana jest specjalna komenda, aby stworzyć nowy wiersz. Na przykład, jesli w szablonie napiszesz poniższy tekst:

    jeden
    dwa

W podglądzie karty zobaczysz:

    jeden dwa

Aby dodać nową linię, wystarczy, że pomiędzy dwoma słowami wstawiamy znacznik &lt;br&gt;, jak poniżej:

    jeden<br>
    dwa

Znacznik ten pochodzi z języka HTML i jest skrótem od angielskiego wyrażenia "(line) br(eak)" czyli "łamanie wiersza".

W ten sam sposób można wyświetlać pola notatki. Jeżeli chciałbyś, żeby jedno pole znajdowało sie zaraz pod drugim:

    {{Pole 1}}<br>
    {{Pole 2}}

## Tekst na mowę (Text to Speech - TTS)

Na funkcjonalność wymaga Anki 2.1.20, lub AnkiMobile 2.0.56. AnkiDroid obecnie nie obsługuje tej metody.

Aby Anki czytało pole Przód przykładowo w języki angielskim amerykańskim, możesz umiescić ponizszy tekst w szablonie karty.

    {{tts en_US:Przód}}

Na systemach Windows, MacOS i iOS Anki użyje wbudowanych plików głosowych. Na Linuksie nie ma wbudowanych głosów, ale moga one być udostępnione przez dodatki takie [jak ten](https://ankiweb.net/shared/info/391644525).

Aby zobaczyć listę dostepnych języków/głosów, umiesc poniższy tekst na szablonie karty:

    {{tts-voices:}}

Jeśli jest kilka dostępnych głosów dla danego języka możesz doprecyzować w liście, których głosów chcesz używać, a Anki odtworzy pierwszy dostepny głos. Przykład: 

    {{tts ja_JP voices=Apple_Otoya,Microsoft_Haruka:Field}}

Ta komenda sprawi, że Anki użyje głosu Otoya na urządzeniu Apple, a głosu Haruka na urządzniu Windows PC. 

Ustawienie innej  szybkości odtwarzania jest możliwe w niektórych wersjach TTS:

    {{tts fr_FR speed=0.8:SomeField}}

Umieszczanie informacji o szybkości i głosach nie jest wymagane, jednak trzeba umieścić kod języka.

Na Makach możesz dostosować dostepne głosy

- Otwórz "Preferencje systemowe"

- Kliknij na "Dostępność"

- Kliknij na "Mowa"

- Kliknij na oknienko przy "Głos systemowy" i wybierz "Dostosuj".

Niektóre głosy brzmią lepiej od innych, wiec możesz poeksperymentować, aby znaleźc ten, który ci odpowiada. Pamiętaj o tym, ze głos Siri moze być używany tlyko przez aplikacje Apple. Po zainstalowaniu nowych głosów musisz uruchomić Anki ponownie, aby nowe głowy stały się dostępne.

Na urządzeniach z systemem Windows, niektó®e głosy takie jak Cortana nie moga zostać wybrane ponieważ Microsoft nie udostępnian ich innym aplikacjom.

## Pola specjalne

Istnieje kilka rodzajów pól specjalnych, których możesz użyć w szablonie:

    Znacznik etykiety: {{Tags}}

    Znacznik typu notatki: {{Type}}

    Znacznik nazwy talii: {{Deck}}

    Znacznik podtalii karty: {{Subdeck}}

    Znacznik typu karty ("Przód", itp.): {{Card}}

    Znacznik zawartości przodu karty (poprawna tylko w szablonie tyłu karty): {{FrontSide}}

Znacznik zawartości przodu karty FrontSide nie skopiuje na jej tył nagrania audio. Jeśli chcesz mieć to samo nagranie na przodzie i tyle karty musisz je tam ręcznie dodać.

Tak jak z innymi polami, w polach specjalnych ważna jest wielkosć liter - musisz używac np. `{{Tags}}` zamiast `{{tags}}`.

## Pola "podpowiedzi"

It’s possible to add a field to the front or back of a card, but make it
hidden until you explicitly show it. We call this a 'hint field'. Before
adding a hint, please bear in mind that the easier you make it to answer
a question in Anki, the less likely you are to remember that question
when you encounter it in real life. Please have a read about the
'minimum information principle' on
<http://www.supermemo.com/articles/20rules.htm> before proceeding.

First, you’ll need to add a field to store the hint in if you have not
already. Please see the [fields](editing.md#customizing-fields) section if you’re not sure how
to do this.

Assuming you’ve created a field called MyField, you can tell Anki to
include it on the card but hide it by default by adding the following to
your template:

    {{hint:MyField}}

This will show a link labeled “show hint”; when you click it, the
content of the field will be displayed on the card. (If MyField is
empty, nothing will be shown.)

If you show the hint on the question and then reveal the answer, the
hint will be hidden again. If you want to have the hint always revealed
when the answer is shown, you will need to remove `{{FrontSide}}` from
your back template and manually add the fields you wish to appear.

It is not currently possible to use a hint field for audio — the audio
will play regardless of whether you’ve clicked on the hint link.

If you want to customize the appearance or behaviour, you’ll need to
implement the hint field yourself. We can not provide any support for
doing so, but the following code should get you started:

    {{#Back}}
    ﻿<a class=hint href="#"
    onclick="this.style.display='none';document.getElementById('hint4753594160').style.display='inline-block';return false;">
    Show Back</a><div id="hint4753594160" class=hint style="display: none">{{Back}}</div>
    {{/Back}}

## Dictionary Links

You can also use field replacement to create dictionary links. Imagine
you’re studying a language and your favourite online dictionary allows
you to search for text using a web URL like:

    http://example.com/search?q=myword

You could add an automatic link by doing the following in your template:

    {{Expression}}

    <a href="http://example.com/search?q={{Expression}}">check in dictionary</a>

The template above would allow you to search for each note’s expression
by clicking on the link while reviewing. There is a caveat however, so
please see the next section.

## HTML Stripping

Like templates, fields are stored in HTML. In the dictionary link
example above, if the expression contained the word "myword" without any
formatting, then the HTML would be the same: "myword". But when you
include formatting in your fields, extra HTML is included. If "myword"
was bolded for example, the actual HTML would be
"&lt;b&gt;myword&lt;/b&gt;".

This can present a problem for things like dictionary links. In the
above example, the dictionary link would end up being:

    <a href="http://example.com/search?q=<b>myword</b>">check in dictionary</a>

The extra characters in the link would likely confuse the dictionary
site, and you’re likely not to get any matches.

To solve this, Anki provides the ability to strip formatting from fields
when they are replaced. If you prefix a field name with text:, Anki will
not include any formatting. So a dictionary link that worked even with
formatted text would be:

    <a href="http://example.com/search?q={{text:Expression}}">check in dictionary</a>

## Right To Left Text

If you’re using a language that reads from right to left, you’ll need
to adjust the template like so:

    <div dir=rtl>{{FieldThatHasRTLTextInIt}}</div>

## Media & LaTeX

Anki does not scan templates for media references, because it is slow to
do so. This has implications for including media on the template.

### Static Sounds/Images {docsify-ignore}

If you wish to include images or sounds on your cards that are the same
for every card (eg, a company logo at the top of each card):

1.  Rename the file so it starts with an underscore, eg "\_logo.jpg".
    The underscore tells Anki that the file is used by the template and
    it should be exported when sharing the deck.

2.  Add a reference to the media on your front or back template, like:

<!-- -->

    <img src="_logo.jpg">

### Field References {docsify-ignore}

Media references to fields are not supported. They may or may not display
during review, and will not work when checking for unused media,
importing/exporting, and so on. Examples that won’t work:

    <img src="{{Expression}}.jpg">

    [sound:{{Word}}]

    [latex]{{Field 1}}[/latex]

Instead, you should include the media references in the field. Please
see the importing section for more information.

## Checking Your Answer

You can watch [a video about this
feature](http://www.youtube.com/watch?v=5tYObQ3ocrw&yt:cc=on) on
YouTube.

The easiest way to check your answer is to click "Basic" at the top
left of the card adding screen, and select "Basic (type in the answer)".

If you have downloaded a shared deck and would like to type in the answer
with it, you can modify its card template. If it has a template like:

    {{Native Word}}

    {{FrontSide}}

    <hr id=answer>

    {{Foreign Word}}

To type in the foreign word and check if you are correct, you need to
edit your front template so that it looks like this:

    {{Native Word}}
    {{type:Foreign Word}}

Note that we have added `type:` in front of the field we want to
compare. Since FrontSide is on the back of the card, the type answer box
will appear on the back as well.

When reviewing, Anki will display a text box where you can type in the
answer, and upon hitting enter or showing the answer, Anki will show you
which parts you got right and which parts you got wrong. The text box’s
font size will be the size you configured for that field (via the
“Fields” button when editing).

This feature does not change how the cards are answered, so it’s still
up to you to decide how well you remembered or not.

Only one typing comparison can be used on a card. If you add the above
text multiple times, it will not work. It also only supports a single
line, so it is not useful for comparing against a field that is
comprised on multiple lines.

Anki uses a monospaced font for the answer comparison so that the
“provided” and “correct” sections line up. If you wish to override the
font for the answer comparison, you can put the following at the bottom
of your styling section:

    code#typeans { font-family: "myfontname"; }

Which will affect the following HTML for the answer comparison:

    <code id=typeans>...</code>

Advanced users can override the default type-answer colours with the css
classes 'typeGood', 'typeBad' and 'typeMissed'. AnkiMobile supports
'typeGood' and 'typeBad', but not 'typeMissed'.

If you wish to override the size of the typing box and don’t want to
change the font in the Fields dialog, you can override the default
inline style using `!important`, like so:

    #typeans { font-size: 50px !important; }

It is also possible to type in the answer for cloze deletion cards. To
do this, add `{{type:cloze:Text}}` to both the front and back
template, so the back looks something like this:

    {{cloze:Text}}
    {{type:cloze:Text}}
    {{Extra}}

Note that since the cloze type does not use FrontSide, this must be
added to both sides on a cloze note type.

If there are multiple sections elided, you can separate the answers in
the text box with a comma.

Type answer boxes will not appear in the ["preview"
dialog](templates/intro.md) in the browser. When you review or look at
the preview in the card types window, they will display.
