# Week 9 - RISC-V SoC Tapeout Journey (Divya Darshan)
[![Repo Size](https://img.shields.io/github/repo-size/DivyaDarshan09/Divya_Darshan-VSD-RISCV-week-9)](https://github.com/DivyaDarshan09/Divya_Darshan-VSD-RISCV-week-9)
[![Owner](https://img.shields.io/badge/Owner-DivyaDarshan09-red)](https://github.com/DivyaDarshan09)
---
## VSD Baby SoC – Physical Design (RTL to GDSII)
- This repository documents the complete ASIC Physical Design (PD) flow carried out for the VSD RISC-V Baby SoC, using the open-source SKY130 PDK and industry-standard open-source EDA tools.
- The objective of this project is to take a synthesizable RISC-V SoC design through every stage from RTL to final GDSII, similar to a real production-grade chip tape-out flow.
---
## Project Summary

1. **Architecture:** VSD Baby RISC-V SoC
2. **Technology Node:** SkyWater SKY130
3. **Implementation Flow:** RTL → Synthesis → Floorplan → Placement → CTS → Routing → SPEF → Post Route STA → DRC & LVS → GDSII

```
┌───────────────────────────┐
│        Toolchain Used         │
├───────────────────────────┤                   
│ • Yosys                       │
│ • OpenROAD                    │
│ • Magic                       │                  
│ • KLayout                     │
│ • OpenSTA                     │
│ • SkyWater SKY130 PDK         │
└───────────────────────────┘
```


---
# 📚 Table of Contents

- [0 - Definition](0-Definition.md)
- [1.1 – Synthesis](1.1_Synthesis.md)
- [1.2 – Post Synthesis GLS](1.2_Post_Synthesis_GLS.md)
- [2 – Pre Route STA](2_Pre_Route_STA.md)
- [3 – Floorplan](3_Floorplan.md)
- [4 – Placement](4_Placement.md)
- [5 – Clock Tree Synthesis (CTS)](5_CTS.md)
- [6 – Routing](6_Routing.md)
- [7 – SPEF Analysis](7_SPEF_Analysis.md)
- [8 – Post Route STA](8_Pre_Route_STA.md)
- [PVT - Pre Route Analysis](PVT-Analysis_Pre_Route.md)
- [PVT - Post Route Analysis](PVT-Analysis_Post_Route.md)

---
##  Navigation

Each stage of the flow has its own markdown file containing:
```bash
- Commands used  
- Logs and reports  
- Screenshots  
- Observations and results
```
---

## 🏁 Final Results Summary

| Stage               | Status        |
|---------------------|---------------|
| RTL Synthesis       | ✅ Completed  |
| Floorplanning       | ✅ Completed  |
| Placement           | ✅ Completed  |
| CTS                 | ✅ Completed  |
| Routing             | ✅ Completed  |
| SPEF Extraction     | ✅ Completed  |
| STA                 | ✅ Passed     |
| DRC                 | ✅ Clean      |
| LVS                 | ✅ Clean      |
| GDSII               | ✅ Generated  |

---

**This project demonstrates a fully open-source end-to-end ASIC physical design flow, successfully completing layout, sign-off for the VSD Baby RISC-V SoC.**

---
## 🙌 Personal Note

- I began this journey with prior knowledge in digital and hardware design, and through this project, I was able to strengthen my understanding even more. By working hands-on through each stage — from RTL to GDSII — I gained deeper practical experience, clearer insights, and greater confidence in implementing a real RISC-V SoC flow.

- All the work, analysis, debugging, and documentation in this repository have been completed independently by **Divya Darshan VR**. I am proud of the progress I have made, and I know there is still much more to learn — and I am excited for the journey ahead.

- All the work, experiments, analysis, documentation, and results in this repository have been completed by **Divya Darshan VR** with full dedication and continuous learning throughout the RISC-V SoC tapeout journey.  

- I am truly happy and proud to have come this far and to be a part of this wonderful learning experience. I hope that my effort, consistency, and passion help me earn a place among the **Top 50 selected students**.

- 1 more week to go !!!!!!

- Thank you for reviewing my work!

- Thank You Kunal Sir and VSD Team for this wonderful oppurtunity.

---

