# 💾 メモリ技術入門

📌 本資料は「edusemi」リポジトリの特別編として構成されています。  
メインの第1〜6章に加え、**半導体メモリ技術に関する応用的・実務的な知識**を補足する目的で作成されています。

---

## 📘 概要

SoC（System-on-Chip）設計では、演算処理や制御回路だけでなく、**適切なメモリ構成の選定**が製品の性能・コスト・消費電力に直結します。  
中でもSRAMは、論理プロセスに直接統合可能な「組込みメモリ」として広く使われており、**SRAMマクロの活用**は設計上の基本スキルの一つです。

本特別編では、SRAMを起点としてDRAM、FeRAM、MRAM、3D NANDまで、メモリ技術の全体像を実務視点で整理し、**SoC設計との関係を意識した技術理解**を深めることを目的としています。

---

## 📂 セクション構成（ロジック親和性順）

| ファイル | 内容概要 |
|---------|----------|
| [`sram.md`](./sram.md)       | SRAM（Static RAM）：SoC内部キャッシュやレジスタファイルとして統合される高速揮発性メモリ |
| [`dram.md`](./dram.md)       | DRAM（Dynamic RAM）：外部メモリとして構成されるメインメモリ用途（LPDDR/DDR系など） |
| [`feram.md`](./feram.md)     | FeRAM（強誘電体RAM）：アナログ/ロジック混載LSI向け。高速・不揮発・高書換え耐性 |
| [`mram.md`](./mram.md)       | MRAM（磁気RAM）：不揮発メモリの注目技術。STT/SOT-MRAMが今後のSoC統合候補 |
| [`3dnand.md`](./3dnand.md)   | 3D NANDフラッシュ：ストレージ系不揮発メモリ。大容量・低コストだが階層的な扱いが必要 |

---

## 🎯 対象読者

- 半導体の基本構造を理解した初学者  
- SoC設計におけるメモリ技術選定に関心のある若手エンジニア  
- 教育機関・教材開発に関わる関係者  

---

## 🔧 今後の展開（予定）

- 次世代メモリ（ReRAM, PCMなど）の追加  
- システム応用（キャッシュ設計、メモリマップ構成）の補足  
- メモリ選定と消費電力・性能バランスの設計観点の提示  

---

## 🔗 本リポジトリのメイン章（参照推奨）

本資料は「特別編」であり、以下の **第1〜6章が本編の中心** です。  
まずはこちらを学習することを強く推奨します：

| 章 | 内容 | 最新更新 |
|----|------|-----------|
| [`chapter1_digital_mos`](../../chapter1_digital_mos/) | デジタル回路とMOS基礎 | `etc/`ディレクトリ削除済 |
| [`chapter2_process_history`](../../chapter2_process_history/) | 半導体プロセス史とFinFET展開 | [`2.4_finfet_gaa.md`](../../chapter2_process_history/2.4_finfet_gaa.md) 新規作成済 |
| [`chapter3_cmos018`](../../chapter3_cmos018/) | 0.18μm CMOSと特性評価 | [`3.6_summary.md`](../../chapter3_cmos018/3.6_summary.md) 更新済 |
| [`chapter4_soc_design`](../../chapter4_soc_design/) | SoC設計基礎と設計フロー | [`4.4_design_flow.md`](../../chapter4_soc_design/4.4_design_flow.md) 更新済 |
| [`chapter5_test_package`](../../chapter5_test_package/) | テスト・パッケージと信頼性 | [`5.3_final_test_reliability.md`](../../chapter5_test_package/5.3_final_test_reliability.md) 更新済 |
| [`chapter6_design_review`](../../chapter6_design_review/) | デザインレビューと組織連携 | [`README.md`](../../chapter6_design_review/README.md) 更新済 |

---

© 2025 Shinichi Samizo / MIT License
