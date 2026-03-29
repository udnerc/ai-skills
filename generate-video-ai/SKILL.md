---
name: generate-video-ai
version: "1.0.6"
displayName: "Generate Video AI â Instant AI Video Creation from Text and Image Prompts"
description: >
  Generate Video AI â Instant AI Video Creation from Text and Image Prompts.
  Need video content fast without sourcing footage? Generate Video AI creates original video from your text prompt â specify the scene, mood, duration, and style, and receive a finished clip. Works for marketing teams that need visual assets on demand, creators building content libraries, and developers prototyping video-heavy features. Describe exactly what you need: 'a 30-second product demonstration with a clean studio background' or 'an outdoor lifestyle scene with warm lighting and upbeat energy.' The AI handles visual generation, scene composition, motion, and audio selection. Combine generated clips with uploaded footage in one session â mix AI-generated and real footage seamlessly. Batch generation available for multiple clips per session. Export as MP4.
  
  Works by connecting to the NemoVideo AI backend at mega-api-prod.nemovideo.ai.
  Supports MP4, MOV, AVI, WebM. Free trial available.
homepage: https://nemovideo.com
repository: https://github.com/nemovideo/nemovideo_skills
metadata: {"openclaw": {"emoji": "ð¬", "requires": {"env": [], "configPaths": ["~/.config/nemovideo/"]}, "primaryEnv": "NEMO_TOKEN"}}
license: MIT-0
---

## 0. First Contact

When the user opens this skill or sends their first message, **greet them immediately**:

> 📝 Ready to generate video ai! Just send me a video or describe your project.

**Try saying:**
- "generate a video from this description"
- "create a 30-second promo video"
- "make a slideshow"

**IMPORTANT**: Do NOT wait silently. Always greet the user proactively on first contact.

### Auto-Setup

When the user first interacts, set up the connection:

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

Let the user know briefly: "Setting things up… ready!" then proceed with their request.

# Generate Video AI â Instant AI Video Creation from Text and Image Prompts

Generate videos instantly from prompts. Fast AI video creation from text and images.

## Quick Start
Ask the agent to generate a video from your text or image prompt.

## What You Can Do
- Generate videos instantly from text prompts
- Create video from image uploads with AI motion
- Produce multiple video variations quickly
- Generate B-roll and stock footage on demand
- Create social media video content in seconds

## API
Uses NemoVideo API (mega-api-prod.nemovideo.ai) for all video processing.
