# 🚀 Linkedln Post Generator

This is an AI-powered LinkedIn Post Generator built with [LangChain](https://www.langchain.com/), [Streamlit](https://streamlit.io/), and [GROQ](https://groq.com/)'s blazing-fast LLaMA-3 LLM. It helps you generate high-quality, context-aware LinkedIn posts using few-shot learning from curated examples.

---

## 📸 Demo

![Screenshot from 2025-06-07 17-26-59](https://github.com/user-attachments/assets/ec5cbb0e-a4f9-4a74-b9f4-4667785dc2ec)

---

## 📦 Features

- 🎯 **Topic-Specific**: Choose from a range of curated post topics.
- 📝 **Length Control**: Generate short, medium, or long posts.
- 🗣️ **Bilingual**: Supports **English** and **Hinglish** (English script).
- 🤖 **Few-Shot Learning**: Enhances output quality with real-world examples.
- 🧠 **Tag & Metadata Extraction**: Uses LLMs to analyze and enrich post metadata.
- ⚙️ **Streamlit UI**: Simple and interactive web interface.

---

## 🗂️ Project Structure

```bash
📁 LinkedIn_Post_Generator/
├── main.py                # Streamlit frontend
├── post_generator.py      # Core logic to create LinkedIn post prompts
├── few_shot.py            # Loads and filters example posts for few-shot learning
├── preprocess.py          # Extracts metadata (tags, language, length) from raw posts
├── llm_helper.py          # LLM client initialization (LangChain + Groq)
├── data/
│   ├── raw_posts.json     # Raw input LinkedIn posts
│   └── processed_posts.json  # Preprocessed posts with enriched metadata
```

---

## 🛠️ Setup Instructions

1. **Clone the repo**

```bash
git clone https://github.com/Sarang9Gupta/Linkedln_Post_Generator.git
cd Linkedln_Post_Generator
```

2. **Create a virtual environment**

```bash
python -m venv venv
source venv/bin/activate  # or `venv\Scripts\activate` on Windows
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Set up `.env` file**

Create a `.env` file in the root directory with:

```
TOKEN=your_groq_api_key_here
```

> You can get your Groq API key from https://console.groq.com/

5. **Run the app**

```bash
streamlit run main.py
```

---

## 🧠 How It Works

1. The user selects a **topic**, **language**, and **post length**.
2. `post_generator.py` builds a prompt using few-shot examples from processed LinkedIn posts.
3. The LLaMA-3 model (via GROQ API) generates a tailored post.
4. Results are shown instantly in the Streamlit UI.

---

## 📌 Requirements

- Python 3.8+
- Streamlit
- LangChain
- dotenv
- pandas
- groq (via LangChain provider)

> Use `pip freeze > requirements.txt` to export your current environment.
