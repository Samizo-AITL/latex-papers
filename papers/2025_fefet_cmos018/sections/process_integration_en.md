\subsection*{Baseline and Added Steps}
We insert the FE gate stack after polysilicon definition; added steps are summarized in Table~\ref{tab:masks}.

% --- Figure (IEEEtran style) ---
\begin{figure}[!t]
  \centering
  \includegraphics[width=0.85\linewidth]{figs/flow_overview.pdf}
  \caption{Process module placement within the 0.18\,\si{\micro\meter} logic flow.}
  \label{fig:flow}
\end{figure}

% --- Table (IEEEtran style) ---
\begin{table}[!t]
  \centering
  \caption{Extra masks / steps compared to baseline.}
  \label{tab:masks}
  \begin{tabular}{@{}lcc@{}} % IEEEtran推奨の左右詰め
    \toprule
    \textbf{Item} & \textbf{Mask} & \textbf{Comment} \\
    \midrule
    FE metal gate & +1 & Shared with analog option \\
    Anneal (FE)   & 0  & Uses BEOL furnace \\
    \bottomrule
  \end{tabular}
\end{table}

\subsection*{Device Stack}
Gate: TiN / Hf$_{0.5}$Zr$_{0.5}$O$_2$ (10\,nm) / SiO$_2$ interfacial layer / p-Si.
