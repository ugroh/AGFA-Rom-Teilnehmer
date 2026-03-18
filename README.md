# Rom-Seminar: LaTeX-Vorlage für Teilnehmer (Stand 2026-03-07)

### Inhaltsverzeichnis

- [Worum geht es](#einstieg)
- [Was wird genutzt](#latex)
- [Der Aufbau der Vorlage](#aufbau)
- [Ergänzende Literatur](#lit-latex)
- [Was ist in `preamble`](#preamble)
- [Aktualisierungen](#sonstiges)

---

<a name="einstieg"></a>

### Worum geht es

Diese Vorlage dient als Grundlage für die Beiträge im Rahmen des Rom-Seminars. Die Basis ist KOMA-Script, das auf den deutschen Sprachraum abgestimmt ist. Alle benötigten Pakete sind in `./preamble/Rom-Beitrag.sty` enthalten – bitte in den Dateien unter `./preamble/` **keine** eigenständigen Änderungen vornehmen.

Wünsche oder Ergänzungen bitte an [ulgr@math.uni-tuebingen.de](mailto:ulgr@math.uni-tuebingen.de).

Ein Beispiel mit den wichtigsten typografischen Regeln: [`beispiel/Rom-ulgr.pdf`](https://github.com/ugroh/AGFA-Rom-Teilnehmer/blob/main/beispiel/Rom-ulgr.pdf) – bitte unbedingt lesen.

**Installation**: Die Vorlage als `ZIP`-Datei von GitHub herunterladen (grüner **Code**-Schalter → **Local** → **Download ZIP**), entpacken und lokal installieren.
Für die lokale Nutzung: [MacTeX](https://www.tug.org/mactex/) (macOS) oder [TeX Live](https://tug.org/texlive/) (Linux/Windows).

> **Hinweis zu Overleaf**: Die Vorlage ist für die lokale Nutzung ausgelegt und dort getestet.
> Eine Nutzung auf Overleaf wird nicht offiziell unterstützt.
> Wer Overleaf dennoch nutzen möchte, bitte [mich kontaktieren](mailto:ulgr@math.uni-tuebingen.de).

Vor der Abgabe bitte den Text mit dem [LanguageTool](https://languagetool.org/de) auf Rechtschreib- und Grammatikfehler prüfen.

---

<a name="latex"></a>

### Was wird genutzt

LaTeX ist ein [WYSIWYM](https://de.wikipedia.org/wiki/WYSIWYM)-System: Man *programmiert* den Inhalt, um ein typografisch korrektes Ergebnis zu erhalten. Für einen Einstieg empfehle ich [*lshort*](https://ctan.org/pkg/lshort-german) und weitere Literaturhinweise finden sich im Abschnitt [Ergänzende Literatur](#lit-latex).

Wer mehr erfahren möchte: [https://tex.social](https://tex.social).

*Kleine Ergänzung* Der [LaTeX Online Course](https://www.learnlatex.org/) ist bestens geeignet sich einzuarbeiten - auch geeignet fur alle, die LaTeX kennen.
---

<a name="aufbau"></a>

### Der Aufbau der Vorlage

**Namensgebung**: Das Kürzel `abcd` ist durch die übliche AGFA-Abkürzung der E-Mail-Adresse zu ersetzen (z.B. `ulgr` für Ulrich Groh). Bei mehreren Autoren gilt der alphabetisch erste Name. Bitte **alle** Dateien mit `abcd` entsprechend umbenennen.

Das Hauptverzeichnis `Rom-Seminar-Teilnehmer` enthält:

- `Rom-abcd.tex` – Master-Datei; bitte Struktur nicht ändern
- `Rom-abcd.pdf` – kompiliertes Beispiel
- `Rom-Beamer.tex` – Beamer-Vorlage für die Präsentation

Unterverzeichnisse:

- **`beispiel`** – Musterbeitrag `Rom-ulgr.pdf` mit LaTeX-Tipps
- **`LaTeX-Tipps`** – Tipps zu Literaturverwaltung und Querverweisen
- **`content-abcd`** – 
  - Dateien des Beitrags: `Beitrag-abcd.tex`, Bilder, 
  -  `Defn-abcd.tex` für eigene Definitionen (bereits via `\input{Defn-abcd}` eingebunden). 
  - Literaturdatei `Biblio-abcd.bib` mit Mustereinträgen. Für die Erstellung des Literaturverzeichnisses wird `biber` benötigt – bitte im Editor einstellen.
- **`preamble`** – alle Formatierungsdateien; bitte **nicht** verändern

**Workflow**: Text in `./content-abcd/Beitrag-abcd.tex` schreiben, kompilieren mit `Rom-abcd.tex`.
Die erste Zeile von `Beitrag-abcd.tex` lautet:

```
% !TEX root = ../Rom-abcd.tex
```

Damit kann die Datei direkt kompiliert werden (z.B. mit [TeXShop](https://pages.uoregon.edu/koch/texshop/) auf macOS oder [TeXworks](https://tug.org/texworks/) auf Linux/Windows).

**Wichtig**: In `Beitrag-abcd.tex` folgende Angaben anpassen:

```latex
\renewcommand{\LongTitel}{Langform des Titels}
\renewcommand{\ShortTitel}{Kurzform des Titels}
\renewcommand{\AutorenBeitrag}{Autor1, Autor2 \& Autor3}
```

Wenn alles fertig ist: Verzeichnis `Rom-Seminar-Teilnehmer` (mit angepasstem `abcd`) als `ZIP`-Datei einsenden.

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

- **`Rom-Beitrag.sty`** – Hauptpaket; lädt alle weiteren Pakete (eingebunden via `\usepackage{Rom-Beitrag}` in `Rom-abcd.tex`)
- **`Rom-Abkuerzungen.sty`** – Abkürzungen für korrekte Schreibweise (z.B. `\dh` für d.\,h.)
- **`Rom-BibLaTeX.sty`** – Formatierung des Literaturverzeichnisses; benötigt `biber`-Lauf (sichergestellt durch `% !TEX TS-program = pdflatexmk` in der ersten Zeile). Tipp: [BibDesk](https://bibdesk.sourceforge.io/) (macOS) oder [JabRef](https://www.jabref.org/) zur Pflege der `bib`-Datei
- **`Rom-Layout.sty`** – Layout (Kopfzeilen, Schriften, Abstände). `\section*` und `\subsection*` wie üblich; `\subsubsection` erzeugt eine Nummer und kann zur Untergliederung verwendet werden
- **`Rom-Mathematik.sty`** – mathematische Definitionen (z.B. `\N`, `\norm{}`, `\abs{}`); Übersicht im Unterverzeichnis `beispiel`
- **`Rom-Theorem.sty`** – mathematische Umgebungen (nummeriert und unnummeriert); Details in der Übersicht unter `beispiel`
- **`Rom-Pakete.sty`** – ergänzende LaTeX-Pakete; Dokumentation via `texdoc paketname` oder [ctan.org](https://ctan.org/)

---

<a name="sonstiges"></a>

### Aktualisierungen

Wünsche und Fehler bitte melden: [ulgr@math.uni-tuebingen.de](mailto:ulgr@math.uni-tuebingen.de)
