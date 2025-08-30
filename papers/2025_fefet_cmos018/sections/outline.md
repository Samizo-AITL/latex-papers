# 論文アウトライン / Paper Outline

---

## 1. Abstract
- **日本語**：研究の目的・提案・成果を簡潔にまとめる。  
- *English*: Concise summary of objective, approach, and main contribution.  

---

## 2. Introduction
- **背景 / Background**  
  - 不揮発性メモリ（NVM）の進展とFeFETの位置づけ  
  - 22nm以降の先端ノードでは大容量化を目指す流れ  

- **課題 / Problem Statement**  
  - Endurance, Retention, TDDB の信頼性課題  
  - 車載・IoT用途に必要な長寿命要求とのギャップ  

- **本研究の提案 / Proposed Approach**  
  - 0.18 µm CMOS ラインに最小追加投資で FeFET を統合  
  - Gate-Last方式での HZO ALD導入＋TiNスパッタ流用  
  - FeFETは大容量ではなく「SRAM補助用途」に限定  

- **貢献ポイント / Contributions**  
  1. 老朽化CMOSライン活用の具体的な統合フロー  
  2. 信頼性課題を踏まえた「補助NVM戦略」提示  
  3. 車載/IoTにおける新しい応用方向性の提示  

---

## 3. Process Integration
- **Baseline 0.18 µm CMOS**（1.8V/3.3Vロジック）  
- **FeFET Gate-Last Module**  
  - ダミーゲート除去  
  - ALD: Al₂O₃ / HZO / Al₂O₃  
  - TiNゲート形成（既存スパッタ流用可）  
  - 熱予算（<500℃）管理  
- **モジュール統合図 / Integration Flow Diagram**  

---

## 4. Reliability Characterization
- **Endurance**（10⁴–10⁵ cycles、十分な範囲）  
- **Retention**（85℃で10³–10⁴ s 相当、125℃換算10年議論）  
- **TDDB**（酸素空孔由来のリークパス）  
- **Wake-up**（初期サイクルでのドリフト）  
- **戦略的割り切り**：「大容量化を狙わず補助用途に限定」  

---

## 5. Results & Discussion
- **E-test テンプレート**（Id–Vg, P/E cycling, Retention試験）  
- **SRAM+FeFET マクロ概念**  
  - Instant-On動作  
  - 設定値保持  
  - セキュアキー保存  
- **歩留まり・コスト改善シナリオ**  

---

## 6. Conclusion & Future Work
- **まとめ / Conclusion**  
  - 0.18 µm CMOS + FeFET Gate-Last の実現性  
  - 信頼性課題を踏まえた実用戦略  

- **今後の展望 / Future Work**  
  - 車載・IoTノードへの適用検証  
  - 材料改良（例：Nb添加）の研究的可能性  
  - 教材・教育的利用（edusemi連携）  
