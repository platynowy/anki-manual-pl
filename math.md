# Matematyka i symbole

## MathJax

[MathJax](https://www.mathjax.org) to nowoczesny, oparty na przeglądarce 
system składu tekstu, przydatny przy równaniach matematycznych i chemicznych. Nie wymaga instalacji żadnego dodatkowego programu, przez co jest łatwy w użyciu i polecany dla większości użytkowników.

MathJax dostepny jest od razu po instalacjii Anki 2.1+, AnkiMobile, i
AnkiDroid 2.9+.

Aby go wypróbować:

1.  Wpisz poniższy tekst w polu:

        \sqrt{x}

2.  Zaznacz ten tekst.

3.  Klknij w edytorze przycisk pierwszy po prawej i wybierz z menu "liniowy MathJax". Anki zmieni tekst, przez co będzie wyglądał on tak:

        \(\sqrt{x}\)

4.  Jeśli naciśniesz przycisk Karty…​, zobaczysz podgląd tego, jak równanie pojawi się na karcie podczas nauki.

Anki oczekuje użycie zawartości MathJax w formacie TeX. Jeśli nie jesteś zaznajomiony z formatowaniem TeX, zobacz [tę ściągawkę](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference). Zauważ, że punkt 2 nie ma zastosowania w Anki - program używa `\(` oraz `\)` dla równań liniowych i `\[` i `\]` dla równań wyświetlanych.

Jeśli chcesz wstawiać nowe linie w MathJax, używaj Shift+Enter zamiast samego klawisza Enter (przejście do nowej linii tylko enterem spowoduje, że nowa linia uniemożliwi poprawne działanie MathJax).

W Anki można używać mhchem, aby renderować równania chemiczne. Zobacz w linku rozdział "chemical equations" jak i następne rozdziały, aby dowiedzieć się więcej:<https://mhchem.github.io/MathJax-mhchem/>

## LaTeX 

LaTeX to oprogramowanie do składu tekstu, przydatne do wprowadzania równań, na przykład matematycznych, chemicznych lub notatcji muzycznej. Anki oferuje w pewnym stopniu wsparcie dla LaTeX, przez co możesz wpisywać kod LaTeX w swoich kartach. Kiedy powtarzasz karte Anki odczyta LaTeX i pokaże wygenerowany obraz.

Jeśli chodzi o LaTeX, trzeba się bardziej wysilić przy jego konfigurowaniu, a obrazy mogą być generowane tylko na komputerowej wersji Anki. Jednak jeśli już raz zostaną one wygenerowane, mogą być pokazywane również na urządzeniach mobilnych. LaTeX jest o wiele bardziej skomplikowany, dlatego jest polecany tylko tym  użytkownikom, którym nie wystarczają funkcjonalności MathJax. 

**Instrukcja użytkowania LaTeX w Anki nie jest obecnie dostępna w języku polskim.**

### Oczekiwana wiedza (język angielski)

Anki’s LaTeX support is not turn-key: it is assumed that you know how to
use LaTeX already, and that you have it installed. If you have no
experience with LaTeX, please consult one of the many guides available
on the internet. If you are having trouble with markup, please ask on a
LaTeX forum.

To install LaTeX, on Windows use MiKTeX; on OSX use MacTex, and on Linux
use your distro’s package manager. Dvipng must also be installed.

On Windows, go to Settings in MikTek’s maintenance window, and make sure
"Install missing packages on the fly" is set to "No", not to "Ask me
first". If you continue to have difficulties, one user reported that
running Anki as an administrator until all the packages were fetched
helped.

On OSX, LaTeX has only been tested with MacTex and BasicTex. If you use
BasicTex, you need to install dvipng separately, with the following
command:

    sudo tlmgr update --self; sudo tlmgr install dvipng

The command may not be on the path, so you may need to provide the full
path, eg /usr/local/texlive/2014basic/bin/x86_64-darwin/tlmgr.

If you are not using the above LaTeX packages, you will need to use the
"edit LaTeX" add-on to specify the full path to latex and dvipng.

### AnkiWeb/urządzenia mobilne (język angielski)

When you review a card with LaTeX on it, Anki will generate an image for
that LaTeX and place the image in your collection’s media folder for
future use. The web & mobile clients will display these images if they
already exist, but can not generate the images on their own.

To avoid having to review all your cards at least once before you can
study on the other clients, Anki can generate the images in bulk for
you. To generate all the images, please go to Tools&gt;Check Media.
After that, syncing should upload the generated media to AnkiWeb and the
other clients.

### Przykład (język angielski)

The most general way to input LaTeX content is to surround it with
\[latex\]\[/latex\] tags. There’s a shortcut button for this documented
in the [editor](editing.md) section.

\[latex\] tags must be used inside a field - placing them in the card
template will [cause problems](templates/fields.md).

For example, entering the following on the front of an Anki flashcard:

    Does [latex]\begin{math}\sum_{k = 1}^{\infty}\frac{1}{k}\end{math}[/latex] converge?

will produce this when the flashcard is viewed:

![convergence question](math/convergence_question.png)

The formula in the example above is called a 'text formula', because it
is displayed right within the non-mathematical text. In contrast, the
following example shows a 'displayed formula':

    Does the sum below converge?

    [latex]\begin{displaymath}\sum_{k = 1}^{\infty}\frac{1}{k}\end{displaymath}[/latex]

![convergence question 2](math/convergence_question_2.png)

'Text formulas' and 'display formulas' are the most common type of LaTeX
expressions, so Anki provides abbreviated versions of them. Expressions
of the form:

    [latex]\begin{math}...\end{math}[/latex]

can be shortened to

    [$]...[/$]

and expressions of the form

    [latex]\begin{displaymath}...\end{displaymath}[/latex]

can be shortened to

    [$$]...[/$$]

For example, the two LaTeX snippets shown before are equivalent to

    Does [$]\sum_{k = 1}^{\infty}\frac{1}{k}[/$] converge?

and

    Does the sum below converge?

    [$$]\sum_{k = 1}^{\infty}\frac{1}{k}[/$$]

respectively.

### Pakiety (język angielski)

Anki allows you to customize the LaTeX preamble so you can import custom
packages for chemistry, music and so on. For example, imagine you find
an example file for chemtex on the internet:

    \documentclass[a4paper,12pt]{report}
    \usepackage{chemtex}
    \begin{document}

    \initial
    \begin{figure}[h]\centering
    \parbox{.3\textwidth}{\ethene{H}{H$_3$C}{CH$_3$}{Br}}
    \hfil
    \parbox{.3\textwidth}{\cbranch{H}{S}{H}{S}{C}{S}{}{S}{H}
      \xi=-200 \cright{}{Q}{C}{D}{O}{S}{OH}}
    \hfil
    \parbox{.3\textwidth}{\hetisix{Q}{Q}{Q}{Q}{Q}{Q}{O}{Q}{O}
      \xi=-171 \fuseup{Q}{Q}{Q}{Q}{D}{Q}{D}{Q}{D}}
    \caption{Chemie mit {\tt CHEMTEX}\label{a1}}
    \end{figure}

    \end{document}

Firstly, follow the documentation of the package and MiKTeX/MacTex in
order to install the package. To check the package is working, you’ll
want to put code like the above into a .latex file and test you can
compile it from the command line. Once you’ve confirmed that the package
is available and working, we can integrate it with Anki.

To use the package with Anki, click "Add" in the main window, then click
the note type selection button. Click the "Manage" button, then select
the note type you plan to use and click "Options". The LaTeX header and
footer are shown. The header will look something like:

    \documentclass[12pt]{article}
    \special{papersize=3in,5in}
    \usepackage{amssymb,amsmath}
    \pagestyle{empty}
    \setlength{\parindent}{0in}
    \begin{document}

To use chemtex, you’d add the usepackage line in the earlier example, so
it looks like:

    \documentclass[12pt]{article}
    \special{papersize=3in,5in}
    \usepackage{amssymb,amsmath}
    \usepackage{chemtex}
    \pagestyle{empty}
    \setlength{\parindent}{0in}
    \begin{document}

After that, you should be able to include lines like the following in
your Anki cards:

    [latex]\ethene{H}{H$_3$C}{CH$_3$}{Br}[/latex]

### Konflikty z szablonami (język angielski)

As of Anki 2.1.20 / AnkiMobile 2.0.56, this workaround is no longer
required, as `{{field}}` text inside fields no longer causes problems.
If you need to support AnkiDroid or older Anki versions and want to keep
using this syntax, please make sure you place the `{{=<% %>=}}` string
at the very top of your front and back template, as recent Anki versions
will not recognize it anywhere but the start.

For older versions:

It’s not uncommon for {{ and }} to pop up in LaTeX code when writing
mathematical equations. To ensure that your LaTeX equations don’t
conflict with Anki’s field replacements, it’s possible to change the
separator to something else.

For example, if you have a template:

    {{latex field}}

Changing it to the following will make it unlikely that the LaTeX will
conflict:

    {{=<% %>=}}
    <%latex field%>

### Konflikty z lukami (język angielski)

Cloze deletions are terminated with `}}`, which can conflict with a `}}`
appearing in your LaTeX. To prevent LaTeX from being interpreted as a closing
cloze marker, you can put a space between any double closing braces that do not
indicate the end of the cloze, so

    {{c1::[$]\frac{foo}{\frac{bar}{baz}}[/$] blah blah blah.}}

will not work, but

    {{c1::[$]\frac{foo}{\frac{bar}{baz} }[/$] blah blah blah.}}

will (and LaTeX ignores spaces in math mode, so your equation will
render the same). If you want to avoid adding the extra space into the
rendered text (for example, when you are making Cloze cards for learning
programming languages), another option is to use a HTML comment when
editing the card in HTML mode:

    {{c1::[$]\frac{foo}{\frac{bar}{baz}<!-- -->}[/$] blah blah blah.}}

You may use either workaround if you need to use the `::` character
sequence within the Cloze-deleted text. The first card generated for the
following note text will read `[type] in C++ is a type-safe union`:

    {{c1::std:<!-- -->:variant::~type~}} in C++ is a {{c2::type-safe union}}

### Niebezpieczne polecenia (język angielski)

Anki prohibits certain commands like \\input or \\def from being used on
cards or in templates, because allowing them could allow malicious
shared decks to damage your system. (To be on the safe side, these
commands are prohibited even in comments, so if you’re getting this
error but don’t think you’ve used one, please double-check any comments
you have in your headers, templates, and cards.) If you need to use
these commands, please add them to a system package and import that
package as described in the previous section. 
