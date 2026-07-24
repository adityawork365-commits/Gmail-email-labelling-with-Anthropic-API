# 📧 AI-Powered Gmail Automated Email Labelling Agent

<!-- BADGES SECTION -->
<p align="center">
  <img src="https://img.shields.io/badge/n8n-Automation-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n Badge" />
  <img src="https://img.shields.io/badge/Anthropic%20Claude-AI%20Model-D97706?style=for-the-badge&logo=anthropic&logoColor=white" alt="Anthropic Badge" />
  <img src="https://img.shields.io/badge/Gmail-API%20Integration-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail Badge" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License Badge" />
</p>

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

## 🔄 Workflow Diagram

<img width="1863" height="893" alt="Screenshot 2026-07-24 232101" src="https://github.com/user-attachments/assets/438df0a1-2075-4971-88fe-850371f14043" />

## 🖼️ Output & Screenshots

<img width="315" height="272" alt="Screenshot 2026-07-24 232302" src="https://github.com/user-attachments/assets/87601311-3306-43f0-b25a-3f2a6c972760" />
