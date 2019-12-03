\newcommand{\snII}[5]{#1: \left( \begin{matrix} {#2} & {#4} \\ #3 & #5 \end{matrix} \right)}
\newcommand{\snIV}[9]{#1: \left( \begin{matrix} {#2} & {#4} & {#6} & {#8} \\ #3 & #5 & #7 & #9 \end{matrix} \right)}
\newcommand{\sII}[3] {#1: \left( \begin{matrix} s_1 & s_2 \\ #2 & #3 \end{matrix} \right)}
\newcommand{\sIII}[4] {#1: \left( \begin{matrix} s_1 & s_2 & s_3 \\ #2 & #3 & #4 \end{matrix} \right)}
\newcommand{\sIV}[5] {#1: \left( \begin{matrix} s_1 & s_2 & s_3 & s_4 \\ #2 & #3 & #4  & #5 \end{matrix} \right)}
\newcommand{\sVI}[7] {#1: \left( \begin{matrix} s_1 & s_2 & s_3 & s_4 & s_5 & s_6 \\ #2 & #3 & #4 & #5 & #6 & #7\end{matrix} \right)}
\newcommand{\sVIII}[9] {#1: \left( \begin{matrix} s_1 & s_2 & s_3 & s_4 & s_5 & s_6 & s_7 & s_8\\ #2 & #3 & #4 & #5 & #6 & #7 & #8 & #9 \end{matrix} \right)}
\newcommand{\fIoII}{\frac{1}{2}}
\newcommand{\fIoIII}{\frac{1}{3}}
\newcommand{\fIoIV}{\frac{1}{4}}
\newcommand{\fIoV}{\frac{1}{5}}
\newcommand{\fIoVI}{\frac{1}{6}}
\newcommand{\fIoVII}{\frac{1}{7}}
\newcommand{\fIoVIII}{\frac{1}{8}}
%\addtobeamertemplate{block begin}{}{\setlength{\parskip}{35pt plus 1pt minus 1pt}}
%\addtobeamertemplate{block begin}{}{\setlength{\parskip}{35pt plus 1pt minus 1pt}}
 
%\usetheme{default}
\usetheme{Madrid}
\setbeamertemplate{footline}{} % disable footer
%\usecolortheme{whale}
\setbeamertemplate{itemize items}[default]
\setbeamertemplate{enumerate items}[default]
\setbeamercolor{section name}{fg=white}  % Make section number white so it's not visible, see https://tex.stackexchange.com/a/468134
\setbeamercolor{subsection name}{fg=white}  % Make section number white so it's not visible, see https://tex.stackexchange.com/a/468134

\setbeamersize{text margin left=15pt}

\newcommand{\grtlessH}{\underset{{H_0}}{\overset{H_{1}}{\gtrless}}}
\renewcommand{\vec}[1]{\mathbf{#1}}
\newcommand*{\underuparrow}[1]{\ensuremath{\underset{\uparrow}{#1}}} 
\newcommand{\erf}{\operatorname{erf}}
\newcommand{\maketiny}[1]{\begingroup\tiny #1 \endgroup}

\usepackage{algorithm}
\usepackage{algorithmic}
\usepackage{bm}
