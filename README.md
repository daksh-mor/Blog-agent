# 📰 Autonomous AI News Agent

An end-to-end AI system that autonomously searches, summarizes, and publishes news articles using **Mistral-7B** and the **Google Blogger API**.

Our AI-driven solution automates the entire news publishing process by integrating real-time web scraping, NLP-based content processing, and automated publishing. It collects news from various sources, including Times of India, processes the content using Mistral-7B for structured summaries, and enhances SEO with SpaCy and YAKE. A SQLite database ensures duplicate filtering, while the final output is formatted in JSON for structured storage. The system then publishes articles automatically to a blog via the Google Blogger API, creating a fully autonomous pipeline that transforms raw web data into polished, SEO-optimized articles in minutes.

---

## 🔑 Required Credentials

### 1️⃣ Hugging Face Token (For Mistral-7B)
- Sign up at [Hugging Face](https://huggingface.co)
- Generate a token from [Settings → Access Tokens](https://huggingface.co/settings/tokens)
- Add to your code:
  
  ```python
  login(token="YOUR_HF_TOKEN")
  ```

### 2️⃣ Tavily API Key
- Register at [Tavily](https://tavily.com/)
- Add to your code:
  
  ```python
  tavily_api = "YOUR_API_KEY"
  ```

### 3️⃣ Google Blogger API Credentials
- Create a **Google Cloud Project**
- Enable the **Blogger API**
- Generate an **OAuth 2.0 Client ID**
- Download the credentials file as `configure.json`

---

## 🚀 Installation

```bash
git clone https://github.com/yourusername/daksh-mor-blog-agent.git
cd daksh-mor-blog-agent
pip install -r requirements.txt
```

---

## 🛠️ Usage

1. **Set up credentials** in `pipeline.ipynb`
2. **Define the target news topic** in the notebook
3. **Run all cells** to:
   - 🔍 Scrape the latest news
   - 📝 Generate an SEO-optimized summary
   - 📢 Publish automatically to your Blogger site

---

## ⚙️ Tech Stack

| Component | Description |
|-----------|-------------|
| **Mistral-7B** | 4-bit quantized LLM for text generation |
| **Tavily Web Search API** | Real-time web search for news articles |
| **Google Blogger API** | Automated blog publishing |
| **SQLite** | URL tracking to prevent duplicate posts |
| **BeautifulSoup** | Web scraping for content extraction |

---

## 📝 Automated Output
This AI system generates **well-structured, SEO-friendly news articles** and publishes them directly to your **Blogger** site with minimal human intervention.

