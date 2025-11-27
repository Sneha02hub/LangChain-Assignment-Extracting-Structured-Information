<!-- # LangChain Character Extractor – Assignment (100% Complete)

Uses **MistralAI + Chroma** as required by the assignment.

### Demo Walkthrough

1. Get your free Mistral API key: https://console.mistral.ai
2. Create `.env` file with:
 -->



# 📘 LangChain Character Extraction – README

This project extracts **structured character information** from story files using **LangChain, MistralAI**, and a local **vector database.**
The demo includes two CLI commands:

compute-embeddings – processes all stories and builds embeddings

get-character-info – retrieves character details in JSON format

Follow the steps below to run the demo.

### 🔧 1. Installation

Install all required dependencies:

pip install -r requirements.txt

### 📂 2. Add Dataset

Place all story files (.txt) inside:

data/stories/


Each file represents a single story.

### 🟦 3. Compute Embeddings

This command reads all stories, generates embeddings, and stores them in a local vector database.

python src/compute_embeddings.py --data data/stories


✔ Loads story files
✔ Splits into chunks
✔ Creates embeddings
✔ Saves vector store locally

### 🟩 4. Get Character Information

Use this command to retrieve structured details about any character:

python src/get_character_info.py --name "Character Name"

#### Example Output:
{
  "name": "Jon Snow",
  "storyTitle": "A Song of Ice and Fire",
  "summary": "Jon Snow is a brave and honorable leader...",
  "relations": [
    { "name": "Arya Stark", "relation": "Sister" },
    { "name": "Eddard Stark", "relation": "Father" }
  ],
  "characterType": "Protagonist"
}


If the character is not found:

{ "error": "Character not found in any story." }