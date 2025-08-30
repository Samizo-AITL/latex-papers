# Reliability Characterization

---

## 4.1 Endurance

**日本語**  
FeFET の書換寿命（Endurance）は典型的に 10⁴〜10⁵ サイクルに制約される。これはフラッシュや ReRAM と比較すると桁が小さいが、SRAM マクロの補助用途（設定値保持、Instant-On、セキュアキー保存）では十分である。さらに、Nb 添加などの研究的アプローチにより 10¹²〜10¹⁵ サイクル級の報告もあるが、プロセス均一性や量産性の点で現実的ではないため、本研究では HZO ベースの安定プロセスを採用する。  

*English*  
The endurance of FeFETs is typically limited to 10⁴–10⁵ program/erase cycles, which is lower than Flash or ReRAM. However, this is sufficient for auxiliary applications such as SRAM backup, instant-on, and secure key storage. While Nb-doped variants have demonstrated endurance up to 10¹²–10¹⁵ cycles in research, their process uniformity and manufacturability remain challenging. Thus, this work adopts an HZO-based process for stability.  

---

## 4.2 Retention

**日本語**  
保持特性（Retention）は高温動作で劣化しやすく、85 ℃ で 10³〜10⁴ 秒相当の測定で窓幅が 20〜30% 縮小する例がある。車載応用における 125 ℃ での 10 年保持要求を満たすには課題が残る。ただし、SRAM 補助用途では長期保持よりも「瞬断後の即時リカバリ」が重視されるため、実用上は許容可能と考えられる。  

*English*  
Retention characteristics degrade under elevated temperatures, with typical measurements showing 20–30% window loss at 85 ℃ after 10³–10⁴ seconds. Meeting the 10-year retention requirement at 125 ℃ for automotive applications remains challenging. Nevertheless, for auxiliary use cases, the critical requirement is instant recovery after power interruption rather than long-term data storage, making this acceptable.  

---

## 4.3 TDDB (Time-Dependent Dielectric Breakdown)

**日本語**  
HZO 膜に存在する酸素空孔はリーク経路を形成し、TDDB による寿命短縮を引き起こす。これは大面積アレイ化した場合に顕著となるが、小規模の補助 NVM 構成であれば、歩留まりと信頼性のバランスを維持できる。  

*English*  
Oxygen vacancies in HZO layers may create leakage paths, accelerating time-dependent dielectric breakdown (TDDB). This effect becomes critical in large-scale memory arrays, but for small auxiliary NVM configurations, a practical balance between yield and reliability can be maintained.  

---

## 4.4 Wake-up Effect

**日本語**  
FeFET では初期サイクルにおいてドメイン配向が変化し、しきい値窓幅が拡大する「Wake-up」現象が報告されている。本研究では 10〜100 回程度の軽サイクルを事前に行い、セル特性を安定化させることを前提とする。  

*English*  
FeFETs exhibit a “wake-up” effect, where domain reorientation during the first few cycles increases the memory window. In this work, we assume light pre-cycling (10–100 cycles) to stabilize device characteristics before use.  

---

## 4.5 戦略的割り切り / Strategic Approach

**日本語**  
以上の信頼性課題から、FeFET を大容量 NVM として展開することは困難である。しかし、SRAM マクロを補助する小規模用途に限定することで、信頼性課題を実用範囲に収めつつ、歩留まり改善とコスト低減を両立できる。本研究の戦略は、あえて「大容量化を目指さず、補助用途に特化する」点にある。  

*English*  
Given these reliability limitations, large-scale NVM deployment with FeFETs is impractical. Instead, by restricting FeFETs to auxiliary use cases supporting SRAM macros, reliability challenges can be kept within practical limits while achieving yield improvement and cost reduction. The strategy is to deliberately avoid pursuing high-density scaling and focus on auxiliary functionality.  
