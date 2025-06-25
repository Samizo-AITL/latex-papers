# 第2部：用途別 素子技術の体系

本部では、実際のアナログ／ミックスドシグナル／RF回路設計で用いられる主要な素子群を、用途・アーキテクチャ・性能指標・プロセス適性の観点から整理します。

---

## 第7章：ADC（Analog to Digital Converter）

- 代表方式：SAR型 / パイプライン型 / Sigma-Delta型
- 性能指標：ENOB, SNR, SFDR, INL/DNL, BW
- 設計観点：分解能 vs サンプリング速度のトレードオフ
- プロセス適性：
  - SAR型：65nm CMOS〜FinFET（低電力系）
  - Pipeline型：0.18μm〜65nm（中速・高分解能）
  - SD型：医療・センサ向け、CMOS+1bitDACで小型化可

---

## 第8章：LDO（Low Dropout Regulator）と電源制御

- 構成：Error Amp + パス素子（PMOS/NMOS）+ フィードバック
- 性能指標：PSRR, Load/Line Regulation, Noise, Quiescent Current
- LDO設計の実務観点：
  - スタビリティ設計（位相余裕の確保）
  - 出力コンデンサ依存性への対応（内部補償型など）
- プロセス適性：0.35μm〜65nm CMOS、FinFETでは難易度高
- アナログ系電源、RFバイアス、PLL供給などで使用

---

## 第9章：PLL（Phase-Locked Loop）／周波数合成系

- 構成要素：PD, CP, LF, VCO, Divider
- 方式：Integer-N / Fractional-N / Digital PLL / ADPLL
- 性能指標：ジッタ, ロック時間, スプリアス, フェーズノイズ
- VCO設計：LC型（高精度）、Ring型（小面積）、DCO（ADPLL用）
- プロセス適性：
  - CMOS：Ring/Digital PLL向き
  - SOI/SiGe：高性能LC型PLLに最適
  - FinFET：ADPLL主流（全デジタル化）

---

## 第10章：AFE（Analog Front-End）全体構成と応用事例

- 構成ブロック：LNA → Mixer → Filter → VGA → ADC（受信系）
- 設計視点：ゲイン配分、ノイズマッチング、帯域設計、プロセス適合
- 用途別構成例：
  - 無線通信：RF AFE（PLL + Mixer + ADC + PA）
  - センサ向けAFE：Chopper Amp + SAR ADC（低雑音）
  - 医療用AFE：低電流・高分解能・低ジッタクロックが必須
- 統合設計：AFE全体の電源・GND設計、パッケージ干渉対策

---

## 🗂 第2部まとめ

- 各用途に応じて素子の設計目標・構成・プロセス選定が変化
- SoC統合時には、デジタル領域との境界設計（Clock Tree, Isolation）も重要
- 第1部の基礎と組み合わせることで、AFEレベルの回路設計力が養成可能

次章では、補足資料（Appendix）として、プロセス比較マトリクスや演習・実装ガイドをまとめます。
