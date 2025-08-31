\subsection*{Endurance}
Program/erase (P/E) cycling induces gradual memory-window shrinkage due to domain pinning and interface charge trapping in Hf$_{0.5}$Zr$_{0.5}$O$_2$ (HZO). In our 0.18\,$\mu$m flow targeting 1.8\,V operation, we use internal charge pumps to apply $\pm(2.3\text{–}2.7)$\,V, $t_\mathrm{pulse}=1\text{–}50\,\mu\mathrm{s}$ for cycling. Devices typically sustain $10^4\text{–}10^5$ cycles before $\Delta V_\mathrm{th}$ degrades by $\sim$20–30\%, consistent with literature trends~\citep{mueller2015endurance,Khan2015}.

\begin{figure}[t]
  \centering
  \begin{tikzpicture}
    \begin{axis}[
      width=0.85\linewidth,
      height=5.2cm,
      xlabel={P/E Cycles},
      ylabel={Memory Window $\Delta V_\mathrm{th}$ [V]},
      xmode=log,
      xmin=1e2, xmax=1e6,
      ymin=0, ymax=2.0,
      grid=both,
      legend pos=south west,
      legend style={font=\footnotesize, cells={anchor=west}},
      tick label style={/pgf/number format/fixed}
    ]
      % Schematic trend for two pulse conditions
      \addplot[thick,mark=*] coordinates {
        (1e2,1.6) (1e3,1.55) (1e4,1.35) (1e5,1.10)
      };
      \addlegendentry{$\pm 2.5$ V, $10\,\mu$s}

      \addplot[thick,dashed,mark=square*] coordinates {
        (1e2,1.7) (1e3,1.60) (1e4,1.40) (1e5,1.20)
      };
      \addlegendentry{$\pm 2.7$ V, $5\,\mu$s}
    \end{axis}
  \end{tikzpicture}
  \caption{Schematic endurance behavior of HZO-FeFETs in a 0.18\,$\mu$m flow. Memory window decreases with cycling; shorter pulses at slightly higher voltage can trade off endurance and speed.}
  \label{fig:endurance}
\end{figure}

\subsection*{Retention and Wake-up}
Retention at elevated temperature is assessed via Arrhenius extrapolation~\citep{Yamazaki2018}. With an activation energy example $E_a\approx0.6\text{–}0.8$\,eV, data acquired at $T=\{25,~85\}\,^\circ$C and $10^3\text{–}10^5$\,s map to $>$10-year window retention at 85\,$^\circ$C for the auxiliary-NVM use case when an initial $\Delta V_\mathrm{th}\sim 0.8\text{–}1.0$\,V is ensured. Early-cycle “wake-up” typically enlarges the window over the first $10^2\text{–}10^3$ P/E cycles as domains stabilize~\citep{boscke2011hafnium,mueller2012fefet}.

\begin{figure}[t]
  \centering
  \begin{tikzpicture}
    \begin{axis}[
      width=0.85\linewidth,
      height=5.2cm,
      xlabel={Time $t$ [s] (log scale)},
      ylabel={Normalized Window $\Delta V_\mathrm{th}(t)/\Delta V_\mathrm{th}(t_0)$},
      xmode=log,
      xmin=1e0, xmax=1e6,
      ymin=0.5, ymax=1.05,
      grid=both,
      legend pos=south west,
      legend style={font=\footnotesize, cells={anchor=west}},
      tick label style={/pgf/number format/fixed}
    ]
      \addplot[thick,mark=*] coordinates {
        (1e0,1.00) (1e2,0.98) (1e3,0.96) (1e4,0.93) (1e5,0.90) (1e6,0.88)
      };
      \addlegendentry{$85\,^\circ$C projection}

      \addplot[thick,dashed,mark=square*] coordinates {
        (1e0,0.95) (1e1,0.98) (1e2,1.00) (1e3,1.01) (1e4,1.01)
      };
      \addlegendentry{Wake-up (early cycles)}
    \end{axis}
  \end{tikzpicture}
  \caption{Retention (Arrhenius-projected) and early-cycle wake-up illustration. For auxiliary-NVM targets, a normalized window $\gtrsim 0.7$ over mission lifetime is sufficient for robust sensing.}
  \label{fig:retention}
\end{figure}

\subsection*{TDDB and Gate Stack Considerations}
Time-dependent dielectric breakdown (TDDB) in HZO stacks is impacted by oxygen-vacancy–mediated leakage paths and interfacial layer quality. A thin Al$_2$O$_3$ interfacial layer (1–2\,nm) deposited by ALD and a moderate crystallization anneal (RTA 450–500\,$^\circ$C) help suppress leakage while promoting the FE orthorhombic phase~\citep{polakowski2014reliability,schenk2019review}. Write voltages are limited to $\pm(2\text{–}3)$\,V to bound oxide stress during P/E.

\subsection*{Yield and Variability}
Cycle-to-cycle variability and device-to-device spread remain larger than in logic MOSFETs, constraining bit-cell scaling for large arrays. In this work, FeFETs are positioned as **auxiliary NVM** (instant-on, SRAM state backup, key storage) rather than high-density arrays—relaxing variation/yield requirements while preserving system-level value for automotive/IoT.

\subsection*{Test Conditions (Reference)}
\begin{itemize}
  \item HZO thickness: 8–12\,nm (ALD), Al$_2$O$_3$ IL: 1–2\,nm; TiN gate 30–50\,nm.
  \item Gate area (test FETs): $W/L=\{10/0.18,~5/0.18\}\,\mu$m; retention caps optional for E-test.
  \item P/E bias: $\pm(2.3\text{–}2.7)$\,V, $t_\mathrm{pulse}=1\text{–}50\,\mu$s, 10\,kHz max burst.
  \item Retention: $25/85\,^\circ$C, $10^3\text{–}10^5$\,s, Arrhenius projection to 10\,yr at $85\,^\circ$C.
  \item Read: $V_\mathrm{DS}=50$\,mV, $I_\mathrm{D}$–$V_\mathrm{G}$ double-sweep (2 loops).
\end{itemize}

\subsection*{Positioning Summary}
By not pursuing large-capacity FeFET arrays and keeping the role to **small auxiliary NVM blocks** supporting 1.8\,V SRAM macros, the integration fits legacy 0.18\,$\mu$m lines with minimal modules (ALD + TiN sputter reuse), while meeting endurance/retention windows required by embedded use cases~\citep{mitsubishi2003automotive,park2020nbdoping}.
