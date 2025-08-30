# Introduction

**日本語**  
近年、強誘電体を利用した不揮発性メモリ（NVM）デバイスとして、強誘電体トランジスタ（FeFET）が注目を集めている。HfO₂ 系強誘電体は、CMOS プロセス互換性、低電圧動作、スケーリング適合性といった利点を有し、22 nm 以降の先端ノードでは大容量メモリセルへの応用が積極的に検討されてきた。しかし、Endurance（書換寿命）、Retention（データ保持）、TDDB（時間依存絶縁破壊）といった信頼性課題は依然として大きく、特に車載や IoT のような高温環境・長寿命が要求される応用では、従来型 NVM に比べて実用化が制約される。  

一方、成熟ノードである 0.18 µm CMOS プロセスは依然として産業用途で広く利用されている。特に車載 ECU や産業 IoT 向け SoC では、低コスト・高信頼性・長期供給といった要件から、0.18 µm 世代の製造ラインが継続的に稼働している。しかしこれらのラインは「老朽化ライン」とみなされ、新しい製品展開を模索することが困難になりつつある。  

本研究では、0.18 µm CMOS プロセスに対し、最小限の追加投資で FeFET を統合する手法を提案する。具体的には、Gate-Last 方式により Hf₀․₅Zr₀․₅O₂ (HZO) 強誘電ゲートスタックを ALD で形成し、既存の TiN スパッタ装置を流用してゲート電極を形成する。このアプローチにより、追加設備は ALD のみとなり、既存 CMOS ラインへの適用が現実的となる。  

さらに、本研究では FeFET を大容量 NVM として利用するのではなく、SRAM マクロを補助する小規模用途に限定する戦略を提示する。これにより、信頼性課題を許容範囲に抑えつつ、瞬断対策、Instant-On、セキュアキー保持といった応用が可能となる。本論文の貢献点は以下の通りである：  
1. 0.18 µm CMOS プロセスにおける FeFET Gate-Last モジュール統合フローの提案  
2. 信頼性課題を踏まえた「補助 NVM」への戦略的応用方針の提示  
3. 車載 ECU および IoT ノード向けに、成熟ノードを活用した新しい製品展開可能性の実証  

---

*English*  
Ferroelectric field-effect transistors (FeFETs) have recently attracted considerable attention as promising candidates for non-volatile memory (NVM) devices. HfO₂-based ferroelectrics offer CMOS compatibility, low-voltage operation, and scaling potential, and have been extensively investigated for high-density memory arrays in advanced nodes beyond 22 nm. However, their practical deployment remains constrained by reliability challenges such as endurance, retention, and time-dependent dielectric breakdown (TDDB). These issues are particularly critical in applications requiring high-temperature operation and long lifetime, such as automotive electronics and IoT systems, where FeFETs still lag behind conventional NVMs.  

Meanwhile, the mature 0.18 µm CMOS node continues to be widely used in industrial applications. In particular, automotive ECUs and industrial IoT SoCs rely on this node for its low cost, high reliability, and long-term supply stability. Nevertheless, such fabrication lines are increasingly regarded as "legacy nodes," and developing new product opportunities on them has become difficult.  

In this work, we propose a cost-effective integration of FeFETs into a 0.18 µm CMOS process with minimal additional investment. Specifically, we employ a gate-last approach to form an Hf₀․₅Zr₀․₅O₂ (HZO) ferroelectric stack by atomic layer deposition (ALD) and reuse existing TiN sputtering tools for gate electrodes. This approach requires only the addition of ALD equipment, ensuring feasibility for existing production lines.  

Moreover, instead of pursuing FeFETs as large-scale NVMs, we strategically restrict their use to small auxiliary applications supporting SRAM macros. This mitigates reliability concerns while enabling instant-on operation, power-interruption tolerance, and secure key storage. The key contributions of this paper are as follows:  
1. Proposal of a gate-last FeFET module integration flow on 0.18 µm CMOS.  
2. Strategic use of FeFETs as auxiliary NVMs considering reliability constraints.  
3. Demonstration of a new product opportunity for mature nodes in automotive ECUs and IoT nodes.  
