
GAA Multi-Nanosheet FET

Step 1 Substrate Preparation
	•	Process name Substrate Preparation
	•	Objective Provide a defect-free 300 mm starting wafer capable of handling multilayer Si/SiGe epitaxy.
	•	Typical wafer spec
	•	300 mm p-type Si, ⟨100⟩, resistivity < 10 Ω·cm
	•	Thickness: 775 ± 25 µm (before back-grind)
	•	Optional base variants
	•	Thin SiGe buffer (20–50 nm, 20–30 % Ge) for strain management
	•	20–40 nm BOX if an SOI base is chosen (rare for nanosheet nodes)
	•	Critical controls
	•	Particles < 0.12 µm: < 10 / wafer
	•	TTV < 1 µm, Bow < 40 µm
	•	Integration notes
	•	All subsequent epi and CMP targets reference this starting surface height.
	•	SiGe buffer must survive CMP slurry chemistry in Step 3.

Step 2 Superlattice Epitaxial Growth
	•	Process name Si/SiGe Superlattice Epitaxy
	•	Stack example (3-sheet design)
	1.	Si 5 nm (channel)
	2.	SiGe (25 – 30 % Ge) 8 nm (sacrificial)
	3.	Si 5 nm
	4.	SiGe 8 nm
	5.	Si 5 nm
	•	Deposition method 
	•	Reduced-pressure CVD at 650 – 700 °C, HCl-free to minimise Ge loss
	•	MBE can be used for R&D lots but is <2 wph; production uses RPCVD (10–15 wph)
	•	Key parameters
	•	Ge-content uniformity: ±0.5 % across wafer
	•	Thickness uniformity (1σ): Si ±0.1 nm, SiGe ±0.2 nm
	•	Surface roughness (AFM Rq): < 0.15 nm after final Si cap
	•	Challenges / remarks
	•	Ge memory effect between layers must be purged (<0.1 % residual) to avoid inter-diffusion.
	•	Final Si cap can be omitted if a selective STI process (Step 7) uses a SiN hardmask.

Step 3 CMP (Epitaxial Planarisation)
	•	Process name Epi Planarisation CMP
	•	Objective Flatten the superlattice stack and expose the top SiGe layer with ±2 nm height control.
	•	Tool set 12 kN-class CMP polisher, 50 cm platen, oxide “soft” pad, inline eddy-current sensor.
	•	Slurry / pad
	•	Colloidal silica, pH ~ 10.5, removal rate 40 ± 3 nm min⁻¹ on Si, 34 ± 2 nm min⁻¹ on SiGe
	•	Pad wear window < 1.5 % across 500 wafers; pad conditioning every 25 wafers
	•	End-point strategy In-situ spectro-reflectometry (555 nm) to detect Si→SiGe spectral shift; backup: time-mode + 50 nm over-polish margin.
	•	Target metrics
	•	Global thickness variation (GTV) after polish: < ±2 nm
	•	Local non-uniformity (20 mm window): < 1 nm p-v
	•	Post-CMP surface roughness (AFM Rq): < 0.2 nm
	•	Integration notes
	•	Exposed SiGe must be oxide-free; wafers go directly to hard-mask deposition (Step 4) within 60 min to avoid native oxide (>0.3 nm) that degrades sub-10 nm SADP pitch.
	•	Residual slurry silica <5 ng cm⁻² after megasonic DI rinse; verified by TXRF.

Step 4 Hardmask Deposition
	•	Process name Hardmask Deposition (Fin/GAA patterning base)
	•	Objective Provide an etch-resistant and conformal hardmask stack to define nanosheet patterns.
	•	Typical stack
	•	SiN or SiCN (Plasma-enhanced CVD or LPCVD): 25 – 35 nm
	•	Optional: thin oxide (~2 nm) for adhesion promotion
	•	Deposition method
	•	PECVD: 400 – 450 °C, SiH₄/NH₃/N₂, step coverage > 90 %
	•	LPCVD: 750 – 800 °C for lower hydrogen content (better CD uniformity)
	•	Film properties
	•	Etch selectivity: SiN : SiGe > 10:1
	•	Stress tuning: ±250 MPa possible (used later for channel stress pre-biasing)
	•	Thickness uniformity: < ±2 % (1σ across wafer)
	•	Integration notes
	•	Hardmask must be compatible with multi-patterning (SADP/SAQP) using oxide spacers.
	•	Adhesion to CMP-finished SiGe must be ensured via pre-clean (e.g., diluted HF 0.5%, 10 sec + N₂ dry).
	•	Surface roughness < 0.5 nm RMS before lithography.

Step 5 Lithography (GAA Fin Patterning)
	•	Process name EUV Lithography for Nanosheet Fin Patterns
	•	Objective Define sub-20 nm wide fin-like lines that map to stacked nanosheets.
	•	Tool EUV scanner (13.5 nm, NA = 0.33, single exposure), optional SADP or SAQP
	•	CD targets
	•	Critical dimension (post-develop): 15 – 18 nm
	•	Line pitch: 32 – 40 nm
	•	LER (Line Edge Roughness): < 2.0 nm (3σ), LWR: < 2.5 nm
	•	Photoresist stack
	•	EUV CAR (chemically amplified resist), 30–40 nm thick
	•	Optional underlayer: SiARC or organic BARC, 10–15 nm
	•	Post-exposure process
	•	PEB: 100 °C, 60 sec, N₂ atmosphere
	•	Development: TMAH 2.38 %, 45 sec, followed by DI rinse
	•	Patterning method
	•	Single EUV exposure followed by spacer-based SADP (Self-Aligned Double Patterning) or SAQP (Quadruple Patterning)
	•	Spacer material: SiO₂ or SiN (20 – 30 nm) deposited conformally and etched back anisotropically
	•	Remarks
	•	Defectivity threshold < 0.05/cm² for CD excursions >10%
	•	Overlay error target: < 1.5 nm (to STI and hardmask alignment marks)

Step 6 Fin Stack Etch (Si/SiGe Multilayer)
	•	Process name Fin Stack Etching
	•	Objective Etch down through the hardmask and superlattice to form narrow fin-like stacks of alternating Si / SiGe.
	•	Etch profile targets
	•	Verticality: < 1° taper (ideal < 0.5°)
	•	CD control (bottom vs top): ±2 nm
	•	Aspect ratio: up to 6:1 (depth:width ~50:8 nm)
	•	Etch chemistry
	•	RIE with multi-step sequence:
	•	Hardmask breakthrough: CF₄/O₂
	•	Si/SiGe main etch: HBr/Cl₂ + He backside cooling
	•	SiGe selectivity steps (optional): low-pressure SF₆/NF₃
	•	End-point detection
	•	Optical Emission Spectroscopy (OES) monitoring for Ge and Si signals
	•	Total etch depth: ~30–40 nm from hardmask top
	•	Post-etch clean
	•	Wet clean: diluted SC1/SC2 + Megasonic rinse
	•	Residual polymer removal using O₂/N₂ downstream plasma
	•	Integration notes
	•	Fin integrity (no collapse, no line bending) depends on maintaining profile symmetry across multiple SiGe/Si interfaces
	•	CD uniformity target: < ±3 nm across wafer
	•	Etch damage to Si nanosheets must be limited to <1 nm amorphization depth (verified by XTEM or spectroscopic ellipsometry)

 Step 7 Shallow Trench Isolation (STI) Oxide Deposition
	•	Process name STI Oxide Deposition (for nanosheet trench fill)
	•	Objective Fill gaps between etched fin/nanosheet stacks with dielectric to isolate individual devices.
	•	Oxide type
	•	TEOS-based SiO₂ (PECVD or SACVD) or High-Density Plasma (HDP) oxide
	•	Target thickness: ≥ 100 nm above fin top to enable overfill and polish margin
	•	Deposition conditions
	•	TEOS: 400 – 450 °C, O₃ or O₂ carrier, pressure ~50 Torr
	•	HDP: 300 – 350 °C, Ar/O₂/SiH₄ plasma, conformal reflow enabled
	•	Film quality targets
	•	Gap-fill capability for trench widths: 30 – 40 nm
	•	Voids/Seam defect rate: < 1/cm² across wafer
	•	Refractive index: 1.46 – 1.47 @ 633 nm
	•	Integration notes
	•	Over-deposition is deliberate to ensure CMP process window
	•	Trench refill must maintain nanosheet edge definition; no oxide pushback allowed
	•	Prior to oxide deposition, optional liner (5–10 nm SiN) may be used to suppress stress concentration

Step 8 CMP (STI Planarization)
	•	Process name STI CMP (Shallow Trench Isolation planarization)
	•	Objective Remove overfilled STI oxide and stop precisely at the top of the hardmask or SiN cap.
	•	CMP parameters
	•	Tool: 300 mm CMP polisher, active pad zone, real-time friction monitoring
	•	Slurry: Silica-based, pH ~10, oxide-to-nitride selectivity ~100:1
	•	Polish rate:
	•	Oxide: ~80–100 nm/min
	•	SiN/SiCN: <1 nm/min (ideal stopper)
	•	End-point control
	•	In-situ motor torque + interferometry for oxide removal
	•	Stop layer detection via secondary reflectance or motor signature shifts
	•	Post-CMP targets
	•	Global planarization tolerance: < ±5 nm
	•	Dishing (oxide recess over fin): < 10 nm
	•	Erosion (oxide loss in dense areas): < 5 % (within 500 µm region)
	•	Post-process cleaning
	•	Brush clean + SC1 + dilute HF (0.5%) to remove slurry residuals
	•	Contamination targets: Metal ions < 10 ppt, particles < 5 @ >0.1 µm

Step 9 Sacrificial Oxide Formation
	•	Process name Sacrificial Oxide Growth
	•	Objective Grow a thin, clean SiO₂ layer that will later be removed to clean up and recondition the nanosheet surfaces.
	•	Growth parameters
	•	Dry O₂ furnace oxidation
	•	Temperature: 800 – 900 °C
	•	Thickness: 3 – 5 nm (target ~4 nm)
	•	Time: ~2 – 4 min depending on temperature
	•	Oxide characteristics
	•	Uniformity (3σ): < ±0.3 nm
	•	Interface trap density (Dit): < 5 × 10¹⁰ cm⁻²·eV⁻¹
	•	Surface roughness increase: < 0.1 nm (AFM Rq)
	•	Integration notes
	•	This oxide will be completely removed prior to High-k deposition (Step 17)
	•	Functions as a surface polish layer, removing damage from RIE and CMP
	•	May also assist in stress relaxation in Si nanosheets

Step 10 Dummy Gate Oxide Formation
	•	Process name Dummy Gate Oxide Growth
	•	Objective Form a temporary gate dielectric (SiO₂) layer over the nanosheet stack to support dummy gate formation.
	•	Oxide type Thermal SiO₂
	•	Growth parameters
	•	Dry O₂ oxidation
	•	Temperature: 800 – 850 °C
	•	Target thickness: 1.5 – 2.0 nm
	•	Time: ~2–3 min (controlled for uniform tunneling thickness)
	•	Film characteristics
	•	Thickness uniformity (3σ): < ±0.2 nm across wafer
	•	Breakdown voltage: > 7 MV/cm
	•	Interface state density (Dit): < 1×10¹¹ cm⁻²·eV⁻¹
	•	Integration notes
	•	This oxide will be etched later and replaced with High-k dielectric (Step 17)
	•	Growth must be strictly isotropic to preserve nanosheet thickness symmetry
	•	Gate alignment CD depends partly on oxide uniformity due to its role in etch selectivity

Step 11 Dummy Poly Gate Deposition
	•	Process name Dummy Polycrystalline Silicon Deposition
	•	Objective Deposit a conformal poly-Si layer over the dummy gate oxide to serve as a placeholder gate stack.
	•	Deposition method LPCVD
	•	Process conditions
	•	Temperature: 580 – 620 °C
	•	Precursor: SiH₄ or Si₂H₆
	•	Target thickness: 80 – 100 nm (to allow CMP margin)
	•	Conformality: > 95 % over nanosheet edges
	•	Film properties
	•	Resistivity: 10 – 30 mΩ·cm
	•	Grain size: 20 – 100 nm (affects etch behavior later)
	•	Integration notes
	•	Must fully fill gate trench regions without voids or seams
	•	Step coverage into high aspect ratio features must be validated (via cross-section SEM)
	•	Hydrogen content < 2 at% to minimize gate shrink during anneal

Step 12 CMP (Dummy Poly Planarization)
	•	Process name Dummy Gate Poly CMP
	•	Objective Planarize the dummy gate surface to define a flat top surface, stopping at ILD or hardmask.
	•	CMP setup
	•	Slurry: Silica or alumina-based, poly-Si:oxide selectivity ~20:1
	•	Pad: IC1000 + Suba IV, downforce ~2.5 psi
	•	Removal rate: ~100 nm/min on poly-Si
	•	Control targets
	•	Final thickness over nanosheets: 0 ±5 nm
	•	Topography variation (within-die): < ±10 nm
	•	Dishing (poly-Si recess): < 5 nm
	•	Post-polish clean
	•	Brush scrub + SC1 + diluted HF (if oxide residue present)
	•	Metallic contamination <10 ppt
	•	Integration notes
	•	Surface must be uniform to ensure consistent gate etch and S/D spacer process
	•	Gate CD laterally depends on CMP-induced edge rounding → must monitor profile with AFM or XSEM

Step 13 Gate Lithography and Etch (Dummy Gate Patterning)
	•	Process name Dummy Gate Patterning
	•	Objective Define narrow gate structures aligned to the nanosheet channel using EUV lithography and etching.
	•	Lithography
	•	Tool: EUV scanner (13.5 nm), NA = 0.33
	•	CD target (gate length): 15 – 20 nm
	•	Overlay tolerance to fin: < ±2 nm
	•	LER/LWR: < 2.0 nm / 2.5 nm (3σ)
	•	Resist stack
	•	EUV photoresist: 30 – 40 nm
	•	Anti-reflection layer (if used): SiARC, 10 nm
	•	Etch process
	•	RIE chemistry: HBr/Cl₂/O₂ or HBr/NF₃, multi-step
	•	Etch selectivity:
	•	Poly-Si : oxide > 30:1
	•	Poly-Si : SiGe > 15:1
	•	Etch depth: ~100 nm
	•	CD uniformity: < ±2 nm (3σ) across wafer
	•	Post-etch cleaning
	•	O₂ plasma ash + SC1 wet clean
	•	Residue-free surface required for accurate S/D spacer formation
	•	Integration notes
	•	Dummy gate defines eventual High-k/Metal gate cavity (after replacement)
	•	Sidewall angle must be >88° (nearly vertical) to support conformal wrap-around later
	•	Misalignment causes underlap/overlap → direct impact on drive current

Step 14 S/D Spacer Deposition
	•	Process name Source/Drain Spacer Deposition
	•	Objective Deposit spacer layer to separate gate from source/drain region, ensuring controlled junction distance.
	•	Spacer material
	•	Typically SiN, SiOC, or multilayer (SiN + SiCN)
	•	Thickness target: 5 – 10 nm (per side)
	•	Deposition method
	•	LPCVD or PEALD (for tight CD control)
	•	Temperature: 400 – 550 °C
	•	Conformality: > 90 % on gate sidewalls
	•	Film properties
	•	Stress: tunable between ±500 MPa (used in stress engineering)
	•	Dielectric constant: k = 5–7
	•	Wet etch rate (vs SiGe): < 0.5 nm/min (selective spacer retention)
	•	Integration notes
	•	Spacer defines offset length between gate and S/D junctions
	•	Spacer thickness variability → major contributor to threshold voltage variation
	•	Etch-back step comes later (Step 21) to expose the S/D regions

Step 15 Selective SiGe Etch (Sacrificial Layer Removal)
	•	Process name Selective Etch of Sacrificial SiGe Layers
	•	Objective Remove SiGe layers between Si nanosheets to release suspended channel structures (GAA)
	•	Etch chemistry
	•	Wet: HCl vapor or VHF (for high selectivity)
	•	Dry: Remote plasma HCl (for R&D), not scalable for HVM
	•	Etch conditions
	•	Temperature: 350 – 500 °C
	•	Pressure: 1 – 5 Torr
	•	Time: 1 – 5 min depending on layer count and uniformity
	•	Selectivity
	•	SiGe : Si > 100:1 (critical to prevent Si sheet thinning)
	•	Target Ge content: 25–30 % for optimal etch rate and contrast
	•	Etch profile goals
	•	Uniform cavity formation between nanosheets
	•	No attack on STI oxide or gate sidewalls
	•	Post-etch process
	•	Immediate SC1 clean or IPA vapor dry to avoid stiction
	•	Structural inspection: SEM or XTEM for nanosheet release confirmation
	•	Integration notes
	•	Step creates air-gaps below nanosheets enabling full GAA behavior
	•	Mechanical integrity of floating Si sheets must be verified (no collapse or warp)
	•	This step is irreversible: defective etch leads to device loss

 Step 16 Nanowire Cleaning
	•	Process name Nanowire/Nanosheet Surface Cleaning
	•	Objective Remove residual contaminants and etch damage from nanosheet surfaces prior to gate dielectric deposition.
	•	Cleaning chemistry
	•	Standard clean 1 (SC1): NH₄OH + H₂O₂ + H₂O (1:1:5), 75–80 °C, 1–2 min
	•	Standard clean 2 (SC2): HCl + H₂O₂ + H₂O (1:1:6), 75–80 °C, 1–2 min
	•	Additional treatments
	•	Optional dilute HF dip (0.5 %), 15–30 s to remove native oxide
	•	Megasonic agitation to minimize surface damage
	•	Target results
	•	Surface roughness Rq < 0.2 nm (AFM)
	•	Minimal surface amorphization (<0.5 nm)
	•	Residual metallic contamination < 1 × 10¹⁰ atoms/cm²
	•	Integration notes
	•	Cleaning must preserve nanosheet geometry and avoid stiction/collapse
	•	Timing is critical: minimize air exposure after clean to avoid re-oxidation
	•	Surface hydrophobicity controlled for optimal ALD nucleation

Step 17 High-k Gate Dielectric Deposition
	•	Process name High-k Dielectric Deposition (HfO₂)
	•	Objective Form ultra-thin, uniform, conformal high-k gate insulator with EOT ~0.85 nm.
	•	Material Hafnium oxide (HfO₂)
	•	Deposition method Atomic Layer Deposition (ALD)
	•	Process conditions
	•	Temperature: 250 – 300 °C
	•	Precursor: HfCl₄ or TEMAH + H₂O or O₃ oxidant
	•	Thickness: 1.5 – 2.0 nm (physical thickness)
	•	Growth per cycle (GPC): ~0.1 nm/cycle
	•	Film properties
	•	EOT target: ~0.85 nm (measured by ellipsometry / electrical)
	•	Leakage current density < 1 × 10⁻³ A/cm² at Vfb + 1 V
	•	Dielectric constant: 18 – 20
	•	Integration notes
	•	Precursor dosing and purge times critical to avoid C contamination
	•	Surface must be oxide-free and hydroxylated for uniform ALD nucleation
	•	Post-ALD anneal in N₂ or O₂ at 400 – 500 °C to densify film and reduce traps

Step 18 Metal Gate Deposition
	•	Process name Metal Gate Electrode Formation
	•	Objective Deposit conformal metal gate layer (TiN or alternative) surrounding nanosheets (wrap-around gate).
	•	Material Titanium Nitride (TiN) or alternative metal nitride
	•	Deposition method ALD or Physical Vapor Deposition (PVD)
	•	Process conditions
	•	ALD temperature: 250 – 350 °C
	•	PVD sputtering power: 200 – 300 W, Ar/N₂ atmosphere
	•	Thickness: 5 – 10 nm (conformal thickness)
	•	Film properties
	•	Resistivity: < 200 μΩ·cm
	•	Work function tuning possible by doping or bilayer metal stacks
	•	Stress: low tensile to prevent nanosheet deformation
	•	Integration notes
	•	Conformality critical for uniform gate coverage on multiple nanosheet layers
	•	No voids or seams allowed to ensure continuous gate control
	•	Interface cleanliness with high-k is mandatory to avoid Fermi-level pinning

Step 19 Gate Fill
	•	Process name Gate Fill (Tungsten or Cobalt)
	•	Objective Fill the gate trench with metal to complete the gate electrode stack and ensure low resistance.
	•	Materials
	•	Tungsten (W) or Cobalt (Co) depending on process flow
	•	Deposition method
	•	Atomic Layer Deposition (ALD) seed layer + Chemical Vapor Deposition (CVD) bulk fill
	•	Process conditions
	•	ALD seed: ~10 nm thickness for conformality
	•	CVD bulk fill: Temperature 350–400 °C, Pressure ~1 Torr
	•	Target thickness: Complete fill without voids; overfill ~20 nm for CMP margin
	•	Film properties
	•	Resistivity: W ~ 5–10 μΩ·cm, Co ~ 6–8 μΩ·cm
	•	Stress: Low intrinsic stress to avoid gate deformation
	•	Integration notes
	•	High aspect ratio fill (>5:1) requires careful process tuning to avoid seams
	•	Post-deposition anneal (300–400 °C) to improve grain structure and reduce resistivity
	•	Avoid contamination of gate dielectric or adjacent spacers

Step 20 CMP (Gate Metal Planarization)
	•	Process name Gate Metal CMP
	•	Objective Planarize gate fill metal, stopping on hardmask or dielectric, achieving uniform gate topography.
	•	CMP parameters
	•	Slurry: Alumina or silica based, high selectivity to hardmask/dielectric
	•	Downforce: ~3 psi
	•	Removal rate: ~80–100 nm/min on tungsten/cobalt
	•	Control targets
	•	Thickness uniformity: ±5 nm across wafer
	•	Dishing < 10 nm
	•	Residual metal particles < 1/cm²
	•	Post CMP cleaning
	•	Brush scrub, megasonic rinse
	•	Metal contamination < 5 ppt required
	•	Integration notes
	•	Surface roughness < 0.5 nm RMS for subsequent lithography
	•	Check gate CD uniformity post CMP for critical dimension control

Step 21 Source/Drain Spacer Etch Back
	•	Process name Spacer Etch Back
	•	Objective Etch spacer layer selectively to open source/drain contact regions while preserving gate protection.
	•	Etch chemistry
	•	Reactive Ion Etching (RIE) with CF₄/CHF₃ or CF₄/H₂ plasma
	•	Process parameters
	•	Pressure: 10–20 mTorr
	•	RF power: 200–300 W
	•	Endpoint detection: Optical emission spectroscopy (OES) to detect Si or N emissions
	•	Etch targets
	•	Spacer thickness after etch: 3–5 nm remaining on gate sidewalls
	•	No damage or undercut of gate metal or dummy gate oxide
	•	Integration notes
	•	Etch uniformity critical to avoid junction leakage variations
	•	Over-etch must be minimized to prevent channel exposure or S/D junction damage
	•	Post-etch cleaning to remove polymer residues mandatory

Step 22 Source/Drain Implantation or Epitaxy
	•	Process name Source/Drain (S/D) Formation
	•	Objective Create heavily doped S/D regions either by ion implantation or epitaxial growth for low resistance contacts.
	•	Options
	•	Ion Implantation:
	•	Species: As⁺ for n-type, B⁺ for p-type
	•	Dose: 1×10¹⁵ to 5×10¹⁵ cm⁻²
	•	Energy: 10–30 keV (shallow junctions)
	•	Tilt: 0° to 7° to reduce channel damage
	•	Temperature: Room temperature or elevated (~200 °C) to reduce channel amorphization
	•	Selective Epitaxial Growth (SEG):
	•	Material: Si:B for pFET, Si:P or Si:C for nFET
	•	Thickness: 10–20 nm
	•	Temperature: ~700 °C
	•	Precursors: SiH₄ + B₂H₆ or PH₃
	•	Integration notes
	•	Epi growth preferred for strain engineering (compressive or tensile)
	•	Implant damage must be minimized to preserve nanosheet integrity
	•	Implantation angle and energy are tuned to avoid gate spacer and channel overlap
	•	Dopant activation follows in Step 23

Step 23 Rapid Thermal Anneal (RTA)
	•	Process name Dopant Activation Anneal
	•	Objective Activate implanted dopants and repair lattice damage with minimal diffusion.
	•	Process parameters
	•	Anneal type: Spike or Flash RTA
	•	Peak temperature: 1000 – 1050 °C
	•	Ramp rate: > 100 °C/s (fast ramp-up and ramp-down)
	•	Duration: milliseconds to seconds (spike) or ~10 s (flash)
	•	Integration notes
	•	Minimize junction depth broadening and dopant diffusion
	•	Stress management important to avoid nanosheet deformation
	•	Anneal ambient: N₂ or Ar, sometimes forming gas (N₂/H₂) post-anneal
	•	Electrical activation > 90 % expected

Step 24 Stress Layer Deposition
	•	Process name Strain Engineering Layer Deposition
	•	Objective Deposit tensile or compressive stress films to enhance carrier mobility in channel.
	•	Materials
	•	Tensile SiN (for nFET)
	•	Compressive SiGe or SiN (for pFET)
	•	Deposition method
	•	LPCVD or PECVD
	•	Thickness: 20 – 30 nm
	•	Stress level: ±200 to ±500 MPa
	•	Integration notes
	•	Film uniformity critical to avoid wafer bowing
	•	Stress orientation tailored to maximize mobility enhancement
	•	Thickness optimized to avoid cracking or delamination
	•	Compatible with subsequent ILD deposition (Step 25)

Step 25 Interlayer Dielectric (ILD) Deposition
	•	Process name Interlayer Dielectric Deposition
	•	Objective Deposit dielectric insulating layer over source/drain and gate regions to isolate metal interconnects.
	•	Materials
	•	Low-k dielectric: SiCOH (k ~ 2.7–3.0) or conventional CVD SiO₂
	•	Deposition method
	•	Plasma Enhanced Chemical Vapor Deposition (PECVD) or sub-atmospheric CVD (SACVD)
	•	Process conditions
	•	Temperature: 350–400 °C
	•	Thickness: ~300 nm (adjusted per integration scheme)
	•	Film properties
	•	Dielectric constant: low-k target < 3.0
	•	Film uniformity: ±5 % thickness variation
	•	Stress: low intrinsic stress (<100 MPa tensile or compressive)
	•	Integration notes
	•	Good step coverage over topography essential
	•	Porosity controlled for reliability
	•	Surface roughness < 1 nm RMS for CMP

Step 26 Contact Hole Etch
	•	Process name Contact Via Etch
	•	Objective Create contact holes through ILD down to source/drain and gate regions for subsequent metal filling.
	•	Etch chemistry
	•	Reactive Ion Etching (RIE) with CH₄/O₂ or CF₄/CHF₃ plasma
	•	Process conditions
	•	Pressure: 10–30 mTorr
	•	RF power: 200–300 W
	•	Etch characteristics
	•	Critical dimension (CD): 30–50 nm
	•	Sidewall profile: vertical, taper < 5°
	•	Etch selectivity: ILD to underlying layers > 10:1
	•	Integration notes
	•	Endpoint detection critical to avoid over-etching S/D or gate
	•	Residue-free sidewalls mandatory to ensure barrier adhesion
	•	Post-etch wet clean recommended

Step 27 Barrier and Fill Metal Deposition (Contact)
	•	Process name Barrier and Tungsten Fill for Contacts
	•	Objective Deposit diffusion barrier and fill contact holes with low-resistivity metal.
	•	Materials
	•	Barrier: TiN or TaN (~5–10 nm) by ALD or PVD
	•	Fill: Tungsten (W) via CVD
	•	Deposition conditions
	•	Barrier: Conformal coverage critical, temperature ~250–300 °C
	•	Tungsten: CVD at 350–400 °C, pressure ~1 Torr
	•	Target fill thickness: complete fill with slight overfill for CMP margin
	•	Film properties
	•	Barrier resistivity: < 300 μΩ·cm
	•	Tungsten resistivity: 5–10 μΩ·cm
	•	Integration notes
	•	Barrier prevents metal diffusion into silicon and dielectric
	•	Voids or seams in fill degrade electrical performance
	•	Post-deposition anneal may be performed to improve film properties

Step 28 CMP (Contact Planarization)
	•	Process name Contact Metal CMP
	•	Objective Planarize tungsten-filled contact holes, stopping on ILD surface to create smooth, defect-free topography.
	•	CMP parameters
	•	Slurry: Silica or alumina-based, high selectivity to tungsten over ILD
	•	Removal rate: ~100 nm/min on tungsten
	•	Downforce: ~3 psi
	•	Process control
	•	End-point detection by motor current and optical monitoring
	•	Post-CMP tungsten residual: < 5 nm
	•	Post-CMP cleaning
	•	Brush scrub, megasonic rinse
	•	Contamination: metal particles < 1/cm², ionic contaminants < 5 ppt
	•	Integration notes
	•	Planar surface required for subsequent ILD deposition and lithography
	•	Avoid dishing and erosion, critical for contact resistance uniformity

Step 30a Interlayer Dielectric (ILD) Deposition Before M0
	•	Process name Pre-Metal 0 (M0) ILD Deposition
	•	Objective Deposit dielectric insulating layer above contacts to isolate first-level metal layer.
	•	Material CVD SiO₂ or low-k dielectric (k ~ 2.7–3.0)
	•	Deposition parameters
	•	Thickness: 200–300 nm
	•	Temperature: 350–400 °C
	•	Uniformity: ±5 %
	•	Integration notes
	•	Good gap-fill and step coverage required
	•	Low defect density to ensure interconnect reliability

Step 30b Lithography and Etch for M0 Contact
	•	Process name M0 Contact Patterning
	•	Objective Pattern contact openings in ILD to M0 metal layer using lithography and etching.
	•	Lithography
	•	Tool: 193 nm ArF immersion scanner
	•	Critical dimension (CD): 30–50 nm
	•	Etch
	•	Chemistry: RIE with CH₄/O₂ or CF₄/CHF₃ plasma
	•	Endpoint: Optical emission spectroscopy (OES)
	•	Integration notes
	•	Overlay tolerance: < ±3 nm
	•	Vertical sidewalls and smooth profiles required
	•	Avoid substrate damage and maintain low defectivity

Step 31 M0 Barrier and Seed Layer Deposition
	•	Process name Barrier and Cu Seed Layer Deposition for Metal 0 (M0)
	•	Objective Deposit diffusion barrier and copper seed layers for subsequent Cu electrochemical plating.
	•	Materials
	•	Barrier: Tantalum (Ta) or Tantalum Nitride (TaN), thickness 5–10 nm
	•	Seed: Copper (Cu), thickness ~50 nm
	•	Deposition methods
	•	Barrier: Physical Vapor Deposition (PVD) or Atomic Layer Deposition (ALD)
	•	Seed: PVD sputtering
	•	Film properties
	•	Barrier resistivity: < 300 μΩ·cm
	•	Seed layer continuity and uniformity critical for plating quality
	•	Integration notes
	•	Barrier must provide excellent adhesion and prevent Cu diffusion into ILD
	•	Seed layer coverage must be conformal and continuous over via/contact bottom and sidewalls
	•	Thickness uniformity: ±5 % across wafer

Step 32 M0 Copper Electrochemical Plating (ECP)
	•	Process name Copper Electrochemical Plating for Metal 0
	•	Objective Fill vias and trenches with copper to form the M0 metal wiring layer.
	•	Process conditions
	•	Electrolyte: Acidic Cu sulfate bath with organic additives for leveling and brightening
	•	Current density: 10–30 mA/cm²
	•	Thickness: 200–400 nm (overfill margin for CMP)
	•	Temperature: 20–25 °C
	•	Film properties
	•	Low resistivity: ~1.7 μΩ·cm (bulk Cu)
	•	Smooth, void-free fill essential for reliability
	•	Integration notes
	•	Plating uniformity and absence of voids/defects verified by cross-sectional SEM
	•	Additives controlled to suppress bottom-up fill issues and to avoid overplating

Step 33 M0 Copper CMP
	•	Process name Copper Chemical Mechanical Polishing
	•	Objective Planarize copper layer, removing overburden and preparing surface for next ILD deposition.
	•	CMP parameters
	•	Slurry: Alumina or silica based, selective to Cu over barrier and ILD
	•	Removal rate: ~100 nm/min on Cu
	•	Downforce: ~3 psi
	•	Process control
	•	Endpoint detection by motor current and optical monitoring
	•	Residual Cu thickness after CMP: < 5 nm over ILD areas
	•	Post-CMP cleaning
	•	Brush scrub and megasonic rinse to remove slurry particles and contaminants
	•	Metal contamination < 1/cm²
	•	Integration notes
	•	Surface roughness < 0.5 nm RMS required for next lithography steps
	•	Avoid dishing and erosion, critical for line resistance and reliability

Step 34 Interlayer Dielectric (ILD) Deposition Between M0 and M1
	•	Process name ILD Deposition (M0–M1)
	•	Objective Deposit dielectric insulating layer between the first (M0) and second (M1) metal layers to ensure electrical isolation.
	•	Material
	•	Low-k dielectric, typically SiCOH (k ~ 2.7–3.0)
	•	Deposition method
	•	Plasma Enhanced CVD (PECVD) or Sub-atmospheric CVD (SACVD)
	•	Process conditions
	•	Thickness: 300–500 nm
	•	Temperature: 350–400 °C
	•	Film properties
	•	Low dielectric constant (k) to minimize parasitic capacitance
	•	Uniform thickness and low intrinsic stress
	•	Integration notes
	•	Good step coverage and gap fill are essential to avoid voids
	•	Surface roughness minimized for next lithography

Step 35 Lithography for M1 Wiring
	•	Process name M1 Metal Layer Patterning
	•	Objective Define wiring patterns for the first metal interconnect layer (M1) by lithography.
	•	Lithography details
	•	Exposure tool: ArF immersion scanner or EUV lithography (depending on technology node)
	•	Wavelength: 193 nm (ArF) or 13.5 nm (EUV)
	•	Critical dimension (CD): 20–30 nm
	•	Overlay tolerance: < ±3 nm
	•	Resist and process
	•	High resolution resist, thickness 40–50 nm
	•	Post-exposure bake and development optimized for LER/LWR control
	•	Integration notes
	•	Precise alignment critical for multilayer interconnect accuracy
	•	Defectivity and resist profile carefully monitored

Step 36 Dual Damascene Etching (Via and Metal Line)
	•	Process name Dual Damascene Via and Line Etch
	•	Objective Etch via holes and metal line trenches into ILD for M1 wiring.
	•	Etching chemistry
	•	Reactive Ion Etching (RIE) using CF₄/Ar/O₂ plasma
	•	Process conditions
	•	Pressure: 10–30 mTorr
	•	RF power: 200–300 W
	•	Etch characteristics
	•	Vertical sidewalls, taper angle < 5°
	•	High selectivity to ILD and barrier layers
	•	CD control within ±2 nm
	•	Integration notes
	•	Etch uniformity critical for reliable metal fill
	•	Endpoint detection employed to avoid over-etching into underlying layers
	•	Post-etch clean to remove polymer residues and avoid contamination

Step 37 M1 Barrier and Seed Layer Deposition
	•	Process name Barrier and Cu Seed Layer Deposition for Metal 1 (M1)
	•	Objective Deposit diffusion barrier and copper seed layers to enable electrochemical plating for M1 wiring.
	•	Materials
	•	Barrier: Tantalum (Ta) or Tantalum Nitride (TaN), thickness 5–10 nm
	•	Seed: Copper (Cu), thickness ~50 nm
	•	Deposition methods
	•	Barrier: Physical Vapor Deposition (PVD) or Atomic Layer Deposition (ALD)
	•	Seed: PVD sputtering
	•	Film properties
	•	Barrier resistivity: < 300 μΩ·cm
	•	Seed layer uniformity and continuity critical for defect-free plating
	•	Integration notes
	•	Barrier prevents Cu diffusion into ILD and device regions
	•	Seed layer must be continuous with no voids or discontinuities

Step 38 M1 Copper Electrochemical Plating (ECP)
	•	Process name Copper Electrochemical Plating for Metal 1
	•	Objective Fill vias and trenches defined in Step 36 with copper metal to form M1 wiring.
	•	Process conditions
	•	Electrolyte: Acidic Cu sulfate bath with additives (levelers, suppressors, brighteners)
	•	Current density: 10–30 mA/cm²
	•	Thickness: 200–400 nm (with overfill margin for CMP)
	•	Temperature: 20–25 °C
	•	Film properties
	•	Resistivity close to bulk copper (~1.7 μΩ·cm)
	•	Void-free and smooth fill essential for reliability
	•	Integration notes
	•	Additive control critical to avoid defects such as overplating or bottom voids
	•	Monitoring via cross-sectional inspection (SEM, FIB)

Step 39 M1 Copper CMP
	•	Process name Copper Chemical Mechanical Planarization
	•	Objective Planarize copper layer, removing overburden and preparing surface for next ILD deposition.
	•	CMP parameters
	•	Slurry: Alumina or silica-based, selective to Cu over barrier and ILD
	•	Removal rate: ~100 nm/min
	•	Downforce: ~3 psi
	•	Process control
	•	Endpoint detection using motor current and optical monitoring
	•	Residual Cu thickness: < 5 nm over ILD areas
	•	Post-CMP cleaning
	•	Brush scrub and megasonic rinse to remove slurry and metal particles
	•	Metal contamination: < 1 particle/cm²
	•	Integration notes
	•	Surface roughness < 0.5 nm RMS required for subsequent lithography
	•	Avoid dishing and erosion to maintain line integrity

Step 40 Cap Layer Deposition
	•	Process name Cap Layer Deposition
	•	Objective Deposit a protective cap layer over the top metal layer to prevent copper diffusion and mechanical damage.
	•	Materials
	•	Silicon Nitride (SiN) or Silicon Carbon Nitride (SiCN)
	•	Deposition method
	•	Plasma Enhanced Chemical Vapor Deposition (PECVD) or Low Pressure Chemical Vapor Deposition (LPCVD)
	•	Process conditions
	•	Thickness: 20–50 nm
	•	Temperature: 300–400 °C
	•	Film properties
	•	Dense, pinhole-free film
	•	Good adhesion to copper and ILD layers
	•	Integration notes
	•	Film stress controlled to avoid wafer bowing or cracking
	•	Acts as diffusion barrier and mechanical protection

Step 41 RC Extraction
	•	Process name Resistance and Capacitance (RC) Extraction
	•	Objective Analyze and extract parasitic RC parameters of wiring layers to predict circuit performance.
	•	Methods
	•	TCAD simulation based on layout and process data
	•	Measurement via test structures (Kelvin resistors, capacitance test arrays)
	•	Parameters
	•	Target RC delay: < 60 ps/mm wire length
	•	Capacitance and resistance per unit length characterized
	•	Integration notes
	•	RC data used to optimize wiring materials and dimensions in future designs
	•	Feedback to process engineers for process tuning

Step 41a Pad Opening Lithography and Etch
	•	Process name Pad Opening Patterning
	•	Objective Define and etch openings in cap and ILD layers to expose Under Bump Metallization (UBM) pads for packaging.
	•	Lithography
	•	Tool: 193 nm ArF scanner
	•	CD tolerance: ±5 μm (pad openings are large)
	•	Etch process
	•	Reactive Ion Etching (RIE) with fluorine-based chemistries to remove SiN/SiCN and ILD
	•	Integration notes
	•	Avoid damage to underlying UBM pads
	•	Maintain clean, smooth sidewalls for reliable bump bonding

Step 42 UBM and Pad Formation
	•	Process name Under Bump Metallization (UBM) and Pad Formation
	•	Objective Form robust metal pads for solder bump attachment in packaging.
	•	Materials
	•	NiV (Nickel Vanadium), Cu, Au multilayers
	•	Deposition methods
	•	Physical Vapor Deposition (PVD) or Electroplating
	•	Thickness
	•	Total thickness ~10 μm
	•	Integration notes
	•	UBM provides good adhesion, diffusion barrier, and mechanical strength
	•	Pad metallurgy tuned for reliability in thermal cycling and mechanical stress

Step 43 Wafer Thinning (Back Grinding)
	•	Process name Wafer Thinning / Back Grinding
	•	Objective Reduce wafer thickness to improve thermal dissipation and enable 3D integration.
	•	Process details
	•	Target thickness: ~100 µm or less
	•	Grinding method: Mechanical grinding followed by chemical mechanical polishing (CMP) for surface finish
	•	Stress control: Minimize wafer warpage and cracking
	•	Integration notes
	•	Surface damage from grinding removed by CMP
	•	Thickness uniformity critical for stacking and TSV alignment

Step 44 Through Silicon Via (TSV) and Micro Bump Formation
	•	Process name TSV / μBump Formation
	•	Objective Form vertical interconnects (TSVs) and micro bumps for 3D integration and packaging.
	•	TSV details
	•	Diameter: 3–10 µm typical
	•	Aspect ratio: High (10:1 or more) etching using deep reactive ion etching (DRIE)
	•	Liner: Dielectric isolation liner (SiO₂ or SiN)
	•	Barrier/seed layers: TiN/TaN for Cu plating
	•	Fill: Electroplated Cu
	•	Micro bump details
	•	Materials: SnAg, Pb-free solder alloys
	•	Height: ~20–30 µm
	•	Integration notes
	•	TSV filling must be void-free to ensure reliability
	•	Micro bumps formed by electroplating or solder bump deposition techniques
	•	Critical for high-density 2.5D/3D packaging

Step 45 Final Passivation
	•	Process name Final Passivation Layer Formation
	•	Objective Protect the completed wafer/die with a final passivation layer to ensure device reliability and protect against contamination.
	•	Materials
	•	SiN and/or SiO₂ deposited by PECVD
	•	Process parameters
	•	Thickness: 0.5–1.0 µm
	•	Temperature: 300–400 °C
	•	Film properties
	•	Dense and pinhole-free for moisture and contaminant barrier
	•	Low stress to avoid wafer bow or cracking
	•	Integration notes
	•	Passivation covers all active areas except bonding pads
	•	Compatible with subsequent dicing and packaging processes

 Step 46 Wafer Test and Dicing
	•	Process name Wafer Electrical Testing and Dicing
	•	Objective Perform electrical tests on wafer-level devices to identify good dies and separate the wafer into individual chips.
	•	Testing methods
	•	Electrical test: Parametric, functional, and leakage tests using prober equipment
	•	Test patterns: Speed, leakage, threshold voltage, I-V characteristics
	•	Marking
	•	Ink or laser marking of good/bad dies
	•	Dicing process
	•	Method: Laser scribing and/or mechanical saw cutting (singulation)
	•	Kerf width: Minimized for die size optimization
	•	Die attach film and tape applied during dicing for mechanical support
	•	Integration notes
	•	Careful handling to avoid chipping or cracking
	•	Alignment and kerf control critical for packaging yield

Step 47 Packaging
	•	Process name Chip Packaging and Assembly
	•	Objective Encapsulate and interconnect dies for final product assembly.
	•	Packaging types
	•	Flip Chip Chip Scale Package (FC-CSP)
	•	Wafer Level Package (WLP)
	•	Fan-Out Wafer Level Package (FOWLP)
	•	Process details
	•	Die attach, wire bonding or flip chip bonding
	•	Encapsulation with mold compound or epoxy
	•	Underfill for mechanical stability
	•	Integration notes
	•	High-density interconnects for advanced nodes
	•	Thermal and electrical performance optimization
	•	Reliability under mechanical and thermal stress

Step 48 Final Test
	•	Process name Final Device Testing and Qualification
	•	Objective Verify device functionality and reliability before shipment.
	•	Test items
	•	Speed performance
	•	Leakage current
	•	Electrostatic discharge (ESD) robustness
	•	Temperature and voltage stress tests
	•	Test methods
	•	Automated test equipment (ATE) at wafer and packaged device levels
	•	Integration notes
	•	Failure analysis and binning for product sorting
	•	Yield data collection for process improvement

 
