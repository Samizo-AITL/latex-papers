\section*{Reliability}

\subsection*{Endurance}
Program/erase (P/E) cycling up to $10^5$ operations exhibits less than 20\% degradation in the threshold-voltage window $\Delta V_{\mathrm{th}}$ (Fig.~\ref{fig:endurance}), consistent with reports on HfO$_2$-based FeFETs~\citep{mueller2015endurance,park2020nbdoping}.

\begin{figure}[t]
  \centering
  \IfFileExists{figs/endurance.pdf}{
    \includegraphics[width=0.85\linewidth]{endurance}
  }{
    \fbox{\parbox{0.85\linewidth}{
      \centering \vspace{18mm}
      \textbf{FIG PLACEHOLDER}\\[2mm]
      Put \texttt{figs/endurance.pdf} here.\\
      (Endurance at $V_{\mathrm{PGM}}=X$\,V, pulse $t=Y\,\mu$s)
      \vspace{18mm}
    }}
  }
  \caption{Endurance measured at $V_{\mathrm{PGM}} = X$\,V with pulse width $t = Y\,\mu$s.}
  \label{fig:endurance}
\end{figure}

\subsection*{Retention}
Retention is projected for 10 years at 85$^\circ$C using an Arrhenius activation model~\citep{Yamazaki2018}, in line with trends summarized in~\citep{schenk2019review}.
