# HexStrike AI - Advanced Cybersecurity Automation Platform

**HexStrike AI v6.0** - AI-Powered Penetration Testing & Red Team Automation Framework

🚀 **Bug Bounty | CTF | Red Team | Security Research**

## Overview

HexStrike AI is a comprehensive cybersecurity automation platform that integrates AI-powered intelligence with 150+ security tools for penetration testing, vulnerability assessment, and red team operations. Built with FastMCP framework for seamless AI agent communication.

## Features

### 🤖 AI-Powered Automation
- **Intelligent Tool Selection**: AI-driven decision engine for optimal tool selection
- **Automated Workflows**: End-to-end security assessment pipelines
- **Smart Parameter Optimization**: Context-aware tool parameter configuration

### 🔧 150+ Integrated Security Tools
- **Network Reconnaissance**: nmap, masscan, rustscan, autorecon
- **Web Application Security**: nuclei, sqlmap, wpscan, dalfox, ffuf
- **Binary Analysis**: ghidra, radare2, pwntools, angr
- **Cloud Security**: prowler, scout-suite, trivy
- **OSINT & Intelligence**: sherlock, recon-ng, maltego

### 🌐 Modern Architecture
- **Dual-Script System**: `hexstrike_server.py` + `hexstrike_mcp.py`
- **FastMCP Integration**: Seamless AI agent communication
- **RESTful API**: Flask-based web interface
- **Real-time Monitoring**: Live progress tracking and reporting

## Quick Start

### Prerequisites
- Python 3.8+
- Kali Linux 2024.1+ (recommended) or Ubuntu/Debian
- Chrome/Chromium browser for web automation

### Installation

```bash
# Create virtual environment
python3 -m venv hexstrike_env
source hexstrike_env/bin/activate

# Install dependencies
python3 -m pip install -r requirements.txt

# Start the server
python3 hexstrike_server.py

# In another terminal, start the MCP client
python3 hexstrike_mcp.py
```

### Configuration

Edit `hexstrike-ai-mcp.json` to configure your MCP server settings:

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

## Architecture

### Core Components

1. **HexStrike Server** (`hexstrike_server.py`)
   - Main application server with REST API
   - Tool orchestration and workflow management
   - Real-time monitoring and reporting

2. **MCP Client** (`hexstrike_mcp.py`)
   - AI agent communication interface
   - Tool execution and result processing
   - Integration with external AI frameworks

### Supported Tool Categories

- 🔍 **Network Reconnaissance**: 25+ tools
- 🌐 **Web Application Security**: 40+ tools  
- 🔐 **Authentication & Password**: 12+ tools
- 🔬 **Binary Analysis & RE**: 25+ tools
- ☁️ **Cloud & Container Security**: 20+ tools
- 🏆 **CTF & Forensics**: 20+ tools
- 🕵️ **OSINT & Intelligence**: 20+ tools

## Usage Examples

### Basic Security Assessment

```bash
# Start the server
python3 hexstrike_server.py

# The server will be available at http://localhost:8888
# Use the MCP client to interact with AI agents
```

### Integration with AI Frameworks

HexStrike AI supports integration with various AI frameworks through the MCP protocol:

- Claude Desktop
- Cursor AI
- Other MCP-compatible AI tools

## Security Features

- **Defensive Security Focus**: Designed for legitimate security testing
- **Controlled Automation**: Manual approval for sensitive operations
- **Audit Logging**: Comprehensive activity tracking
- **Safe Defaults**: Secure configuration out-of-the-box

## Contributing

We welcome contributions! Please see our contributing guidelines for details.

## License

This project is licensed for educational and authorized security testing purposes only.

## Disclaimer

HexStrike AI is designed for authorized security testing, educational purposes, and legitimate cybersecurity research. Users are responsible for ensuring they have proper authorization before using this tool on any network or system.

---

**HexStrike AI v6.0** - Redefining Cybersecurity Automation with AI Intelligence