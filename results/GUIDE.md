# FPGA Design Architecture - Results & Outputs Guide

## Welcome!

This comprehensive guide documents all the outputs, reports, and visualizations from the **10-day FPGA workshop** covering:
- **Day 1**: Vivado Basics & Counter Design
- **Day 2**: OpenFPGA, VPR & VTR
- **Day 3**: RISC-V Core Programming in Vivado
- **Day 4**: SOFA FPGA Fabric Introduction
- **Day 5**: RISC-V Core on Custom SOFA Fabric

---

## 📁 Directory Structure

```
results/
├── README.md (Main guide - this file)
│
├── day1-vivado-basics/
│   ├── README.md
│   ├── timing-analysis/          # Post-synthesis & implementation timing
│   ├── synthesis-reports/        # RTL synthesis details
│   └── screenshots/              # Vivado interface snapshots
│
├── day2-openfpga-vpr-vtr/
│   ├── README.md
│   ├── timing-analysis/          # VPR post-route timing
│   ├── power-analysis/           # VTR power reports (45nm PTM)
│   ├── place-route/              # Floorplan & routing visualizations
│   └── reports/                  # Tool logs and summaries
│
├── day3-riscv-vivado/
│   ├── README.md
│   ├── timing-analysis/          # RISC-V timing closure
│   ├── synthesis-reports/        # Synthesis statistics
│   ├── implementation-reports/   # Place & route on Basys3
│   └── bitstream/                # .bit, .bin files
│
├── day4-sofa-fabric/
│   ├── README.md
│   ├── area-utilization/         # Resource metrics
│   ├── post-implementation-sim/  # Simulation results
│   └── resource-mapping/         # Detailed mapping info
│
└── day5-riscv-custom-fabric/
    ├── README.md
    ├── timing-analysis/          # End-to-end timing
    ├── power-analysis/           # SOFA power consumption
    ├── place-route/              # Final P&R visualization
    └── final-reports/            # Project summary
```

---

## 🎯 Quick Start Guide

### Finding Specific Outputs

| What You're Looking For | Location |
|------------------------|----------|
| **Counter simulation waveforms** | `day1-vivado-basics/screenshots/` |
| **VPR placement visualization** | `day2-openfpga-vpr-vtr/place-route/` |
| **VPR routing details** | `day2-openfpga-vpr-vtr/place-route/` |
| **RISC-V bitstream** | `day3-riscv-vivado/bitstream/` |
| **RISC-V timing closure** | `day3-riscv-vivado/timing-analysis/` |
| **SOFA resource utilization** | `day4-sofa-fabric/area-utilization/` |
| **RISC-V on SOFA power** | `day5-riscv-custom-fabric/power-analysis/` |
| **Final project report** | `day5-riscv-custom-fabric/final-reports/` |

---

## 📊 File Naming Convention

All files follow a consistent naming pattern for easy identification:

```
[Day][ContentType]_[Description]_[Date].[extension]

Examples:
Day1_Timing_Counter_20260604.txt
Day2_PowerReport_VTR_20260604.pdf
Day3_SynthesisReport_RISC-V_20260604.log
Day5_PlaceRoute_Final_20260604.png
```

---

## 📋 Report Types Overview

### **Timing Analysis Reports**
- Critical path information
- Worst negative slack (WNS)
- Total negative slack (TNS)
- Setup/hold time violations
- Maximum achievable frequency

### **Power Analysis Reports**
- Static power consumption
- Dynamic power consumption  
- Power per component/block
- Power efficiency metrics
- Technology node specifications

### **Synthesis Reports**
- Gate count statistics
- LUT utilization breakdown
- Timing estimates
- Resource predictions
- Warning and error logs

### **Place & Route Reports**
- Block/LUT placement coordinates
- Routing congestion maps
- Resource utilization (LUTs, FFs, BRAMs)
- Critical path routing
- Area summaries

### **Screenshots & Visualizations**
- Design schematics
- Package pin assignments
- Floorplan layouts
- Routing diagrams
- Signal waveforms

---

## 🔍 Key Metrics Summary

### Day 1: Counter Design
- **Design**: 4-bit up counter with clock division
- **FPGA Board**: Basys 3 (Artix-7)
- **Status**: RTL → Synthesis → Implementation → Bitstream

### Day 2: VPR/VTR Flow
- **Packing**: Primitives → Complex blocks
- **Placement**: Blocks placed on FPGA grid
- **Routing**: Interconnections determined
- **Analysis**: Timing & Power calculated

### Day 3: RISC-V Core
- **Design**: 4-stage pipelined RVMYTH core
- **Language**: Verilog (compiled from TL-Verilog)
- **Target**: Basys 3 FPGA (xc7a35tcpg236-1)
- **Output**: Executable bitstream

### Day 4: SOFA Fabric
- **Fabric**: FPGA1212_QLSOFA_HD_PNR
- **Process**: SkyWater 130nm
- **Resources**: 1152 LUTs, 2304 FFs, 1152 Adders
- **Frequency**: 50MHz max

### Day 5: RISC-V on SOFA
- **Integration**: RVMYTH + SOFA + OpenFPGA + VTR
- **Process**: Complete open-source flow
- **Outputs**: Timing, Power, P&R results
- **Analysis**: Full design metrics

---

## 📈 How to Use These Results

### For Documentation
1. Reference specific timing reports when writing technical docs
2. Use screenshots for presentations and tutorials
3. Cite power analysis in design papers

### For Analysis
1. Compare results across days to track improvements
2. Identify performance bottlenecks from critical paths
3. Analyze resource utilization trends
4. Study routing efficiency metrics

### For Learning
1. Understand the complete FPGA design flow
2. Learn tool-specific outputs (Vivado, VPR, VTR)
3. Examine how designs map to FPGA fabric
4. Study timing and power trade-offs

### For Future Projects
1. Use as reference for similar designs
2. Compare baseline metrics
3. Identify optimization opportunities
4. Reuse working configurations

---

## 📝 Notes & Important Information

### Timing Analysis
- All timing assumes specified clock constraints from files
- Critical paths highlight design bottlenecks
- Slack values indicate timing margin or violation

### Power Analysis
- Day 2 uses 45nm PTM (Predictive Technology Model)
- Day 5 uses SkyWater 130nm process
- Power figures assume typical switching activity
- Static power dominates at 130nm

### Post-Implementation Simulation
- Includes actual routed delays and parasitic effects
- More accurate than pre-routing simulation
- Useful for timing verification

### Resource Utilization
- Measured on target FPGA device
- Includes routing overhead
- Higher utilization may impact timing closure

---

## 🔗 Cross-References

### Day-to-Day Progression
- Day 1 Counter → baseline design
- Day 2 VPR/VTR → academic flow on same counter
- Day 3 RISC-V → more complex design
- Day 4 SOFA → alternative fabric
- Day 5 RISC-V on SOFA → complete custom flow

### Tool Relationships
- **Vivado** (Days 1, 3): Commercial Xilinx tool
- **VTR** (Day 2): Open-source framework
- **VPR** (Day 2, 5): Place and route engine
- **OpenFPGA** (Days 4, 5): FPGA generation framework

---

## 📚 Related Documentation

For more information, refer to:
- Main repository README.md
- Individual day-specific README files
- FPGA Report.docx (project documentation)
- Day-specific image files and screenshots

---

## ✅ Verification Checklist

Use this to verify your understanding of the results:

- [ ] Understand the role of each day's output
- [ ] Can identify timing critical paths
- [ ] Know how to interpret power reports
- [ ] Understand resource utilization metrics
- [ ] Can trace design flow from RTL to bitstream
- [ ] Know differences between commercial and open-source tools

---

**Last Updated**: June 4, 2026  
**Workshop Duration**: 10 days  
**Primary Design Examples**: 4-bit Counter, RVMYTH RISC-V Core  
**Target Platforms**: Basys 3 FPGA, SOFA Fabric (SkyWater 130nm)

---

For questions or contributions, refer to the main repository or contact the workshop organizers.
