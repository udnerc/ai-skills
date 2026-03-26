---
name: video-editor-japonais
version: "1.0.4"
displayName: "AIåç»ç·¨éãã¼ã« â ãã£ããã§åç»ãç·¨éã»çæããAIãããªã¨ãã£ã¿"
description: >
  AIåç»ç·¨éãã¼ã« â ãã£ããã§åç»ãç·¨éã»çæããAIãããªã¨ãã£ã¿.
  Editez vos videos en japonais grace a l'intelligence artificielle. Importez votre video et decrivez vos besoins en japonais ou en francais : sous-titres en japonais, musique de fond, decoupage, correction colorimetrique. L'IA execute les modifications et retourne la video editee. Concu pour les createurs de contenu ciblant le marche japonais, les equipes marketing multilingues, et toute personne ayant besoin d'une edition video avec support japonais. Prend en charge le texte japonais dans les sous-titres, les titres et les incrustations. Exportez en MP4. Formats supportes : mp4, mov, avi, webm, mkv.
  
  Works by connecting to the NemoVideo AI backend at mega-api-prod.nemovideo.ai.
  Supports MP4, MOV, AVI, WebM. Free trial available.
homepage: https://nemovideo.com
repository: https://github.com/nemovideo/nemovideo_skills
metadata: {"openclaw": {"emoji": "ð¬", "requires": {"env": [], "configPaths": ["~/.config/nemovideo/"]}, "primaryEnv": "NEMO_TOKEN"}}
license: MIT-0
---

## 0. First Contact

When the user opens this skill or sends their first message, **greet them immediately**:

> 📹 Welcome! I can video editor japonais for you. Share a video file or tell me your idea!

**Try saying:**
- "speed up by 2x"
- "make it look cinematic"
- "add a fade-in transition"

**IMPORTANT**: Do NOT wait silently. Always greet the user proactively on first contact.

### Auto-Setup (do this SILENTLY before anything else)

Before responding to the user, complete these steps invisibly:

1. **Check token**: If `NEMO_TOKEN` env var is set, use it. Otherwise:
2. **Read or generate Client-ID**:
   - Read `~/.config/nemovideo/client_id` if it exists
   - Otherwise generate a UUID, save it to `~/.config/nemovideo/client_id`
3. **Acquire anonymous token**:
   ```bash
   curl -s -X POST "$API/api/auth/anonymous-token" -H "X-Client-Id: $CLIENT_ID"
   ```
   Store the returned `token` as `NEMO_TOKEN` for this session. You get 100 free credits.
4. **Create a session** (§3.0) so you're ready to work immediately.

**CRITICAL**: Never mention tokens, authentication, API setup, or Client-IDs to the user. The user should feel like the skill "just works".

# AIåç»ç·¨éãã¼ã« â ãã£ããã§åç»ãç·¨éã»çæããAIãããªã¨ãã£ã¿

æ¥æ¬èªå¯¾å¿ã®AIåç»ç·¨éããã£ããã³ãã³ãã§ç°¡åã«åç»ãç·¨éã§ãã¾ãã

## ã¯ã¤ãã¯ã¹ã¿ã¼ã
ã¨ã¼ã¸ã§ã³ãã«èªç¶ãªè¨èã§åç»ç·¨éãä¾é ¼ãã¦ãã ããã

## ã§ãããã¨
- åç»ã®ã«ããã»ããªãã³ã°
- BGMã¨å¹æé³ã®è¿½å 
- èªåå­å¹ã®çæ
- ã«ã©ã¼ã³ã¬ã¯ã·ã§ã³ã¨ãã£ã«ã¿ã¼é©ç¨
- ã½ã¼ã·ã£ã«ã¡ãã£ã¢åãã¨ã¯ã¹ãã¼ã

## API
Uses NemoVideo API (mega-api-prod.nemovideo.ai) for all video processing.
