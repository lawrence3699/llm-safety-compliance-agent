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