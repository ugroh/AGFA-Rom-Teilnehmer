## AGFA-Rom Vorlage (Stand 2023/02/02)

Dies ist die Vorlage für die Beiträge im Rahmen des Rom-Seminars. Die Basis hierfür ist [KOMA-Script](https://www.ctan.org/pkg/koma-script), da dieses Paket auf den deutschen Sprachraum und dessen Eigenheiten abgestimmt ist. 

Die Vorlage ist wie folgt aufgebaut:

* Die Vorlage findet man auf GitHub unter [ugroh/AGFA-Rom-Teilnehmer](https://github.com/ugroh/AGFA-Rom-Teilnehmer) und man kann sich dieses als ein ZIP-File herunterladen. Dazu geht man auf den grünen, mit __Code__ bezeichneten Schalter und öffnet diesen. Der Rest sollte klar sein: Als ZIP-File herunterladen und durch Entpacken installieren. 

Wer das System [Overleaf](https://www.overleaf.com) nutzt, kann dieses ZIP-File als neues Projekt in Overleaf installieren.

* Um die verschiedenen Beiträge bei der Erstellung des Buches zum Seminar unterscheiden zu können, ist folgende Namensgebung erforderlich: Das `abcd` wird abgeändert in die in der AGFA üblichen Abkürzung für die E-Mail-Adresse. Ist also der Name des Referenten  `Rainer Nagel`, so ist `abcd = rana` (sollte klar sein, wie es geht). Sind es mehrere Autoren, so bitte den Namen dafür nehmen, der alphabetisch an erster Stelle kommt.

* Im Verzeichnis `AGFA-Rom-Teilnehmer` befinden sich die folgenden Unterverzeichnisse:

	- `bib-abcd`: Hier findet dich die Datei mit der benutzten Literatur, `abcd-Biblio.bib`. Der Aufbau dieser genügt den Regeln für die Nutzung in LaTeX. Eine kleine Anleitung dazu findet man in den LaTeX-Tipps.
	
	- `content-abcd`: In diesem Unterverzeichnis finden sich alle genutzten Dateien des Vortrags, also `abcd-Beitrag-.tex` für den Beitrag, eventuelle Bilder u. ä. Hierzu gehören auch die zusätzlichen Definitionen, die man eventuell benötigt. Bitte diese in die Datei `abcd-Defn.tex` schreiben, dabei aber darauf achten, dass man nichts definiert, was bereits vorhanden ist oder Fehler erzeugt. Diese Datei ist bereits mittels `\input{abcd-Defn}` eingebunden. 
	
	- `preamble`: Hier befinden sich alle Dateien, die zur Erstellung des Dokuments mithilfe von LaTeX erforderlich sind. An diesen Dateien bitte **nichts** verändern. Sollte mal etwas nicht funktionieren oder spezielle Wünsche vorhanden sein, so bitte ich darum, mir dies mitzuteilen.
	Im Einzelnen sind dies: 

		>`Rom-Abkuerzungen.tex`: Hier finden sich die Abkürzungen für die Richtige Schreibweise etwa von d.h. u.a. 
			
		> `Rom-BibLaTeX.tex`: Für die Darstellung der Referenzen im Literaturverzeichnis. 
	
		> `Rom-Layout.tex`: Alles, was für das Layout zuständig ist.
	
		> `Rom-Pakete.tex`: Aus meiner Sicht nützliche Pakete, die die Möglichkeiten von LaTeX ergänzen. 

* Im Stammverzeichnis befindet sich die Datei `Rom-abcd.tex`, die für die Erstellung des eignen Beitrags verwendet wird. Also: Schreiben des Textes in  die Datei `abcd-Beitrag-.tex` und dann kompilieren der Datei `Rom-abcd.tex`. 	

	Die Datei `abcd-Beitrag-.tex` enthält als erste Zeile `% !TEX root = ../Rom-abcd.tex` (`magic command line`). Dadurch ist es möglich, diese Datei direkt mit LaTeX zu kompilieren, da dann die Stammdatei aufgerufen wird. Dies geht mit _TeXShop_ als Editor (für Apple OS) oder  entsprechend auch mit [TeXworks](https://tug.org/texworks/), der Linux und Windows unterstützt. Meine generelle Empfehlung ist es, diesen Editor für die TeX-Welt zu nutzen. 

* Im Unterverzeichnis `preamble` findet sich noch die Datei `ReadMe.pdf`, die weitere Erläuterungen für die Anfertigung des Beitrags enthält.
	


Wünsche, Fehler etc. bitte an: <ulgr@math.uni-tuebingen.de>

