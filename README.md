# 💤 自动休眠电脑，保持规律作息

一个基于 Windows 任务计划程序的轻量化项目，通过**递进式自动休眠机制**，逐步“劝退”用户离开电脑，从而改善作息，拒绝熬夜。

---

## ✨ 项目功能

该项目通过导入任务计划实现以下操作：

- 🕤 **每日 22:30 自动休眠一次**（温和提醒）
- 🕥 **每日 22:45 再次自动休眠**（加强提醒）
- ⏱️ **每日 22:50 起，每分钟自动休眠一次，持续 6 小时**（高强度劝退）

配合 Windows 系统的休眠机制，让电脑在设定时间自动进入休眠状态，强制中断“无限刷屏”。

---

## 🧠 原理说明

该项目通过 [任务计划程序 (Task Scheduler)](https://learn.microsoft.com/en-us/windows/win32/taskschd/task-scheduler-start-page) 配合系统指令：

```bash
rundll32.exe powrprof.dll,SetSuspendState
