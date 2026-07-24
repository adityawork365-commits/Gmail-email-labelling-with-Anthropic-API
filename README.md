# 📧 AI-Powered Gmail Automated Email Labelling Agent

An intelligent, end-to-end email categorization and workflow automation system built with **n8n**, **Anthropic Claude API**, and **Gmail API integration**.

---

## 📌 Executive Summary

Modern inbox management often consumes valuable hours due to manual sorting and triage. This project implements a fully autonomous **AI Agent Workflow** in n8n that monitors incoming Gmail messages, evaluates their content using **Anthropic's Claude LLM**, automatically generates appropriate category labels, and tags incoming messages in real-time.

---

## 📐 Workflow Architecture

The architecture relies on n8n's **LangChain Agent Framework**, combining persistent memory, tools, and LLM orchestration to make dynamic context-aware decisions:

```text
+------------------+      +----------+      +---------------------------+
|  Gmail Trigger   | ---> |   Wait   | ---> |   Gmail Labelling Agent   |
| (Incoming Email) |      +----------+      |    (Anthropic Claude)     |
+------------------+                        +-------------+-------------+
                                                          |
                 +-------------------+--------------------+-------------------+
                 |                   |                    |                   |
        +--------v-------+  +--------v-------+   +--------v-------+  +--------v-------+
        | Window Buffer  |  |  Gmail Tools   |   |  Gmail Tools   |  |  Gmail Tools   |
        |    Memory      |  | (Get Message)  |   | (Create Label) |  | (Add Label)    |
        +----------------+  +----------------+   +----------------+  +----------------+
