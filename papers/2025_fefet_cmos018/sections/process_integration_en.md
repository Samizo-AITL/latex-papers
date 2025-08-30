\subsection*{Baseline and Added Steps}
We insert the FE gate stack after polysilicon definition; added steps are summarized in Table~\ref{tab:masks}.

% --- Figure (safe LaTeX in md) ---
\begin{figure}[t]
  \centering
  \includegraphics[width=.8\linewidth]{figs/flow_overview.pdf}
  \caption{Process module placement within the 0.18\,\si{\micro\meter} logic flow.}
  \label{fig:flow}
\end{figure}

% --- Table ---
\begin{table}[t]
  \centering
  \caption{Extra masks / steps vs. baseline.}
  \label{tab:masks}
  \begin{tabular}{lcc}
    \toprule
    Item & Mask & Comment\\
    \midrule
    FE metal gate & +1 & Shared with analog option\\
    Anneal (FE)   & 0  & Inherits BEOL furnace\\
    \bottomrule
  \end{tabular}
\end{table}

\subsection*{Device Stack}
Gate: TiN / Hf$_{0.5}$Zr$_{0.5}$O$_2$ (10\,nm) / SiO$_2$ interfacial layer / p-Si.
