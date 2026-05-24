# Telegram Cloud

[![Python Version](https://img.shields.io/badge/python-3.10-blue.svg)](https://www.python.org/)
[![PySide6](https://img.shields.io/badge/GUI-PySide6%2BQFluentWidgets-green)](https://doc.qt.io/qtforpython-6/)
[![Telegram API](https://img.shields.io/badge/Telegram-Pyrogram-0088cc)](https://pyrogram.org/)

**Telegram Cloud** 是一款将 Telegram 作为无限云存储的桌面客户端。它提供了类似网盘的界面，支持文件上传、下载、在线预览、目录管理以及本地文件夹自动同步。程序可最小化至系统托盘，在后台自动同步，不影响前台操作。

---

## 功能特性

- 🔐 **Telegram 账号登录**  
  支持 API ID / API Hash 登录，会话持久化，可随时登出。

- 📁 **文件管理**  
  列表/图标双视图、拖拽移动、批量删除、重命名、属性查看。右键菜单支持下载、移动、新建文件夹等操作。

- 👀 **文件预览**  
  支持图片、音频（带进度条）、视频、文本文件的在线预览，超过 20 MB 文件禁止预览。

- 📤 **上传与下载**  
  可选择文件或文件夹批量上传，带重试机制。下载任务进度实时显示，支持后台线程异步处理。

- 📂 **目录与频道**  
  软件内目录与 Telegram 频道自动绑定，支持多级子目录。频道失效或数据库记录丢失时智能重建。

- 🔄 **自动同步**  
  添加本地文件夹，按分钟/小时/天定时同步到 Telegram 目录。同步仅在窗口最小化到托盘时运行，打开窗口时自动暂停。同步过程中自动维护本地与远程的目录结构一致。

- 🖥️ **系统托盘**  
  关闭窗口最小化到托盘，右键菜单提供“打开网盘”和“退出程序”。双击托盘图标恢复窗口。

- 🌐 **本地同步操作**  
  在自动同步文件夹内，新建、重命名、移动、删除文件或子目录时，本地磁盘会同步发生相同变更。删除同步根目录只清理 Telegram 频道和数据库，不删除本地文件。

- 🔍 **智能搜索**  
  支持按文件名模糊搜索，小数据量直接 LIKE 查询，数据量大时自动启用 jieba 分词 + 倒排索引加速，兼顾效率与准确性。

- 📊 **上传限制**  
  可启用每日上传大小/数量限制，基于东八区（北京时间）统计，侧边栏通过滑块实时显示今日用量与限额的关系。

- 🧩 **任务队列**  
  弹窗展示上传/下载进度及自动同步状态，记录持久化到数据库，支持按时间排序。

- 🎨 **现代界面**  
  基于 QFluentWidgets 提供美观的控件，支持深色/浅色主题。侧边栏目录树中，自动同步根文件夹带有特殊图标标识。

- 📝 **日志系统**  
  日志同时输出到控制台和文件，按天轮转保留最近 7 天，并过滤冗余的 Pyrogram 会话日志。

---

> Telegram API 凭据申请：访问 [my.telegram.org](https://my.telegram.org/)，创建应用获取 api_id 和 api_hash。

---

##  [下载最新版](https://github.com/ydtg1993/telegram_cloud/releases/download/v1.1.0/TelegramCloud_Setup.exe)
<a href="https://github.com/ydtg1993/telegram_cloud/releases/download/v1.1.0/TelegramCloud_Setup.exe"><img src="https://cdn.jsdelivr.net/gh/ydtg1993/telegram_cloud@main/tc.png"/></a>

## 界面预览
<table>
  <tr>
    <td><img width="300" src="https://cdn.jsdelivr.net/gh/ydtg1993/telegram_cloud@main/Capture1.PNG"/></td>
    <td><img width="300" src="https://cdn.jsdelivr.net/gh/ydtg1993/telegram_cloud@main/Capture2.PNG"/></td>
    <td><img width="300" src="https://cdn.jsdelivr.net/gh/ydtg1993/telegram_cloud@main/Capture3.PNG"/></td>
  </tr>
</table>

## 技术栈与依赖

- [PySide6](https://pypi.org/project/PySide6/) - Qt for Python 绑定
- [QFluentWidgets](https://qfluentwidgets.com/) - 流畅 GUI 组件库
- [Pyrogram](https://pyrogram.org/) - Telegram MTProto API 客户端
- SQLite3（WAL 模式） - 本地数据库

## 许可证

本项目仅供个人学习与研究使用。使用 Telegram 存储文件请遵守 Telegram 服务条款及相关法律法规。开发者不对因使用本工具产生的任何数据丢失或账号风险承担责任。

---

## 贡献

欢迎提交 Issue 或 Pull Request，共同改进这个项目。

---

**感谢使用 Telegram Cloud！如有问题或建议，请在 Issues 中提出。**


