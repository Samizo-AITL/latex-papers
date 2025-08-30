# Process Integration

---

## 3.1 Baseline 0.18 µm CMOS Flow

**日本語**  
本研究のベースラインは、1.8 V / 3.3 V 動作をサポートする標準的な 0.18 µm CMOS プロセスである。主要な特徴は以下の通りである：  
- STI による素子分離  
- 標準/Deep Well の多電圧構成  
- G2/G3 酸化膜による 1.8 V / 3.3 V ゲート絶縁膜厚制御  
- Poly-Si ゲート形成（KrFリソ対応）  
- LDD＋Spacer構造による短チャネル制御  
- Salicide (CoSi₂) による接触抵抗低減  

*English*  
The baseline process is a standard 0.18 µm CMOS supporting 1.8 V / 3.3 V operation, with the following key features:  
- Shallow Trench Isolation (STI)  
- Multi-voltage well structures (standard and deep wells)  
- Gate oxide thickness tuning by G2/G3 oxidation steps (1.8 V / 3.3 V)  
- Poly-Si gate patterning with KrF lithography  
- LDD + spacer structure for short-channel control  
- Salicide (CoSi₂) for contact resistance reduction  

---

## 3.2 FeFET Gate-Last Module

**日本語**  
ベースライン FEOL とサリサイド形成完了後に、FeFETセル領域のダミーゲートを除去し、強誘電ゲートスタックを形成する。  
工程の概要は以下の通りである：  

| No. | 工程 | 手法 | 条件例 |
|----:|------|------|--------|
| 1 | ダミー Poly 除去 | RIE (HBr/Cl₂) | — |
| 2 | ゲート酸化膜リフレッシュ | HF dip (~0.5%) | 数十秒 |
| 3 | 界面層形成 (Al₂O₃) | ALD | 200–250 ℃, 1–2 nm |
| 4 | 強誘電膜堆積 (HZO) | ALD | 200–300 ℃, 8–12 nm |
| 5 | キャップ (Al₂O₃, optional) | ALD | 1–2 nm |
| 6 | TiN 電極形成 | PVD (ロングスロー/コリメータ) or ALD | 30–50 nm |
| 7 | ゲートパターニング | KrFリソ＋RIE | — |
| 8 | 結晶化アニール | RTA | 450–500 ℃, 30–60 s |
| 9 | Forming Gas Anneal | Furnace | 350 ℃, 20–30 min |
| 10 | ILD 充填・CMP | HDP/TEOS | — |

*English*  
After completion of FEOL and salicide, the dummy gates in FeFET regions are removed, and a ferroelectric gate stack is inserted. The main steps are:  
1. Dummy poly removal (RIE)  
2. Gate oxide refresh (HF dip)  
3. Interfacial layer deposition (Al₂O₃, ALD, 200–250 ℃, 1–2 nm)  
4. Ferroelectric HZO deposition (ALD, 200–300 ℃, 8–12 nm)  
5. Optional Al₂O₃ capping (ALD, 1–2 nm)  
6. TiN electrode deposition (PVD with long-throw/collimator or ALD, 30–50 nm)  
7. Gate patterning (KrF lithography + RIE)  
8. Crystallization anneal (RTA, 450–500 ℃, 30–60 s)  
9. Forming Gas Anneal (350 ℃, 20–30 min)  
10. ILD fill and CMP  

---

## 3.3 Equipment Reuse and Investment Minimization

**日本語**  
本統合の特徴は、既存 0.18 µm CMOS ラインにおいて **追加設備は ALD のみ**で済む点にある。TiN 電極は既存のスパッタ装置にロングスローまたはコリメータを適用することで対応可能であり、新規導入は不要である。これにより、老朽化ラインに対して最小限の投資で FeFET を組み込める。  

*English*  
A key feature of this integration scheme is that only ALD equipment needs to be newly introduced into a 0.18 µm CMOS line. TiN electrodes can be deposited using existing sputter tools with long-throw or collimator configurations, eliminating the need for new deposition systems. Thus, FeFET integration can be realized with minimal investment in legacy fabs.  

---

## 3.4 Integration Considerations

**日本語**  
- **熱予算**：結晶化アニール後は >500 ℃ 工程を避け、BEOL は低温プロセスに限定する。  
- **金属反応**：TiN とサリサイドとの反応を抑制するため、適切なシーケンス管理が必要。  
- **レイアウト**：FeFET 領域と 3.3 V I/O 領域はルール分離を行う。CMP 段差や密度制御も考慮する。  

*English*  
- **Thermal budget**: After crystallization anneal, subsequent processes must be limited to <500 ℃ (low-temperature BEOL).  
- **Metal interaction**: Careful sequencing is required to avoid TiN reaction with silicide.  
- **Layout rules**: Separation between FeFET regions and 3.3 V I/O devices is required, with additional attention to CMP step height and density control.  
