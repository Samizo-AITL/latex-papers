\subsection*{Baseline and Added Steps}
The ferroelectric (FE) gate stack is inserted after polysilicon definition. Additional process steps are minimized and summarized in Table~\ref{tab:masks}. Fig.~\ref{fig:flow} shows placement within the baseline.

\begin{figure}[!t]
  \centering
  \includegraphics[width=0.85\linewidth]{figs/flow_overview.pdf}
  \caption{Placement of the FeFET module within the 0.18\,\si{\micro\meter} CMOS baseline flow.}
  \label{fig:flow}
\end{figure}

\begin{table}[!t]
  \centering
  \caption{Added masks / process steps relative to baseline logic.}
  \label{tab:masks}
  \begin{tabular}{@{}lcc@{}}
    \toprule
    \textbf{Step} & \textbf{Mask} & \textbf{Comment}\\
    \midrule
    FE metal gate & +1 & Reuses analog option mask\\
    FE anneal     & 0  & Performed in BEOL furnace\\
    \bottomrule
  \end{tabular}
\end{table}

\subsection*{Device Stack}
TiN / Hf$_{0.5}$Zr$_{0.5}$O$_2$ (10\,nm ALD) / SiO$_2$ interfacial layer / p-Si.
