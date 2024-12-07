### Zehn Tipps für die Eingabe 

* Unbedingt `./beispiel/Rom-ulgr.pdf` lesen.
	
* Jeder neue Satz beginnt auf einer neuen Zeile – dies vereinfacht die Fehlersuche und macht das Lesen des Textes leichter.
	
* Einen neuen Absatz erreicht man mit Hilfe einer Leerzeile. Bitte nicht `\\`, `\newline` oder ähnliche Konstruktionen nutzen – eine Leerzele genügt.
	
* Die richtigen »_Gänsefüßchen_« erreicht man mit Hilfe von `\enquote{Text}`. Weiteres hierzu in `./beispiel/Rom-ulgr.pdf`, Seite 3.

* Hervorhebungen im Text (kursiv) nicht mit `\textit{}` sondern stets mit `\emph{}` – der erste Befehl ist für längere Textstellen.

* Die Eingabe von fremdsprachlichen Text erfolgt entweder mit 
		`\selectlanguage{sprache} Text \selectlanguage{ngerman}`
	oder mit	
	
	```
		\begin{otherlanguage}{sprache}
			Text
		\end{otherlanguage}
	```
	
	Als Sprache etwa `english` oder `french`. Beispiele hierzu findet man in `./beispiel/Rom-ulgr.pdf`.
	
* Ein Gedankenstrich ist etwas anderes wir ein Bindestrich oder ein Minuszeichen – siehe hierzu `./beispiel/Rom-ulgr.pdf`, Seite 5.

* Will man etwa d.h. typografisch korreckt eingeben, dann gehört nach dem ersten Punkt ein kleiner Abstand zum folgenden `h` und es muss auch klar sein, dass der Punkt nach diesem kein Schlusspunkt eines Satzes ist. Dazu dient dann der Befehl `\dh` und viele weitere. Dies findet man auf der Seite 6 des o.g. PDF.

* Die  Eingabe von Listen erfolgt mittels
  `\begin{enumerate}[label]`
  `\item`
  `\end{enumerate}`
  wobei `label` etwa `(i)` für eine römische Nummrierung ist. Weiteres auf Seite 7 in  `./beispiel/Rom-ulgr.pdf`.

* Die Eingabe mathematischen Textes ist ausführlich in  `./beispiel/Rom-ulgr.pdf`  beschrieben. Es schadet nicht, sich dieses anzusehen – vermeidet mache Frustrationen.