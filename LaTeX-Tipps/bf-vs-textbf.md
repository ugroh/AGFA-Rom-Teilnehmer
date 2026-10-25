# `\bf` vs. `\textbf`: Warum man `\bf`, `\it` etc. nicht mehr nutzen sollte

Kurz gesagt: `\bf`, `\it` und Co. stammen aus Plain TeX bzw. LaTeX 2.09. In LaTeX2e gibt es sie nur noch aus Kompatibilitätsgründen, und sie verhalten sich an mehreren Stellen ungünstig.

## 1. Sie lassen sich nicht kombinieren

Jeder der alten Befehle setzt zuerst *alle* Schriftattribute zurück und ändert dann genau eins:

```latex
{\bf\it Text}            % ergibt nur kursiv, nicht fett
\textbf{\textit{Text}}   % ergibt fett und kursiv
{\bfseries\itshape Text} % ebenfalls fett und kursiv
```

LaTeX2e trennt die Schrift in unabhängige Achsen: Familie (`\rmfamily`, `\sffamily`, `\ttfamily`), Serie (`\bfseries`, `\mdseries`) und Form (`\itshape`, `\slshape`, `\scshape`, `\upshape`). Die neuen Befehle ändern jeweils nur ihre eigene Achse und lassen die anderen in Ruhe.

## 2. Keine automatische Kursivkorrektur

`\textit{...}` fügt am Ende von selbst die Kursivkorrektur `\/` ein. Bei `{\it Wort} danach` muss man sie selbst setzen, sonst stößt der kursive Buchstabe an das folgende aufrechte Zeichen, etwa bei *f*) oder *f*].

## 3. Sie gehören nicht mehr zum LaTeX-Kern

Definiert werden sie von den Dokumentklassen, und darauf ist kein Verlass. In `article`, `book` usw. sind sie noch vorhanden. KOMA-Script (`scrartcl`, `scrbook`, …) beschwert sich in neueren Versionen dagegen deutlich, je nach Version mit einer Warnung oder einem Fehler. Andere Klassen definieren sie gar nicht.

## 4. Im Mathemodus unklar

In manchen Klassen funktioniert `\bf` im Mathemodus, in anderen nicht. Sauber ist es so: `\mathbf`, `\mathit` usw. für Formeln, `\text...` für Text.

## Was man stattdessen nimmt

| alt   | für kurze Stellen | als Schalter (Gruppen, Umgebungen) |
|-------|-------------------|------------------------------------|
| `\bf` | `\textbf{}`       | `\bfseries`                        |
| `\it` | `\textit{}`       | `\itshape`                         |
| `\sl` | `\textsl{}`       | `\slshape`                         |
| `\sc` | `\textsc{}`       | `\scshape`                         |
| `\tt` | `\texttt{}`       | `\ttfamily`                        |
| `\sf` | `\textsf{}`       | `\sffamily`                        |
| `\rm` | `\textrm{}`       | `\rmfamily` (bzw. `\normalfont`)   |

Will man etwas inhaltlich hervorheben, ist `\emph{}` meist besser als `\textit{}`. Es schaltet in schon kursivem Kontext automatisch auf aufrecht zurück, und das Aussehen lässt sich zentral umdefinieren.

## Weiterführend

**l2tabu** („Sündenregister“ für LaTeX, auch auf Deutsch). Dort stehen die alten Schriftbefehle ganz oben auf der Liste der Altlasten.
