# Results & Outputs

This folder contains all the outputs, reports, and visualizations generated from the 10-day FPGA workshop project, organized by day and analysis type.

## Folder Structure

```
results/
├── day1-vivado-basics/
│   ├── timing-analysis/
│   ├── synthesis-reports/
│   └── screenshots/
├── day2-openfpga-vpr-vtr/
│   ├── timing-analysis/
│   ├── power-analysis/
│   ├── place-route/
│   └── reports/
├── day3-riscv-vivado/
│   ├── timing-analysis/
│   ├── synthesis-reports/
│   ├── implementation-reports/
│   └── bitstream/
├── day4-sofa-fabric/
│   ├── area-utilization/
│   ├── post-implementation-sim/
│   └── resource-mapping/
└── day5-riscv-custom-fabric/
    ├── timing-analysis/
    ├── power-analysis/
    ├── place-route/
    └── final-reports/
```

## Contents by Day

### Day 1: Vivado Basics & Counter Design
- **Timing Analysis**: Timing reports from synthesis and implementation
- **Synthesis Reports**: RTL synthesis details, gate-level netlist information
- **Screenshots**: Vivado project manager, schematic views, constraint specification

### Day 2: OpenFPGA, VPR & VTR
- **Timing Analysis**: Timing results from VPR place and route
- **Power Analysis**: Power consumption reports from VTR flow
- **Place & Route**: Placement maps, routing visualizations, utilization stats
- **Reports**: Log files, detailed analysis reports from VPR/VTR runs

### Day 3: RISC-V Core in Vivado
- **Timing Analysis**: Critical path analysis, slack reports
- **Synthesis Reports**: RISC-V RTL synthesis details
- **Implementation Reports**: Place and route results, resource utilization
- **Bitstream**: Generated bitstream files for FPGA deployment

### Day 4: SOFA FPGA Fabric
- **Area Utilization**: LUT, flipflop, and adder utilization metrics
- **Post-Implementation Simulation**: Behavioral simulation results
- **Resource Mapping**: Mapping details on SOFA fabric (FPGA1212_QLSOFA_HD_PNR)

### Day 5: RISC-V on Custom SOFA Fabric
- **Timing Analysis**: End-to-end timing closure results
- **Power Analysis**: Power consumption on custom fabric
- **Place & Route**: Final placement and routing visualizations
- **Final Reports**: Comprehensive project summary and performance metrics

## File Naming Convention

For consistency, please follow this naming convention:

```
[Day][ContentType]_[Description]_[Date].[ext]

Examples:
- Day1_Timing_Counter_20260604.txt
- Day2_PowerReport_VTR_20260604.log
- Day3_SynthesisReport_RISC-V_20260604.pdf
- Day5_PlaceRoute_Final_20260604.png
```

## How to Use This Folder

1. **For Documentation**: Reference specific reports and screenshots when writing project documentation
2. **For Analysis**: Compare results across different days to track improvements
3. **For Presentations**: Use screenshots and visualizations for project presentations
4. **For Archival**: Keep a complete record of all design iterations and results

## Report Types

### Timing Analysis Reports
- Critical path information
- Setup and hold time violations
- Slack analysis
- Frequency/performance metrics

### Power Analysis Reports
- Static power consumption
- Dynamic power consumption
- Power distribution by component

### Synthesis Reports
- Gate count statistics
- LUT utilization
- Slice/block utilization
- Warning and error logs

### Place & Route Reports
- Resource utilization (LUTs, FFs, BRAMs)
- Timing closure status
- Routing congestion maps
- Area summaries

## Quick Reference

| Day | Key Output | Location |
|-----|-----------|----------|
| 1 | Counter synthesis schematic | day1-vivado-basics/screenshots/ |
| 2 | VPR timing analysis | day2-openfpga-vpr-vtr/timing-analysis/ |
| 3 | RISC-V bitstream | day3-riscv-vivado/bitstream/ |
| 4 | SOFA area utilization | day4-sofa-fabric/area-utilization/ |
| 5 | Final P&R results | day5-riscv-custom-fabric/place-route/ |

## Notes

- All timing analysis assumes clock frequency specifications from constraint files
- Power analysis uses default switching activity assumptions
- Post-implementation simulations use actual routed delays
- Resource utilization is measured on target FPGA devices

---

**Last Updated**: June 4, 2026
