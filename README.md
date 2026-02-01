# Google Web Search (Gemini Grounding)

Real-time web search using Gemini API's `google_search` grounding tool.

## Features

- ✅ Real-time web search with grounded citations
- ✅ Natural language answers (no JSON parsing needed)
- ✅ Configurable Gemini model selection
- ✅ Simple Python API

## Quick Start

### 1. Set API Key

```bash
export GEMINI_API_KEY=your_key_here
```

Get your API key at [Google AI Studio](https://aistudio.google.com/app/apikey)

### 2. Use in OpenClaw

```python
from skills.google-web-search.scripts.example import get_grounded_response

# Ask a question
answer = get_grounded_response("What is the weather in Seoul today?")
print(answer)
# Output: Natural language answer with citations
```

### 3. Optional: Change Model

```bash
export GEMINI_MODEL=gemini-3-pro-preview
```

Supported models:
- `gemini-2.5-flash-lite` (default) - Fast & cheap
- `gemini-3-flash-preview` - Latest flash
- `gemini-3-pro-preview` - More capable

## Use Cases

- 📰 Real-time news and events
- 💹 Current prices (stocks, crypto, etc.)
- 🌤️ Weather forecasts
- 📊 Latest statistics and data
- 🔍 Any information requiring recent sources

## vs. google-search Skill

| Feature | google-web-search (this) | google-search |
|---------|--------------------------|---------------|
| API | Gemini + Google Search | Google Custom Search |
| Setup | 1 API key | 2 (API key + CSE ID) |
| Output | Natural language | JSON |
| Use case | Q&A, facts | Search results |

## Requirements

- Python ≥ 3.11
- `google-genai` ≥ 1.50.0
- `pydantic-settings` ≥ 2.0.0

## License

Same as OpenClaw project
