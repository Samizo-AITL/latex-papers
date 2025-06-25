# ノード技術進化一覧表（リソグラフィ・配線・OPC視点）

| ノード     | Tox (nm)   | Vdd (V)     | リソグラフィ           | トランジスタ構造        | High-k / MG | Low-k | 配線          | RET技術（OPC等）               | 備考・用途                      |
|------------|------------|-------------|--------------------------|--------------------------|--------------|--------|---------------|-------------------------------|-------------------------------|
| 0.35µm     | ~15        | 3.3–5.0     | i線 (365nm)              | プレーナ（LOCOS）         | ×            | ×      | Al            | 手動補正                         | 初期量産、高耐圧混載             |
| 0.25µm     | ~8–10      | 2.5–3.3     | i線 / KrF                | プレーナ（LOCOS）         | ×            | ×      | Al            | OPC（第1世代）                   | フォト抵抗特性重要               |
| 0.18µm     | ~4–5       | 1.8–2.5     | KrF                      | プレーナ（STI）           | ×            | ×      | Al            | Rule-based OPC                | アナログ混載、量産期             |
| 0.13µm     | ~2.5–3.0   | 1.2–1.5     | KrF                      | プレーナ                  | ×            | ×      | Al / Cu一部   | Model-based OPC開始            | OPC自動化・収差補正              |
| 90nm       | ~2.0       | ~1.2        | KrF / ArF                | プレーナ                  | High-k検討    | 初期導入 | Cu            | Assist Bar、SRAF              | Maskバイアス問題発生            |
| 65nm       | ~1.8       | ~1.1        | ArF                      | プレーナ限界              | ×            | ◯      | Cu            | ハーフトーン / SRAF             | パターン歪補正が深刻             |
| 45nm       | ~1.2–1.5   | ~1.0        | ArF Immersion            | FinFET準備期              | △            | ◯      | Cu            | OPC高度化、RET統合             | デザイン協調の始まり            |
| 32nm       | ~1.0–1.2   | ~0.9        | ArF Immersion            | FinFET導入                | ◯            | ◯      | Cu            | DPT導入、Inverse OPC           | OPC処理負荷激増                  |
| 22nm       | ~0.9       | ~0.9        | ArF Immersion            | FinFET                    | ◯            | ◯      | Cu            | DPT + SMO                     | マスク工程がボトルネックに       |
| 14/10nm    | ~0.8       | ~0.8        | ArF Imm. + DPT           | FinFET                    | ◯            | ◯      | Cu            | DPT強化、EUV準備               | OPC演算肥大、光学限界            |
| 7nm        | ~0.7       | ~0.7        | EUV（限定）              | FinFET                    | ◯            | ◯      | Cu            | EUV + OPC併用                  | EUVでもOPC不要ではない           |
| 5nm        | ~0.6       | ~0.7        | EUV主流                  | FinFET                    | ◯            | ◯      | Cu            | EUV OPC + Mask Blanking       | Mask Error Factorが顕著          |
| 4nm        | ~0.5–0.6   | ~0.65–0.7   | EUV                      | GAA（Nanosheet）          | ◯            | ◯      | Cu or hybrid  | EUV OPC + DFM融合             | PSM最適化と密接連携             |
| 3nm        | ~0.4–0.5   | ~0.6–0.7    | EUV                      | GAA                        | ◯            | ◯      | Cu or hybrid  | EUV + Inverse Lithography     | マスク製造費高騰・自動補正不可欠 |
| 2nm        | ~0.3–0.4   | ~0.5–0.6    | EUV + High-NA            | GAA（Ribbon）             | ◯            | ◯      | Cu or hybrid  | High-NA対応OPC + AI搭載         | 高NA + AIによる補正進行中         |

---

## 技術進化の観点まとめ

- **リソグラフィ**：`i線 → KrF → ArF → ArF Immersion → EUV → High-NA EUV`
- **トランジスタ構造**：`プレーナ → FinFET → GAA（Nanosheet → Ribbon）`
- **配線材料と絶縁膜**：`Al → Cu + Low-k → Cu/Hybrid（将来Ru等）`
- **OPC進化**：
  - 手動補正 → Rule-based OPC → Model-based OPC → Inverse OPC（EUV以降）
  - EUVになっても **OPCは不要にならず、むしろ複雑化**（Mask Error対策、SMO連携）
- **設計最適化との融合**：
  - 32nm以降：**OPCと設計（DFM）の協調**
  - 7nm以降：**EUVとOPCの統合**
  - 2nm以降：**AIによる高精度補正（Inverse Lithography / SMO）**
