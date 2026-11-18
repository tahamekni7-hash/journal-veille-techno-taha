# Session 4 — Building Jarvis, a local AI assistant
**Date:** 18/11/2026

## What I did
- Chose Ollama so the assistant could run on my computer without a paid AI API.
- Set up the Qwen 3.5 4B model and connected a Python program to Ollama on my computer.
- Added instructions for Jarvis's helpful personality and to help it understand casual English and slang.
- Added tools for arithmetic and checking the time.
- Added a local library of notes so Jarvis can search text and Markdown files for useful information.
- Added chat history and saved preferences on my computer.
- Built a desktop chat window with a dark design, chat history, knowledge, and personalization buttons.

## What I learned
- A language model can be connected to an app through a local service.
- Adding documents to a knowledge library helps an assistant answer questions about those documents; it does not retrain the model.
- Chat history and saved preferences can give an assistant useful context between sessions.

## Difficulties
- I first tried a cloud API, but it required paid credits. I changed the project to use a local model instead.
- I had to connect the model, chat window, saved conversations, and local knowledge features so they worked together.

## Tools used
- Python
- Ollama
- Qwen 3.5 4B
- Tkinter for the desktop interface
