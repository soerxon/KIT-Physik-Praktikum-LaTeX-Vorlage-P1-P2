# KIT-Physik-Praktikum-LaTeX-Vorlage-P1-P2
Diese LaTeX-Vorlage ist geeignet für das Anfängerpraktikum P1 und P2 der Fakultät für Physik am Karlsruher Institut für Technologie. Es wird die Verwendung von Overleaf empfohlen.
Bei Fragen oder Problemen könnt ihr euch gerne an soeren@fachschaft.physik.kit.edu wenden.

## Verwendung
1. In die main.tex wird kein Inhalt geschrieben. Hier werden bei Bedarf benötigte Pakete hinzugefügt oder weitere Kapitel(Aufgaben) importiert.
2. Füllt die Datei Deckblatt.tex im Ordner chapters mit euren Daten aus.
3. Schreibt eure Einführung in den Versuch unter chapters/Einführung.tex. Im Inhaltsverzeichnis erhält die Einführung keine Kapitelnummer um die Aufgabennummer mit der Kapitelnummer gleich zu halten. Das macht es für die Tutor*innen und euch einfacher.
4. Jede Aufgabe wird seperat unter chapters in die passend nummerierte Datei geschrieben. Unter- und Unterunteraufgaben werden mit \section{Name der Unteraufgabe} und \subsection{} begonnen.
5. Anhänge wir Grafiken oder das Messprotokoll werden im Ordner include abgelegt. Es macht Sinn für jede Aufgabe einen Unterordner in include anzulegen um Ordnung zu bewahren. Somit könnt ihr die Grafiken schneller wieder finden, wenn sie ausgetauscht werden müssen.
6. Tauscht die Dateien Aufgabenblatt.pdf und Messptrotokoll.pdf durch das entsprechende Aufgabenblatt und euer eingescanntes, unterschriebenes Messprotokoll aus

## Copy-Paste Vorlagen
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
Grafiken einfügen

\begin{figure}[h] % h for here; t for top; b for bottom; ! overrides internal parameters LaTeX uses for determining "good" float positions
\centering Zentrieren der Grafik auf der Seite
\includegraphics[scale=0.3]{include/}
\caption{} % Grafiken haben Untertitel
\label{} % Label zum refenzieren mit \ref{}
\end{figure}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Tabellen einfügen

\begin{table}[!htb] % h for here; t for top; b for bottom; ! overrides internal parameters LaTeX uses for determining "good" float positions
    \centering % Zentrieren der Tabelle auf der Seite
    \caption{} % Tabellen haben Überschriften!
    \label{} % Label zum refenzieren mit \ref{}
    \begin{tabular}{c|c|c} % c steht für centering des Inhalts in der Spalte, mit | können weitere Spalten hinzugefügt werden
\toprule
Text & Text & Text\\
\midrule
Text & Text & Text\\
\hline
Text & Text & Text\\
\hline
Text & Text & Text\\
\bottomrule
    \end{tabular}
\end{table}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
Gleichungen

\begin{equation} % equation Umgebung wird für einzeilige Gleichungen verwendet
  a^2 + b^2 = c^2
  \laben{} % Label zum refenzieren mit \ref{}
\end{equation}

% align Umgebung wird für mehrzeilige Gleichungen verwendet. Die Gleichungen werden am Gleichheitszeichen (&=) ausgerichtet  
\begin{align}
  a^2 + b^2 &= c^2\\
  c^2 &= a^2 + b^2
  \label{} % Label zum refenzieren mit \ref{}
\end{align}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
Wertangaben

Entweder:
\begin{equation}
  \mathrm{Name} = \SI{Wert}{Einheit}
\end{equation}

oder
\begin{equation}
  \mathrm{Name} = Wert\,\mathrm{Einheit}
\end{equation}

Fehler-Rechnung Wertangabe

\begin{align}
  \mathrm{Name} = Wert \pm Wert \mathrm{(\delta_{stat})} \pm Wert \mathrm{(\delta_{sys})}\mathrm{Einheit}
\end{align}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Fußnote

% kann im Text eingebaut werden. Eine Fußnote erscheint im Text. Der Inhalt erscheint im Footer der Seite
\footnote{Quelle}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Listen erstellen

\begin{itemize}
\item Listenpunkt 1
\item Listenpunkt 2
\end{itemize}