## AGFA-Rom Vorlage (Stand 2023/02/01)

Dies ist die Vorlage für die Beiträge im Rahmen des Rom-Seminars. Der Aufbau ist wie folgt:

* Im Stammverzeichnis befindet sich eine Vorlage ohne Inhalt `Beitrag-abcd.tex`, das als Basis für den Beitrag genommen wird. Dabei wird das `abcd` abgeändert in die in der AGFA üblichen Abkürzung für die Mailadresse, also etwa `Rainer Nagel = rana` des jeweiligen Autoren. Sind es mehrere, so bitte den Namen nehmen, der alphabetisch an erster Stelle kommt. In diese Datei wird dann der Beitrag geschrieben.

* Diese Datei wird in das Unterverzeichnis `content` kopiert und über die Datei `Rom-abcd.tex`, die sich im Stammverzeichnis befindet, aufgerufen. Alle weiteren Dateien, etwa Bilder, Diagramme etc. werden auch mit dem Namen `abcd-weiteres`bezeichnet, wobei `-weiteres` frei vergeben werden kann und finden sich auch im Unterverzeichnis `content`.

* Im Unterverzeichnis `preambel`finden sich alle Dateien, die zur Erstellung des Dokuments mithilfe von LaTeX erforderlich sind. Im Einzelnen sind dies: 

	- `Rom-Abkuerzungen.tex`: Hier finden sich die Abkürzungen für die richtige Schreibweise con d.h.
	- `Rom-BibLaTeX.tex`: Für die Darstellung der Referenzen im Literaturverzeichnis. 
	- `Rom-Layout.tex`: Alles, was für das Layout zuständig ist.
	- `Rom-Pakete.tex`: Aus meiner Sicht nützliche Pakete, die die Möglichkeiten von LaTeX ergänzen. 
	
An diesen Dateien wird bitte **nichts** geändert. Sollte mal etwas nicht funktionieren oder spezielle Wünsche vorhanden sein, so bitte ich darum, mir dies mitzuteilen.

* Eigene Ergänzungen, die erforderlich sind, bitte in die Datei `abcd-defn.tex` aufnehmen und über `\input{abcd-defn}` in die Hauptdatei `Rom-abcd.tex`. Wer dies machen will sollte aber wissen, was er macht und auch gute LaTeX-Kenntnisse besitzen.

* Die Vorlagen bekommt man über []()

#### Wie bekomme ich die Vorlagen:

Für die Teilnehmer: Einfach auf das zip-File gehen (anklicken) und dann herunterladen oder auf `Code`gehen und das zip-File herunterladen. Dann werden die beiden Vorlagen heruntergeladen. Man kann dann diese entsprechend umbenennen bzw. löschen und etwa auf seinen PC entpacken. Wer `Overleaf`nutzt: Dieses dann als zip-File und als neues Projekt hochladen. 