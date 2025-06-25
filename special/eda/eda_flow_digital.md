# デジタル設計フロー（EDA Flow for Digital IC Design）

本ドキュメントでは、デジタルLSI設計における典型的な設計フローを解説します。RTL設計からGDSII出力までを、主にオープンソースEDAツールを用いて段階的に紹介します。

---

## 1. はじめに

デジタルIC設計は大きく次のステップに分かれます：

1. RTL設計（Verilog/VHDL）
2. 論理合成（Synthesis）
3. タイミング制約設定
4. 配置・配線（Place & Route）
5. レイアウト検証（DRC, LVS）
6. GDSII出力（マスクデータ生成）

---

## 2. RTL設計

- **言語**：Verilog, VHDL（ここでは Verilog を前提）
- **記述内容**：
  - モジュール定義、信号の接続、FSM、加算器などの論理構造
- **ツール例**：
  - 任意のテキストエディタ（VS Code など）
  - シミュレーションには Icarus Verilog や Verilator を使用可能

---

## 3. 論理合成（Synthesis）

- **目的**：RTL → 論理ゲート（ネットリスト）変換
- **ツール例**：
  - Yosys（オープンソース論理合成ツール）
- **出力**：
  - `*.blif` や `*.json`（OpenROAD向け）
  - Verilog ネットリスト（ゲートレベル）

- **補足**：
  - セルライブラリ（libファイル）と結びつける必要がある（PDK由来）

---

## 4. タイミング制約（SDC）

- **目的**：クロック周波数やIO遅延の制約を指定し、タイミング最適化を導入
- **ファイル形式**：SDC（Synopsys Design Constraints）形式
- **記述例**：

tcl
create_clock -name clk -period 10.0 [get_ports clk]
set_input_delay 2.0 -clock clk [get_ports in*]
set_output_delay 2.0 -clock clk [get_ports out*]
```

## 5. 配置・配線（Place and Route）

- **目的**：物理配置・配線を行い、チップのレイアウトを生成
- **ツール例**：
  - OpenROAD（OpenROAD-flow-scripts）
    - Floorplanning
    - Placement (RePlAce)
    - Clock Tree Synthesis (CTS)
    - Global & Detail Routing

- **入力**：
  - 合成後ネットリスト（Verilog）
  - SDC制約
  - ライブラリ情報（.lef/.lib）

- **出力**：
  - レイアウト（DEF, GDSII）
  - 配置レポート、タイミングレポート

---

## 6. 検証（DRC / LVS）

- **DRC（Design Rule Check）**：
  - 物理レイアウトがプロセスルールに準拠しているか確認
  - Magic + DRC ルールファイルでチェック可能

- **LVS（Layout vs Schematic）**：
  - レイアウトとネットリストの一致確認
  - Netgen や KLayout + Spice で実施可能

---

## 7. GDSII出力

- **目的**：最終的なマスクデータ形式（GDSII）を生成
- **ツール例**：
  - Magic（`gds write` コマンド）
  - OpenROAD（flow末尾にGDS export機能あり）

---

## 8. 教育用途のオープンフロー例

- **Sky130 PDK + OpenLane**
  - GitHub: [https://github.com/The-OpenROAD-Project/OpenLane](https://github.com/The-OpenROAD-Project/OpenLane)
  - 包括的な自動フロー：RTL → GDSII
  - 含まれるツール：Yosys, OpenROAD, Magic, Netgen, KLayout, etc.

---

## 9. 補足：商用フローとの違い

| フェーズ       | オープンEDA            | 商用EDA                  |
| -------------- | ---------------------- | ------------------------ |
| 合成           | Yosys                  | Design Compiler          |
| 配置配線       | OpenROAD               | Innovus / ICC2           |
| 検証           | Magic, KLayout         | Calibre                  |
| タイミング解析 | OpenSTA                | PrimeTime                |

---

## 10. 今後の拡張予定

- Power / Clock ドメイン分割の実例（UPF/CPF対応）
- SoC構成における複数ブロック設計の扱い
- DFT（Design For Test）やDFM（Design For Manufacturability）との統合

---

## 参考リンク

- OpenROAD Project: https://theopenroadproject.org/
- SkyWater PDK: https://github.com/google/skywater-pdk
- Efabless Platform: https://platform.efabless.com/

