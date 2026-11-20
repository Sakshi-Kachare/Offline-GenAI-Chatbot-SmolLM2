\## 🤖 Offline GenAI Chatbot Using SmolLM2-360M-Instruct



\## 📌 Project Overview

This project implements a lightweight, \*\*100% Offline Generative AI Chatbot\*\* using Hugging Face's \*\*`HuggingFaceTB/SmolLM2-360M-Instruct`\*\* Small Language Model (SLM) and PyTorch\[cite: 4]. Once downloaded and cached locally, the chatbot runs completely offline on a standard \*\*CPU\*\* without requiring an internet connection or external API keys\[cite: 4]. It supports multi-turn conversation history, contextual follow-up answers, and interactive terminal commands.



\## 🎯 Project Objectives

\- Download and save the pretrained `SmolLM2-360M-Instruct` model and tokenizer locally using `transformers`.

\- Load the model in offline mode (`local\_files\_only=True`) optimized for CPU execution.

\- Design a custom `SYSTEM\_PROMPT` to act as a helpful AI teaching assistant.

\- Implement multi-turn conversational memory (`MAX\_HISTORY\_MESSAGES = 6`) for context-aware replies.

\- Build an interactive command-line chat loop with `/reset` and `/exit` commands.



\## 🛠️ Technologies \& Libraries Used

\- Python

\- PyTorch (`torch` - CPU inference)

\- Hugging Face Transformers (`AutoTokenizer`, `AutoModelForCausalLM`)

\- Pathlib

\- Jupyter Notebook



\## 🧠 Model \& Configuration Details

\- \*\*Model ID:\*\* `HuggingFaceTB/SmolLM2-360M-Instruct` (\~724 MB in `safetensors` format)

\- \*\*Hardware Target:\*\* CPU (`torch.set\_num\_threads(4)` with `torch.inference\_mode())

\- \*\*Generation Parameters:\*\*

&#x20; - `max\_new\_tokens = 120

&#x20; - `temperature = 0.7

&#x20; - `top\_p = 0.9

&#x20; - `repetition\_penalty = 1.1



\## 💬 Key Features \& Sample Interactions

1\. \*\*Offline Local Execution:\*\* Loads weights directly from the local `smollm2\_model/` directory (`local\_files\_only=True`) without internet access.

2\. \*\*Context-Aware Multi-Turn Memory:\*\* Retains previous user-assistant turns so follow-up questions like \*"Give me a real-life example of it."\* accurately refer back to earlier topics (e.g., Machine Learning).

3\. \*\*Interactive CLI Chat (`start\_chat()`):\*\*

&#x20;  - Ask any educational or technical question (e.g., Generative AI, Machine Learning, SQL).

&#x20;  - Type `/reset` to clear conversation history.

&#x20;  - Type `/exit` to terminate the chat session.



\## ⚙️ How to Run This Project

1\. Install Python and Jupyter Notebook.

2\. Install PyTorch (CPU) and Hugging Face Transformers:

&#x20;  

&#x20;  pip install torch --index-url \[https://download.pytorch.org/whl/cpu](https://download.pytorch.org/whl/cpu)

&#x20;  pip install --upgrade transformers

&#x20;  

3\. Open `Offline\_GenAI\_Chatbot.ipynb` in Jupyter Notebook.

4\. Run the model download cell once (with internet) to save `smollm2\_model/` locally.

5\. Run the remaining cells to chat completely offline on CPU.



\## 📁 Project Structure



Offline-GenAI-Chatbot-SmolLM2/

│

├── Offline\_GenAI\_Chatbot.ipynb

└── README.md





Email:sakshikachare444@gmail.com



GitHub: https://github.com/Sakshi-Kachare





⭐ This project demonstrates practical Generative AI deployment using Small Language Models (SLMs), local model serialization, prompt formatting with chat templates, and CPU-based offline inference.



