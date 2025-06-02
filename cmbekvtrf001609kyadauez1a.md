---
title: "☕ How I Built My First AI Agent"
datePublished: Mon Jun 02 2025 04:16:59 GMT+0000 (Coordinated Universal Time)
cuid: cmbekvtrf001609kyadauez1a
slug: how-i-built-my-first-ai-agent

---


**“Ek AI agent banate hain jo Hitesh Choudhary jaise baat kare!”** – This casual thought over evening chai turned into one of my most fulfilling coding experiments so far.

In this article, I’ll walk you through how I built my first AI agent – from ideation to writing code, from hitting errors to watching it finally work. If you're someone who loves building things and is curious about AI, this story is for you.

---

## 🎯 The Idea: Making Learning More Personal

I’ve always been a fan of Hitesh Choudhary – his teaching style, his energy, his humor, and how he simplifies complex topics. One day, I thought:

> “What if we could talk to an AI version of Hitesh sir? Like a coding mentor who’s always available?”

And boom – the seed was planted.

**My goal:**  
Build a chat-based AI assistant that talks like Hitesh sir, explains like him, and guides like a real mentor.

---

## 🛠️ Tech Stack I Used

To make this happen, I picked the following tools:

- **Python** – for quick prototyping
- **Streamlit** – to build a fast, clean chat UI
- **Gemini (Google Generative AI)** – as the brain behind the bot
- **Dotenv** – to keep API keys secure
- **Custom Prompt Engineering** – to shape the AI’s desi mentor personality

---

## 📜 The Persona Prompt: Breathing Life into the Agent

The magic ingredient was the `persona_prompt.py` file.

I crafted a detailed prompt in Hinglish that described:

- Hitesh sir’s tone (desi, fun, slightly sarcastic)
- His real-world explanation style
- His typical phrases (e.g., “Namaskar doston”, “Chai leke aao”, “Ab samjho…”)
- His motivational and teaching tone

This gave the AI its unique personality.

---

## 💬 Building the Chat UI (Like WhatsApp!)

I didn’t want it to feel robotic. So, I used Streamlit and added:

- **A modern chat UI** with custom CSS
- **User + AI chat bubbles** (styled like WhatsApp)
- A **typing animation** instead of boring “loading…”
- Color-coded messages (purple for user, orange for AI)
- And of course, some ☕🚀💻 emojis for flavor

---

## 🧠 Making the AI Smarter: Handling Repeated Questions

Sometimes users repeat questions with slight changes. To manage that:

- I added a **hashing mechanism** to detect repeated intent
- The AI then gives a different type of response:
  - Step-by-step explanation
  - Real-world analogy
  - Problem–solution format
  - Industry insights

This kept the experience fresh and helpful.

---

## 🐞 Bugs, Errors & “Kuch toh gadbad hai!”

The journey wasn’t smooth:

- API errors (`401 unauthorized`, `model not found`)
- Streamlit throwing `experimental_rerun` errors
- Blank chat messages
- Typing animations breaking randomly

But each bug taught me something new. And that’s the beauty of building.

---

## 🔐 Handling Secrets & Pushing to GitHub

Good practices I followed:

- Used `.env` to store secrets (like Gemini API key)
- Added `.venv` to `.gitignore` to keep the repo clean
- Added a `requirements.txt` for easy setup
- Wrote a clean `README.md` so others can understand and run it

---

## 🧪 Testing the Final Product

I asked the AI:

> “React kya hota hai?”

It responded in Hinglish, with real-world analogy and ended with:

> *“Ab samjha? Agar nahi, toh batao – ek aur example se samjhata hoon!”*

That’s when I knew… **It worked!**

---

## ❤️ What I Learned

- Prompt engineering is **more important than model tuning**
- Good UI/UX makes dev tools more engaging
- Small touches (like typing animations) leave a big impact
- Most importantly: **Execution > Perfection**

---

## 🚀 What’s Next?

I plan to:

- Add **voice support**
- Let users pick from **different mentor personas**
- Deploy it as a full website to help learners 24x7

---

## 🙌 Final Thoughts

This wasn’t just a side project. It felt like I built a small part of mentorship into software.

If you’ve ever wanted to build your own AI agent, here’s my advice:

> **Start small. Focus on the personality. Let AI do the rest.**  
> Aur haan… Chai leke baithna. Kaam mazedar hoga. ☕😉

---

### 💬 Want to Try the Hitesh AI Agent?

Check it out Live - [Click Here](https://hitesh-ai-agent.streamlit.app/)

> App can take time for initial chat as it is deployed using free hosting by streamkit

