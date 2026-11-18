# Session 4 — Création de Jarvis, un assistant IA local
**Date :** 18/11/2026

## Ce que j'ai fait
- J'ai choisi Ollama pour faire fonctionner Jarvis sur mon ordinateur sans API payante.
- J'ai connecté un programme Python au modèle Qwen 3.5 4B avec Ollama.
- J'ai ajouté des consignes pour définir la personnalité de Jarvis et l'aider à comprendre l'anglais courant et l'argot.
- J'ai ajouté des outils pour faire des calculs et donner l'heure actuelle.
- J'ai créé une bibliothèque locale de notes. Jarvis peut rechercher dans des fichiers texte et Markdown pour trouver des informations utiles.
- J'ai ajouté l'historique des conversations et l'enregistrement des préférences sur l'ordinateur.
- J'ai créé une interface de discussion avec Tkinter, un thème sombre et des boutons pour les conversations, les connaissances et la personnalisation.

## Ce que j'ai appris
- Un modèle de langage peut être relié à une application par un service local.
- Ajouter des documents à une bibliothèque de connaissances aide l'assistant à répondre sur leur contenu, mais ne réentraîne pas le modèle.
- L'historique et les préférences peuvent fournir du contexte à l'assistant entre les conversations.

## Difficultés rencontrées
- L'API en ligne nécessitait des crédits payants. J'ai donc remplacé cette solution par un modèle local.
- J'ai dû relier le modèle, l'interface, l'historique et la bibliothèque de connaissances.

## Outils utilisés
- Python
- Ollama
- Qwen 3.5 4B
- Tkinter pour l'interface graphique
