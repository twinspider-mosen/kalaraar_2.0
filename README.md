# Kalakar Studio — AI Video Captioning & NLE Platform Clone

A production-ready full clone of **Kalakar.io**, engineered specifically for South Asian / Desi creators with word-level accurate subtitles in Urdu, Hindi, Punjabi, Bengali, Tamil, Telugu, and 15+ regional languages.

---

## 🚀 Key Features

* **Real-time Remotion Canvas (`@remotion/player`)**:
  * 9:16 Shorts/Reels/TikTok, 16:9 Landscape, and 1:1 Square aspect ratios.
  * Frame-accurate video playback and animated caption overlay.
* **Viral Creator Subtitle Templates**:
  * **Ali Abdaal**: White rounded badge, smooth fade, sleek black font.
  * **Hormozi Pop**: Bold yellow active pop, thick black text stroke (`-webkit-text-stroke: 8px`).
  * **Neon Cyber Glow**: Pulsing emerald & cyan neon drop shadow.
  * **Kathmandu Gold**: Regional South Asian typography with Tiro Devanagari & Nastaliq scripts.
  * **Bubble Pop**: Glassmorphic pill background with spring bounce.
  * **Karaoke Sweep**: Continuous gradient filling as words are spoken.
* **Multi-Track Non-Linear Timeline (NLE)**:
  * Powered by **Zustand** state store.
  * Multi-track layout: Video, Subtitle, Audio.
  * Razor clip splitting at playhead (`splitClip`).
  * Ripple deletion (`rippleDeleteClip`).
  * Interactive playhead scrubbing and zoom slider.
  * Subject Masking toggle (Text-Behind-Person).
  * AI Audio Enhancement toggle (Voice Cleanup & Background Denoising).
* **Word-by-Word Interactive Transcript Editor**:
  * Click any word to jump playhead to its start timestamp.
  * Real-time inline spelling & text correction.
  * Add word after / delete word.
  * Word-level spotlight highlight toggle.
* **Speech-to-Text AI Pipeline (`/api/transcribe`)**:
  * Supports Groq (Whisper-large-v3) and OpenAI Whisper API.
  * Word-level timestamps (`timestamp_granularities: ['word']`).
  * High-fidelity fallback simulation for regional languages if API key is not yet set.
* **Export & Rendering Engine**:
  * Subtitle files: `.srt`, `.vtt`, `.txt`.
  * Burned-in MP4 Video export.
  * Apple ProRes 4444 with Alpha Channel (transparent background video).
  * Green Screen (Chroma key) video export.
* **Pakistan & Global Payment Gateway Integration (`/api/billing`)**:
  * **Lemon Squeezy / Paddle**: Global international cards, Apple Pay, Google Pay, payouts directly to Pakistani bank accounts / Payoneer.
  * **Safepay / JazzCash / EasyPaisa**: Local Pakistan PKR checkouts and mobile wallet payments.
  * **Aura Gamification System**: 6 tiers of weekly publishing streaks offering compounding subscription discounts from 5% to 30% lifetime off.
* **NLE Desktop Plugins Support**:
  * Architecture ready for Adobe Premiere Pro UXP extensions and DaVinci Resolve Studio scripts.

---

## 🛠️ Tech Stack

* **Framework**: Next.js 15 (App Router, Turbopack)
* **Frontend**: React 19, TypeScript, Tailwind CSS, Radix UI, Lucide Icons
* **Video Engine**: Remotion (`@remotion/player`, `@remotion/shapes`)
* **State Management**: Zustand
* **ASR / AI**: WhisperX / Groq / OpenAI Whisper
* **Database & Auth**: Supabase (PostgreSQL, Row Level Security)
* **Storage**: Cloudflare R2 / AWS S3 + Bunny Stream

---

## 🏁 Getting Started

### 1. Install Dependencies
```bash
npm install
```

### 2. Configure Environment Variables
Copy `.env.example` to `.env.local`:
```bash
cp .env.example .env.local
```
Fill in:
* `GROQ_API_KEY` or `OPENAI_API_KEY` (for speech-to-text)
* `NEXT_PUBLIC_SUPABASE_URL` & `NEXT_PUBLIC_SUPABASE_ANON_KEY`
* `LEMONSQUEEZY_API_KEY` or `SAFEPAY_API_KEY` (for payments)

### 3. Run Development Server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser.

* Landing page: `http://localhost:3000/`
* Studio Editor: `http://localhost:3000/editor/demo`
# kalaraar_2.0
