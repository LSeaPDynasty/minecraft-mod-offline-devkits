# Minecraft Mod 独立离线开发包

每个 Minecraft 版本的每种框架各自一个完整包，包含示例工程、对应 Java、Gradle ZIP、依赖缓存、游戏资源和已编译的 Mod JAR。平台为 Windows x64。

| Minecraft | 框架 | 下载入口 |
| --- | --- | --- |
| 1.7.10 | Forge 10.13.4.1614 | [Release](https://github.com/LSeaPDynasty/minecraft-mod-offline-devkits/releases/tag/mc-1.7.10-forge-2026.11.12) |
| 1.12.2 | Forge 14.23.5.2859 | [Release](https://github.com/LSeaPDynasty/minecraft-mod-offline-devkits/releases/tag/mc-1.12.2-forge-2026.11.12) |
| 1.20.1 | Forge 47.4.28 | [Release](https://github.com/LSeaPDynasty/minecraft-mod-offline-devkits/releases/tag/mc-1.20.1-forge-2026.11.12) |
| 1.20.1 | NeoForge 47.1.106 | [Release](https://github.com/LSeaPDynasty/minecraft-mod-offline-devkits/releases/tag/mc-1.20.1-neoforge-2026.11.12) |
| 1.20.1 | Fabric | [Release](https://github.com/LSeaPDynasty/minecraft-mod-offline-devkits/releases/tag/mc-1.20.1-fabric-2026.11.12) |
| 1.21.1 | Forge 52.1.20 | [Release](https://github.com/LSeaPDynasty/minecraft-mod-offline-devkits/releases/tag/mc-1.21.1-forge-2026.11.12) |
| 1.21.1 | NeoForge 21.1.265 | [Release](https://github.com/LSeaPDynasty/minecraft-mod-offline-devkits/releases/tag/mc-1.21.1-neoforge-2026.11.12) |
| 1.21.1 | Fabric | [Release](https://github.com/LSeaPDynasty/minecraft-mod-offline-devkits/releases/tag/mc-1.21.1-fabric-2026.11.12) |

## 使用

1. 从对应 Release 的 Assets 下载 `mc-版本-框架-offline-windows-x64.zip`。
2. 完整解压到较短路径，例如 `D:\MC\kit`。
3. 双击根目录 `Build-Offline.cmd` 离线构建。Gradle 首次使用时会从包内 ZIP 自动解压。
4. Mod JAR 位于对应工程的 `build/libs`。

GitHub 自动生成的 `Source code` 附件只包含仓库文档，开发包请下载上面指定的 ZIP。各包可以独立使用，不依赖其他版本的包。

## 验证范围

原始 8 套工程均已逐个离线构建并检查了 Mod JAR。压缩过程中核对了入包文件的 SHA-256。按照上传要求，拆分包没有额外完成迁移目录后的重新编译验证；IDE 导入与游戏启动尚未测试。

每个 Release 附有 ZIP 的 `.sha256` 和说明 JSON；包内的 `PACKAGE-MANIFEST.json` 记录逐文件大小及 SHA-256。新增依赖、修改加载器或映射版本后，需要在联网电脑重新准备缓存。

各模板、JDK、Minecraft 资源与第三方库沿用各自许可与条款，随包保留原有许可文件。
