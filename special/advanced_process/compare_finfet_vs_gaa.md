# FinFET vs GAA – Process and Technology Comparison

## 1. Overview

**FinFET (Fin Field-Effect Transistor)** and **GAA (Gate-All-Around)** are advanced transistor architectures used in CMOS technology nodes below 22nm. GAA is considered the evolutionary successor to FinFET, designed to offer better electrostatic control and scalability below the 5nm node.

---

## 2. Structural Comparison

| Feature              | FinFET                  | GAA (Nanosheet)                  |
|----------------------|--------------------------|----------------------------------|
| Gate architecture    | 3-sided gate around fin | 4-sided gate around nanosheet    |
| Channel geometry     | Vertical fin            | Horizontal stacked sheets        |
| Electrostatic control| Good                    | Excellent                        |
| Gate length scaling  | ~20 nm                  | <15 nm                           |
| Subthreshold control | Moderate                | Strong                           |
| Leakage control      | Good                    | Superior                         |

---

## 3. Process Flow Differences

| Process Step         | FinFET                        | GAA                             |
|----------------------|-------------------------------|----------------------------------|
| Substrate            | Bulk Si or SOI                | Bulk Si, sometimes SiGe         |
| Fin/Nanosheet formation | Single Si etch             | Si/SiGe superlattice + selective etch |
| Dummy gate           | PolySi + CMP                  | Similar, tighter CD control     |
| Channel release      | Not applicable                | Selective SiGe etch (sheet suspension) |
| High-k/Metal Gate    | Conformal, on fin             | Fully conformal, wraparound     |
| Spacer & S/D         | Standard spacers + EPI        | Spacer + EPI under nanosheets   |

---

## 4. Performance Comparison

| Metric               | FinFET        | GAA            |
|----------------------|---------------|----------------|
| Subthreshold Swing   | ~70 mV/dec    | <65 mV/dec     |
| DIBL                 | Moderate      | Lower          |
| I<sub>on</sub>/I<sub>off</sub> | High / Low | Higher / Lower |
| Drive current        | High          | Higher         |
| Area efficiency      | Good          | Better         |
| Short channel control| Limited <5nm  | Excellent @3nm |

---

## 5. Manufacturability

| Aspect              | FinFET                 | GAA                              |
|---------------------|------------------------|----------------------------------|
| Process maturity    | Mass production (22nm–)| Early production (3nm)           |
| Complexity          | Moderate               | High (EUV + selective etch)      |
| Cost                | Lower                  | Higher initially                 |
| Yield control       | Well understood        | Variable (early stage)           |
| Main adopters       | Intel, TSMC, Samsung   | Samsung (3nm), TSMC (3nm)        |

---

## 6. Design Flexibility

| Aspect              | FinFET                   | GAA                             |
|---------------------|--------------------------|----------------------------------|
| Gate width control  | Discrete (fin count)     | Continuous (sheet count/width)  |
| Channel tuning      | Fin pitch & height       | Sheet width, count, thickness   |
| Custom sizing       | Difficult                | Easier                          |
| SRAM design         | Stable                   | Under development               |
| ESD robustness      | Good                     | Requires optimization           |

---

## 7. Technology Roadmap

| Node   | FinFET           | GAA                        |
|--------|------------------|----------------------------|
| 22–7nm | ✅ Mainstream     | ❌ Not applicable          |
| 5nm    | ✅ Mature         | ✅ Pilot (Samsung, TSMC)   |
| 3nm    | ⚠️ Scaling limit | ✅ Mass production begins  |
| 2nm    | ❌ Not scalable   | ✅ Target architecture     |
| <2nm   | ❌ Unfeasible     | ✅ Forksheet / CFET evolve |

---

## 8. Summary

FinFET has driven CMOS scaling since the 22nm era, but its limitations in electrostatic control and integration density emerge below 5nm. GAA, particularly in the form of nanosheet FETs, offers improved scalability, design flexibility, and device performance.

However, GAA introduces additional process steps and complexity, requiring advanced lithography and precision etching. As such, it is adopted in leading-edge nodes starting at 3nm.

For educational purposes, comparing these technologies provides essential insight into semiconductor device scaling, fabrication challenges, and architectural innovation.
