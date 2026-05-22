# Physical Design Implementation of PicoRV32a using OpenLANE

This project demonstrates the complete ASIC implementation flow of the PicoRV32a RISC-V processor using the OpenLANE automated design flow with SKY130 technology.
The objective of this work is to understand the RTL-to-GDSII flow and analyze different stages involved in modern ASIC physical design.


# Section 1: Introduction to Open-Source ASIC Design Flow, OpenLANE and SKY130 PDK

## Objectives of this Section

1. Running synthesis for the PicoRV32a RISC-V core using the OpenLANE automated flow.
2. Generating synthesis reports and required design outputs.
3. Understanding the hardware implementation flow using open-source EDA tools.
4. Estimating the flop ratio from the synthesized netlist.

---

## 1. RTL Synthesis of PicoRV32a using OpenLANE

The synthesis stage converts the RTL representation of the PicoRV32a processor into a gate-level netlist using standard cells available in the SKY130 library.  
This process was performed using the OpenLANE automated ASIC flow.

### Launching the OpenLANE Environment

```bash
# Navigate to the OpenLANE working directory
cd Desktop/work/tools/openlane_working_dir/openlane

# Start the docker container for OpenLANE
docker
```

### Starting OpenLANE in Interactive Mode

```bash
./flow.tcl -interactive
```

### Loading OpenLANE Package

```bash
package require openlane 0.9
```

### Preparing the PicoRV32a Design

```bash
prep -design picorv32a
```

### Running RTL Synthesis

```bash
run_synthesis
```

The synthesis process generates the optimized gate-level netlist along with timing, utilization and area reports required for further physical design stages.
