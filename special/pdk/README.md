# 🔧 PDK Documentation Hub

本リポジトリは、**PDK（Process Design Kit）**に関する包括的な技術資料をまとめたものです。  
PDKの基礎から、ベンダー間の違い、プロセスバリエーション対応、設計フローへの適用方法、オープンソースPDKの活用までを網羅的に扱います。

---

## 📂 ファイル構成

| ファイル名 | 内容概要 |
|------------|----------|
| [`pdk_overview.md`](pdk_overview.md) | PDKの基本構成、目的、主要コンポーネント（DRC, LVS, Pcells, SPICEなど）についての総論 |
| [`pdk_process_variants.md`](pdk_process_variants.md) | 同一PDK内のプロセスバリエーション（High-Vt/Low-Vt、thick/thin oxideなど）とその選定基準 |
| [`pdk_usage_in_flow.md`](pdk_usage_in_flow.md) | Schematic → Layout → Simulation → Signoff の設計フローにおけるPDK活用ポイントと統合方法 |
| [`pdk_vendor_comparison.md`](pdk_vendor_comparison.md) | 商用PDKベンダー間の比較（TSMC, GF, Intel, Samsungなど）とそれぞれの特徴・用途 |
| [`pdk_open_source.md`](pdk_open_source.md) | SkyWater 130nm, Google/Sky130, IHP等のオープンPDKの現状・利活用例・制約 |

---

## 🎯 対象読者

- ASIC / SoC 設計者  
- アカデミック向けEDA教育者・研究者  
- オープンPDK・チップ設計に関心のある個人開発者や教育関係者  

---

## 📘 主なトピック

- PDKとは何か？なぜ必要か？  
- 商用PDKとオープンPDKの比較  
- プロセスバリエーションへの対応設計  
- スマートPDK / PDK自動生成への展望  

---

## 📄 ライセンス

本リポジトリの内容は **MITライセンス** のもと公開されています。  
教育・非営利目的での利用を歓迎します。

---

## 🔮 今後の予定

- PDKリバースエンジニアリングに関する技術ノート（予定）  
- Sky130ベースの実習教材例（回路設計・レイアウト演習）  

---

## 🤝 コントリビューション

Pull Request / Issue は歓迎です。特に以下の観点での貢献をお待ちしています：

- オープンPDKの追加事例  
- 商用PDKの運用知見（**非NDA範囲内**）  
- 設計フロー統合ツール（Magic, KLayout, OpenROADなど）との連携情報  
