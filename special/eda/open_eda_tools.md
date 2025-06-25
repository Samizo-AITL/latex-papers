# オープンEDAツールの紹介（Open Source EDA Tools）

本ドキュメントでは、半導体設計における主要なオープンソースEDAツールを紹介し、それぞれの役割や特徴、使いどころを解説します。

---

## 1. オープンEDAとは

- 商用EDAに対し、無償・オープンソースで利用可能なEDAツール群
- 学術研究や教育、個人開発者向けに注目されている
- フロー全体をカバーするためには複数ツールを組み合わせる必要がある

---

## 2. 主要ツール一覧と役割

| ツール名   | 用途                     | 代表的な特徴・備考                   |
|------------|--------------------------|------------------------------------|
| **Yosys**  | 論理合成（RTL → ネットリスト） | Verilog対応。軽量で拡張性あり。      |
| **OpenROAD** | 自動配置配線（P&R）          | フルフロー対応。OpenLANEと連携。    |
| **Magic**  | レイアウトエディタ・DRC      | 古典的ながら強力。教育用に最適。    |
| **KLayout**| レイアウトビューア・LVS     | 豊富なスクリプト機能と拡張性。      |
| **Netgen** | LVS（Layout vs Schematic） | LVSチェック用の標準ツール。         |
| **ngspice**| 回路シミュレータ            | SPICE互換のシミュレータ。           |
| **Verilator**| RTLシミュレータ            | 高速Verilogシミュレーション。       |

---

## 3. ツールの組み合わせ例

- **RTL設計・シミュレーション**  
  - Verilog → Verilatorで機能検証  
- **論理合成**  
  - Yosysで合成しゲートレベルネットリスト生成  
- **配置配線**  
  - OpenROADを使い物理設計まで自動化  
- **レイアウト検証**  
  - Magic/KLayoutでDRC  
  - NetgenでLVS比較  
- **回路シミュレーション**  
  - ngspiceでアナログ動作検証（AMS設計時）

---

## 4. オープンEDAのメリット・課題

### メリット

- 無償で使用できる
- ソースコードが公開されておりカスタマイズが可能
- 教育や研究に適している
- コミュニティによる活発な改善

### 課題

- 商用製品に比べ機能や安定性で劣る場合がある
- ツール連携に熟練が必要
- サポートがコミュニティベース

---

## 5. 代表的なプロジェクト・リポジトリ

- OpenROAD Project: https://github.com/The-OpenROAD-Project/OpenROAD  
- Yosys: https://github.com/YosysHQ/yosys  
- Magic VLSI: https://github.com/RTimothyEdwards/magic  
- KLayout: https://www.klayout.de/  
- ngspice: http://ngspice.sourceforge.net/  

---

## 6. 学習リソース・参考資料

- 「オープンEDAツールによる半導体設計フロー入門」  
- OpenROADのチュートリアル動画・ドキュメント  
- 各ツールの公式Wiki、GitHub Issue

---

## 7. 今後の展望

- フルオープンフローによる設計・製造の民主化  
- AIを活用した自動最適化ツールの統合  
- 高度な物理検証ツールのオープン化  

---

## 参考リンク

- The OpenROAD Project: https://theopenroadproject.org/  
- Efabless OpenLane Flow: https://github.com/The-OpenROAD-Project/OpenLane  
