# Session 4 — Création de Jarvis, un assistant IA local

Jarvis runs its language model on this computer through Ollama. It does not use the OpenAI API, require an API key, or send chat messages to a cloud model.

## How I built Jarvis

1. I chose Ollama so Jarvis could run on my computer without a paid API key.
2. I installed the `qwen3.5:4b` language model and connected the Python program to Ollama running locally.
3. I gave Jarvis instructions for its name, helpful personality, and how to understand casual English and slang.
4. I added simple tools so it can calculate arithmetic and check the current time.
5. I added a local knowledge library. Jarvis can search text and Markdown notes I add and use relevant passages in its answers.
6. I made it save chat history and personal reply preferences on this computer, so they are available when I reopen the app.
7. I built a desktop chat window with buttons for new chats, chat history, adding knowledge, and personalization, then styled it with a dark theme inspired by Vesper.
8. I added a launcher so Jarvis can be opened from the project folder.

The result is a simple desktop assistant that uses a local model, local notes, and locally saved chats.

## First-time setup

1. Install Python 3.13 and [Ollama for Windows](https://ollama.com/download/windows).
2. Double-click **Open Jarvis.bat**.
3. Click **Connect locally**. Jarvis downloads `qwen3.5:4b` the first time (about 3.3–4.0 GB) and then runs it locally.

The first model download needs internet access. After it is downloaded, Jarvis sends chat requests only to Ollama at `127.0.0.1` on your computer. The larger model uses more memory and processor power, so replies may be slower on this computer.

## Features

- Local chat history saved on this computer. Jarvis can reopen past chats and recall relevant details across chats.
- Arithmetic and timezone-aware time tools.
- Add local `.txt` and `.md` notes with **Add knowledge**. Jarvis searches relevant passages and uses them as references.
- Set saved reply preferences with **Personalize**.
- Jarvis addresses Taha by name when appropriate, interprets common texting shorthand and slang, and replies in polished standard English.
- `/reset` clears the conversation and `/quit` exits in the command-line version.

Knowledge notes and personalization settings stay in the Jarvis project folder. Jarvis reads only the notes you add through the app; it does not scan your computer. It does not control your computer or generate images. Knowledge files are treated as reference text, not instructions to follow.

Chat transcripts are stored locally in `Jarvis Memory/chat_history.json`. Use **Chat history** to reopen a saved conversation and **New chat** to start another without deleting earlier chats. Saved chats are not sent to a cloud service; relevant excerpts may be included in later requests to your local Ollama model.

The Kaggle Question-Answer Dataset is included under `Jarvis Knowledge/Kaggle Question Answer Dataset`. Its source and CC BY-SA 3.0 attribution are recorded in `SOURCE.md`; the material is older and should not be used for current facts.

An additional local guide for common informal English and internet slang is in `Jarvis Knowledge/Informal English and Slang Guide.md`. The model already has broad English-language ability; the guide provides examples for interpreting abbreviated messages and is not a model retraining dataset.
