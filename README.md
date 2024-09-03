## Rom-Seminar: Die `LaTeX`-Vorlage für die Teilnehmer (Stand 2024/09/03)

### Inhaltsverzeichnis

* [Um was geht es](#einstieg). 
* [Was wird genutzt](#latex)
* [Der Aufbau der Vorlage](#aufbau)
* [Ergänzende Literatur](#lit-latex)
* [Was ist in `preamble`](#preamble)
* [Aktualisierungen](#sonstiges)


<a name="einstieg"></a>

### Um was geht es

Diese Vorlage dient als Grundlage für die Beiträge im Rahmen des Rom-Seminars. Basis ist KOMA-Script, da es auf den deutschen Sprachraum und dessen Eigenheiten abgestimmt ist. Alle für die Erstellung und Integration des Rom-Buches benötigten Pakete sind in der Datei `./preamble/Rom-Beitrag.sty` enthalten. Bitte daher in dieser und in den weiteren Dateien des Unterverzeichnisses `./preamble/...` **keine** eigenständigen Änderungen vornehmen. Wenn etwas zusätzlich gebraucht wird, dann dieses bitte mir, <ulgr@math.uni-tuebingen.de>, mitteilen.

Ein Beispiel, das auch eine Übersicht über die wichtigsten typografischen Regeln enthält: [Rom-ulgr.pdf](https://github.com/ugroh/Rom-Seminar-Teilnehmer/blob/main/Rom-ulgr.pdf). Bitte dieses lesen und die Anregungen beherzigen. 

Die Vorlage kann sowohl lokal auf einem eigenen Rechner genutzt werden als auch auf [_Overleaf_](https://www.overleaf.com). Für beides muss man sich die Vorlage als ein `ZIP`-File herunterladen. Dazu geht man auf den grünen, mit __Code__ bezeichneten Schalter, geht auf __Local__ und öffnet diesen. Der Rest sollte klar sein: Als `ZIP`-File herunterladen und durch Entpacken in einem geeigneten Unterverzeichnis auf dem PC installieren. 

Wer das System [_Overleaf_](https://www.overleaf.com) nutzt, muss dann dieses `ZIP`-File in Overleaf als neues Projekt installieren. Die Vorlage habe ich dort getestet und es hat alles funktioniert. Und bitte beachten: In dem Menüpunkt `Recompile` den Unterpunkt `Stop on first error` auswählen. Dann stoppt Overleaf bei einem Fehler und es wird angezeigt, in welcher Zeile sich dieser befindet. Um die Fehlersuche zu erleichtern, bitte jeden `neuen` Satz auf einer `neuen` Zeile beginnen, d.h. den Text nicht als Fließtext schreiben. Für die Endredaktion ist ein fehlerfreies Manuskript erforderlich.

Wer `LaTeX` lokal verwenden will: Bitte entweder [MaCTeX](https://www.tug.org/mactex/) nutzen, wenn man einen Apple-PC hat oder die aktuelle [TeX Live-Version](https://tug.org/texlive/) für Linux oder Windows. Die Installation ist auf den jeweiligen Webseiten beschrieben (siehe auch [https://www.latex-project.org/get/](https://www.latex-project.org/get/)). 

<a name="latex"></a>

### Was wird genutzt

Basis ist das `LaTeX`-System und man sollte sich, zumindest rudimentär, etwas damit auskennen. LaTeX ist ein sog. [WYSIWYM](https://de.wikipedia.org/wiki/WYSIWYM)-System und kein Textverarbeitungsprogramm, mit dem man einen Fließtext schreibt, wie bei Word. Es basiert auf [TeX](https://de.wikipedia.org/wiki/TeX), das ein Programm ist, mithilfe dessen man Texte, die auf einem Computer geschrieben wurden, in eine druckbare Version umwandelt. Dies sollte man bei der Erstellung eines Textes berücksichtigen, d.h. man _»programmiert«_ den Inhalt seines Textes, um ein _schönes_ Ergebnis zu bekommen. 

Daher muss man die Möglichkeiten und Grenzen des Systems lernen und berücksichtigen. Meine Empfehlungen für das Lernen und einem ersten Verstehen:

* [_lsshort_](https://ctan.org/pkg/lshort-german): Eine kleine, aber übersichtliche Einführung in LaTeX mit sinnvollen Tipps und einer kleinen Übersicht zur Entwicklung von TeX und LaTeX.

Weitere Literatur zur Erstellung eines Beitrags findet man in dem Abschnitt [Ergänzende Literatur](#lit-latex). 

<a name="aufbau"></a> 

### Der Aufbau der Vorlage

Um die verschiedenen Beiträge bei der Erstellung des Buches zum Seminar unterscheiden zu können, ist folgende Namensgebung **unbedingt** erforderlich: Das `abcd` wird abgeändert in die in der AGFA üblichen Abkürzung für die E-Mail-Adresse. Ist also der Name des Referenten  `Rainer Nagel`, so ist `abcd = rana` (sollte klar sein, wie es geht). Sind es mehrere Autoren, so bitte den Namen dafür nehmen, der alphabetisch an **erster** Stelle kommt.

Beim Installieren wird das Hauptverzeichnis __`Rom-Seminar-Teilnehmer`__ angelegt. Dieses enthält folgende Dateien:  

* `README.md` und `README.pdf`: Diese enthält einige Erläuterungen zur Installation und was es sonst noch gibt.
	
* `Rom-Muster.pdf` ist ein Beispiel und enthält die Details zu den Makros und einige Ratschläge. Diese Datei ist auch ein »Muster« für einen Beitrag.
	
* `Rom-abcd.tex` : Diese ist die Master-Datei für die Erstellung des eigenen Beitrags. Diese Datei benötigt man nur zur Erstellung des `PDF` des Beitrags. Und bitte: in dieser nichts ändern, es sei denn, man muss einiges ergänzen, was aber in dieser Datei explizit angegeben ist.  

* `Rom-Beamer.tex`: Eine Beamer-Vorlage zur Erstellung der eigenen Präsentation. Diese ist bewusst schlicht gehalten, da viel Farbe nichts mit der Qualität eines Beitrags zu tun hat.
	

Des Weiteren finden sich die Unterverzeichnisse:
	
* __`beispiel`__: Hier findet sich mein Beitrag zu einem virtuellen Rom-Seminar als `Rom-ulgr.pdf`. In diesem finden sich Tipps zu `LaTeX`und alles zur Nutzung der Vorlage.

* __`LaTeX-Tipps`__: Hier finden sich meine LaTeX-Tipps, insbesondere für die Literaturverwaltung und zu den Querverweisen. Diese ersetzen aber nicht die Nutzung weitergehender Literatur zu `LaTeX`.

* __`bib-abcd`__: Hier findet dich die Datei mit der benutzten Literatur, `Biblio-abcd.bib`. Der Aufbau dieser genügt den Regeln für die Nutzung in `LaTeX`. Eine kleine Anleitung zur Erstellung eines eigenen Literaturverzeichnisses dazu findet man in den LaTeX-Tipps. Ich empfehle jedem, sich diesen Tipp anzusehen. Und noch etwas: Nutzt man alles nicht auf `Overleaf`, dann muss man im Editor einstellen, dass man `biber` für die Erstellung des Literaturverzeichnisses nutzt. Wie man diese `bib`-Datei pflegt, ist in den Tipps beschrieben. 
	
* __`content-abcd`__: In diesem Unterverzeichnis finden sich alle genutzten Dateien des Vortrags, also `Beitrag-abcd.tex` für den Beitrag, eventuelle Bilder etc. Hierzu gehören auch die zusätzlichen eigenen Definitionen, die man eventuell benötigt. Bitte diese in die Datei `Defn-abcd.tex` schreiben, dabei aber darauf achten, dass man nichts definiert, was bereits vorhanden ist oder Fehler erzeugt. Diese Datei ist bereits mittels `\input{Defn-abcd}` eingebunden. 

* Im Stammverzeichnis befindet sich die Datei `Rom-abcd.tex`, die für die Erstellung des eigenen Beitrags verwendet wird. Also: Schreiben des Textes erfolgt in  die Datei `./content-abcd/Beitrag-abcd.tex`. Diese ergibt dann nach dem Setzen mit der Datei `Rom-abcd.tex` den Beitrag als `PDF`-Datei. Die Datei `Beitrag-abcd.tex` enthält als erste Zeile 
		
			% !TEX root = ../Rom-abcd.tex  
	

Dadurch ist es möglich, diese Datei direkt mit `LaTeX` zu kompilieren, da dann die Stammdatei aufgerufen wird. Dies geht mit [TeXShop](https://pages.uoregon.edu/koch/texshop/obtaining.html) als Tool auf Apple OS oder entsprechend auch mit [TeXworks](https://tug.org/texworks/), der Linux und Windows unterstützt. Meine generelle Empfehlung ist es, diesen Editor für die TeX-Welt zu nutzen, wenn man keinen Apple-Computer hat. 
	
**Wichtig**: Bitte in dieser Datei die entsprechenden Ergänzungen bei
	
		\renewcommand{\LongTitel}{Langform des Titels}
		\renewcommand{\ShortTitel}{Kurzform des Titel}
		\renewcommand{\AutorenBeitrag}{Autor1, Autor2 \& Autor3}

vornehmen. Alles Weitere wird dann von `TeX` erledigt. Weiter unten dann die Angabe zum obligatorischen Bild und wer noch einen klugen Spruch hat. Ein Beispiel dazu: Siehe `Betrag-abcd.pdf` und `./content-abcd/Beitrag-abcd.tex`. 

* __`preamble`__: Hier befinden sich alle Dateien, die zur Erstellung des Dokuments mithilfe von LaTeX erforderlich sind. An diesen Dateien bitte **nichts** verändern. Sollte mal etwas nicht funktionieren oder spezielle Wünsche vorhanden sein, so bitte ich darum, mir dieses mitzuteilen. In dem Abschnitt [Was ist in der `preamble`](#preamble) ist dieses alles detailliert beschrieben. 

Wen alles bearbeitet ist, bitte ich darum, das Verzeichnis __`Rom-Seminar-Teilnehmer`__ als `zip`-Datei mir zu schicken (vorher aber `abcd` anpassen) oder, wer Overleaf nutzt, mich als Teilnehmer zu benennen. 

<a name="lit-latex"></a> 

### Ergänzende Literatur

Weitere Literatur zur Erstellung eines Beitrags für das Rom-Seminar – und nicht nur für diesen.

* Wer sich intensiver mit `LaTeX`beschäftigen will: [H. Voss, _Einführung in LaTeX_](https://www.lehmanns.de/shop/mathematik-informatik/33589289-9783865417985-einfuehrung-in-latex) und wer `KOMA-Script`verstehen will: [M. Kohm, KOMA-Script](https://www.lehmanns.de/shop/mathematik-informatik/51375541-9783965430976-koma-script) als Buch oder man verwendet das Manual, das man auf [CTAN](https://ctan.mirror.norbert-ruehl.de/macros/latex/contrib/koma-script/doc/scrguide-de.pdf) findet.

* Da wir es mit einem Text auf Deutsch zu tun haben, sollte Rechtschreibung und die Zeichensetzung stimmen. Dabei hilft das [_LanguageTool_](https://languagetool.org/de) und [_IDS-Mannheim_](https://grammis.ids-mannheim.de): Einfach den Text Abschnittsweise in das `Langauge-Tool` kopieren, korrigieren und zurückkopieren. 

* Natürlich sind auch einige typografische Regeln zu beachten, etwa der Unterschied zwischen Bindestrich, Gedankenstrich und Minuszeichen:  Dabei hilft das [_TypoLexikon._](https://www.typolexikon.de bzw. in meinen Tipps.

* Für einen Einstieg in die Umsetzung mathematischer Formeln empfiehlt sich der [_AMS ShortMathGuide_](https://ctan.org/pkg/short-math-guide), der vollkommen ausreichend ist. Auch hier sind einige typografische Regeln zu beachten, die man unter dem Stichwort [_Formelsatz_](http://www.moritz-nadler.de/formelsatz.pdf) findet.

* Wer mehr verstehen oder lernen will – einfach mal auf [_Dante – Literatur und mehr_](https://www.dante.de/dante-e-v/literatur/) nachsehen. Ein schöner Artikel zu TeX findet man  [_etwa hier_](https://www.ams.org/publications/authors/Communication_of_Mathematics_with_TEX.pdf).

* Regeln zur Verfassung eines mathematischen Artikels findet man bei [P. Halmos: _How to Write Mathematics](https://www2.cs.duke.edu/donaldlab/Teaching/add/2011/resources/halmos.pdf) und [D. Knuth: Mathematical Writing](https://jmlr.csail.mit.edu/reviewing-papers/knuth_mathematical_writing.pdf). Letzteres ist eine Vorlesung, die man auch auf  [YouTube](https://www.youtube.com/watch?v=mert0kmZvVM&list=PLABJEFgj0PWV22nvw3YKXvR_n1NB6fn5D) findet und an der auch [P. Halmos](https://www.youtube.com/watch?v=Cy_1JgYfKmE) beteiligt ist. 

<a name="preamble"></a> 

### Was ist in `preamble`

* __`Rom-Beitrag.sty`__: Dies ist das Hauptpaket, mithilfe dessen alle anderen Dateien, die zur Formatierung erforderlich sind, aufgerufen werden. Diese Datei wird mittels `\usepackage{Rom-Beitrag}` eingebunden (siehe hierzu  `Rom-abcd.tex`), 

*  __`Rom-Abkuerzungen.sty`__: Hier finden sich die Abkürzungen für die richtige Schreibweise etwa für d.h., 
	
*  __`Rom-BibLaTeX.sty`__:  Diese Datei ist für die Darstellung der Referenzen im Literaturverzeichnis zuständig. Bitte darauf achten, dass man einen zusätzlichen Lauf benötigt – einmal mit `biber` und dann nochmals mit `latex`. Mithilfe von 
		
				% !TEX TS-program = pdflatexmk
	

in der ersten Zeile ist dies sichergestellt (`magic command line`). Das zugehörige `bib`-File findet sich in `content-abcd/bib-abcd` und heißt `Biblio-abcd.bib`. In diese Datei werden die Referenzen eingetragen und gepflegt. Tipp hierzu: Auf einem Mac das Programm `BibDesk` nutzen. Ansonsten ist etwa [JabRef](https://www.jabref.org) zu empfehlen. In meinen LaTeX-Tipps habe ich hierzu etwas zusammengestellt, dass man im Unterverzeichnis `beispiel` findet – [LasTeX-Tipp5](https://github.com/ugroh/Rom-Seminar-Teilnehmer/tree/main/beispiel). Diesen Tipp kann man sich online ansehen oder herunterladen (kleines Download-Symbol rechts in der grauen Leiste). Wer Hilfe benötigt: Mail an mich. 

**Wichtig:** Bitte im Editor prüfen, ob als `biber` als Tool für die Erstellung des Literaturverzeichnisses eingestellt ist. In Overleaf ist dies bereits der Fall. 
	
*  __`Rom-Layout.sty`__:  Alles, was für das Layout zuständig ist. Dabei funktioniert `\section` und `\subsection` wie üblich. Meiner Meinung nach ist  `\subsubsection` entbehrlich und es wird bei der Nutzung eine Nummer ausgegeben – kann man relativ gut nutzen, um etwas besser zu untergliedern. Auch sollen die erstgenannten Befehle mit ihrer *-Variante genutzt werden. Eine Nummerierung ist nicht erforderlich.
	
*  __`Rom-Mathematik.sty`__: Enthält Definitionen, etwa `\N` für den Blackboard-Stil für die Darstellung der natürlichen Zahlen. Alle Definitionen habe ich separat zusammengestellt und die Übersicht findet sich auch in dem Unterverzeichnis `beispiel`.
	
*  __`Rom-Theorem.sty`__: Wie der Name schon sagt: In dieser Datei finden sich die Definitionen der mathematischen Umgebungen für Theoreme etc. Da gibt es zwei Varianten: Einmal nicht nummeriert, was ich für die Beiträge sinnvoll halte und die Möglichkeit, diese auch zu nummerieren. Alles Weitere in der oben erwähnten Übersicht.
	
*  __`Rom-Pakete.tex`__:  Aus meiner Sicht nützliche Pakete, die die Möglichkeiten von LaTeX ergänzen. Wer mehr zu den Paketen wissen will, der kann einmal auf [ctan.org](https://ctan.org) nach diesen suchen und sich das Manual ansehen, oder `texdoc name-des-pakets` am PC aufrufen oder mal H. Voss: _Einführung in LaTeX_ nutzen. Wichtig: _Learning-by-Doing_ ist dann angesagt. 

<a name="sonstiges"></a> 

### Aktualisierungen 

* (2028/09/03) Korrektur in `Rom-BibLaTeX.sty`, damit bei der Eingabe von `date={JJJJ-MM-DD}` das Datum korrekt angezeigt wird, also etwa für `2024-09-03` dann `3. Sep. 2024`.

* (2028/08/29) Korrektur der Fußnoten: Klammern im Text waren unterschiedlich. Bitte `Rom-Layout.sty` ersetzen. 

* (2028/08/27) Kleine Korrektur im `Biblio-abcd.bib` (`@url` war falsch, muss `@online` heißen) und an der Mustervorlage. 

* (2024/08/21) Korrektur von zwei Meldungen, die bei der Nutzung von Overleaf angezeigt werden und irritieren können. Bitte daher `preamble/Rom-Layout.sty` und `preamble/Rom-Beitrag.sty` austauschen.

* (2024/08/13) `Issues` und `Discussion` eingerichtet. Dieses findet sich in der grauen Querleiste. 

* (2024/07/19) Bei mehreren Autoren erscheint im Text nur der erste Name, die restlichen als `et al.`, also etwa `Engel et al.` Im Literaturverzeichnis dann aber alle, also `Engel, K. & Nagel, R.`

* (2024/07/18) Über `review`kann erreicht werden, dass im erzeugten PDF der Zeilenabstand verdoppelt ist. Dies erleichtert die schriftliche Bearbeitung und Korrektur des erzeugten PDFs. Für die finale Version bitte auskommentieren. Dazu das `Rom-Beitrag.sty` austauschen.

* (2024/06/17) `LuaLaTeX` funktioniert jetzt korrekt. Bitte auch hier darauf achten, dass man mehrere Kompilierungen benötigt. 

* Wünsche, etwaige Fehler etc. bitte an <ulgr@math.uni-tuebingen.de> melden.



