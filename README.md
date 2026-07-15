# Dragon Library - 个人图书馆
欢迎来到 **Dragon Library**！这是一个专注于数字集成电路（IC）设计与计算机体系架构的个人学习与知识管理仓库。目录结构按照 **架构**、**硬件** 和 **软件** 三大维度组织，涵盖从指令集、微架构到EDA工具链的完整知识体系。

---

## 📂 目录结构说明
# 目录结构说明

```plaintext
Dragon_Library/
├── Architecture/
│   ├── ARM/
│   ├── MIPS/
│   └── RISC_V/
├── Hardware/
│   ├── Microarchitecture/
│   │   ├── Bus_Protocol/
│   │   │   └── CHI/
│   │   ├── MianPipeline/
│   │   ├── Prediction/
│   │   │   ├── Branch/
│   │   │   ├── Data/
│   │   │   ├── Instr/
│   │   │   ├── LoadStore/
│   │   │   ├── Total/
│   │   │   └── way/
│   │   └── Quantification/
├── Software/
│   └── Tool_Usage/
│       └── Cadence/
│           ├── Genus/
│           ├── Palladium/
│           └── Xcelium/
└── Synopsys/
    ├── DC_Design_Compiler/
    ├── FC_Fusion_Compiler/
    ├── Formality/
    ├── PT_PrimeTime/
    ├── SpyGlass/
    ├── StarRC/
    ├── VCS/
    ├── Verdi/
    └── VIP/
```

## 📖 各目录作用详细介绍

### 根目录
- **Library/** — 个人图书馆的根目录，存放所有架构、硬件、工具相关文档与脚本。

---

### Architecture/ — 指令集架构（ISA）
存放不同处理器指令集架构的规范、手册、开源实现及学习笔记。

- **ARM/** — ARM 架构相关文档（如 ARMv8/v9 手册、Cortex 系列微架构笔记）。
- **MIPS/** — MIPS 架构资料（包括经典 MIPS 五级流水线、指令集参考）。
- **RISC_V/** — RISC-V 开源架构（规范、特权模式、向量扩展，以及开源核如 Rocket Chip、BOOM 的文档）。

---

### Hardware/ — 硬件设计与微架构
涵盖数字电路设计、流水线、缓存、预测器及性能评估等核心硬件知识。

- **Microarchitecture/** — 微架构设计顶层目录，包含流水线、总线、预测、量化等子模块。
  - **Bus_Protocol/** — 片上总线协议（如 AMBA AXI/AHB/ACE）的学习资料。
    - **CHI/** — ARM Coherent Hub Interface 协议详解，包括一致性、链式传输等。
  - **MianPipeline/** — 主流水线设计（取指、译码、执行、访存、写回），含各阶段实现细节。
  - **Prediction/** — 预测技术总目录，涵盖分支预测、数据预取、指令预取等。
    - **Branch/** — 分支预测器（Gshare、TAGE、感知器、BTB 等）。
    - **Data/** — 数据预取（流预取、指针预取、基于步长的预取）。
    - **Instr/** — 指令预取 / 缓存预取策略。
    - **LoadStore/** — 访存单元（Load/Store 队列、重排序、内存依赖检测）。
    - **Total/** — 全局预测器 / 混合预测器设计（组合多种预测算法）。
    - **way/** — 组相联缓存路数预测（Way Prediction，减少访问延迟）。
  - **Quantification/** — 性能量化分析（CPI、IPC、Cache Miss 率、功耗评估等模型与脚本）。

---

### Software/ — EDA 工具与验证环境
存放主流 EDA 工具的使用流程、Tcl/Shell 脚本、约束模板及调试经验。

- **Tool_Usage/** — 工具使用文档的顶层目录。
  - **Cadence/** — Cadence 工具套件。
    - **Genus/** — 逻辑综合（Synthesis）脚本、综合约束、时序优化指南。
    - **Palladium/** — 硬件仿真加速器（Emulation）使用手册与测试用例。
    - **Xcelium/** — 数字仿真器（Simulation）命令行选项、覆盖率收集方法。
- **Synopsys/** — Synopsys 工具套件（独立于 Tool_Usage，按公司归类）。
  - **DC_Design_Compiler/** — 设计综合（Design Compiler）综合策略、DC Tcl 示例。
  - **FC_Fusion_Compiler/** — Fusion 综合（RTL-to-GDSII 融合流程）指导。
  - **Formality/** — 形式验证（Formal Verification）等效性检查脚本与 debug 案例。
  - **PT_PrimeTime/** — 静态时序分析（STA）约束、时序报告分析、ECO 方法。
  - **SpyGlass/** — RTL 静态检查（CDC、功耗、可测试性、lint）规则配置。
  - **StarRC/** — 寄生参数提取（RC Extraction）工艺文件与提取脚本。
  - **VCS/** — 仿真编译（Verilog/VHDL 仿真）选项、编译加速技巧。
  - **Verdi/** — 波形调试与追踪（Debug）使用技巧、自定义触发器设置。
  - **VIP/** — 验证 IP（如 AMBA、PCIe、DDR 协议 VIP）的集成与测试用例。

---

---

## 🧭 如何使用

- **架构学习**：进入 `Architecture/` 对应子目录，阅读指令集手册、微架构对比或开源实现（如 Rocket Chip、BOOM）。
- **硬件设计**：`Hardware/Microarchitecture/` 下存放流水线设计文档、总线协议解析、预测算法推导及性能评估脚本。
- **EDA 工具**：`Software/` 中各工具目录包含：
  - 常用命令行选项
  - Tcl/Shell 脚本模板
  - 时序约束示例
  - 常见问题与调试笔记

所有文档均以 Markdown 或 PDF 格式整理，部分结合代码示例（Verilog/SystemVerilog）。

---

## 🛠️ 维护原则

1. **分层清晰**：按功能域严格分类，避免交叉存放。
2. **版本追踪**：关键文档与脚本使用 Git 管理，重要变更记录在 CHANGELOG。
3. **引用规范**：外部资料（白皮书、论文）统一放入 `References/`（待建）并注明来源。

---

## 📌 当前状态

- ✅ 基础目录已建立
- 🔄 持续补充 ARM/RISC-V 微架构笔记
- 📝 正在整理 Genus 综合约束模板

---

## 🤝 贡献与交流

本库为个人学习仓库，但欢迎通过 Issue 或 Pull Request 提出建议、指正错误或分享相关资源。

**Happy Learning & Designing!**  
— Dragon
