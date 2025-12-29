# 🎬 SDR To HDR Converter

![Version](https://img.shields.io/badge/version-1.0-blue.svg) ![Python](https://img.shields.io/badge/Python-3.10+-yellow.svg) ![Platform](https://img.shields.io/badge/Platform-Windows-0078D6.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg)

**SDR To HDR Converter** 是一款专业的视频处理工具，专为将 SDR（标准动态范围）视频转换为 HDR（高动态范围）广播级标准而设计。

它基于 **FFmpeg** 和 **NVIDIA NVEnc** 硬件加速技术，通过加载高精度的 3D LUT，实现色彩空间的精确映射（Rec.709 -> Rec.2020/P3），并支持 **PQ** 和 **HLG** 两种主流 HDR 标准。

---

## ✨ 核心功能 (Features)

### 🖥️ 图形化操作界面 (GUI)
- **现代化 UI**：基于 `CustomTkinter` 构建的暗色系界面，简洁直观。
- **双模式运行**：
  - 📄 **单文件转换**：针对单个视频文件进行精细化处理。
  - 📂 **文件夹监控**：自动化监控指定目录，实现批量无人值守处理。

### ⚙️ 强大的视频编码控制
- **硬件加速**：完全利用 NVIDIA GPU (NVEncC) 进行 HEVC/H.265 10bit 编码。
- **HDR 标准**：支持 **PQ (Perceptual Quantizer)** 和 **HLG (Hybrid Log-Gamma)**。
- **色彩空间**：支持 **Rec.2020** 和 **DCI-P3** 广色域。
- **专业参数**：
  - 分辨率、帧率 (FPS)、GOP 长度自定义。
  - **码率控制**：支持 CBR (固定码率) 和 VBR (动态码率)。
  - **编码等级**：开放 Profile (Main10), Level (5.0-6.2), Tier (Main/High) 设置。

### 🎵 多音轨处理
- **多格式支持**：支持 AC3, AAC (libfdk_aac), MP2 等音频编码。
- **双音轨封装**：支持同时封装主音轨（如 5.1 声道）和副音轨（如立体声）。

### 📦 输出格式
- **广播级 TS**：符合电视台播出标准的 MPEG-TS 封装。
- **网络级 MP4**：适合网络分发的高兼容性 MP4 封装。

---

## 🛠️ 环境依赖 (Requirements)

本软件依赖以下组件运行：

1.  **操作系统**: Windows 10/11 (64位)
2.  **硬件**: NVIDIA 显卡 (支持 HEVC 10bit 编码)

---

## 🚀 快速开始 (Quick Start)

### 1. 运行软件
双击 `SDR To HDR Converter.exe` 启动程序。

### 2. 参数设置
- **源文件**: 点击“导入视频”选择 SDR 素材。
- **HDR 模式**: 根据需求选择 `PQ` 或 `HLG`。
- **视频参数**: 推荐使用默认的 `Main10` Profile 和 `5.1` Level。
- **音频设置**: 根据源文件声道情况配置音轨 1 和音轨 2。

### 3. 开始转换
点击底部的 **🚀 开始任务** 按钮。
- 程序会自动调用 FFmpeg 进行色彩映射，并传输给 NVEncC 进行编码。
- 进度条和日志窗口会实时显示处理进度。

---