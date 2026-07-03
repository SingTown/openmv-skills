# OpenMV Skills

[English](README.md) | 简体中文

由 [SingTown](https://singtown.com) 开发的 OpenMV Camera 开发插件。

## 智能体会做什么

当你询问 OpenMV 相关问题时，智能体不会只生成一段代码，而是按嵌入式视觉开发流程工作。它会：

- 自动搜索内置官方示例，找到相似脚本和可靠写法
- 在使用函数或模块前查看本地 OpenMV API 文档，避免臆测不存在的接口
- 编写完整可运行的 MicroPython 脚本，并先保存到本地文件作为唯一源文件
- 当你需要在硬件上测试时，通过 MCP 工具发现并连接 OpenMV 相机
- 在相机上运行已保存的脚本，读取 stdout/stderr 输出，并抓取相机帧
- 检查抓取到的图像结果，对照目标行为判断是否正确
- 根据报错、输出、图像和你的反馈继续调试，调整阈值或参数并重新运行
- 只有在你明确希望开机自启动时，才把脚本部署为 `main.py`

## 安装

在 Claude Code 或 Codex 中输入：

```text
安装 https://raw.githubusercontent.com/SingTown/openmv-skills/refs/heads/main/INSTALL.md
```

## 许可证

[MIT](LICENSE)
