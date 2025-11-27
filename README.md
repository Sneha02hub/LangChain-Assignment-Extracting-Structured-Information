<!-- # LangChain Character Extractor – Assignment (100% Complete)

Uses **MistralAI + Chroma** as required by the assignment.

### Demo Walkthrough

1. Get your free Mistral API key: https://console.mistral.ai
2. Create `.env` file with:
 -->



# LangChain Character Extraction – README

This project is a simple and efficient Character Information Extraction System built using LangChain, MistralAI, and ChromaDB. It takes story files, converts them into embeddings, stores them in a local vector database, and allows you to query any character through a command-line interface. The system works in two phases: first, it reads all .txt stories, splits them into chunks, generates embeddings using MistralAI, and saves everything locally in Chroma. Then, when you search for a character, the system performs a similarity search, retrieves relevant text, and sends it to the Mistral LLM to produce structured JSON output containing summaries, relationships, and character type details.

The workflow is fully automated and easy to run, making it ideal for story analysis, knowledge extraction, or any semantic retrieval task. LangChain handles the processing pipeline, MistralAI provides embeddings and language understanding, and ChromaDB ensures fast retrieval. The CLI tools allow you to compute embeddings once and reuse the vector database anytime you need character information. If the character doesn’t exist in the dataset, the system responds with a clean error message.
