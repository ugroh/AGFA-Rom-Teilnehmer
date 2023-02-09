## AGFA-Rom Vorlage (Stand 2023/02/02)

Dies ist die Vorlage für die Beiträge im Rahmen des Rom-Seminars. Die Basis hierfür ist [KOMA-Script](https://www.ctan.org/pkg/koma-script), da dieses Paket auf den deutschen Sprachraum und dessen Eigenheiten abgestimmt ist. Alle notwendigen Definition sind in der Datei `Rom-Beitrag.sty` enthalten bzw. diese ruft weitere Dateien auf. 

Die Vorlage findet man auf GitHub unter [_ugroh/AGFA-Rom-Teilnehmer_](https://github.com/ugroh/AGFA-Rom-Teilnehmer) und man kann sich dieses als ein ZIP-File herunterladen. Dazu geht man auf den grünen, mit __Code__ bezeichneten Schalter und öffnet diesen. Der Rest sollte klar sein: Als ZIP-File herunterladen und durch Entpacken in einem geeigneten Unterverzeicnis auf dem PC installieren. Wer das System [_Overleaf_](https://www.overleaf.com) nutzt, kann dieses ZIP-File als neues Projekt in Overleaf installieren.

### Der Aufbau der Vorlage

Beim Installieren wird das Verzeichnis __`AGFA-Rom-Teilnehmer`__ angelegt.







in dem die folgenden Unterverzeichnisse enthalten sind: 

* __`bib-abcd`__: Hier findet dich die Datei mit der benutzten Literatur, `Biblio-abcd.bib`. Der Aufbau dieser genügt den Regeln für die Nutzung in LaTeX. Eine kleine Anleitung dazu findet man in den LaTeX-Tipps.
	
* __`content-abcd`__: In diesem Unterverzeichnis finden sich alle genutzten Dateien des Vortrags, also `Beitrag-abcd.tex` für den Beitrag, eventuelle Bilder u. ä. Hierzu gehören auch die zusätzlichen Definitionen, die man eventuell benötigt. Bitte diese in die Datei `Defn-abcd.tex` schreiben, dabei aber darauf achten, dass man nichts definiert, was bereits vorhanden ist oder Fehler erzeugt. Diese Datei ist bereits mittels `\input{Defn-abcd}` eingebunden. 

	Um die verschiedenen Beiträge bei der Erstellung des Buches zum Seminar unterscheiden zu können, ist folgende Namensgebung erforderlich: Das `abcd` wird abgeändert in die in der AGFA üblichen Abkürzung für die E-Mail-Adresse. Ist also der Name des Referenten  `Rainer Nagel`, so ist `abcd = rana` (sollte klar sein, wie es geht). Sind es mehrere Autoren, so bitte den Namen dafür nehmen, der alphabetisch an erster Stelle kommt.

* Im Stammverzeichnis befindet sich die Datei `Rom-abcd.tex`, die für die Erstellung des eignen Beitrags verwendet wird. Also: Schreiben des Textes in  die Datei `Beitrag-abcd.tex` und dann kompilieren der Datei `Rom-abcd.tex`. 	

	Die Datei `Beitrag-abcd.tex` enthält als erste Zeile 
		
			% !TEX root = ../Rom-abcd.tex  
	
	Dadurch ist es möglich, diese Datei direkt mit LaTeX zu kompilieren, da dann die Stammdatei aufgerufen wird. Dies geht mit _TeXShop_ als Editor (für Apple OS) oder  entsprechend auch mit [TeXworks](https://tug.org/texworks/), der Linux und Windows unterstützt. Meine generelle Empfehlung ist es, diesen Editor für die TeX-Welt zu nutzen. 

* __`preamble`__: Hier befinden sich alle Dateien, die zur Erstellung des Dokuments mithilfe von LaTeX erforderlich sind. An diesen Dateien bitte **nichts** verändern. Sollte mal etwas nicht funktionieren oder spezielle Wünsche vorhanden sein, so bitte ich darum, mir dies mitzuteilen.

	Im Einzelnen sind dies: 
	
	- __`Rom-Beitrag.sty`__: Dies ist das Hauptpaket, mit Hilfe dessen alle anderen Dateien, die zur Formatierung erforderlich sind, aufgerufen werden. Diese Datei wird mittels `\usepackage{Rom-Beitrag}` eingebunden (siehe hierzu  `Rom-abcd.tex`).

	- __`Rom-Abkuerzungen.sty`__: Hier finden sich die Abkürzungen für die richtige Schreibweise etwa für d.h. 
			
	- __`Rom-BibLaTeX.sty`__:  Diese Datei ist für die Darstellung der Referenzen im Literaturverzeichnis zuständig. Bitte darauf achten, dass man einen zusätzlichen Lauf benötigt – einmal mit `biber` und dann nochmals mit `latex`. Mithilfe von 
		
				% !TEX TS-program = pdflatexmk
		
		in der ersten Zeile ist dies sichergestellt (`magic command line`). Das zugehörige `bib`-File findet sich in `content-abcd/bib-abcd` und heißt `Biblio-abcd.bib`. In diese Datei werden die Referenzen eingetragen und gepflegt. Tipp hierzu: Auf einem Mac das Programm `BibDesk` nutzen. Ansonsten ist etwa [JabRef](https://www.jabref.org) zu empfehlen. In meinen LaTeX-Tipps habe ich hierzu etwas zusammengestellt, dass man im Unterverzeichnis `beispiel` findet.
	
		- __`Rom-Layout.tex`__:  
		Alles, was für das Layout zuständig ist.
	
		- __`Rom-Pakete.tex`__:  
		Aus meiner Sicht nützliche Pakete, die die Möglichkeiten von LaTeX ergänzen. Wer mehr zu den Paketen wissen will, der kann einmal auf [ctan.org](https://ctan.org) nach diesen suchen und sich das Manual ansehen, oder `texdoc name-des-pakets` am PC aufrufen oder in das Buch von H. Voss: _Einführung in LaTeX_ reinsehen. Wichtig: _Learning-by-Doing_ ist dann angesagt. 



### Die Erstellung eines Beitrags mit LaTeX 

LaTeX ist ein sog. [WYSIWYM](https://de.wikipedia.org/wiki/WYSIWYM)-System und kein Textverarbeitungsprogramm, mit dem man einen Fließtext schreibt, wie bei Word. Es basiert auf [TeX](https://de.wikipedia.org/wiki/TeX), das ein Programm ist, mithilfe dessen  man Texte, die auf einem Computer geschrieben wurden, in eine druckbare Version umwandelt. Dies sollte man bei der Erstellung eines Textes berücksichtigen, d. h. man _programmiert_ den Inhalt seines Textes, um ein _schönes_ Ergebnis zu bekommen. 

Daher muss man die Möglichkeiten und Grenzen des Systems lernen und berücksichtigen. Meine Empfehlungen für das Lernen und Verstehen:

* [_lsshort_](https://ctan.org/pkg/lshort-german): Eine kleine, aber übersichtliche Einführung in LaTeX mit sinnvollen Tipps und einer kleinen Übersicht zur Entwicklung von TeX und LaTeX

* Da wir es mit einem Text auf Deutsch zu tun haben, sollte Rechtschreibung und die Zeichensetzung stimmen. Dabei hilft [_LanguageTool_](https://languagetool.org/de) und [_IDS-Mannheim_](https://grammis.ids-mannheim.de).

* Natürlich sind auch einige typografische Regeln zu beachten, etwa der Unterschied zwischen Bindestrich, Gedankenstrich und Minuszeichen. Dabei hilft das [_TypoLexikon._](https://www.typolexikon.de)

* Für einen Einstieg in die Umsetzung mathematischer Formeln empfiehlt sich der [_AMS ShortMathGuide_](https://ctan.org/pkg/short-math-guide), der völlig ausreichend ist. Auch hier sind einige typografische Regeln zu beachten, die man unter dem Stichwort [_Formelsatz_](http://www.moritz-nadler.de/formelsatz.pdf) findet.

* Wer mehr verstehen oder lernen will – einfach mal auf [_Dante – Literatur und mehr_](https://www.dante.de/dante-e-v/literatur/) nachsehen. Ein schöner Artikel zu TeX findet man  [_etwa hier_](https://www.ams.org/publications/authors/Communication_of_Mathematics_with_TEX.pdf).

* Einige Regeln zur Verfassung eines mathematischen Artikels findet man bei [P. Halmos: _How to Write Mathematics](https://www2.cs.duke.edu/donaldlab/Teaching/add/2011/resources/halmos.pdf) und [D. Knuth: _Mathematical Writing](https://jmlr.csail.mit.edu/reviewing-papers/knuth_mathematical_writing.pdf).


### Sonstiges 

* Die Datei `Rom-Muster.pdf` ist ein Beispiel, basierend auf `./beispiel/Rom-Muster.tex`. Diese Datei kann man sich ansehen, um noch weitere Details zu erfahren, wie die Eingabe der Beispiele erfolgt ist.

* __TODO__ Ein LaTeX-Paket aus den Dateien in der Preambel erstellen, um die Eingabe einfacher und die Vorlage kompakter zu machen. 


* Wünsche, Fehler etc. bitte an: <ulgr@math.uni-tuebingen.de>

