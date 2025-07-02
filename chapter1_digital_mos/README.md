# 第1章：デジタル基礎とMOSトランジスタの原理

本章では、半導体設計における「論理回路とMOSトランジスタ」の基礎を体系的に学びます。  
第0章で学んだ物性知識（PN接合やMOS構造）を土台として、以下のステップで論理回路設計の本質を理解していきます。

---

## 🔍 節構成

### 1.1 論理の基本（2進数・AND/OR/NOT）

- 0と1の世界、ビットと論理演算の基本  
- 真理値表による「完全な論理」の理解  
- ✅ すべてのデジタル回路はここから始まる

📄 [1.1_binary_logic.md](1.1_binary_logic.md)

---

### 1.2 論理ゲートの記号と組合せ

- AND / OR / NOT ゲートの図記号と接続法  
- 簡単な組み合わせ回路と出力の導出  
- 応用ゲート（NAND, NOR, XOR）への展開

📄 [1.2_logic_gates.md](1.2_logic_gates.md)

---

### 1.3 CMOSインバータの構造と動作

- PMOSとNMOSを組み合わせた反転回路の基本  
- 回路図とスイッチモデルによる直感的理解  
- 出力波形とトランジスタON/OFFの関係性

📄 [1.3_cmos_inverter.md](1.3_cmos_inverter.md)

---

### 1.4 MOSで構成する論理回路

- NAND / NOR をMOSトランジスタで実現する構成法  
- NMOS直列 / PMOS並列の基本ルール  
- 真理値と配線構造の対応関係を理解する

📄 [1.4_mos_logic_construction.md](1.4_mos_logic_construction.md)

---

### 1.5 電圧波形と遅延の基礎

- CMOS回路が時間軸で動作する理由  
- 伝搬遅延（propagation delay）の定義とRCモデル  
- 回路速度の限界・実務への応用視点

📄 [1.5_waveform_delay.md](1.5_waveform_delay.md)

---

### 1.6 まとめと設計への展開

- 章全体の学習内容を振り返り、実務設計との接点を整理  
- CMOS論理 → 標準セル設計 → SoC全体設計へつなぐ視野を獲得  
- RTL設計、PDK、タイミング設計への導入となる基礎

📄 [1.6_summary_and_next.md](1.6_summary_and_next.md)

---

## 🧾 フォルダ構成（v3.1対応）

```
chapter1_digital_mos/
├── 1.1_binary_logic.md
├── 1.2_logic_gates.md
├── 1.3_cmos_inverter.md
├── 1.4_mos_logic_construction.md
├── 1.5_waveform_delay.md
├── 1.6_summary_and_next.md
└── README.md  ← 本ファイル
```

旧構成のファイルはすべて `old/` フォルダに保存されています。

---

## 🔗 関連リンク

- 第0章（物性編）: [chapter0_semiconductor_basics/](../chapter0_semiconductor_basics/)
- 今後の実習計画（Sky130 / Python自動化）: [今後の展開](../#今後の展開v2x-以降)
