# LaTeX-examples

## Informationen über den Code

### Textbasierte Struktur
- **Meta-Informationen:** Alle wichtigen Daten sind in der Datei `meta/authorinfo.tex` zu finden.
- **Kapitelinhalt:** Alle Kapitel werden in den Verzeichnissen `content/*` hinzugefügt und in der Hauptdatei (`main`) referenziert.
- **Abkürzungen:** Alle Abkürzungen werden in der Datei `meta/acro.tex` definiert.
- **Glossar:** Alle Begriffe für das Glossar sind in `meta/gls.tex` festgelegt.
- **Hervorhebungen:** Um Text hervorzuheben, wird der Befehl `\highlight{}` verwendet.

### Erweiterungen
- **Pakete:** Alle erforderlichen Pakete werden in der Präambel des Dokuments hinzugefügt.

### Alle wichtigen Befehle auf einen Blick
- **Überschrift:** `\section{}`, `\subsection{}`, `\subsubsection{}`
- **Hervorheben:** `\highlight{}`
- **Hervorheben zwei:** `\highlightB{}`
- **Anführungszeichen:** `\enquote{}`
- **Zitat:** `\begin{quote} ... \end{quote}`
- **Code:** `\verb|Code|` oder `\texttt{Code}`
- **Abkürzungen:** `\acrlong{}`, `\acrshort{}`, `\acrfull{}`
- **Glossar:** `\gls{}`, `\Gls{}`, `\glspl{}`, `\Glspl{}`, `\acrshort{}`
- **Fußnote:** `\footnote{}`
- **Literatur:** `\cite{}`
- **Abkürzung (z. B.)** `\zB`
- **Kommentar:** `\todo{}`
- **Sonderzeichen:** `\&`

## Ausführen der datei: 

`pdflatex main`

`makeglossaries main`

`pdflatex main`


# Einführung in die LaTeX-Befehle 

## Text darstellung

## Textdarstellung

- **Fetter Text:** `\textbf{fett}`
- **Kursiver Text:** `\textit{kursiv}`
- **Unterstrichen:** `\underline{unterstrichen}`
- **Durchgestrichen:** `\sout{durchgestrichen}` (benötigt das Paket `ulem`)
- **Farbe:** `\textcolor{red}{Text}` (benötigt das Paket `xcolor`)
- **Absatz:** Leere Zeile im Quelltext
- **Zeilenumbruch:** `\\`
- **Listen:** 
    - Aufzählung: 
        ```
        \begin{itemize}
            \item Erster Punkt
            \item Zweiter Punkt
        \end{itemize}
        ```
    - Nummeriert: 
        ```
        \begin{enumerate}
            \item Erster Punkt
            \item Zweiter Punkt
        \end{enumerate}
        ```

## Bild einfügen

```
\begin{figure}[h]
    \centering
    \includegraphics[width=0.4\textwidth]{images/bild.png}
    \caption{Abbildung}
    \label{fig:bild}
\end{figure}
```

## Tabellen einfügen

```
\begin{table}[h]
    \centering
    \begin{tabular}{|p{5cm}|p{5cm}|}
        \hline
        \textbf{Vorteile} & \textbf{Nachteile} \\
        \hline
        Vorteil 1 & Nachteil 1 \\
        Vorteil 2 & Nachteil 2 \\
        Vorteil 3 & Nachteil 3 \\
        \hline
    \end{tabular}
    \caption{Vor- und Nachteile einer bestimmten Sache}
    \label{tab:beispiel}
\end{table}
```

## Code einfügen

Java 

- Präamble
    ```
    \definecolor{codeblue}{HTML}{0000FF}   % Keywords
    \definecolor{codered}{HTML}{A31515}   % Strings
    \definecolor{codegreen}{HTML}{008000} % Comments
    \definecolor{codetype}{HTML}{267F99}  % Types
    \definecolor{codegray}{HTML}{3B3B3B}  % Default text
    \definecolor{annotationgray}{HTML}{646695} % Annotations

    \lstdefinestyle{lightplus}{
        backgroundcolor=\color{white},
        basicstyle=\ttfamily\color{codegray},
        keywordstyle=\color{codeblue}\bfseries,
        commentstyle=\color{codegreen}\itshape,
        stringstyle=\color{codered},
        identifierstyle=\color{codegray},
        morekeywords={[2]String, int, boolean, void},       % types
        keywordstyle={[2]\color{codetype}\bfseries},
        morekeywords={[3]@Test, @Override},                  % annotations
        keywordstyle={[3]\color{annotationgray}},
        showstringspaces=false,
        numberstyle=\tiny\color{gray},
        numbers=left,
        numbersep=5pt,
        tabsize=4,
        breaklines=true,
        captionpos=b
    }
    ```
- Code 
    ```
    \begin{lstlisting}[style=lightplus, language=Javacaption={bubbleSort()}]
    package com.example;

    public class Main {
        public static void main(String[] args) {
            System.out.println("Hello world!");
        }
    }
    \end{lstlisting}
    ```



## Mathematik

### Allgemein darstellung:
- **Formeln im Text einfügen:** `$  $`, `\(  \)`
- **Rechnungen darstellen OHNE ZAHLEN:** `\begin{align*}`
- **Rechnungen darstellen MIT ZAHLEN:** `\begin{align}`
- **untereinander schreiben:** `&`, `&&`, `&&&`... z. B. `&=` 
- **neue zeile:** `\\`

### Mathematische darstellung
- **Einheiten einfügen:** `\SI{}{}` z. B. `\SI{10}{\kilo\volt}`
- **SI-Einheiten:** `\volt`, `\ampere`, `\ohm`, `\watt`, `\joule`, `\meter`, `\second`, `\kelvin`, `\mole`, `\candela`
- **Bruch:** `\frac{Zähler}{Nenner}` z. B. `\frac{a}{b}`
- **Wurzel:** `\sqrt{}` z. B. `\sqrt{a}`
- **Summe:** `\sum_{i=1}^{n} a_i`
- **Ausdruck mit Auswertungsstrich:** `\left. x + 2 \right|_{x=0}`
- **Produkt:** `\prod_{i=1}^{n} a_i`
- **Integral:** `\int_{a}^{b} f(x)\,dx`
- **Grenzwert:** `\lim_{x \to \infty} f(x)`
- **Vektor:** `\vec{a}`
- **Matrix:** `\begin{pmatrix} a & b \\ c & d \end{pmatrix}`
- **Ableitung:** `\frac{d}{dx} f(x)`
- **Partielle Ableitung:** `\frac{\partial}{\partial x} f(x)`
- **Summe mit Index:** `\sum_{k=1}^{n} k^2`
- **Delta:** `\Delta x`
- **Alpha, Beta, Gamma:** `\alpha`, `\beta`, `\gamma`
- **Ungefähr:** `\approx`
- **Gleich:** `=`
- **Ungleich:** `\neq`
- **Klein gleich / Groß gleich:** `\leq`, `\geq`
- **Pfeile:** `\rightarrow`, `\Leftarrow`, `\leftrightarrow`
- **Punkt:** `\cdot`
- **Klammern:** `\left(  \right)`, `\left{  \right}`, `\left[  \right]`
- **Index:** `U_{R_1}`
- **unendlich:** `\infty`
- **Texte einfügen:** `\text{}`

