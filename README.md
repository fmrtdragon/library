# Dragon Library - 个人图书馆
欢迎来到 **Dragon Library**！这是一个专注于数字集成电路（IC）设计与计算机体系架构的个人学习与知识管理仓库。目录结构按照 **架构**、**硬件** 和 **软件** 三大维度组织，涵盖从指令集、微架构到EDA工具链的完整知识体系。

---

## 📂 目录结构说明
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

Dragon_Library/
├── Architecture/ # 指令集架构 (ISA)
│ ├── ARM/ # ARM 架构文档、手册、笔记
│ ├── MIPS/ # MIPS 架构相关资料
│ └── RISC_V/ # RISC-V 开源架构规范与实现
│
├── Hardware/ # 硬件设计与微架构
│ ├── Microarchitecture/ # 微架构设计（流水线、乱序、缓存等）
│ │ ├── Bus_Protocol/ # 总线协议（如 AXI、AHB、ACE）
│ │ │ └── CHI/ # ARM Coherent Hub Interface 协议详解
│ │ ├── MianPipeline/ # 主流水线设计（取指、译码、执行、访存、写回）
│ │ ├── Prediction/ # 分支预测与数据预取
│ │ │ ├── Branch/ # 分支预测（Gshare、TAGE、BTB 等）
│ │ │ ├── Data/ # 数据预取（流预取、指针预取）
│ │ │ ├── Instr/ # 指令预取 / 缓存预取
│ │ │ ├── LoadStore/ # 访存单元与重排序
│ │ │ ├── Total/ # 全局预测器 / 混合预测器
│ │ │ └── way/ # 组相联缓存路数预测 / 路选择
│ │ └── Quantification/# 性能量化分析（CPI、IPC、Cache Miss 率等）
│ └── ... # 其他硬件子模块
│
└── Software/ # EDA 工具与验证环境
├── Tool_Usage/ # 主流 EDA 工具的使用脚本、流程、TCL 命令
│ └── Cadence/ # Cadence 工具套件
│ ├── Genus/ # 逻辑综合（Synthesis）
│ ├── Palladium/ # 硬件仿真加速器（Emulation）
│ └── Xcelium/ # 数字仿真器（Simulation）
└── Synopsys/ # Synopsys 工具套件
├── DC_Design_Compiler/ # 设计综合（Design Compiler）
├── FC_Fusion_Compiler/ # Fusion 综合（RTL-to-GDSII 融合）
├── Formality/ # 形式验证（Formal Verification）
├── PT_PrimeTime/ # 静态时序分析（STA）
├── SpyGlass/ # RTL 静态检查（CDC、功耗、可测试性）
├── StarRC/ # 寄生参数提取（RC Extraction）
├── VCS/ # 仿真编译（Verilog/VHDL 仿真）
├── Verdi/ # 波形调试与追踪（Debug）
└── VIP/ # 验证 IP（总线、接口协议）

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
