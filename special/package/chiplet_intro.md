# 🧩 チップレットと2.5D/3D実装の基礎

---

## 📝 はじめに

チップレット（Chiplet）とは、SoCを一枚の大規模ダイとして製造するのではなく、**機能ごとに分割した小さなダイ（IPブロック）を、パッケージ上で接続する手法**です。これにより、歩留まり改善、コスト最適化、再利用性の向上が図れます。

---

## 🧱 チップレット化の背景

- **微細化コストの増大**  
  最先端ノードで大規模SoCを作ると歩留まりが悪化し、コストが急上昇します。
  
- **IPの再利用・分割統治設計**  
  アナログ/RF/IOなどを別ダイに分けて再利用。設計のモジュール化が可能になります。

- **異種統合（Heterogeneous Integration）**  
  同一パッケージ内に、ロジック、メモリ、RF、光I/O、センサなどを異なる技術ノードで集積可能。

---

## 📐 実装方式の種類

| 手法      | 概要 | 代表例 |
|-----------|------|--------|
| **2.5D**  | シリコンインターポーザ上に複数チップを配置。中継配線あり | Xilinx Virtex UltraScale+, TSMC CoWoS |
| **3D IC** | チップを**縦に積層**。TSVなどを用いて垂直接続 | Intel Foveros, Samsung ePop |
| **Fan-Out** | 配線層を拡張し、チップ間を**RDL（再配線層）**で接続 | TSMC InFO, ASE FOCoS |

---

## 🧰 接続技術の例

- **TSV（Through Silicon Via）**  
  チップ貫通型ビア。3D積層接続に不可欠。
  
- **インターポーザ（Silicon/GaAs/RDL）**  
  中継基板。高密度配線が可能で、2.5D実装に用いられる。
  
- **マイクロバンプ / Hybrid Bonding**  
  極小ピッチでの低抵抗・低寄生容量接続。

---

## 🏢 実例紹介（代表的チップレット製品）

| メーカー | プラットフォーム | 特徴 |
|----------|------------------|------|
| AMD      | Infinity Fabric + Chiplet | CPU/IO分離構造（Ryzen/EPYC） |
| Intel    | Foveros + EMIB           | 3D積層+インターポーザ融合技術 |
| Apple    | Mシリーズ（M1〜）        | チップレットとは別路線の大規模モノリシック設計も参考に比較 |

---

## ⚠️ 設計上の課題

- **インターコネクト仕様の非互換**  
  各社が独自方式を採用し、IPの再利用性や他社との連携に制限がある。

- **熱・応力設計の複雑化**  
  異種材料・異なる消費電力・積層構造により、温度分布や反りの制御が困難になる。

- **テスト工程の煩雑化**  
  複数ダイの接続性・歩留まりの個別評価が必要。

---

## 🔗 関連技術と規格化動向

- [UCleT（Universal Chiplet Interconnect）](./uclet_intro.md)  
  異ベンダーチップ間の相互接続標準規格

- BoW（Bunch of Wires） by CHIPS Alliance  
  シンプルな物理層ベース接続の標準化

- UCIe（Universal Chiplet Interconnect Express）  
  PCIe世代互換の高帯域チップ間接続標準

---

## 📷 例図（図挿入位置）

> ※画像ファイルは `./images/chiplet_interposer_example.png` に格納してください

```text
[イメージ図例]：
+--------------------------+
|      Package Substrate   |
|  +---------+  +--------+ |
|  | Chiplet |  | Chiplet| |
|  +---------+  +--------+ |
|         ↑    ↑          |
|     Microbump / TSV     |
|         ↓    ↓          |
|     Interposer Layer    |
+--------------------------
```

## 🧠 演習課題（任意）

次のトピックについて、調査・比較を行ってみましょう：

	•	TSMC CoWoS、Intel Foveros、AMD Infinity Fabric のチップレット接続方式の違い
	•	「モノリシックSoC vs チップレット化」の設計・製造コストの比較
	•	将来的にUCleTなどの標準規格が持つ業界的意義

---

## 📝 参考リンク
	•	Open Compute Project - UCleT
	•	TSMC CoWoS技術概要 (TSMC公式)
	•	IEEE Spectrum – Why Chiplets Are the Future

