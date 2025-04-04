## Rom-Seminar: Die `LaTeX`-Vorlage für die Teilnehmer (Stand 2025/04/02)

### Inhaltsverzeichnis

- [Worum geht es](file:///Users/ugroh/GitHub/AGFA-Rom-Teilnehmer/README.md#einstieg) 
- [Was wird genutzt](file:///Users/ugroh/GitHub/AGFA-Rom-Teilnehmer/README.md#latex)
- [Der Aufbau der Vorlage](file:///Users/ugroh/GitHub/AGFA-Rom-Teilnehmer/README.md#aufbau)
- [Ergänzende Literatur](file:///Users/ugroh/GitHub/AGFA-Rom-Teilnehmer/README.md#lit-latex)
- [Was ist in `preamble`](file:///Users/ugroh/GitHub/AGFA-Rom-Teilnehmer/README.md#preamble)
- [Aktualisierungen](file:///Users/ugroh/GitHub/AGFA-Rom-Teilnehmer/README.md#sonstiges)

<a name="einstieg"></a>

### Worum geht es

Diese Vorlage dient als Grundlage für die Beiträge im Rahmen des Rom-Seminars. Die Basis ist KOMA-Script, da es auf den deutschen Sprachraum und dessen Eigenheiten abgestimmt ist. Alle für die Erstellung und Integration des Rom-Buches benötigten Pakete sind in der Datei `./preamble/Rom-Beitrag.sty` enthalten. Bitte daher in dieser und in den weiteren Dateien des Unterverzeichnisses `./preamble/...` **keine** eigenständigen Änderungen vornehmen. Wenn etwas zusätzlich gebraucht wird, dann dieses bitte mir, [ulgr@math.uni-tuebingen.de](mailto:ulgr@math.uni-tuebingen.de), mitteilen.

Ein Beispiel, das auch eine Übersicht über die wichtigsten typografischen Regeln enthält: [beispiel/Rom-ulgr.pdf](https://github.com/ugroh/AGFA-Rom-Teilnehmer/blob/main/beispiel/Rom-ulgr.pdf) – bitte die enthalten Anregeungen nutzen.. 

Die Vorlage kann sowohl lokal auf einem eigenen Rechner genutzt werden als auch auf [*Overleaf*](https://www.overleaf.com/). Für beides muss man sich die Vorlage als ein `ZIP`-File herunterladen. Dazu geht man in GitHub auf den grünen, mit **Code** bezeichneten Schalter, geht auf **Local** und öffnet diesen. Der Rest sollte klar sein: Als `ZIP`-File herunterladen und durch Entpacken in einem geeigneten Unterverzeichnis auf dem PC installieren. 

Wer das System [*Overleaf*](https://www.overleaf.com/) nutzt, muss dann dieses `ZIP`-File in Overleaf als neues Projekt installieren. Die Vorlage habe ich dort getestet und es hat alles funktioniert. Und bitte beachten: In dem Menüpunkt `Recompile` den Unterpunkt `Stop on first error` auswählen. Dann stoppt Overleaf bei einem Fehler und es wird angezeigt, in welcher Zeile sich dieser befindet. Um die Fehlersuche zu erleichtern, bitte jeden `neuen` Satz auf einer `neuen` Zeile beginnen, d.h. den Text nicht als Fließtext schreiben. Für die Endredaktion ist ein fehlerfreies Manuskript erforderlich.

Wer `LaTeX` lokal verwenden will: Bitte entweder [MacTeX](https://www.tug.org/mactex/) nutzen, wenn man einen Apple-PC hat oder die aktuelle [TeX Live-Version](https://tug.org/texlive/) für Linux oder Windows. Die Installation ist auf den jeweiligen Webseiten beschrieben (siehe auch https://www.latex-project.org/get/). 

Zu guter Letzt noch ein Hinweis: Der Beitrag sollte frei von Fehlern sein – Rechtschreibfehler, Tippfehler, sprachliche Fehler u.a. Um dieses zu erreichen, empfehle ich das [LanguageTool](https://languagetool.org/de). Mein Tipp: Den Text abschnittsweise via Cut-and-Paste kopieren, prüfen lassen und dann mittels der angebotenen Kopierfunktion zurückkopieren. 

<a name="latex"></a>

### Was wird genutzt

Die Basis ist das `LaTeX`⁣-System, und man sollte sich, zumindest rudimentär, etwas damit auskennen. LaTeX ist ein sog. [WYSIWYM](https://de.wikipedia.org/wiki/WYSIWYM)-System und kein Textverarbeitungsprogramm, mit dem man einen Fließtext schreibt, wie bei Word. Es basiert auf [TeX](https://de.wikipedia.org/wiki/TeX), das ein Programm ist, mithilfe dessen man Texte, die auf einem Computer geschrieben wurden, in eine druckbare Version umwandelt. Dies sollte man bei der Erstellung eines Textes berücksichtigen, d.h. man *programmiert* den Inhalt seines Textes, um ein *schönes* Ergebnis zu bekommen. 

Daher muss man die Möglichkeiten und Grenzen des Systems lernen und berücksichtigen. Meine Empfehlungen für das Lernen und ein erstes Verstehen:

- [*lshort*](https://ctan.org/pkg/lshort-german): Eine übersichtliche Einführung in LaTeX mit sinnvollen Tipps und einer kleinen Übersicht zur Entwicklung von TeX und LaTeX.

Weitere Literatur zur Erstellung eines Beitrags findet man in dem Abschnitt [ergänzende Literatur](file:///Users/ugroh/GitHub/AGFA-Rom-Teilnehmer/README.md#lit-latex). Und bitte unbedingt in die _Zehn Tipps_ reinsehen. Wer mehr wissen will: es lohnt, einen Blick auf  [https://tex.social](https://tex.social) zu werfen.

<a name="aufbau"></a> 

### Der Aufbau der Vorlage

Um die verschiedenen Beiträge bei der Erstellung des Buches zum Seminar unterscheiden zu können, ist folgende Namensgebung **unbedingt** erforderlich: Das `abcd` wird abgeändert in die in der AGFA üblichen Abkürzung für die E-Mail-Adresse. Ist also der Name des Referenten `Ulrich Groh`, so ist `abcd = ulgr`. Sind es mehrere Autoren, so bitte den Namen dafür nehmen, der alphabetisch an **erster** Stelle kommt. Bitte **alle** Dateien, die dieses `abcd` enthalten entsprechend ändern, bevor mir diese Dateien zugeschickt werden.

Beim Installieren wird das Hauptverzeichnis `Rom-Seminar-Teilnehmer` angelegt. Dieses enthält folgende Dateien:  

- `README.md` und `README.pdf`: Diese enthält einige Erläuterungen zur Installation und was es sonst noch gibt.
- `Rom-abcd.tex`: Diese ist die Master-Datei für die Erstellung des eigenen Beitrags. Diese Datei nutzt man zur Erstellung und zum Testen des eigenen Beitrags. Und bitte: An der Struktur dieser Datei nichts ändern, es sei denn, man muss einiges ergänzen – dafür aber eine Information an mich.  
- `Rom-abcd.pdf`: Die kompilierte Version des Beispiels `Rom-abcd.tex`, die wiederum die Datei `./content-abcd/Beitrag-abcd.tex` aufruft. Diese Datei ist die Basis für den eigenen Beitrag. Und auch hier gilt: An der Struktur dieser Datei nichts ändern.
- `Rom-Beamer.tex`: Eine Beamer-Vorlage zur Erstellung der eigenen Präsentation. Diese ist bewusst schlicht gehalten, da viel Farbe nichts mit der Qualität eines Beitrags zu tun hat.

Des Weiteren finden sich die Unterverzeichnisse: 

- **`beispiel`**: Hier findet sich mein Beitrag zu einem virtuellen Rom-Seminar als `Rom-ulgr.pdf`. In diesem finden sich Tipps zu `LaTeX`und alles zur Nutzung der Vorlage.

- **`LaTeX-Tipps`**: Hier finden sich meine LaTeX-Tipps, insbesondere für die Literaturverwaltung und zu den Querverweisen. Diese ersetzen aber nicht die Nutzung weitergehender Literatur zu `LaTeX`.

- **`bib-abcd`**: Hier findet dich die Datei mit der benutzten Literatur, `Biblio-abcd.bib`. Der Aufbau dieser genügt den Regeln für die Nutzung in `LaTeX`. Eine kleine Anleitung zur Erstellung eines eigenen Literaturverzeichnisses dazu findet man in den LaTeX-Tipps. Ich empfehle jedem, diesen Tipp anzusehen. Und noch etwas: Nutzt man alles nicht auf `Overleaf`, dann muss man im Editor einstellen, dass man `biber` für die Erstellung des Literaturverzeichnisses nutzt. Wie man diese `bib`-Datei pflegt, ist in den Tipps beschrieben. 

- **`content-abcd`**: In diesem Unterverzeichnis finden sich alle genutzten Dateien des Vortrags, also `Beitrag-abcd.tex` für den Beitrag, eventuelle Bilder etc. Hierzu gehören auch die zusätzlichen eigenen Definitionen, die man eventuell benötigt. Bitte diese in die Datei `Defn-abcd.tex` schreiben, dabei aber darauf achten, dass man nichts definiert, was bereits vorhanden ist oder Fehler erzeugt. Diese Datei ist bereits mittels `\input{Defn-abcd}` eingebunden. 

- Im Stammverzeichnis befindet sich die Datei `Rom-abcd.tex`, die für die Erstellung des eigenen Beitrags verwendet wird. Also: Schreiben des Textes erfolgt in die Datei `./content-abcd/Beitrag-abcd.tex`. Diese ergibt dann nach dem Setzen mit der Datei `Rom-abcd.tex` den Beitrag als `PDF`-Datei. Die Datei `Beitrag-abcd.tex` enthält als erste Zeile  

  ```
  % !TEX root = ../Rom-abcd.tex  
  ```

Dadurch ist es möglich, diese Datei direkt mit `LaTeX` zu kompilieren, da dann die Stammdatei aufgerufen wird. Dies geht mit [TeXShop](https://pages.uoregon.edu/koch/texshop/obtaining.html) als Tool auf Apple OS oder entsprechend auch mit [TeXworks](https://tug.org/texworks/), der Linux und Windows unterstützt. Meine generelle Empfehlung ist es, diesen Editor für die TeX-Welt zu nutzen, wenn man keinen Apple-Computer hat.  

**Wichtig**: Bitte in dieser Datei die entsprechenden Ergänzungen vornehmen bei 

```
\renewcommand{\LongTitel}{Langform des Titels für die Überschrift des Beitrags}
\renewcommand{\AutorenBeitrag}{Autor1, Autor2 \& Autor3}
\renewcommand{\ShortTitelTOC}{Kurzform des Titels für das Inhaltsverzeichnis}
\renewcommand{\ShortTitelKopfzeile}{Kurzform des Titels für die Kopfzeile}
```

Alles Weitere wird dann von `TeX` erledigt. Weiter unten dann die Angabe zum obligatorischen Bild und wer noch einen klugen Spruch hat. Ein Beispiel dazu: Siehe `Betrag-abcd.pdf` und `./content-abcd/Beitrag-abcd.tex`. 

- **`preamble`**: Hier befinden sich alle Dateien, die zur Erstellung des Dokuments mithilfe von LaTeX erforderlich sind. An diesen Dateien bitte **nichts** verändern. Sollte mal etwas nicht funktionieren oder spezielle Wünsche vorhanden sein, so bitte ich darum, mir dieses mitzuteilen. In dem Abschnitt [Was ist in der `preamble`](file:///Users/ugroh/GitHub/AGFA-Rom-Teilnehmer/README.md#preamble) ist dieses alles detailliert beschrieben. 

Wenn alles bearbeitet ist, bitte das Verzeichnis **`Rom-Seminar-Teilnehmer`** als `zip`-Datei mir zu schicken (vorher aber `abcd` anpassen) oder, wer Overleaf nutzt, mich als Teilnehmer zu benennen. 

<a name="lit-latex"></a> 

### Ergänzende Literatur

Weitere Literatur zur Erstellung eines Beitrags für das Rom-Seminar – und nicht nur für diesen.

- Wer sich intensiver mit `LaTeX`beschäftigen will: [H. Voss, *Einführung in LaTeX*](https://www.lehmanns.de/shop/mathematik-informatik/33589289-9783865417985-einfuehrung-in-latex) und wer `KOMA-Script`verstehen will: [M. Kohm, *KOMA-Script*](https://www.lehmanns.de/shop/mathematik-informatik/51375541-9783965430976-koma-script) als Buch oder man verwendet das Manual, das man auf [CTAN](https://ctan.mirror.norbert-ruehl.de/macros/latex/contrib/koma-script/doc/scrguide-de.pdf) findet.
- Da wir es mit einem Text auf Deutsch zu tun haben, sollten Rechtschreibung und die Zeichensetzung stimmen. Dabei hilft das [*LanguageTool*](https://languagetool.org/de) und [*IDS-Mannheim*](https://grammis.ids-mannheim.de/): Einfach den Text abschnittsweise in das `Langauge-Tool` kopieren, korrigieren und zurückkopieren. 
- Natürlich sind auch einige typografische Regeln zu beachten, etwa der Unterschied zwischen Bindestrich, Gedankenstrich und Minuszeichen: Dabei hilft das [*TypoLexikon*](https://www.typolexikon.de/) oder eventuelle meine Tipps.
- Für einen Einstieg in die Umsetzung mathematischer Formeln empfiehlt sich der [*AMS ShortMathGuide*](https://ctan.org/pkg/short-math-guide), der vollkommen ausreichend ist. Auch hier sind einige typografische Regeln zu beachten, die man unter dem Stichwort [*Formelsatz*](http://www.moritz-nadler.de/formelsatz.pdf) findet.
- Wer mehr verstehen oder lernen will – einfach mal auf [*Dante – Literatur und mehr*](https://www.dante.de/dante-e-v/literatur/) nachsehen. Ein schöner Artikel zu TeX findet man [*etwa hier*](https://www.ams.org/publications/authors/Communication_of_Mathematics_with_TEX.pdf).
- Regeln zur Verfassung eines mathematischen Artikels findet man bei [P. Halmos: _How to Write Mathematics](https://www2.cs.duke.edu/donaldlab/Teaching/add/2011/resources/halmos.pdf) und [D. Knuth: Mathematical Writing](https://jmlr.csail.mit.edu/reviewing-papers/knuth_mathematical_writing.pdf). Letzteres ist eine Vorlesung, die man auch auf  [YouTube](https://www.youtube.com/watch?v=mert0kmZvVM&list=PLABJEFgj0PWV22nvw3YKXvR_n1NB6fn5D) findet und an der auch [P. Halmos](https://www.youtube.com/watch?v=Cy_1JgYfKmE) beteiligt ist. 

<a name="preamble"></a> 

### Was ist in `preamble`

- **`Rom-Beitrag.sty`**: Dies ist das Hauptpaket, mithilfe dessen alle anderen Dateien, die zur Formatierung erforderlich sind, aufgerufen werden. Diese Datei wird mittels `\usepackage{Rom-Beitrag}` eingebunden (siehe hierzu  `Rom-abcd.tex`), 

- **`Rom-Abkuerzungen.sty`**: Hier finden sich die Abkürzungen für die richtige Schreibweise, etwa für d.h., 

- **`Rom-BibLaTeX.sty`**:  Diese Datei ist für die Darstellung der Referenzen im Literaturverzeichnis zuständig. Bitte darauf achten, dass man einen zusätzlichen Lauf benötigt – einmal mit `biber` und dann nochmals mit `latex`. Mithilfe von  

  ```
  % !TEX TS-program = pdflatexmk
  ```

in der ersten Zeile ist dies sichergestellt (`magic command line`). Das zugehörige `bib`-File findet sich in `content-abcd/bib-abcd` und heißt `Biblio-abcd.bib`. In diese Datei werden die Referenzen eingetragen und gepflegt. 

Tipp hierzu: Auf einem Mac das Programm `BibDesk` nutzen. Ansonsten ist etwa [JabRef](https://www.jabref.org/) zu empfehlen. In meinen LaTeX-Tipps habe ich hierzu etwas zusammengestellt, das man im Unterverzeichnis `beispiel` findet – [LaTeX-Tipp5](https://github.com/ugroh/Rom-Seminar-Teilnehmer/tree/main/beispiel). Diesen Tipp kann man sich online ansehen oder herunterladen (kleines Download-Symbol rechts in der grauen Leiste). Wer Hilfe benötigt: Mail an mich. 

**Wichtig:** Bitte im Editor prüfen, ob `biber` als Tool für die Erstellung des Literaturverzeichnisses eingestellt ist. In Overleaf ist dies bereits der Fall.  

- **`Rom-Layout.sty`**:  Alles, was für das Layout zuständig ist. Dabei funktioniert `\section` und `\subsection` wie üblich. Meiner Meinung nach ist  `\subsubsection`  entbehrlich und es wird bei der Nutzung eine Nummer ausgegeben – kann man relativ gut nutzen, um etwas besser zu untergliedern. Auch sollen die erstgenannten Befehle mit ihrer *-Variante genutzt werden. Eine Nummerierung ist nicht erforderlich.
- **`Rom-Mathematik.sty`**: Enthält Definitionen, etwa `\N` für den Blackboard-Stil für die Darstellung der natürlichen Zahlen. Alle Definitionen habe ich separat zusammengestellt und die Übersicht findet sich auch in dem Unterverzeichnis `beispiel`. 
- **`Rom-Theorem.sty`**: Wie der Name schon sagt: In dieser Datei finden sich die Definitionen der mathematischen Umgebungen für Theoreme etc. Da gibt es zwei Varianten: Einmal nicht nummeriert, was ich für die Beiträge sinnvoll halte und die Möglichkeit, diese auch zu nummerieren. Alles Weitere in der oben erwähnten Übersicht.
- **`Rom-Pakete.tex`**:  Aus meiner Sicht nützliche Pakete, die die Möglichkeiten von LaTeX ergänzen. Wer mehr zu den Paketen wissen will, der kann einmal auf [ctan.org](https://ctan.org/) nach diesen suchen und sich das Manual ansehen, oder `texdoc name-des-pakets` am PC aufrufen oder mal H. Voss: *Einführung in LaTeX* nutzen. Wichtig: *Learning-by-Doing* ist dann angesagt. 

<a name="sonstiges"></a> 

### Aktualisierungen 

- (2025/04/02) `bib` nach `content-abcd`
- (2025/03/16) Kleinere Korrekturen
- (2024/12/07) Überarbeitung und _Zehn Tipps_ beigefügt.
- (2024/09/03) Korrektur in `Rom-BibLaTeX.sty`, damit bei der Eingabe von `date={JJJJ-MM-DD}` das Datum korrekt angezeigt wird, also etwa für `2024-09-03` dann `3. Sep. 2024`.
- (2024/08/29) Korrektur der Fußnoten – Bitte `Rom-Layout.sty` ersetzen. 
- (2024/08/27) Kleine Korrektur im `Biblio-abcd.bib` (`@url` war falsch, muss `@online` heißen) und an der Mustervorlage. 
- (2024/08/21) Korrektur von zwei Meldungen, die bei der Nutzung von Overleaf angezeigt werden und irritieren können. Bitte daher `preamble/Rom-Layout.sty` und `preamble/Rom-Beitrag.sty` austauschen.
- (2024/08/13) `Issues` und `Discussion` eingerichtet. Dieses findet sich in der grauen Querleiste. 
- (2024/07/19) Bei mehreren Autoren erscheint im Text nur der erste Name, die restlichen als `et al.`, also etwa `Engel et al.` Im Literaturverzeichnis dann aber alle, also `Engel, K. & Nagel, R.`
- (2024/07/18) Über `review`kann erreicht werden, dass im erzeugten PDF der Zeilenabstand verdoppelt ist. Dies erleichtert die schriftliche Bearbeitung und Korrektur des erzeugten PDFs. Für die finale Version bitte auskommentieren. Dazu das `Rom-Beitrag.sty` austauschen.
- (2024/06/17) `LuaLaTeX` funktioniert jetzt korrekt. Bitte auch hier darauf achten, dass man mehrere Kompilierungen benötigt. 
- Wünsche, etwaige Fehler etc. bitte an [ulgr@math.uni-tuebingen.de](mailto:ulgr@math.uni-tuebingen.de) melden.
