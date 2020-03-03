# qasm2circ-tex
LaTeX integration of [qasm2circ](https://www.media.mit.edu/quanta/qasm2circ/). Tested on Overleaf.
Note that this implementation is UNOFFICIAL.


# Requirements
- Python 2
- pdflatex

# Usage
## usepackage
```latex
\usepackage{qasm2circ}
```
## Inline qasm
```latex
\begin{qasm}[teleport]
    qubit a,\psi
    qubit b,0
    qubit c,0
    def c-X,1,'X'
    def c-Z,1,'Z'
    H b
    cnot b,c
    cnot a,b
    H a
    nop b
    measure a
    measure b
    c-X b,c
    c-Z a,c
\end{qasm}
```
## Define qasm and use
```latex
\begin{defqasm}[teleport]
    qubit a,\psi
    qubit b,0
    qubit c,0
    def c-X,1,'X'
    def c-Z,1,'Z'
    H b
    cnot b,c
    cnot a,b
    H a
    nop b
    measure a
    measure b
    c-X b,c
    c-Z a,c
\end{defqasm}
```
For usage:
```latex
\useqasm{teleport}
```
or
```latex
\includegraphics[valign=c, max width=0.4\textwidth, max height=0.2\textheight]{\useqasmpdf{teleport}}
```

# Acknowledgements
[qasm2circ](https://www.media.mit.edu/quanta/qasm2circ/)
