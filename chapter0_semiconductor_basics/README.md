# 第0章：半導体物性の基礎

## 📘 概要

この章では、「半導体とは何か？」という根本的な問いに答えるため、  
電子のふるまいや結晶構造、キャリア、PN接合といった**物性レベルの基礎知識**を学びます。

MOSトランジスタやデジタル回路の理解に必要な前提を、初学者にもわかりやすく解説する構成です。

---

## 🧭 学習の流れ

| セクション | 内容の要点 |
|------------|------------|
| [`00_what_is_semiconductor.md`](00_what_is_semiconductor.md) | 半導体の定義とバンド構造の基本、導体／絶縁体との違い |
| [`01_silicon_doping.md`](01_silicon_doping.md) | シリコン結晶とN型／P型ドーピングのしくみ |
| [`02_carrier_dynamics.md`](02_carrier_dynamics.md) | 電子・正孔の生成、移動、再結合と電流の成り立ち |
| [`03_pn_junction_basics.md`](03_pn_junction_basics.md) | 空乏層、内蔵電位、順・逆バイアスによる動作原理 |
| [`04_diode_iv_characteristics.md`](04_diode_iv_characteristics.md) | ダイオードのI-V特性とPythonでの演習可視化 |
| [`05_diode_applications.md`](05_diode_applications.md) | LED、ツェナー、フォトダイオード、太陽電池など応用紹介 |
| [`06_summary_and_mos_intro.md`](06_summary_and_mos_intro.md) | 学習内容のまとめと、MOS構造への導入的つながり |

---

## 🧠 この章で身につくこと

- 半導体における**電子と正孔の役割**が直感的に理解できる  
- **ドーピングとPN接合**の構造と動作原理を正確に説明できる  
- ダイオードのI-V特性を**数式・グラフ・応用**の3視点で把握できる  
- **MOSトランジスタの土台**となる空乏層・反転層の概念が身につく  

---

## 🔗 関連章への接続

本章で扱った「キャリア物理」「PN接合の振る舞い」は、  
第1章「デジタル基礎とMOSトランジスタの原理」で学ぶ**CMOS回路・インバータ・論理ゲート**に直結します。

📚【本章】物性 → 構造理解 → 【第1章】MOS動作 → デジタル論理

---

## 📂 フォルダ構成
```
chapter0_semiconductor_basics/
├── 00_what_is_semiconductor.md
├── 01_silicon_doping.md
├── 02_carrier_dynamics.md
├── 03_pn_junction_basics.md
├── 04_diode_iv_characteristics.md
├── 05_diode_applications.md
├── 06_summary_and_mos_intro.md
└── README.md
```
---

## 📜 ライセンス

本教材は **MITライセンス** に基づき公開されています。  
教育・研修・学習用途での自由な利用・改変・再配布を歓迎します。

---

## 👤 著者

**三溝 真一（Shinichi Samizo）**  
半導体デバイス技術エンジニア／技術教育コンテンツ制作者  

- GitHub: [@Samizo-AITL](https://github.com/Samizo-AITL)
