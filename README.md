


red-team, penetration-testing, cybersecurity, ai-agent, ollama, mitre-attck, 
ethical-hacking, security-tools, pentesting-framework, bug-bounty, cve-exploit, 
malware-analysis, zero-day-hunting, offensive-security, infosec


# 🚀 G33kBot - AI-Powered Red Team Orchestration Agent

<p align="center">
  <img src="https://img.shields.io/badge/Version-4.0-red.svg">
  <img src="https://img.shields.io/badge/License-MIT-blue.svg">
  <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg">
  <img src="https://img.shields.io/badge/OS-Linux%20%7C%20macOS-lightgrey.svg">
  <img src="https://img.shields.io/badge/AI-Ollama-important.svg">
  <img src="https://img.shields.io/badge/MITRE-ATT%26CK-orange.svg">
</p>

<p align="center">
  <b>"Automating the attack chain, one zero day at a time"</b>
</p>

---

## 📋 Overview

G33kBot is an advanced AI-powered red teaming orchestration agent that integrates multiple security tools, uncensored language models, and MITRE ATT&CK framework to automate and enhance penetration testing engagements. It acts as your AI copilot for offensive security operations.

### ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🧠 **AI-Powered** | Integrates with Ollama models (dolphin-mistral, phi3, codellama) for uncensored security analysis |
| 🔧 **Tool Calling** | Executes 50+ security tools with intelligent output parsing |
| 🎯 **MITRE ATT&CK** | Full attack chain visualization and tactic-based orchestration |
| 📚 **RAG Knowledge** | Retrieval-Augmented Generation from local exploit/malware repositories |
| 🕵️ **Zero Day Hunting** | CVE feed integration, fuzzing tools, malware analysis |
| 🚫 **Uncensored Mode** | True unfiltered responses for legitimate security research |
| 🎨 **Beautiful UI** | Colored terminal dashboard with real-time stats |
| 💾 **Session Management** | Persistent chat sessions with history logging |
| 🔄 **Auto-Motivation** | Security quotes to keep you engaged |
| 🐳 **Docker Support** | Containerized deployment option |

---

## 🚀 Quick Start

### Prerequisites

```bash
# Install Ollama
curl -fsSL https://ollama.com/install.sh | sh

# Pull required models
ollama pull dolphin-mistral:latest
ollama pull phi3:instruct
ollama pull codellama:latest
One-Line Install
bash
git clone https://github.com/jokerpen/G33kBot.git
cd G33kBot
chmod +x setup.sh
./setup.sh
Manual Install
bash
# Clone repository
git clone https://github.com/jokerpen/g33kbot-ai-redteam.git
cd g33kbot-ai-redteam

# Make executable
chmod +x g33kbot.sh

# Create directories
mkdir -p ~/rag-data/{exploits,malware,zero-day,cves,techniques,payloads}
mkdir -p ~/web-tools

# Run
./g33kbot.sh
🎮 Usage Examples
Basic Commands
bash
# Start G33kBot
./g33kbot.sh

# Inside G33kBot session:
/help                    # Show help menu
/scan 192.168.1.1       # Quick port scan
/cve CVE-2026-2789      # Get CVE details
/analyze malware.exe     # Analyze suspicious file
/unfiltered on          # Enable uncensored mode
/tactic privilege-escalation  # Set MITRE tactic
Attack Chain Example
bash
# Set your target
/target 10.10.10.50

# Follow MITRE attack chain
/tactic reconnaissance
> "Scan target and identify open ports"

/tactic initial-access
> "Find vulnerabilities in web application"

/tactic privilege-escalation
> "Escalate privileges on compromised host"

/tactic persistence
> "Establish persistence mechanism"

/tactic exfiltration
> "Exfiltrate sensitive data"
Tool Integration
bash
# Direct tool calling
/tool nmap -sV 10.10.10.50
/tool hydra -l admin -P wordlist.txt ssh://10.10.10.50
/tool sqlmap -u http://10.10.10.50/page.php?id=1

# Smart tool recommendations
/exploit                    # Launch metasploit
/wifi                       # Start wireless audit
/crack                      # Password cracking tools
/fuzz http://target.com     # Start fuzzing
🛠️ Integrated Tools
G33kBot integrates with 50+ security tools across categories:

Network Scanning
nmap, masscan, rustscan, naabu

Web Application
gobuster, ffuf, burpsuite, zap, sqlmap, nikto, wpscan

Password Attacks
hydra, john, hashcat, medusa, ncrack

Wireless
aircrack-ng, wifite, kismet, reaver

Exploitation
msfconsole, searchsploit, empire, covenant

Sniffing & Spoofing
wireshark, tshark, tcpdump, bettercap, responder

OSINT
theharvester, recon-ng, sherlock, whatweb

Reverse Engineering
ghidra, radare2, gdb, checksec

Malware Analysis
capa, floss, volatility, cuckoo

Zero Day Hunting
afl-fuzz, honggfuzz, syzkaller

📁 RAG Knowledge Base Setup
bash
# Create RAG structure
mkdir -p ~/rag-data/{exploits,malware,zero-day,cves,techniques,payloads}

# Add your knowledge base
cp exploit-code/* ~/rag-data/exploits/
cp malware-samples/* ~/rag-data/malware/
cp cve-reports/* ~/rag-data/cves/

# Update RAG index
/rag update
🐳 Docker Deployment
bash
# Build container
docker build -t g33kbot .

# Run with Docker
docker run -it --network host \
  -v ~/rag-data:/root/rag-data \
  -v ~/web-tools:/root/web-tools \
  -v /tmp/.X11-unix:/tmp/.X11-unix \
  g33kbot

# Or use docker-compose
docker-compose up -d
docker-compose exec g33kbot ./g33kbot.sh
⚙️ Configuration
Model Configuration (config/models.yaml)
yaml
models:
  primary: "dolphin-mistral:latest"
  fast: "phi3:instruct"
  coder: "codellama:latest"
  attack: "wizard-vicuna:latest"

settings:
  temperature: 0.7
  max_tokens: 4096
  context_window: 8192
Tool Configuration (config/tools.yaml)
yaml
tools:
  nmap:
    enabled: true
    timeout: 300
    args: "-T4 -F"
  metasploit:
    enabled: true
    workspace: "g33kbot"
    console_timeout: 3600
🔒 Legal & Ethical Use
G33kBot is designed for authorized security testing only. Users must:

Obtain explicit written permission before testing any system

Comply with all applicable laws and regulations

Use only on systems you own or have permission to test

Follow responsible disclosure practices

The maintainers assume no liability for misuse.

🤝 Contributing
We welcome contributions! See CONTRIBUTING.md for guidelines.

Development Setup
bash
# Fork repository
git clone https://github.com/jokerpen/g33kbot-ai-redteam.git
cd g33kbot-ai-redteam

# Create branch
git checkout -b feature/amazing-feature

# Make changes
# Test your changes
./g33kbot.sh --test

# Commit and push
git commit -m "Add amazing feature"
git push origin feature/amazing-feature

# Create Pull Request
Contribution Areas
🐛 Bug fixes

✨ New features

📚 Documentation

🔧 Tool integrations

🌐 Web UI improvements

🐳 Docker enhancements

📊 Roadmap
Version 1.1
Web-based dashboard

Multi-user collaboration

Real-time attack visualization

Automated report generation

Version 1.2
Machine learning for exploit prediction

Automated phishing campaigns

Cloud service integration (AWS/Azure/GCP)

Mobile device testing

Version 2.0
Custom AI model training

Autonomous attack orchestration

Real-time threat intelligence

Blockchain security testing

📈 Stats
https://img.shields.io/github/stars/jokerpen/G33kBot?style=social
https://img.shields.io/github/forks/jokerpen/G33kBot?style=social
https://img.shields.io/github/watchers/jokerpen/G33kBot?style=social
https://img.shields.io/github/issues/jokerpen/G33kBot
https://img.shields.io/github/issues-pr/jokerpen/G33kBot

📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙏 Acknowledgments
MITRE Corporation for ATT&CK framework

Ollama team for local AI models

All tool developers and contributors

The offensive security community

📞 Contact
GitHub: @jokerpen

Discord: z3r0h4ck

Email: geoffreygeek@protonmail.com

<p align="center"> <b>Star ⭐ this repo if you find it useful!</b><br> <i>Happy Hacking! 🖥️</i> </p> ```
CONTRIBUTING.md
markdown
# Contributing to G33kBot

First off, thank you for considering contributing to G33kBot! It's people like you that make G33kBot such a great tool.

## Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check the issue list as you might find out that you don't need to create one. When you are creating a bug report, please include as many details as possible:

* Use a clear and descriptive title
* Describe the exact steps to reproduce the problem
* Provide specific examples (commands, outputs, screenshots)
* Describe the behavior you observed vs what you expected
* Include your OS and environment details

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, please include:

* A clear and descriptive title
* Step-by-step description of the suggested enhancement
* Explain why this enhancement would be useful
* List any alternative solutions you've considered

### Tool Integration Requests

To request integration with a new security tool:

1. Check if the tool is already in our roadmap
2. Provide tool name and official repository
3. Describe common use cases
4. Include installation instructions
5. Provide example commands

### Pull Requests

1. Fork the repo and create your branch from `main`
2. If you've added code that should be tested, add tests
3. Ensure your code follows existing style conventions
4. Update documentation as needed
5. Issue that pull request!

## Development Setup

```bash
# Clone your fork
git clone https://github.com/jokerpen/g33kbot-ai-redteam.git
cd g33kbot-ai-redteam

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Make scripts executable
chmod +x g33kbot.sh scripts/*.sh

# Run tests
./tests/run_tests.sh
Style Guidelines
Bash Scripts
Use #!/bin/bash shebang

Use 4 spaces for indentation

Quote variables

Use [[ ]] for tests

Add comments for complex logic

Python Code
Follow PEP 8

Use type hints

Write docstrings

Keep functions focused

Commit Messages
Follow Conventional Commits:

text
feat: add new tool integration
fix: correct RAG indexing error
docs: update installation instructions
style: improve UI colors
refactor: optimize tool calling
test: add tool wrapper tests
Testing
Before submitting PR:

bash
# Run all tests
./tests/run_all.sh

# Test specific component
./tests/test_tools.sh
./tests/test_ai_engine.py

# Lint check
shellcheck g33kbot.sh scripts/*.sh
Documentation
Update documentation for any changed functionality:

README.md for general changes

docs/ for detailed documentation

Code comments for complex logic

Questions?
Feel free to open an issue with your question or contact the maintainers directly.

Thank you for contributing! 🚀

text

---

## CHANGELOG.md

```markdown
# Changelog

All notable changes to G33kBot will be documented in this file.

## [1.0.0] - 2026-03-08

### Added
- Complete rewrite with red team orchestration
- MITRE ATT&CK framework integration
- Tool calling for 50+ security tools
- RAG knowledge base support
- Zero day hunting capabilities
- Unfiltered mode for uncensored responses
- Beautiful colored UI dashboard
- Session management with history
- Auto-motivation quotes
- Docker deployment support
- Web UI (beta)

### Changed
- Removed aichat dependency (was malfunctioning)
- Direct Ollama API integration
- Enhanced error handling
- Improved performance

### Fixed
- Tool execution timeout handling
- RAG context retrieval
- Session persistence

## [3.0.0] - 2026-02-01

### Added
- Initial version with aichat integration
- Basic model switching
- Simple RAG support

### Known Issues
- aichat malfunctions with tool calling
- Limited tool integration
setup.sh
bash
#!/bin/bash

# G33kBot Installation Script

set -e

echo "🚀 Installing G33kBot v1.0"

# Check OS
if [[ "$OSTYPE" != "linux-gnu"* ]] && [[ "$OSTYPE" != "darwin"* ]]; then
    echo "❌ Unsupported OS. Linux or macOS required."
    exit 1
fi

# Create directories
echo "📁 Creating directories..."
mkdir -p ~/.g33kbot/{sessions,logs,temp,reports,tool-output,cve-feed,exploits}
mkdir -p ~/rag-data/{exploits,malware,zero-day,cves,techniques,payloads}
mkdir -p ~/web-tools

# Install dependencies
echo "📦 Installing dependencies..."

if [[ "$OSTYPE" == "linux-gnu"* ]]; then
    sudo apt-get update
    sudo apt-get install -y curl wget git jq bc net-tools
elif [[ "$OSTYPE" == "darwin"* ]]; then
    brew install curl wget git jq
fi

# Install Ollama
if ! command -v ollama &> /dev/null; then
    echo "🦙 Installing Ollama..."
    curl -fsSL https://ollama.com/install.sh | sh
fi

# Pull models
echo "🤖 Pulling AI models (this may take a while)..."
ollama pull dolphin-mistral:latest
ollama pull phi3:instruct
ollama pull codellama:latest
ollama pull wizard-vicuna:latest

# Install Python tools if Python is available
if command -v pip3 &> /dev/null; then
    echo "🐍 Installing Python tools..."
    pip3 install sherlock-project xsstrike capa floss
fi

# Install Go tools if Go is available
if command -v go &> /dev/null; then
    echo "🔧 Installing Go tools..."
    go install github.com/projectdiscovery/httpx/cmd/httpx@latest
    go install github.com/projectdiscovery/nuclei/v2/cmd/nuclei@latest
    go install github.com/ffuf/ffuf@latest
fi

# Make scripts executable
echo "🔧 Setting permissions..."
chmod +x g33kbot.sh scripts/*.sh 2>/dev/null || true

echo "✅ G33kBot installed successfully!"
echo ""
echo "Run with: ./g33kbot.sh"
echo ""
echo "For help: ./g33kbot.sh --help"
