# latextemplate
LaTex Template für wissenschaftliche Arbeiten.

# Todos
- Anleitung zur Nutzung des Templates erweitern 
- Template bereinigen

# Nutzung
Ladet euch das aktuelles Release herunter und nutzt ein völlig Funktionsfähiges LaTex-Template für wissenschaftliche Arbeiten.

# Credits
sebastianreinig.de

# Allgemeine Hinweise
.tex Files werden von einem LaTeX Compiler kompiliert. Dabei entstehen zunächst .aux, .log, und .dvi Files. Aus dem .dvi File kann ein PS (PostScript) oder direkt ein PDF Dokument erzeugt werden. Die Kompilierung kann auf der Command Line z. B. mit dem Befehl latex gestartet werden, sie kann aber auch durch ein Tool mit grafischer Oberfläche ausgelöst werden. Die entsprechende Software muss dafür installiert sein. Eine Beschreibung des Vorgehens mit einem grafischen Tool unter macOS ist unten zu finden.  

# Verwendung des Templates mit Hilfe von TeXShop unter macOS
## Typesetting
TeXShop kann man [hier](https://pages.uoregon.edu/koch/texshop/obtaining.html) herunterladen. Es ist kostenlos.

Grundsätzlich wird als Ausgangsbasis für die Kompilierung das File bib.tex verwendet, da es die Deklaration des "documents" 
```
\begin{document}
```
beinhaltet. In TeXShop kann auf 'Typeset' geklickt werden, um ein PDF aus dem .tex File zu erzeugen. Die einzelnen Kapitel werden im content Verzeichnis abgelegt. Werden weitere Kapitel-Files angelegt, dann sind diese in das bib.tex File einzufügen. 
```
\include{content/chapter_n}
```

## Einfügen eines Literaturverzeichnisses
Literaturquellen werden in (mindestens einem) .bib File gepflegt. Das File ist im Template bereits an der richtigen Stelle in bib.tex eingefügt. 
````
\addbibresource{bib.bib}
````
Um das Literaturverzeichnis zu bearbeiten, wird von TeXShop das Programm BibDesk mitgeliefert. Dort können die Literaturquellen verwaltet werden. Die Optionen, die für das Zitieren sowie das Literaturverzeichnis von Bedeutung sind, werden im File preamble.tex bearbeitet. Es wird das Package biblatex verwendet.

Um das Literaturverzeichnis zu erzeugen, sind Befehle auf der Command Line auszuführen.  Dazu zählt zunächst die Kompilierung mit
```
latex bib.tex
```

sowie die Ausführung von
```
biber bib 
```

im Verzeichnis latextemplate/template. Danach ist (mindestens einmal) das PDF per 'Typeset' zu erzeugen. 

... weitere Infos folgen in Kürze.
