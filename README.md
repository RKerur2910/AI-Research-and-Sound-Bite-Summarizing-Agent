# 🧠 AI Research and Sound Bite Summarization Agent  

**Tech Stack:** n8n • Perplexity API • OpenAI Chat Models • Text-to-Speech (TTS)  

---

## 📘 Overview  

This project is a **no-code AI workflow built in n8n** that automates research and delivers **topic-based executive summaries as audio files** directly to a user’s inbox.
It combines **AI-powered research, summarization, and voice generation** in one streamlined automation—no manual coding required.

The agent takes a user-submitted topic, performs **AI-assisted research via the Perplexity API**, generates a structured summary using **OpenAI chat models**, and converts that summary into speech using OpenAI TTS all within a single n8n workflow.

---

## ⚙️ Key Features  

- 🧩 **Fully automated pipeline:** From topic input → research → summary → speech output.  
- 🧠 **AI summarization:** Uses OpenAI chat models to create concise and coherent summaries.  
- 🔊 **Audio delivery:** Converts summaries into sound bites and sends them to the user’s email inbox.  
- 🚀 **Error handling and optimization:** Debugged node mapping, implemented chunking logic to overcome input length limits, and ensured stable end-to-end execution.  
- 🎯 **Scalable design:** Optimized for single-user, single-topic execution for reliability and focused performance.  

---

## 🧰 Workflow Architecture  

User Form  
   ↓  
Perplexity API (Research Node)  
   ↓  
OpenAI Chat Node (Summarization)  
   ↓  
OpenAI TTS Node (Audio Generation)  
   ↓  
Email Node (Output Delivery)

---

### Visual Workflow  
You can visualize the process with screenshots (insert yours here 👇):   

#### 1️⃣ Form Input  
This is the user-facing form where a topic and time period are entered.  
![Form Input](assets/form_input.jpg)

#### 2️⃣ Automated Email Output  
The workflow automatically sends the generated audio summary to the user’s email inbox.  
![Email Output](assets/email_output.jpg)  

#### 3️⃣ n8n Workflow Overview  
The full automation pipeline — connecting Perplexity API, OpenAI Chat Models, TTS, and Gmail nodes.  
![Workflow Overview](assets/workflow_overview.jpg)  

---

## 📝 Process
- User submits a topic and time window to focus the research
- Agent orchestrates research → summarization → audio generation
- Includes an evaluation step for violations; OpenAI chat models generate reliable, clean insights
- Final audio file is emailed to the user
  
---

## ⚡ Challenges & Fixes
- Blank audio output: Re-ran the workflow node-by-node; root cause was incorrect TTS node mapping → fixed mapping, added blank-summary checks, chunking, and stronger file handling for resilience
- Length constraints: TTS accepts ~4,096 characters → streamlined the summarization prompt to keep outputs within limits, improving consistency and reliability

---

## 🔍 Use Cases
- Automated daily research updates
- Turning news/whitepapers into short audio briefs
- Research assistant for creators, journalists, analysts

---

## ▶️ Next Steps
- Deliver summaries as a mini-podcast / ≤60-second clip
- Multi-topic batching + daily digest emails
- Export transcripts alongside audio
  
**Riya Kalyan Kerur**  
Master’s Student, Computer Engineering — California State University, Sacramento  
📧 [riya.kerur2910@gmail.com](mailto:riya.kerur2910@gmail.com)  
🌐 [LinkedIn](https://www.linkedin.com/in/riya-kerur/)  

---
