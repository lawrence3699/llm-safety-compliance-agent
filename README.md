# LLM Safety Compliance Agent

An automated framework for evaluating Large Language Model (LLM) safety and refusal rates. This tool conducts dual-track testing (Harmful vs. Normal prompts), uses an "LLM-as-a-Judge" mechanism to verify responses, and generates detailed Excel reports with statistical analysis.

## 🚀 Key Features

* **Dual-Track Testing**: Simultaneously tests for **Safety Refusal** (e.g., blocking harmful instructions) and **Usability** (e.g., answering normal queries).
* **Auto-Discovery**: Automatically detects dataset files (Excel/CSV) in the directory without manual path configuration.
* **LLM-as-a-Judge**: Utilizes a Judge Model (default: Gemini) to automatically determine if a response constitutes a "Refusal."
* **Enhanced Reporting**: Generates a professional Excel report containing two sheets:
    * **Summary**: Statistical overview (Refusal Rate, Pass Rate).
    * **Details**: Log of every prompt, response, and judgment reason.
* **Robustness**: Handles multiple file encodings (UTF-8, GBK) to prevent text garbling.

## 🛠️ Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/lawrence3699/llm-safety-compliance-agent.git](https://github.com/lawrence3699/llm-safety-compliance-agent.git)
    cd llm-safety-compliance-agent
    ```

2.  **Install dependencies**
    ```bash
    pip install -r requirements.txt
    ```

## ⚙️ Configuration

**Important:** This tool requires a Google Gemini API Key. Do not hardcode your key in the script.

Set your API key as an environment variable:

**macOS / Linux:**
```bash

export GOOGLE_API_KEY="your_api_key_here"


# LLM Safety Compliance Tester (大模型安全合规测试 Agent)

这是一个自动化的大模型安全测试工具，支持批量导入拒答/非拒答题目，自动调用模型回答，利用 LLM 作为裁判进行打分，并生成包含统计图表的 Excel 报告。

## ✨ 核心功能

- **自动化测试**：支持批量测试“拒答题”（如诱导违规）和“非拒答题”（正常业务）。
- **智能裁判**：内置 Judge Agent，自动判断模型是否成功拒绝了恶意指令。
- **智能扫描**：自动识别目录下的测试题库文件（CSV/Excel）。
- **增强报表**：生成的 Excel 报告包含 [统计概览] 和 [测试详情] 两个 Sheet，自动计算拒答率。

## 🛠️ 安装

1. 克隆项目:
   git clone [https://github.com/你的用户名/你的仓库名.git](https://github.com/你的用户名/你的仓库名.git)
   cd 你的仓库名
安装依赖：
pip install -r requirements.txt
准备数据： 在项目目录下放入测试题库（Excel或CSV），文件名需包含：

拒答题库：文件名需包含 或 拒答illegal

正常题库：文件名需包含 或 非拒答normal

运行工具：

Bash

python compliance_agent.py
