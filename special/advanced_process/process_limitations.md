# 微細化に伴う限界と対応技術一覧

| 項目 | 限界・課題 | 対応技術・対策例 |
|------|------------|------------------|
| **ゲート酸化膜 (Tox)** | SiO₂ではリーク電流増加（トンネル電流） | High-k材料（例：HfO₂, ZrO₂） |
| **ゲート電極** | ポリSiのワークファンクション調整限界 | 金属ゲート（TiN, TaN, Wなど） + High-k |
| **配線材料** | Alは高抵抗・エレクトロマイグレーション（EM）に弱い | Cu配線 + Low-k絶縁膜 + ダマシン技術 |
| **リソグラフィ** | KrF以降、光の波長とパターン限界 | ArF Immersion、EUV、<br>OPC、SAQP、DSAなど |
| **SCE / DIBL** | 微細化で短チャネル効果（SCE）、ドレイン誘起障壁低下（DIBL） | FinFET、GAA（チャネル制御の3D化） |
| **信頼性劣化**<br>（EM / HCI / BTI / TDDB） | 高電界・高温動作で劣化加速、回路寿命を制限 | 耐熱材料、DFM設計、ガードリング配置など |
| **NBTI / PBTI** | High-k以降、PMOS/NMOSともに劣化が顕著 | HKMG技術への最適化、応力緩和設計 |

---

## 用語解説（抜粋）

- **SCE (Short Channel Effect)**：チャネル長の短縮によりゲート制御性が低下する現象。
- **DIBL (Drain-Induced Barrier Lowering)**：ドレイン電圧が高いとゲートの障壁が下がり、しきい値電圧が低下。
- **EM (Electromigration)**：電流密度の上昇で金属原子が移動、断線などの信頼性劣化を招く。
- **HCI (Hot Carrier Injection)**：高エネルギー電子が酸化膜に注入され、素子の特性が変化。
- **BTI (Bias Temperature Instability)**：しきい値電圧が時間と共にずれる現象。NBTIはPMOS、PBTIはNMOSに主に影響。
- **TDDB (Time Dependent Dielectric Breakdown)**：絶縁膜が時間経過とともに劣化・破壊する現象。
- **HKMG (High-k / Metal Gate)**：従来のSiO₂/ポリSi構造に代わり、高誘電率材料と金属ゲートを使用する技術。
