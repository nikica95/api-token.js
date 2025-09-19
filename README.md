# Vercel Stream Token API

Ova Vercel funkcija generira **server-side JWT token** za [Stream.io](https://getstream.io) koristeći službeni `stream-chat` SDK.

## 🔧 Setup

### 1. Environment varijable
U [Vercel Dashboardu](https://vercel.com/dashboard):
- Idi na **Project Settings → Environment Variables**
- Dodaj:
  - `STREAM_API_KEY` → tvoj Stream API key
  - `STREAM_API_SECRET` → tvoj Stream API secret

Dodaj ih za **Production** i **Preview** okruženja.

---

### 2. Deploy

1. Napravi novi **GitHub repozitorij** (npr. `vercel-stream-token-api`)
2. Uploadaj ovaj sadržaj (ili kloniraj moj ako želiš)
3. U Vercelu klikni **Add Project → Import GitHub repo**
4. Odaberi taj repo i klikni **Deploy**

Nakon deploya dobit ćeš endpoint:

