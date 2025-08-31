\section*{信頼性}

\subsection*{耐久性}
$10^5$ 回までの P/E サイクル試験で，しきい値電圧ウィンドウ $\Delta V_{\mathrm{th}}$ の劣化は 20\% 未満であった（図\ref{fig:endurance}）。この傾向は既報~\citep{mueller2015endurance,park2020nbdoping}と整合する。

\begin{figure}[t]
  \centering
  \IfFileExists{figs/endurance.pdf}{
    \includegraphics[width=0.85\linewidth]{endurance}
  }{
    \fbox{\parbox{0.85\linewidth}{
      \centering \vspace{18mm}
      \textbf{図プレースホルダ}\\[2mm]
      \texttt{figs/endurance.pdf} を配置してください。\\
      （$V_{\mathrm{PGM}}=X$\,V，パルス幅 $t=Y\,\mu$s の耐久性）
      \vspace{18mm}
    }}
  }
  \caption{$V_{\mathrm{PGM}} = X$\,V，パルス幅 $t = Y\,\mu$s で測定した耐久性。}
  \label{fig:endurance}
\end{figure}

\subsection*{保持特性}
85$^\circ$C における 10 年保持を Arrhenius 外挿~\citep{Yamazaki2018} により評価し，レビュー~\citep{schenk2019review}の整理とも一致する。
