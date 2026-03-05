# LLM Text Embeddings

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/TowCenter/llm-text-embeddings)

Use this repo to generate text embeddings, allowing for interactive mapping to understand similarity across text. 

Using the NICAR 2026 schedule, **semantic-map.ipynb** generates numeric representations of text and plots them on a 2D chart. Users can also customize notebook to fit their own data's structure.

## Setup

Add OpenAI API key to **.env** file.

```
OPENAI_API_KEY=""
```

## Running the notebook

Open **semantic-map.ipynb**. For the demo, no changes should be needed.

**If you have your own data** in CSV format, update the configuration cell at the top of the notebook with your file path and column names. The notebook loads a CSV by default (Option A). If your data is a folder of `.txt` files instead, comment out Option A and uncomment Option B in the data loading cell.
