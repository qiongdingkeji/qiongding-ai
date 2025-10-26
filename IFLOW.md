# HexStrike AI - IFLOW 项目上下文文档

## 项目概述

**HexStrike AI v6.0** 是一个先进的网络安全自动化平台，集成了人工智能驱动的智能与 150+ 安全工具，用于渗透测试、漏洞评估和红队操作。项目基于 FastMCP 框架构建，支持无缝的 AI 代理通信。

### 项目类型
- **类型**: 网络安全自动化框架
- **主要技术**: Python, Flask, FastMCP
- **架构**: 双脚本系统 + RESTful API

## 核心组件

### 主要文件
- `hexstrike_server.py` - 主应用服务器，包含 REST API 和工具编排
- `hexstrike_mcp.py` - MCP 客户端，用于 AI 代理通信
- `hexstrike-ai-mcp.json` - MCP 服务器配置
- `requirements.txt` - Python 依赖包列表
- `README.md` - 项目文档

## 构建和运行

### 前提条件
- Python 3.8+
- Kali Linux 2024.1+ (推荐) 或 Ubuntu/Debian
- Chrome/Chromium 浏览器用于 Web 自动化

### 安装步骤
```bash
# 创建虚拟环境
python3 -m venv hexstrike_env
source hexstrike_env/bin/activate

# 安装依赖
python3 -m pip install -r requirements.txt

# 启动服务器
python3 hexstrike_server.py

# 在另一个终端启动 MCP 客户端
python3 hexstrike_mcp.py
```

### 配置
编辑 `hexstrike-ai-mcp.json` 来配置 MCP 服务器设置：
```json
{
  "mcpServers": {
    "hexstrike-ai": {
      "command": "python3",
      "args": [
        "/hexstrike-ai/hexstrike_mcp.py",
        "--server",
        "http://localhost:8888"
      ],
      "description": "HexStrike AI v6.0 - Advanced Cybersecurity Automation Platform"
    }
  }
}
```

## 项目架构

### 核心功能模块
1. **AI 驱动自动化**
   - 智能工具选择引擎
   - 自动化工作流管道
   - 上下文感知工具参数配置

2. **150+ 集成安全工具**
   - 网络侦察 (nmap, masscan, rustscan, autorecon)
   - Web 应用安全 (nuclei, sqlmap, wpscan, dalfox, ffuf)
   - 二进制分析 (ghidra, radare2, pwntools, angr)
   - 云安全 (prowler, scout-suite, trivy)
   - OSINT 和情报 (sherlock, recon-ng, maltego)

3. **现代架构特性**
   - 双脚本系统设计
   - FastMCP 集成
   - RESTful API
   - 实时监控和报告

## 开发约定

### 代码风格
- 使用 Python 3.8+ 语法
- 遵循 PEP 8 代码风格指南
- 使用类型注解
- 统一的错误处理和日志记录

### 安全特性
- 防御性安全设计，专注于合法的安全测试
- 敏感操作的受控自动化
- 全面的审计日志记录
- 开箱即用的安全配置

## 依赖管理

### 核心依赖
- `flask>=2.3.0,<4.0.0` - Web 框架
- `requests>=2.31.0,<3.0.0` - HTTP 库
- `fastmcp>=0.2.0,<1.0.0` - MCP 框架
- `selenium>=4.15.0,<5.0.0` - 浏览器自动化
- `psutil>=5.9.0,<6.0.0` - 系统工具

### 外部工具依赖
项目集成了 150+ 外部安全工具，需要单独安装：
- Kali Linux 2024.1+ 包含大部分工具
- Ubuntu/Debian 用户应从官方仓库安装
- 部分工具需要从源码编译

## 使用示例

### 基本安全评估
```bash
# 启动服务器
python3 hexstrike_server.py

# 服务器将在 http://localhost:8888 可用
# 使用 MCP 客户端与 AI 代理交互
```

### AI 框架集成
HexStrike AI 通过 MCP 协议支持与各种 AI 框架集成：
- Claude Desktop
- Cursor AI
- 其他 MCP 兼容的 AI 工具

## 重要提醒

### 安全声明
此项目仅用于授权的安全测试、教育目的和合法的网络安全研究。用户在使用此工具对任何网络或系统进行测试前，需确保获得适当的授权。

### 文件说明
- `.hexstrike_mcp.py.swp` - Vim 交换文件（可安全删除）
- 项目使用统一的红黑色主题配色方案
- 支持实时进度跟踪和彩色输出显示

---

**最后更新**: 2025-10-26  
**版本**: HexStrike AI v6.0  
**用途**: 为 iFlow CLI 提供项目上下文信息