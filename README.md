# LaTeX-examples

## Informationen über den Code

### Textbasierte Struktur
- **Meta-Informationen**: Alle wichtigen Daten sind in der Datei `meta/authorinfo.tex` zu finden.
- **Kapitelinhalt**: Alle Kapitel werden in den Verzeichnissen `content/*` hinzugefügt und in der Hauptdatei (`main`) referenziert.
- **Abkürzungen**: Alle Abkürzungen werden in der Datei `meta/acro.tex` definiert.
- **Glossar**: Alle Begriffe für das Glossar sind in `meta/gls.tex` festgelegt.
- **Hervorhebungen**: Um Text hervorzuheben, wird der Befehl `\highlight{}` verwendet.

### Erweiterungen
- **Pakete**: Alle erforderlichen Pakete werden in der Präambel des Dokuments hinzugefügt.

### Alle wichtigen Befehle auf einen Blick
- **Überschrift**: `\section{}`, `\subsection{}`, `\subsubsection{}`
- **Hervorheben**: `\highlight{}`
- **Hervorheben zwei**: `\highlightB{}`
- **Anführungszeichen**: `\enquote{}`
- **Abkürzungen**: `\acrlong{}`, `\acrshort{}`, `\acrfull{}`
- **Glossar**: `\gls{}`, `\Gls{}`, `\glspl{}`, `\Glspl{}`, `\acrshort{}`
- **Fußnote**: `\footnote{}`
- **Literatur**: `\cite{}`
- **Abkürzung** (z.B.): `\zB`
- **Abbildung**: `\myFigure{groesse=}{dateiname=}{beschreibung=}`
- **Kommentar**: `\todo{}`

## Ausführen der datei: 

`pdflatex main`

`makeglossaries main`

`pdflatex main`
