🌐 [Website](https://nexora-tools.github.io/Tower-of-Mystery/)

# 🏰 Tower OF Mystery

### Enter the tower. Answer the questions. Reach the top.

Tower Mystery is an interactive quiz game where players climb a mysterious tower by answering questions across different game modes.

Play solo or create a room and challenge friends in multiplayer. The game combines different challenges, scoring, health, timers, multiplayer gameplay and AI-powered questions to create a fresh experience every time.

---

## ✨ Features

- 🧠 AI-powered question generation
- 🎮 Solo Mode
- 🏰 Multiplayer Mode
- 🔗 Unique room codes
- 😂 Funny Mode
- 😡 Angry Mode
- 🧠 IQ Mode
- 🎂 Age Mode
- ❤️ Love Mode
- 🧩 Puzzle Mode
- 🔥 Hardcore Mode
- 👶 Baby Mode
- 💡 Hints
- 🏆 Score system
- ❤️ Health system
- ⏱️ Optional question timer
- 🔄 Fresh questions throughout gameplay
- ⚡ Questions prepared in advance for faster gameplay
- 📱 Responsive design
- 🌐 Browser-based gameplay
- 🔐 Secure AI API handling
- 🔁 Multiple AI providers with fallback support

---

## 🧩 How It Works

Players can choose Solo Mode or create a multiplayer room.

Solo gameplay starts by selecting a game mode and the number of questions. Multiplayer allows players to create or join a room using a unique room code.

The game then presents questions with four answer options. Players answer questions to progress through the tower while managing their score and health.

AI-generated questions are prepared ahead of time so players do not have to wait for a new question after every round.

---

## 🤖 AI Question Generation

Tower Mystery uses a Cloudflare Worker as a secure connection between the game and AI providers.

The Worker can use providers such as Gemini, OpenRouter, Groq and Mistral to generate new questions.

Questions are generated in batches and prepared in the background while the player is playing. Ready questions are stored in a queue so the next question can appear immediately instead of waiting for the AI request to finish.

Generated questions are also validated before being shown to players to ensure they contain four different options and a valid correct answer.

If an AI provider fails, another configured provider can be attempted. The existing local question system can also act as a fallback so gameplay can continue.

---

## 🏰 Multiplayer

Each multiplayer game uses a unique room code.

The host can select the game mode, number of questions and optional timer before starting the game.

Players join the same room and receive the shared game state through Firebase Realtime Database.

The multiplayer system keeps track of players, rounds, questions and answers while the game is running.

---

## 🔗 Room System

Every created room receives a unique code that other players can use to join.

The general flow is:

Create Room → Share Code → Players Join → Choose Settings → Start Game → Play

---

## 🔐 API Security

AI API keys are kept on the Cloudflare Worker instead of being placed directly inside the public game.

The frontend communicates with the Worker, and the Worker communicates with the configured AI providers.

This prevents the provider API keys from being exposed directly in the game's frontend source code.

---

## 🛠️ Technology

HTML  
CSS  
JavaScript  
Firebase Realtime Database  
Cloudflare Workers  
Gemini  
OpenRouter  
Groq  
Mistral  
GitHub Pages

---

## 🎯 Vision

> **Turn a simple quiz into an adventure.**

The idea behind Tower Mystery is to make answering questions feel like progressing through a mysterious tower rather than simply completing a normal quiz.

The goal is to combine mystery, competition, AI-generated questions and multiplayer gameplay into one interactive experience.

---

## 🚀 Project Status

**Active project**

The project is continuously being improved with new game modes, AI capabilities, multiplayer features, performance improvements and new gameplay ideas.

---

## 📌 Creator

**Nexora**

Building websites, digital tools, games and creative web experiences.

---

### © 2026 Nexora
