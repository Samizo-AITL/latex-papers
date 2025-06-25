# EDA（Electronic Design Automation）

本ディレクトリでは、半導体設計におけるEDA（Electronic Design Automation）ツール群と設計フロー全体の理解を深めるための資料をまとめています。アナログ・デジタル回路設計における各フェーズの自動化、代表的なオープンソース/商用ツール、および設計スクリプトの実例を網羅します。

## 目的

- EDA設計フローの体系的理解
- オープンEDAツールの導入促進
- アナログ・デジタル両分野での実践的な設計演習支援
- PDK・設計ツールとの統合方法の把握

## 構成ファイル（予定含む）

| ファイル名 | 内容概要 |
|------------|----------|
| `eda_overview.md` | EDAの全体像とツールチェーン（論理合成、配置配線、レイアウト検証など） |
| `eda_flow_digital.md` | RTL設計からGDSII生成までのデジタル設計フロー（OpenROAD等の実例） |
| `eda_flow_analog.md` | 回路図入力からレイアウト・検証までのアナログ設計フロー（Magic/KLayout活用） |
| `open_eda_tools.md` | オープンEDAツール（Yosys, Magic, KLayout, ngspice等）の概要と使い方 |
| `eda_scripting.md` | EDA自動化スクリプト（SKILL, Tcl, Python等）の基礎と活用例 |
| `eda_vs_vendor.md` | 商用EDAとの比較（Cadence, Synopsys, Siemens）※非NDA範囲での技術解説 |

## 主なツール例

- **オープンEDA：**
  - RTL合成：Yosys
  - 配置配線：OpenROAD, TritonRoute
  - レイアウト：Magic, KLayout
  - 回路シミュレータ：ngspice, Xyce
- **商用EDA（参考）：**
  - Cadence Virtuoso, Innovus
  - Synopsys Design Compiler, IC Compiler
  - Siemens Calibre など

## 関連ディレクトリとの関係

- [`../pdk/`](../pdk/)：PDKとEDAツールの統合方法を補足
- [`../ams/`](../ams/)：アナログ設計対象としての実回路例
- [`../memory/`](../memory/)：SRAM等のマクロ設計におけるEDA活用

## 対象読者

- 回路設計に興味を持つ学生・初学者
- オープンEDAに関心のある研究者・開発者
- 商用EDAとの比較検討をしたい技術者

## ライセンス

MITライセンスのもと、教育・非営利目的で自由に活用できます。

---

今後、OpenLaneやSky130を使った実習テンプレート、DFTや物理検証フローの追加も予定しています。
