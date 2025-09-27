# Eucossa OpenAI - Frontier Model APIs Tutorial

Welcome to Week 2 of the Frontier Model APIs course! This Jupyter notebook demonstrates how to connect and work with multiple AI model APIs including OpenAI, Anthropic (Claude), Google (Gemini), and optionally DeepSeek.

## 🌟 Getting Started

### Prerequisites

- Python 3.8 or higher
- Jupyter Lab or Jupyter Notebook
- Basic knowledge of Python programming

### 🛠️ Installation

1. **Clone or Fork this repository**
   ```bash
   git clone <your-repository-url>
   cd eucossa
   ```

   Or simply **fork** this repository on GitHub and star ⭐ it if you find it useful!

2. **Install required packages**
   ```bash
   pip install -r requirements.txt
   ```

   If `requirements.txt` doesn't exist, install packages manually:
   ```bash
   pip install jupyter openai anthropic google-generativeai python-dotenv ipython
   ```

3. **Launch Jupyter**
   ```bash
   jupyter lab
   ```
   or
   ```bash
   jupyter notebook
   ```

## 🔑 API Key Setup

### Step 1: Create API Keys

You'll need to create API keys for the services you want to use:

| Provider | Website | Notes |
|----------|---------|--------|
| **OpenAI** | https://openai.com/api/ | Required for GPT models |
| **Anthropic** | https://console.anthropic.com/ | Optional - for Claude models |
| **Google** | https://ai.google.dev/gemini-api | Optional - for Gemini models |
| **DeepSeek** | https://platform.deepseek.com/ | Optional - alternative model |

> **💡 Cost-Saving Tip:** If you want to avoid extra API costs, you can focus on just OpenAI for learning purposes, or substitute some providers with local models using Ollama.

### Step 2: Create Environment File

1. Create a file named `.env` in the project root directory
2. Add your API keys to this file:

```env
OPENAI_API_KEY=your_openai_api_key_here
ANTHROPIC_API_KEY=your_anthropic_api_key_here
GOOGLE_API_KEY=your_google_api_key_here
DEEPSEEK_API_KEY=your_deepseek_api_key_here
```

⚠️ **Important:** Never commit your `.env` file to version control. It should be included in `.gitignore`.

### Step 3: Restart Kernel

After adding your API keys:
1. In Jupyter, go to `Kernel` → `Restart Kernel`
2. Run all cells from the beginning

## 🤖 What You'll Learn

This notebook covers:

- **API Integration**: Connect to multiple AI model providers
- **Model Comparison**: See how different models respond to the same prompts
- **Streaming Responses**: Real-time response generation
- **Temperature Control**: Adjust creativity/randomness in responses
- **Conversation Management**: Build multi-turn conversations
- **Advanced Exercises**: Chatbot-to-chatbot conversations

## 📋 Featured Models

### OpenAI Models
- `gpt-4o-mini` - Fast and cost-effective
- `gpt-4.1-mini` - Enhanced mini version
- `gpt-4.1-nano` - Extremely fast and cheap
- `gpt-4.1` - Full GPT-4.1 model
- `o4-mini` - Reasoning model (if you have access)

### Anthropic Models
- `claude-sonnet-4-20250514` - Claude 4.0 Sonnet

### Google Models
- `gemini-2.0-flash` - Via Google's library
- `gemini-2.5-flash` - Via OpenAI-compatible endpoint

### DeepSeek Models
- `deepseek-chat` - General chat model
- `deepseek-reasoner` - Reasoning/thinking model

## 🚀 Quick Start Guide

1. **Run the setup cells** to import libraries and load API keys
2. **Test your connections** with the key verification cell
3. **Try the joke examples** to see how different models respond
4. **Experiment with the exercises** at the end of the notebook

## 🎯 Exercises to Try

1. **Word Count Challenge**: "How many words are there in your answer to this prompt"
2. **Creative Description**: "In 3 sentences, describe the color Blue to someone who's never been able to see"
3. **Logic Puzzle**: The bookshelf worm riddle (great for testing reasoning capabilities)

## 🐛 Troubleshooting

### Common Issues

**Google Gemini kernel crash:**
- Skip the Google library import cell and use the OpenAI-compatible endpoint instead

**Claude streaming display issues (Windows):**
- Replace `print(text, end="", flush=True)` with:
  ```python
  clean_text = text.replace("\n", " ").replace("\r", " ")
  print(clean_text, end="", flush=True)
  ```

**DeepSeek API errors:**
- The service may be over-subscribed; try again later
- Ensure you've topped up your account with at least $2

**Environment variables not loading:**
- Restart the Jupyter kernel after creating/updating `.env`
- Check that your `.env` file is in the correct directory
- Verify there are no extra spaces in your API keys

## 📁 Project Structure

```
eucossa/
├── eucossaOpenai.ipynb    # Main tutorial notebook
├── .env                   # Your API keys (create this)
├── README.md             # This file
└── requirements.txt      # Python dependencies
```

## 🤝 Contributing

Feel free to:
- ⭐ **Star** this repository if you find it helpful
- 🍴 **Fork** it to create your own version
- 🐛 Report issues or suggest improvements
- 📝 Share your own model experiments

## 📄 License

This project is open source. Please check the LICENSE file for details.

## 🙏 Acknowledgments

This tutorial is part of a comprehensive course on Frontier Model APIs. Special thanks to all students who have contributed exercises and improvements!

---

**Ready to explore the world of AI models? Open `eucossaOpenai.ipynb` and start your journey!** 🚀