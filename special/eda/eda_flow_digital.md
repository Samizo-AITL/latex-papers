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

```tcl
create_clock -name clk -period 10.0 [get_ports clk]
set_input_delay 2.0 -clock clk [get_ports in*]
set_output_delay 2.0 -clock clk [get_ports out*]
