# AI Receptionist — Live Demo (Phase 0)

Browser-based voice demo: **Deepgram** (speech-to-text + text-to-speech) + **Groq** (jawab sochna, free tier).
Koi phone line nahi chahiye, koi server nahi chahiye — sirf ek static page.
(Gemini/Google AI Studio Pakistan mein available nahi, is liye Groq use ho raha hai — OpenAI-compatible API.)

## Chalane ka tareeqa

1. Is repo pe GitHub Pages on karo: **Settings → Pages → Deploy from a branch → `main` → Save**
2. `https://<tumhara-username>.github.io/ai-receptionist-demo/` kholo (phone pe bhi chalega — HTTPS zaroori hai taake mic kaam kare)
3. Page pe do keys dalo (sirf tumhare browser mein save hongi, kahin nahi bheji jatin):
   - **Deepgram API Key** — deepgram.com → Console → API Keys (signup pe $200 free credits, card nahi chahiye)
   - **Groq API Key** — console.groq.com → API Keys (free tier, card nahi chahiye)
4. Mic dabao, bolo — AI jawab bolegi.

## Kya hota hai (pipeline)

Mic → Deepgram `nova-3` (STT) → Groq `llama-3.3-70b-versatile` (system prompt = receptionist ka kirdaar) → Deepgram `aura-2` (TTS) → awaz.

## Agla step (Phase 1)

Twilio trial number jor ke yehi pipeline asli phone calls pe chalana.
