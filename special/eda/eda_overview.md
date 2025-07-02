# 🛠️ eda_overview.md

## EDA（Electronic Design Automation）とは？

EDAは、半導体回路設計・検証・物理実装の各フェーズを**自動化・最適化**するためのツール群および技術体系です。  
数百万～数十億トランジスタ規模のLSIを、効率的かつ正確に開発するために不可欠な要素です。

---

## 🧭 全体フローと対応ツール

EDAフローは、大きく以下の5フェーズに分けられます：

| フェーズ | 内容 | 主なツール（オープン／商用） |
|----------|------|-------------------------------|
| 1. 回路設計（RTL/回路図） | Verilog/VHDLや回路図での機能設計 | Yosys, Vivado / Design Compiler, Virtuoso |
| 2. 検証（シミュレーション） | 論理シミュレーション・SPICE波形検証 | Verilator, ngspice / VCS, Spectre |
| 3. 論理合成 | RTLを標準セルネットリストへ変換 | Yosys / Design Compiler |
| 4. 物理設計（配置・配線） | セル配置、クロックツリー、配線 | OpenROAD / Innovus, IC Compiler II |
| 5. 設計検証・サインオフ | DRC, LVS, STA, PEX, GDS出力 | Magic, KLayout / Calibre, StarRC |

---

## 📦 EDAの基本構成要素

### ◾ HDL記述とシミュレーション

- **HDL言語**：Verilog / VHDL  
- **テストベンチ**：波形生成・自動比較による論理検証  
- **SPICEシミュレーション**：トランジスタレベルでの波形確認（アナログ向け）

### ◾ 論理合成（Synthesis）

- **入力**：RTL（Verilogなど）  
- **出力**：ゲートレベルネットリスト（.v）、タイミング情報（SDF）  
- **タイミング制約**：.sdc ファイルによるクロック・遅延設定

### ◾ 物理設計（Place & Route）

- **配置（Placement）**：標準セルをチップ領域に自動配置  
- **配線（Routing）**：配線制約を考慮し、メタル層を自動生成  
- **CTS**：クロックツリー合成（Clock Tree Synthesis）

### ◾ 設計検証（Signoff）

- **DRC**：デザインルール違反の検出（配線間隔、層制限など）  
- **LVS**：回路図とレイアウトの論理整合性を確認  
- **STA**：静的タイミング解析（Setup/Hold Margin確認）  
- **GDSII**：ファウンドリ提出用マスクデータ

---

## 🧰 オープンEDA vs 商用EDAの比較

| 項目 | オープンEDA | 商用EDA |
|------|-------------|----------|
| 代表ツール | Yosys, OpenROAD, Magic | Synopsys, Cadence, Siemens |
| 導入難易度 | やや高い（PDK整備が必要） | サポート充実で導入しやすい |
| 学習教材 | 豊富（Sky130など） | NDAの制限あり |
| 精度・機能 | 実務レベルまで進化中 | 高精度・大規模対応可 |

---

## 📚 教育・演習への活用

| 教育内容 | 演習例 |
|----------|--------|
| デジタル設計基礎 | RTL記述＋Yosys合成＋OpenROAD配置配線 |
| アナログ設計基礎 | 回路図入力＋ngspice波形検証＋Magicレイアウト |
| 検証の基礎 | DRC/LVSエラー解析・STAによるクロックマージン確認 |

---

## 🔗 関連ドキュメントへのリンク

- [eda_flow_digital.md](eda_flow_digital.md)：デジタル設計フローの詳細  
- [eda_flow_analog.md](eda_flow_analog.md)：アナログ設計フローとシミュレーション  
- [open_eda_tools.md](open_eda_tools.md)：オープンEDAツール一覧と使い方  
- [eda_scripting.md](eda_scripting.md)：EDAスクリプトによる自動化技術  
- [eda_vs_vendor.md](eda_vs_vendor.md)：商用EDAとの比較分析  

---

## 📄 ライセンス

この資料は MIT ライセンスに基づいて公開されています。教育目的・非営利での活用を歓迎します。
