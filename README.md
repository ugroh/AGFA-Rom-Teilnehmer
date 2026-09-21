# Rom-Seminar: LaTeX-Vorlage für Teilnehmer (Stand 2026-09-21)

### Inhaltsverzeichnis

- [Worum geht es](#einstieg)
- [Was wird genutzt](#latex)
- [Der Aufbau der Vorlage](#aufbau)
- [Kompilieren](#kompilieren)
- [Ergänzende Literatur](#lit-latex)
- [Was ist in `preamble`](#preamble)
- [Querverweise, Sätze und eigene Makros](#hinweise)
- [Häufige Fehler](#fehler)
- [Aktualisierungen](#sonstiges)

---

<a name="einstieg"></a>

### Worum geht es

Diese Vorlage dient als Grundlage für die Beiträge im Rahmen des Rom-Seminars. Die Basis ist KOMA-Script, das auf den deutschen Sprachraum abgestimmt ist. Alle benötigten Pakete werden von `./preamble/Rom-Beitrag.sty` geladen – bitte in den Dateien unter `./preamble/` **keine** eigenständigen Änderungen vornehmen.

Wünsche oder Ergänzungen bitte an [ulgr@math.uni-tuebingen.de](mailto:ulgr@math.uni-tuebingen.de).

Ein Beispiel mit den wichtigsten typografischen Regeln: [`beispiel/Rom-ulgr.pdf`](https://github.com/ugroh/AGFA-Rom-Teilnehmer/blob/main/beispiel/Rom-ulgr.pdf) – bitte unbedingt lesen.

**Installation**: Die Vorlage als `ZIP`-Datei von GitHub herunterladen (grüner **Code**-Schalter → **Local** → **Download ZIP**), entpacken und lokal installieren.
Für die lokale Nutzung: [MacTeX](https://www.tug.org/mactex/) (macOS) oder [TeX Live](https://tug.org/texlive/) (Linux/Windows), jeweils in der Version 2023 oder neuer.

> **Hinweis zu Overleaf**: Die Vorlage ist für die lokale Nutzung ausgelegt und dort getestet.
> Eine Nutzung auf Overleaf wird nicht offiziell unterstützt.
> Wer Overleaf dennoch nutzen möchte, bitte [mich kontaktieren](mailto:ulgr@math.uni-tuebingen.de).

Vor der Abgabe bitte den Text mit dem [LanguageTool](https://languagetool.org/de) auf Rechtschreib- und Grammatikfehler prüfen.
Gute Idee ist es auch, mal `Claude` oder `ChatGPT` zu befragen.

---

<a name="latex"></a>

### Was wird genutzt

LaTeX ist ein [WYSIWYM](https://de.wikipedia.org/wiki/WYSIWYM)-System: Man *programmiert* den Inhalt, um ein typografisch korrektes Ergebnis zu erhalten. Für einen Einstieg empfehle ich [*lshort*](https://ctan.org/pkg/lshort-german) und weitere Literaturhinweise finden sich im Abschnitt [Ergänzende Literatur](#lit-latex).

Wer mehr erfahren möchte: [https://tex.social](https://tex.social). Und der [LaTeX Online Kurs](https://www.learnlatex.org) ist bestens geeignet, sich einzuarbeiten.

---

<a name="aufbau"></a>

### Der Aufbau der Vorlage

**Namensgebung**: Das Kürzel `abcd` ist durch die übliche AGFA-Abkürzung der E-Mail-Adresse zu ersetzen (z.B. `ulgr` für Ulrich Groh). Bei mehreren Autoren gilt der alphabetisch erste Name. Bitte **alle** Dateien mit `abcd` entsprechend umbenennen.

Das Hauptverzeichnis `Rom-Seminar-Teilnehmer` enthält:

- `Rom-abcd.tex` – Master-Datei; bitte Struktur nicht ändern
- `Rom-abcd.pdf` – kompiliertes Beispiel (Platzhalter; der eigentliche Musterbeitrag liegt unter `beispiel/`)
- `Rom-Beamer.tex` – Beamer-Vorlage für die Präsentation

Unterverzeichnisse:

- **`beispiel`** – Musterbeitrag `Rom-ulgr.pdf` mit LaTeX-Tipps
- **`LaTeX-Tipps`** – Tipps zu Literaturverwaltung und Querverweisen
- **`content-abcd`** –
  - Dateien des Beitrags: `Beitrag-abcd.tex` und Bilder
  - `Defn-abcd.tex` für eigene Definitionen (bereits via `\input{Defn-abcd}` eingebunden)
  - Literaturdatei `Biblio-abcd.bib` mit Mustereinträgen. Für die Erstellung des Literaturverzeichnisses wird `biber` benötigt – bitte im Editor einstellen.
- **`preamble`** – alle Formatierungsdateien; bitte **nicht** verändern. Die Dateien erwarten, dass der Ordner `preamble` direkt neben `Rom-abcd.tex` liegt – bitte die Ordnerstruktur nicht ändern.

**Workflow**: Text in `./content-abcd/Beitrag-abcd.tex` schreiben, kompilieren mit `Rom-abcd.tex`.
Die erste Zeile von `Beitrag-abcd.tex` lautet:

```
% !TEX root = ../Rom-abcd.tex
```

Damit kann die Datei direkt kompiliert werden (z.B. mit [TeXShop](https://pages.uoregon.edu/koch/texshop/) auf macOS – meine Empfehlung – oder [TeXworks](https://tug.org/texworks/) auf Linux/Windows).

**Wichtig**: In `Beitrag-abcd.tex` folgende Angaben anpassen:

```latex
\renewcommand{\LongTitel}{Langform des Titels}
\renewcommand{\ShortTitel}{Kurzform des Titels}
\renewcommand{\AutorenBeitrag}{Autor1, Autor2 \& Autor3}
```

Wenn alles fertig ist: Verzeichnis `Rom-Seminar-Teilnehmer` (mit angepasstem `abcd`) als `ZIP`-Datei einsenden.

---

<a name="kompilieren"></a>

### Kompilieren

- **Programm**: `pdflatex` oder `lualatex`. In TeXShop wird das Programm oben im Fenster ausgewählt; alternativ kann man in die ersten Zeilen von `Rom-abcd.tex` schreiben: `% !TEX TS-program = lualatex` (TeXShop) bzw. `% !TEX program = lualatex` (TeXworks).
- **Reihenfolge**: Erst ein Lauf mit `pdflatex` bzw. `lualatex`, dann `biber`, dann noch mindestens zweimal `pdflatex` bzw. `lualatex`. Die meisten Editoren können das automatisch (Stichwort *Latexmk* bzw. „Typeset-Kette“).
- **Biber und biblatex müssen zusammenpassen**: Beide kommen aus derselben TeX-Live-Version. Bei der Fehlermeldung „control file version“ ist meist eine der beiden veraltet – dann TeX Live aktualisieren.
- **Korrekturlesen**: `Rom-Beitrag.sty` kennt die Option `review` (doppelter Zeilenabstand).

---

<a name="lit-latex"></a>

### Ergänzende Literatur

- **LaTeX allgemein**: [H. Voss, *Einführung in LaTeX*](https://www.lehmanns.de/shop/mathematik-informatik/33589289-9783865417985-einfuehrung-in-latex)
- **KOMA-Script**: [M. Kohm, *KOMA-Script*](https://www.lehmanns.de/shop/mathematik-informatik/51375541-9783965430976-koma-script) oder das [CTAN-Manual](https://ctan.mirror.norbert-ruehl.de/macros/latex/contrib/koma-script/doc/scrguide-de.pdf)
- **Mathematischer Formelsatz**: [AMS ShortMathGuide](https://ctan.org/pkg/short-math-guide), [Formelsatz](http://www.moritz-nadler.de/formelsatz.pdf)
- **Typografie**: [TypoLexikon](https://www.typolexikon.de/)
- **Rechtschreibung/Grammatik**: [LanguageTool](https://languagetool.org/de), [IDS Mannheim](https://grammis.ids-mannheim.de/)
- **Mathematisches Schreiben**: [P. Halmos: *How to Write Mathematics*](https://www2.cs.duke.edu/donaldlab/Teaching/add/2011/resources/halmos.pdf), [D. Knuth: *Mathematical Writing*](https://jmlr.csail.mit.edu/reviewing-papers/knuth_mathematical_writing.pdf) (auch auf [YouTube](https://www.youtube.com/watch?v=mert0kmZvVM&list=PLABJEFgj0PWV22nvw3YKXvR_n1NB6fn5D))
- **Weiteres**: [Dante – Literatur und mehr](https://www.dante.de/dante-e-v/literatur/)

---

<a name="preamble"></a>

### Was ist in `preamble`

- **`Rom-Beitrag.sty`** – Hauptpaket; lädt alle weiteren Pakete (wird in `Rom-abcd.tex` eingebunden). Hauptsprache ist Deutsch (neue Rechtschreibung); Englisch ist für fremdsprachige Stellen mit geladen, weitere Sprachen (z.B. Französisch) sind nicht eingebunden. Anführungszeichen immer mit `\enquote{…}` setzen (ergibt »…«, verschachtelt ›…‹). Englische Stellen:

  | Eingabe | Verwendung |
  |---|---|
  | `\foreignlanguage{english}{The quick brown fox}` | kurze Wörter oder Sätze mitten im Text (englische Silbentrennung) |
  | `\begin{otherlanguage}{english} … \end{otherlanguage}` | längere englische Absätze; `\enquote` ergibt dort “…” |
  | `\foreignquote{english}{He said that this works.}` | englisches Zitat mit englischen Anführungszeichen “…” |
- **`Rom-Abkuerzungen.sty`** – Abkürzungen für die korrekte Schreibweise (mit schmalem Leerraum und ohne Zeilenumbruch):

  | Eingabe | Ausgabe | Eingabe | Ausgabe | Eingabe | Ausgabe |
  |---|---|---|---|---|---|
  | `\zB` | z. B. | `\dh` | d. h. | `\ua` | u. a. |
  | `\iA` | i. A. | `\iAllg` | i. Allg. | `\og` | o. g. |
  | `\oAe` | o. Ä. | `\uAe` | u. Ä. | `\fue` | f. ü. |
  | `\inkl` | inkl. | `\sog` | sog. | `\bzgl` | bzgl. |
  | `\vs` | vs. | `\ca` | ca. | `\bzw` | bzw. |
  | `\etc` | etc. | `\usw` | usw. | `\ggf` | ggf. |
  | `\evtl` | evtl. | `\vgl` | vgl. | | |

  Hat jemand eines dieser Kürzel selbst definiert, gilt die eigene Definition (Ausnahme: `\dh`).
- **`Rom-BibLaTeX.sty`** – Formatierung des Literaturverzeichnisses; benötigt einen `biber`-Lauf (siehe [Kompilieren](#kompilieren)). Bei Büchern wird keine URL ausgegeben. Ist eine DOI angegeben, wird sie als Link hinterlegt.

  Mein Tipp: [BibDesk](https://bibdesk.sourceforge.io/) (macOS) oder [JabRef](https://www.jabref.org/) zur Pflege der `bib`-Datei.
- **`Rom-Layout.sty`** – Layout (Kopfzeilen, Schriften, Abstände). `\section*` und `\subsection*` wie üblich; `\subsubsection` erzeugt eine Nummer und kann zur Untergliederung verwendet werden.
- **`Rom-Mathematik.sty`** – mathematische Definitionen; Übersicht im Unterverzeichnis `beispiel`:

  | Eingabe | Bedeutung |
  |---|---|
  | `\N`, `\Z`, `\Q`, `\R`, `\C`, `\K` | Zahlbereiche ℕ, ℤ, ℚ, ℝ, ℂ, 𝕂 |
  | `\norm{x}`, `\abs{x}` | Norm und Betrag (mit `*` wachsende Klammern) |
  | `\diff{x}`, `\dx`, `\dt`, `\ds`, `\dg`, `\dy`, `\dr` | Differential mit korrektem Abstand |
  | `\eu`, `\iu` | Eulersche Zahl e, imaginäre Einheit i (aufrecht) |
  | `\P` | im Mathemodus Potenzmenge 𝔓, im Text das Absatzzeichen ¶ |
  | `\L{E,F}` | im Mathemodus ℒ(E,F); im Text bleibt `\L` das polnische Ł |
- **`Rom-Theorem.sty`** – mathematische Umgebungen, siehe [Sätze](#saetze).
- **`Rom-Pakete.sty`** – ergänzende LaTeX-Pakete; Dokumentation via `texdoc paketname` oder [ctan.org](https://ctan.org/)

---

<a name="hinweise"></a>

### Querverweise, Sätze und eigene Makros

**Querverweise mit `\vref`**: `\vref{label}` liefert Name, Nummer und – falls nötig – einen Seitenhinweis, z. B. „Satz 1.1 auf der vorherigen Seite“. Auf derselben Seite steht nur „Satz 1.1“. Der Name (Satz, Lemma, Abschnitt, Gleichung, Abbildung …) richtet sich nach der Umgebung, nicht nach dem Label; Präfixe wie `prop:` oder `eq:` sind nur eine Merkhilfe. **Der Name darf deshalb nicht noch einmal davorgeschrieben werden** („Satz~\vref{…}“ ergäbe „Satz Satz 1.1“). `\ref{}` und `\autoref{}` funktionieren wie gewohnt. `\cref` und `\Cref` (Paket *cleveref*) gibt es bewusst nicht.

<a name="saetze"></a>

**Sätze und Umgebungen**: Alle nummerierten Umgebungen teilen sich **einen** Zähler, der in jedem Abschnitt neu beginnt (Theorem 1.1, Lemma 1.2, Satz 1.3 …). Zu jedem Namen gibt es eine Kurzform, eine `n`-Form und eine lange Form; sie sind gleichwertig. Ohne Nummer gibt es die Umgebungen in der letzten Spalte. Dazu kommen `proof` (Beweis) sowie unnummeriert `summary` (Zusammenfassung) und `question` (Frage).

| Name | Kurzform | `n`-Form | lang | unnummeriert |
|---|---|---|---|---|
| Theorem | `thm` | `nthm` | `ntheorem` | `theorem` |
| Satz | `prop` | `nprop` | `nproposition` | `proposition` |
| Lemma | `lem` | `nlem` | `nlemma` | `lemma` |
| Korollar | `cor` | `ncor` | `ncorollary` | `corollary` |
| Beispiel | `exam` | `nexamp` | `nexample` | `example` |
| Beispiele | `exams` | `nexamps` | `nexamples` | `examples` |
| Definition | `defn` | `ndefn` | `ndefinition` | `definition` |
| Anmerkung | `rem` | `nrem` | `nremark` | `remark` |
| Anmerkungen | `rems` | `nrems` | `nremarks` | `remarks` |

**Eigene Makros** gehören in `Defn-abcd.tex`. Vorher bitte prüfen, ob der Name schon vergeben ist (siehe die Tabellen oben und die Makros aus LaTeX selbst). Ist er vergeben, meldet LaTeX „Command … already defined“. Dann entweder einen anderen Namen wählen oder das Makro bewusst mit `\renewcommand` ändern. Für die Kürzel aus `Rom-Abkuerzungen.sty` gilt die Ausnahme, dass die eigene Definition Vorrang hat.

---

<a name="fehler"></a>

### Häufige Fehler

| Meldung / Symptom | Ursache und Lösung |
|---|---|
| `Command \R already defined` (ebenso `\N`, `\C`, `\L` …) | Der Name ist schon in `Rom-Mathematik.sty` vergeben. Anderen Namen wählen oder `\renewcommand` verwenden. |
| `Undefined control sequence` bei `\cref` | `cleveref` ist nicht geladen; stattdessen `\vref` benutzen. |
| Literatur fehlt, `[?]` im Text, „Please (re)run Biber“ | `biber` wurde nicht ausgeführt. Reihenfolge: `lualatex`/`pdflatex` → `biber` → 2× `lualatex`/`pdflatex`. |
| `File './preamble/…' not found` | Ordnerstruktur wurde verändert oder es wird nicht `Rom-abcd.tex` kompiliert. Bitte im Hauptverzeichnis kompilieren. |
| „Satz Satz 1.1“ im Text | Der Name wurde vor `\vref` von Hand geschrieben; einfach weglassen. |

---

<a name="sonstiges"></a>

### Aktualisierungen

Das Paket ist so gestaltet, dass sowohl `pdfLaTeX` als auch `LuaLaTeX` verwendet werden kann.

**2026-09-21**

- `LuaLaTeX` wird vollständig unterstützt (Ladereihenfolge von `amssymb` und `unicode-math`).
- `\vref` liefert jetzt den Namen mit; `cleveref` (`\cref`) wird nicht mehr geladen.
- `thm` und `nthm` teilen den Zähler mit den übrigen nummerierten Umgebungen, es gibt keine doppelten Nummern mehr.
- `\L` und `\P` sind nur noch im Mathemodus umdefiniert; im Text stehen wieder Ł und ¶ (wichtig für Literaturangaben mit polnischen Namen).
- Die Kürzel aus `Rom-Abkuerzungen.sty` verursachen keinen Fehler mehr, wenn sie schon selbst definiert wurden.
- Es werden nur noch Deutsch und Englisch als Sprachen geladen.
- Literaturverzeichnis: Bücher ohne einzelnen Punkt oder Abrufdatum bei vorhandener URL, DOI-Links über `https://doi.org/`.

Wünsche und Fehler bitte melden: [ulgr@math.uni-tuebingen.de](mailto:ulgr@math.uni-tuebingen.de)
