# FPGA Laboratory Works (Labs 1-10)

**Course:** FPGA Design with Vivado  
**Platform:** Xilinx Artix-7 A15T (xc7a15tftg256-2)  
**Tools:** Vivado 2023.2, SystemVerilog

---

## 📚 Laboratory Works

| Lab | Title | Description | Status |
|-----|-------|-------------|--------|
| **1** | **Door Alarm System** | Combinational OR logic gate for alarm trigger | ✅ Complete |
| 2 | Counter | [TBD] | - |
| 3 | Traffic Light Controller | [TBD] | - |
| 4 | Multiplexer | [TBD] | - |
| 5 | UART Interface | [TBD] | - |
| 6 | State Machine | [TBD] | - |
| 7 | Memory Controller | [TBD] | - |
| 8 | PWM Generator | [TBD] | - |
| 9 | Digital Filter | [TBD] | - |
| 10 | Complete System | [TBD] | - |

---

## 🎯 Quick Start

### Lab 1: Door Alarm System

**Navigate to lab:**
```powershell
cd lab01-door-alarm
```

**Project structure:**
```
lab01-door-alarm/
├── src/my_module.sv         # Top module: car (door1, door2 -> lamp)
├── tb/my_module_tb.sv       # Testbench with 4 test cases
├── constraints/
│   ├── car.xdc              # Pin assignments (door1: btn[0], door2: btn[1], lamp: yled)
│   └── board.xdc            # Board definitions
├── scripts/
│   ├── create_vivado_project.tcl
│   ├── synth_vivado.tcl
│   ├── flow_complete.tcl
│   └── program_fpga.tcl
└── README.md                # Lab 1 documentation
```

**Build and program:**
```powershell
cd lab01-door-alarm/scripts

# Synthesis & Implementation
& "C:\Xilinx\Vivado\2023.2\bin\vivado.bat" -mode batch -source flow_complete.tcl

# Program FPGA (requires Digilent cable)
& "C:\Xilinx\Vivado\2023.2\bin\vivado.bat" -mode batch -source program_fpga.tcl
```

---

## 📖 Each Lab Includes

- **src/** — SystemVerilog source code
- **tb/** — Testbenches for simulation
- **constraints/** — XDC pin assignments & timing
- **scripts/** — TCL automation for Vivado
- **README.md** — Lab-specific documentation

---

## 📊 Resource Usage (Lab 1)

| Resource | Used | Total | Util% |
|----------|------|-------|-------|
| Slice LUTs | 1 | 10400 | <0.01% |
| Registers | 0 | 20800 | 0.00% |
| Bonded IOB | 3 | 170 | 1.76% |

---

## ⏱️ Build Times (Lab 1)

- Synthesis: 00:01:28
- Implementation: 00:05:24
- Bitstream generation: ~00:00:25
- **Total: ~00:07:17**

---

## 🔗 References

- [Xilinx Vivado Documentation](https://www.xilinx.com/documentation.html)
- [Artix-7 Datasheet](https://www.xilinx.com/support/documentation/data_sheets/ds181_Artix_7_Data_Sheet.pdf)
- [SystemVerilog LRM](https://ieeexplore.ieee.org/servlet/opac?punumber=6691051)

---

## 📝 Notes

- All labs use Artix-7 A15T FPGA
- LVCMOS33 IO standard (3.3V)
- Vivado 2023.2 for synthesis
- Digilent JTAG for programming

---

**Created:** Feb 8, 2026  
**Last Updated:** Feb 8, 2026
