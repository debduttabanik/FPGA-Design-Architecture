# Day 5: RISC-V on Custom SOFA Fabric

## Overview
Complete integration of RVMYTH RISC-V core on custom SOFA FPGA fabric using OpenFPGA and VTR flow.

## Design Pipeline
1. RTL (TL-Verilog) → Verilog compilation
2. Elaborate & Synthesize (ODIN II)
3. Logic Optimization & Technology Mapping (ABC)
4. Packing, Placement, Routing & Timing (VPR)
5. Power Analysis & Post-sim

## Subfolders

### Timing Analysis
RISC-V on SOFA timing closure:
- Critical path identification
- Setup/hold time verification
- Frequency achievable on 50MHz fabric
- Timing bottlenecks
- Slack distribution

### Power Analysis
Power consumption on SOFA (SkyWater 130nm):
- Total power breakdown
- Static vs dynamic power
- Per-block power analysis
- Power efficiency (mW/MHz)
- Comparison with previous designs

### Place & Route
Final implementation on SOFA:
- Placement visualization
- Routing congestion map
- Resource utilization heatmap
- Critical path routing
- Detailed floorplan

### Final Reports
Project summary and analysis:
- Design summary statistics
- Performance metrics
- Resource utilization summary
- Timing/power closure status
- Key findings and observations
- Recommendations for future work
