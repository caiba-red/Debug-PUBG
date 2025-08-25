# HvGuardDbg

基于 **VMX / EPT** 的虚拟化防护与反调试框架，专为 **逆向工程、安全测试、驱动级调试** 等高强度防护场景设计。  
通过内核级虚拟化与用户态接口相结合，实现 **调试器保护、反反调试与动态控制**。

---

## ✨ 主要功能

- **虚拟化保护**  
  - 基于 VMX / EPT 的内存访问控制  

- **调试器防护**  
  - 隐藏硬件断点与软件断点  
  - 过滤游戏抛异常事件
  - 避免调试窗口被检测  

- **反反调试机制**  
  - 针对 EAC、BattleEye 等反作弊环境的检测规避  

# 📸 软件截图

## 软件图
这里展示前端界面、控制面板等  

<p align="center">
  <img src="Image_1754908639461.png" alt="HvFrontEnd 界面" width="600"/>
</p>

---

# 🎮 游戏测试截图

## 游戏测试图
这里展示在游戏环境下的调试保护效果  

<p align="center">
  <img src="IMG_20250814_091603.png" alt="游戏测试效果" width="600"/>
## ⚠️ 注意事项

使用 HvGuardDbg 可能存在一定的 **系统稳定性风险**，请务必在实验环境或虚拟机中先行测试。  

- **蓝屏风险**  
  - 由于涉及 **VMX / EPT 虚拟化指令** 与 **内核驱动加载**，错误配置可能导致蓝屏 (BSOD)。  
  - 建议在测试前 **保存所有工作文件**，避免数据丢失。  

- **兼容性问题**  
  - 不同版本的 Windows 10 / 11 在内核安全机制上存在差异，可能导致功能失效或冲突。  
  - 某些安全软件、可能与本工具产生兼容性问题。  

- **硬件依赖**  
  - 需确保 CPU 支持 **Intel VT-x / EPT** 并已在 BIOS 中启用。  
  - 在混合架构 (P-Core / E-Core) 平台上，可能存在稳定性差异。  

- **合法合规**  
  - 本工具仅适用于 **安全研究、逆向工程与驱动级调试** 等合法用途。  
  - 请勿用于任何违反法律法规或破坏性场景，否则后果自负。  

# Hypervisor-Guarded Debugger (HvGuardDbg)  
**VMX/EPT-Based Virtualization Protection & Anti-Debugging Framework**  
*For Reverse Engineering, Security Testing & Driver-Level Debugging*  

---

## ✨ Core Features  

### Virtualization Protection  
- **EPT Memory Control**  
  Fine-grained memory access monitoring via Extended Page Tables  
- **VMX Root-Mode Operation**  
  Kernel-level isolation for undetectable debugging operations  

### Debugger Protection  
- **Stealth Breakpoints**  
  Hide hardware/software breakpoints from anti-debuggers  
- **Exception Filtering**  
  Filter game exception events to prevent detection  
- **Window Obfuscation**  
  Mask debugging windows from process scanners  

### Anti-Anti-Debugging  
- **Anti-Cheat Evasion**  
  Bypass EAC, BattleEye, VAC, and kernel-level protections  
- **Dynamic Behavior Masking**  
  Randomize debugger fingerprints during runtime  

---


---

## ⚠️ Critical Usage Notes  

### System Stability Risks  
- **BSOD Potential**  
  > VMX misconfigurations may cause system crashes  
  *Recommendation: Always test in virtualized environments first*  
- **Hardware Requirements**

