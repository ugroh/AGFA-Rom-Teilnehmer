* ### Zehn+ Tipps für die Eingabe 

  Bitte unbedingt `./beispiel/Rom-ulgr.pdf` lesen. 

  Und nun zu einigen Tipps und Regeln für die Eingabe.  

  - Jeder Satz beginnt auf einer neuen Zeile. Das macht die Fehlersuche einfacher und das Lesen leichter.

  - Einen neuen Absatz erreicht man mithilfe einer Leerzeile. Bitte nicht `\\`, `\newline` oder ähnliche Konstruktionen nutzen – eine Leerzeile genügt.

  - Die richtigen »Anführungszeichen« bekommt man mit `\enquote{Text}`. Mehr dazu steht auf Seite 3 von `./beispiel/Rom-ulgr.pdf`.

  - Hervorhebungen im Text (kursiv) nicht mit `\textit{kursiv}`, sondern stets mit `\emph{kursiv}` – der erste Befehl ist für längere Textstellen.

  - Die Eingabe von fremdsprachlichem Text erfolgt entweder mit  `\selectlanguage{sprache} Text \selectlanguage{ngerman}` oder mit	

    ```
      \begin{otherlanguage}{sprache}
        Text
      \end{otherlanguage}
    ```

    Als Sprache etwa `english` oder `french`. Beispiele hierzu findet man in `./beispiel/Rom-ulgr.pdf`.

  - Ein Gedankenstrich ist etwas anderes als ein Bindestrich oder ein Minuszeichen – siehe hierzu `./beispiel/Rom-ulgr.pdf`, Seite 5 

  - Will man etwa d.h. typografisch korrekt eingeben, dann gehört nach dem ersten Punkt ein kleiner Abstand zum folgenden `h` und es muss auch klar sein, dass der Punkt nach diesem kein Schlusspunkt eines Satzes ist. Dazu dient dann der Befehl `\dh` und viele weitere. Dies findet man auf der Seite 6 des o.g. PDF.

  - Die  Eingabe von Listen erfolgt mittels `\begin{enumerate}[label]` `\item` `\end{enumerate}` wobei `label` etwa `(i)` für eine römische Nummerierung ist. Weiteres auf Seite 7 in  `./beispiel/Rom-ulgr.pdf`.

  - Die Eingabe mathematischen Textes ist ausführlich in  `./beispiel/Rom-ulgr.pdf`  beschrieben. Es schadet nicht, sich dieses anzusehen – vermeidet manche Frustrationen.

  - Querverweise: bitte `\vref{link}` nutzen – dann wird auch die korrekte Seite angezeigt. Zu Querverweisen u.ä. findet man weiteres in den `LaTeX-Tipps`. Bitte die `links` sinnvoll benennen (siehe `./beispiel/Rom-ulgr.pdf`  für Beispiele).

  - Zitieren von Literatur: `\textcite[wo-steht-etwas]{link}`. Einiges Weitere dazu finden sich in den `LaTeX-Tipps`⁣. Für die `links` empfehle ich einheitlich `verfasser:jahr` zu verwenden (siehe die beigefügte `bib`-Datei). Vereinfacht das Suchen nach den Literaturstellen (wenn man mal etwas verbessern muss).