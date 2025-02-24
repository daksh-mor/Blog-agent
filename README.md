# 📰 Autonomous AI News Agent

An end-to-end AI-powered system that autonomously searches, summarizes, and publishes news articles using **Mistral-7B** and the **Google Blogger API**.

## 📊 Project Showcase

<div align="center">
  
  <!-- Demo Video (Replace with your actual video link) -->
  <p><b>🎬 Watch the AI News Agent in Action:</b></p>
  <p>[INSERT DEMO VIDEO HERE]</p>
  
  <!-- Sample Blog Post Image (Replace with your actual image) -->
  <p><b>📸 Example AI-Generated Blog Post:</b></p>
  <img width="1320" alt="image" src="https://github.com/user-attachments/assets/3e89227c-ed24-47d3-9edb-c0e74466d072" />

  
  <!-- Process Diagram -->
  <p><b>🔄 End-to-End Pipeline:</b></p>
  <img width="648" alt="image" src="https://github.com/user-attachments/assets/b1293dcd-94a7-40e8-89ae-1028ef139846" />
  
</div>

---

## 🚀 Overview

Our AI-driven solution automates the entire news publishing process by integrating **real-time web scraping, NLP-based content processing, and automated publishing**. It collects news from various sources, including **Times of India**, processes the content using **Mistral-7B** for structured summaries, and enhances SEO with **SpaCy and YAKE**. A **SQLite database** ensures duplicate filtering, while the final output is formatted in **JSON** for structured storage. The system then **publishes articles automatically** to a blog via the **Google Blogger API**, creating a **fully autonomous pipeline** that transforms raw web data into polished, SEO-optimized articles in minutes.

---

## 🔧 How It Works

### **Step 1: Web Scraping for News Collection** 🕵️‍♂️
- Fetches news articles from sources like **Times of India** using **Tavily Web Search API**.
- Uses **BeautifulSoup** for HTML parsing and data extraction.

---

### **Step 2: AI-Based Summarization & SEO Enhancement** 🤖
- **Mistral-7B (4-bit quantized)** generates structured summaries.
- **SpaCy & YAKE** optimize the content for SEO.
- Filters duplicate content using **SQLite**.

---

### **Step 3: JSON Formatting for Structured Storage** 🗄️
- The final output is stored in **JSON format**.
- Ensures compatibility with the Blogger API.

📌 *Example JSON Output:*
```json
{
  "title": "Latest Mumbai Crime: Bank Robbery in Bandra and Police Investigation",
  "summary": "A bank in Bandra was robbed early this morning. The police have launched an investigation...",
  "published_date": "2025-02-24"
}
```

---

### **Step 4: Automated Publishing to Blogger** ✍️
- Uses **Google Blogger API** to auto-publish posts.
- Formats posts with **rich text, images, and structured data**.

---

## 🔑 Required Credentials

| Credential  | Purpose |
|------------|---------|
| **Hugging Face Token** | Access Mistral-7B for AI-based summaries |
| **Tavily API Key** | Web search and scraping |
| **Google Credentials** | Blogger API authentication |

### **🔹 Setup Your Credentials**
1. **Hugging Face Token** (For Mistral-7B)
   - Create an account at [huggingface.co](https://huggingface.co)
   - Get a token from [Settings → Access Tokens](https://huggingface.co/settings/tokens)
   - Add to the code: `login(token="YOUR_HF_TOKEN")`

2. **Tavily API Key**
   - Sign up at [tavily.com](https://tavily.com/)
   - Add to the code: `tavily_api = "YOUR_API_KEY"`

3. **Google Blogger API Credentials**
   - Create a **Google Cloud Project**
   - Enable **Blogger API**
   - Create an **OAuth 2.0 Client ID**
   - Download credentials as `configure.json`

---

## 📥 Installation

```bash
git clone https://github.com/yourusername/daksh-mor-blog-agent.git
cd daksh-mor-blog-agent
pip install -r requirements.txt
```

---

## 🛠️ Usage

1. **Configure Credentials** in `pipeline.ipynb`
2. **Set Target Topic** in the notebook
3. **Run All Cells** to:
   - Scrape latest news
   - Generate SEO-optimized summary
   - Publish to Blogger automatically

---

## ⚙️ Tech Stack

| Component  | Technology Used |
|------------|----------------|
| **AI Model** | Mistral-7B (4-bit quantized) |
| **Web Scraping** | Tavily Web Search API, BeautifulSoup |
| **SEO Optimization** | SpaCy, YAKE |
| **Storage** | SQLite (for URL tracking) |
| **Publishing** | Google Blogger API |

---

## 🌟 Features
✅ Fully automated news generation pipeline  
✅ AI-powered summarization & SEO optimization  
✅ Supports multiple news sources  
✅ JSON-formatted structured storage  
✅ Auto-publishing with Google Blogger API  

---

## 🎯 Future Enhancements
🔹 Support for more news sources  
🔹 Multi-language news summarization  
🔹 Integration with other publishing platforms (e.g., WordPress, Medium)  

---

## 📌 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
