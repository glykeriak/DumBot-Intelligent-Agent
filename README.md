# DumBot-Intelligent-Agent

## Overview
This project implements **DumBot**, an intelligent coding assistant built with **OpenAI, LangChain, and Gradio**.  
The assistant can:
- Engage in **general conversations**.  
- **Generate code** from natural language descriptions.  
- **Debug code** by identifying and fixing errors.  
- **Review code** and provide suggestions for improvement.  

It provides an interactive web UI with **Gradio** and can be run in Google Colab or locally.

Built with:
- [OpenAI API](https://platform.openai.com/) → LLM backend  
- [LangChain](https://www.langchain.com/) → prompt templates & agent orchestration  
- [Gradio](https://gradio.app/) → web-based user interface  
- [ipywidgets](https://ipywidgets.readthedocs.io/) → interactive widgets (Colab)  
- [dotenv](https://pypi.org/project/python-dotenv/) → secure API key handling  

---

## System Architecture

### Agents
- **CodeHelper** → generates code from a description.  
- **CodeDebugger** → detects and fixes errors in code.  
- **CodeReviewer** → suggests improvements for style, readability, and best practices.  
- **CodingAssistant** → central coordinator, combines helper, debugger, and reviewer.  

### Modes of Operation
- **General Conversation** → free-form chat with LLM.  
- **Code Writing** → create functions or scripts from descriptions.  
- **Code Debugging** → fix provided code snippets.  
- **Code Review** → evaluate and suggest improvements.  

### User Interface
- **Gradio-based UI** with:  
  - Mode selection (radio buttons).  
  - Chatbox for conversation & results.  
  - Textbox for user input.  
  - Send button to interact with DumBot.  


---

## Deployment
1. Install Python 3.x.  
2. Install dependencies:  
   ```bash
   pip install openai langchain langchain-openai langchain-community ipywidgets gradio python-dotenv
3. Store your OpenAI API key inside .env: 
   ```bash
   OPENAI_API_KEY=your_api_key_here
4. Run in Google Colab or locally:
    ```bash
    python dumbo_ui.py
5. Open the provided Gradio link in your browser.

---

## Results

- General Conversation: DumBot responds to open-ended questions.
- Code Writing: Generates working code based on natural language descriptions.
- Debugging: Identifies and fixes bugs in code.
- Code Review: Provides suggestions to improve style, readability, and efficiency.
