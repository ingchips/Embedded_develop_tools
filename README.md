# Embedded Develop Tools

本仓库为 **INGChips（桃芯科技）VS Code 开发插件**所依赖的第三方工具提供统一的下载分发接口。

插件在首次安装或环境初始化时，会从本仓库获取所需的命令行工具压缩包，并在本地解压、配置到插件的工作环境中，无需用户手动下载和安装。

## 提供的工具

| 文件 | 说明 |
| --- | --- |
| `arm-none-eabi-toolchain-15.2-slim-lto.7z` | GNU Arm Embedded 交叉编译工具链（slim / LTO 版本），用于编译 Cortex-M 目标固件。 |
| `openocd-0.12.0-rc.7z` | OpenOCD 0.12.0-rc 调试与烧录工具，支持通过 CMSIS-DAP / DAPLink 等探针下载和调试固件。 |
| `make.7z` | GNU Make 构建工具，用于驱动基于 Makefile 的构建流程。 |

## 使用方式

这些压缩包由 INGChips VS Code 插件自动下载和解压，普通用户一般不需要手动使用。

如果需要手动获取，可以直接下载对应文件，使用支持 `.7z` 格式的解压工具（如 7-Zip）解压后，将工具所在目录加入系统 `PATH` 环境变量即可。

## 目录结构

```
.
├── arm-none-eabi-toolchain-15.2-slim-lto.7z
├── make.7z
├── openocd-0.12.0-rc.7z
└── LICENSE
```

## 许可证

本仓库采用 [MIT License](LICENSE) 授权。

仓库中分发的第三方工具（GNU Arm Embedded Toolchain、OpenOCD、GNU Make 等）各自遵循其原始许可证：

- **GNU Arm Embedded Toolchain**：GPLv3（含 GCC Runtime Library Exception）
- **OpenOCD**：GPLv2
- **GNU Make**：GPLv3

使用上述工具时，请同时遵守其各自的许可条款。
