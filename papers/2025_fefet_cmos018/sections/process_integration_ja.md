\section*{プロセス統合}

\subsection*{ベースラインと追加工程}
強誘電（FE）ゲートスタックはポリシリコン形成後に挿入される。追加工程は最小化されており，その概要を表\ref{tab:masks}に示す。図\ref{fig:flow}に，0.18\,$\mu$mロジックフローにおける配置を示す。

\begin{figure}[t]
  \centering
  \IfFileExists{figs/flow_overview.pdf}{
    \includegraphics[width=0.85\linewidth]{flow_overview}
  }{
    \fbox{\parbox{0.85\linewidth}{
      \centering \vspace{18mm}
      \textbf{図プレースホルダ}\\[2mm]
      \texttt{figs/flow_overview.pdf} を配置してください。\\
      （0.18\,$\mu$m ベースライン中のFeFET配置）
      \vspace{18mm}
    }}
  }
  \caption{0.18\,$\mu$m CMOS ベースライン中のFeFETモジュール配置。}
  \label{fig:flow}
\end{figure}

\begin{table}[t]
  \centering
  \caption{ベースラインに対する追加マスク／工程。}
  \label{tab:masks}
  \begin{tabular}{@{}lcc@{}}
    \toprule
    \textbf{工程} & \textbf{マスク} & \textbf{コメント}\\
    \midrule
    FE メタルゲート & +1 & アナログオプションマスクを流用\\
    FE アニール     &  0 & BEOL 炉で実施\\
    \bottomrule
  \end{tabular}
\end{table}

\subsection*{デバイススタック}
TiN / Hf$_{0.5}$Zr$_{0.5}$O$_2$（10\,nm, ALD）/ SiO$_2$界面層 / p型Si。

\subsection*{実装ノート}
1.8\,V/3.3\,V ベースラインに 1.8\,V FeFET オプションを追加。FeFET は 1.8\,V SRAM マクロの補助用途に限定し，大容量化は狙わない。Endurance・Retention・TDDB・歩留まりの課題はあるが，大規模アレイを想定しないため技術的難易度は下がる。0.18\,$\mu$m 老朽ラインの活用を前提に ALD 導入で対応可能。TiN 電極は既存 0.18\,$\mu$m のバリアスパッタ（ロングスロー／コリメータ）で形成可能。FeFET 形成は FEOL の Co サリサイド・ランプアニール後に挿入し，追加マスクは 1 枚でよい。
