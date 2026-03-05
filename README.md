# LLM Text Embeddings

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/TowCenter/llm-text-embeddings)

Use this repo to generate text embeddings, allowing for interactive mapping to understand similarity across text. 

Using portions of President Trump's 2026 State of the Union, **semantic-map.ipynb** generates numeric representations of text and plots them on a 2D chart. Users can also customize notebook to fit their own data's structure.

## Setup

Add OpenAI API key to **.env** file.

```
OPENAI_API_KEY=""
```

## Running the notebook

Open **semantic-map.ipynb**. For the demo, no changes should be needed.

**If you have your own data**, in CSV/JSON/TXT format, you can change the fields to fit parameters.

You'll also want to comment out this code block to run the data loading:

```
# --- Option A: Load from a CSV file ---
# df = pd.read_csv("data/your_file.csv")
# print(f"Loaded {len(df):,} rows from CSV")
```

Comment out or delete this code

```
# --- Option B: Load data from .txt files — one document per file ---
records = []
for fname in sorted(os.listdir(DATA_DIR)):
    if fname.endswith(".txt"):
        fpath = os.path.join(DATA_DIR, fname)
        with open(fpath, "r", encoding="utf-8") as f:
            content = f.read().strip()
        records.append({"filename": os.path.splitext(fname)[0], "text": content})


df = pd.DataFrame(records)
print(f"Loaded {len(df):,} documents from '{DATA_DIR}'")
df.head()
```