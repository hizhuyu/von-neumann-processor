# 🚀 von-neumann-processor

> "I think there is a world market for maybe five computers." - Thomas Watson, 1943
> Let's build one from scratch.

## 🎯 项目愿景
本项目旨在从零开始，通过软件仿真（Logisim）与物理实现（FPGA），完整复现并深入理解现代计算机的基石——**冯·诺依曼架构（Von Neumann Architecture）**。
最终目标是实现一个支持自定义指令集的处理器，并在 FPGA 上完成软硬件协同设计。

## 🏛️ 架构设计 (The Von Neumann Model)
本项目将严格遵循冯·诺依曼架构的五大核心部件进行模块化设计与连线：
1. **运算器 (ALU)**：执行算术与逻辑运算。
2. **控制器 (Control Unit)**：指令译码与时序控制。
3. **存储器 (Memory)**：统一存储指令（ROM/RAM）与数据。
4. **输入设备 (Input)**：拨码开关/按键。
5. **输出设备 (Output)**：LED灯/数码管。

## 🗺️ 路线图 (Roadmap)
- [ ] **Phase 1: 逻辑直觉与仿真** (Logisim-Evolution)
  - [ ] 搭建基础逻辑门与多路选择器 (MUX)
  - [ ] 设计 8 位 ALU 与寄存器堆 (Register File)
  - [ ] 实现程序计数器 (PC) 与指令存储器 (Instruction Memory)
  - [ ] **Milestone**: 拼装单周期冯·诺依曼处理器并跑通斐波那契数列
- [ ] **Phase 2: 硬件描述语言与物理降临** (Verilog & FPGA)
  - [ ] 将 Logisim 设计重构为 SystemVerilog RTL 代码
  - [ ] 在 Vivado 中完成仿真验证与逻辑综合
  - [ ] 烧录至 Xilinx Artix-7 FPGA 开发板
- [ ] **Phase 3: 软硬件协同** (C/C++ & Architecture)
  - [ ] 编写交叉编译器与底层汇编/固件
  - [ ] 设计硬件矩阵乘法加速器 (Hardware Accelerator)

## 📁 目录结构
- `src/`: 核心硬件设计文件 (Logisim `.circ` / Verilog `.v`)
- `sim/`: 仿真测试平台 (Testbenches)
- `docs/`: 架构设计图、ISA(指令集)文档与学习笔记
- `fpga/`: FPGA 引脚约束 (`.xdc`) 与实现脚本
- `sw/`: 运行在自研处理器上的软件代码 (C/Assembly)

## 🛠️ 工具链
- **Logic Simulation**: Logisim-Evolution
- **RTL Simulation & Synthesis**: AMD/Xilinx Vivado
- **Target Hardware**: Digilent Basys 3 / Nexys A7 (Planned)
