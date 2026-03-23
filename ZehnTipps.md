### Tipps und Hinweise zur Eingabe

Bitte unbedingt `./beispiel/Rom-ulgr.pdf` lesen.
Dort finden sich Tipps und Regeln für die Eingabe von Text in ein LaTeX-Dokument.
Und nun zu einigen Hinweisen.

- Jeder Satz beginnt auf einer neuen Zeile.
  Das macht die Fehlersuche einfacher und das Lesen leichter.

- Einen neuen Absatz erreicht man mithilfe einer Leerzeile.
  Bitte nicht `\\`, `\newline` oder ähnliche Konstruktionen nutzen – eine Leerzeile genügt.

- Die richtigen »Anführungszeichen« bekommt man mit `\enquote{Text}`.
  Mehr dazu steht auf Seite 3 von `./beispiel/Rom-ulgr.pdf`.

- Hervorhebungen im Text (kursiv) nicht mit `\textit{kursiv}`, sondern stets mit `\emph{kursiv}` –
  `\textit` ist ein typografischer Befehl, `\emph` dagegen ein semantischer und damit der richtige.

- Die Eingabe von fremdsprachlichem Text erfolgt entweder mit

  ```latex
  \selectlanguage{sprache} Text \selectlanguage{ngerman}
  ```

  oder mit

  ```latex
  \begin{otherlanguage}{sprache}
      Text
  \end{otherlanguage}
  ```

  Als Sprache etwa `english`, `italian` oder `french`.
  Beispiele hierzu findet man in `./beispiel/Rom-ulgr.pdf`.

- Ein Gedankenstrich ist etwas anderes als ein Bindestrich oder ein Minuszeichen –
  siehe hierzu `./beispiel/Rom-ulgr.pdf`, Seite 5.

- Abkürzungen wie d.\,h. werden typografisch korrekt mit `\dh` eingegeben –
  viele weitere Abkürzungen finden sich auf Seite 6 von `./beispiel/Rom-ulgr.pdf`.

- Die Eingabe von Listen erfolgt mittels

  ```latex
  \begin{enumerate}[label]
      \item ...
  \end{enumerate}
  ```

  wobei `label` etwa `\upshape(i)` für eine römische Nummerierung ist.
  Weiteres auf Seite 7 in `./beispiel/Rom-ulgr.pdf`.

- Die Eingabe mathematischen Textes ist ausführlich in `./beispiel/Rom-ulgr.pdf` beschrieben.
  Es lohnt sich, dies zu lesen – es vermeidet manche Frustration.

- Querverweise: bitte `\vref{label}` nutzen – dann wird auch die korrekte Seite angezeigt.
  Labels bitte sinnvoll benennen (siehe `./beispiel/Rom-ulgr.pdf` für Beispiele).
  Weiteres zu Querverweisen findet sich in den `LaTeX-Tipps`.

- Literatur zitiert man mit `\textcite[genaue Stelle]{label}`.
  Für `label` empfiehlt sich das einheitliche Format `verfasser:jahr` (siehe die beigefügte
  `bib`-Datei) – das vereinfacht die Suche nach Literaturstellen.
  Weiteres dazu findet sich in den `LaTeX-Tipps`.

- URL-Links bitte grundsätzlich kürzen, einheitlich mit
  [https://tinyurl.com](https://tinyurl.com) –
  dies gilt auch für URL-Links in Literaturzitaten. Diese können dann mittels
  `\href{link}{Was-auch-immer}` in das `TeX`-Dokument integriert werden.
