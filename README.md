# PDF批注 PDF Annotate

在 Obsidian 内直接批注 PDF / EPUB 文档的插件：**高亮、下划线、删除线、自由画笔、页外浮动批注框**，多步撤销重做。**原始文件永不被修改**，批注单独存储。

## 功能

- 📝 **文本批注**：选中文字 → 高亮 / 下划线 / 删除线，5 色可选；可创建关联的页外批注框。
- ✏️ **自由画笔**：粗细 1–40 可调、颜色可选，带笔刷预览圆点。
- 🧹 **橡皮擦**：点一下擦一下（单击擦除圆内笔迹）。
- 📌 **页外浮动批注框**：放置在 PDF 页面外侧，框内多行文字，颜色可改，可拖拽/缩放/左右翻转。
- 🎨 **编辑批注**：点批注框头部的颜色圆点，可改框颜色、文字标记样式与颜色。
- ↩️ **撤销 / 重做**：多步历史（Ctrl+Z / Ctrl+Y）。
- 🗑️ **清除所有批注**：一键清空（带确认）。
- 💾 **数据安全**：批注保存在 `<文档名>.annotate.json`，**原始 PDF/EPUB 文件完全不变**。

## 安装

### 方式一：BRAT（推荐，可跟踪更新）

1. 安装社区插件 [BRAT](https://github.com/TfTHacker/obsidian42-brat)；
2. 命令面板运行 `BRAT: Add a beta plugin for testing`；
3. 输入本仓库地址（GitHub 仓库链接）即可。

### 方式二：手动安装

1. 到本仓库 [Releases](https://github.com/USER/REPO/releases) 下载最新版 `doc-annotate-<version>.zip`；
2. 解压得到 `main.js`、`manifest.json`、`styles.css` 三个文件；
3. 放入你的 Obsidian 仓库的 `.obsidian/plugins/doc-annotate/` 目录；
4. 设置 → 第三方插件 → 启用 **PDF批注 PDF Annotate**。

## 使用

- 打开一个 PDF 或 EPUB 文件，顶部工具栏出现批注工具；
- **文本批注**：选择「文本批注工具」，选中文字后弹出工具条，选高亮/下划线/删除线或「批注」（创建关联页外框）；
- **画笔**：选择画笔工具，按住拖动书写，右侧滑块调粗细；
- **橡皮擦**：选择橡皮擦，单击擦除笔迹；
- **页外批注框**：点击「添加页外浮动批注框」，在页面边缘生成批注框，可输入文字、拖动位置；
- **修改批注**：点批注框头部颜色圆点 → 编辑颜色/样式；
- **取消批注**：选中已批注文字 → 工具条出现「取消批注」；
- 批注自动保存，切换文档/关闭 Obsidian 不丢失。

## 兼容性

- 桌面版 Obsidian（Windows / macOS / Linux）
- PDF：依赖 Obsidian 原生 PDF 阅读器
- EPUB：本地阅读模式批注

## 数据格式

批注数据：`<文档名>.annotate.json`（与文档同目录），格式为 JSON，包含类型、颜色、坐标、文本等。删除该 JSON 文件即清除该文档全部批注。

## 开发

- 构建：`node esbuild.config.mjs production`
- 产物：`dist/main.js`（含内联 pdf.js worker）

## License

MIT
