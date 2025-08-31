\section{Process Integration}

\subsection*{Baseline and Added Steps}
The ferroelectric (FE) gate stack is inserted after polysilicon definition. 
Additional process steps are minimized and summarized in Table~\ref{tab:masks}. 
Fig.~\ref{fig:flow} shows placement within the baseline.

% ===== Flow Overview Figure =====
\begin{figure}[t]
  \centering
  \begin{tikzpicture}[
    node distance=6mm,
    stage/.style={draw,rounded corners,minimum width=28mm,minimum height=6mm,align=center,font=\footnotesize},
    arr/.style={-{Stealth},thick}
  ]
    \node[stage] (act) {Active / Isolation};
    \node[stage,below=of act] (vt) {V\!T Adjust};
    \node[stage,below=of vt] (poly) {Poly Gate Definition};
    \node[stage,below=of poly] (ldd) {LDD / Spacer};
    \node[stage,below=of ldd] (imp) {Source/Drain Implant};
    \node[stage,below=of imp] (sal) {Salicide (Co)};
    \node[stage,below=of sal] (fefet) {FeFET Gate-Last Module\\
      (ALD IL/FE/CAP + TiN + RTA/FGA)};
    \node[stage,below=of fefet] (ild) {ILD + Vias};

    % arrows
    \draw[arr] (act) -- (vt);
    \draw[arr] (vt) -- (poly);
    \draw[arr] (poly) -- (ldd);
    \draw[arr] (ldd) -- (imp);
    \draw[arr] (imp) -- (sal);
    \draw[arr] (sal) -- (fefet);
    \draw[arr] (fefet) -- (ild);
  \end{tikzpicture}
  \caption{Placement of the FeFET gate-last module in the 0.18\,$\mu$m CMOS baseline flow.}
  \label{fig:flow}
\end{figure}

% ===== Table =====
\begin{table}[t]
  \centering
  \caption{Added masks / process steps relative to baseline logic.}
  \label{tab:masks}
  \begin{tabular}{@{}lcc@{}}
    \toprule
    \textbf{Step} & \textbf{Mask} & \textbf{Comment}\\
    \midrule
    FE metal gate & +1 & Reuses analog option mask\\
    FE anneal     &  0 & Performed in BEOL furnace\\
    \bottomrule
  \end{tabular}
\end{table}

\subsection*{Device Stack}
TiN / Hf$_{0.5}$Zr$_{0.5}$O$_2$ (10\,nm ALD) / SiO$_2$ interfacial layer / p-Si.

\subsection*{Implementation Notes}
The 1.8\,V / 3.3\,V CMOS baseline was extended with an additional 1.8\,V FeFET option. 
FeFET devices are used as auxiliary elements for 1.8\,V SRAM macros, not as large-scale memory blocks. 
Although challenges remain regarding endurance, retention, TDDB reliability, and yield, the technical difficulty is reduced since large array scaling is not targeted. 
The process integration is feasible within a legacy 0.18\,$\mu$m production line by introducing ALD deposition equipment. 
The TiN electrode can be formed using the existing 0.18\,$\mu$m barrier sputtering tools (long-throw or collimated). 
FeFET modules are inserted after FEOL Co salicide and lamp annealing, requiring only one additional mask step.
