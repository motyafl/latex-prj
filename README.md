# latex-prj

Posting this for my future self better understanding of LaTeX language.
This will be a short guide with syntax basics and frequently used stuctures.

## Guide
### Packages

```
\documentclass{article}
\usepackage[a4paper, total={6in, 8in}]{geometry}

% Allow the usage of UTF-8 characters
\usepackage[utf8]{inputenc}

% Allow the usage of graphics (.png, .jpg)
\usepackage[T2A]{fontenc}

%Hyphenation rules
%--------------------------------------
\usepackage{hyphenat}
\hyphenation{ма-те-ма-ти-ка вос-ста-нав-ли-вать}
%--------------------------------------

\usepackage[english, russian]{babel}
\usepackage{wrapfig}
\usepackage{graphicx}
\usepackage{amsmath, amssymb}
```

### Titles and basic equations

Titles and subtitles
```
\paragraph{ Document Title }
\subsubsection*{ Subtitle }
```

Math sections in text
```
Функция $y=f(x)$ называется дифференцируемой в точке $x_0$, если ее приращение $\Delta y$ в этой точке можно записать в виде:
```

Equations
```
\[
 \Delta y = A\cdot\Delta x+\alpha (\Delta x)\cdot\Delta x\text{,}
\]

\begin{equation*}
 \Delta y = A\cdot\Delta x+\alpha (\Delta x)\cdot\Delta x\text{,}
\end{equation*}
```

### Math comments

In our course we write comments for math equations in brackets "[]".
For proper render I frequently used **\Bigr[** and **\left[**. 
Some examples:
```
% Single line comment
\Bigr[ \text{применим теорему о пределе суммы} \Bigr]

% Multi line commen
\begin{equation*}
  \Delta y = A\cdot\Delta x+\alpha(\Delta x)\cdot\Delta x =
    \left[
      \begin{aligned}
      & \text{по теореме о связи дифференцируемости} \\
      & \text{с существованием производной}
      \end{aligned}
    \right ] = f' (x_0)\cdot\Delta x+\alpha(\Delta x)\cdot\Delta x \text{,}
\end{equation*}
```

### Image fitting

On of the problem I faced was to fit the image into a small area alongsidethe text, and it can be done super sipmle. Just past this before the section of the text you want to fit the image in.

```
\begin{wrapfigure}{r}{0.2\textwidth}
  \centering % Center the image if needed
  \includegraphics[width=0.26\textwidth]{images/fun_1.png}
\end{wrapfigure}
```
