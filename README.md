# Spotify Circles — PM Portfolio Project

A fully interactive product prototype demonstrating a proposed social layer for Spotify. Built as a PM portfolio piece to showcase product thinking, user segmentation, and end-to-end feature design.

---

## The Idea

Spotify has 751M users but its social features are passive — you can see what friends are listening to, but you can't react, comment, or experience music together in real time.

**Spotify Circles** is a modular social layer that turns every listen into a potential conversation. The core insight: users are already being social about music, just not on Spotify. They're screenshotting songs for Instagram, running Discord servers for album drops, and texting friends about tracks. Circles brings all of that back in-app.

---

## PM Framework: How I Got Here

### 1. User Segmentation
Rather than designing for all 751M users, I identified two high-intent target segments:

| Segment | % of Users | Pain Point |
|---|---|---|
| **Social Sharers** | ~25% | Screenshot songs to share externally — huge friction, conversation leaves the app |
| **Community Seekers** | ~10% | Fragmented across Discord/Reddit to discuss music — no integration with actual listening |

**Combined target: 260M users** — large enough to move retention metrics, high enough intent to adopt social features immediately.

### 2. Jobs-to-be-Done
- **Social Sharers:** *"When I discover an amazing song, I want to spark a discussion with friends, so I can share the emotional experience"* — currently forced off-platform to do this
- **Community Seekers:** *"When I'm excited about a new release, I want to experience it with like-minded fans, so I feel part of something bigger"* — currently fragmented across 3-5 platforms

### 3. Solutions Mapped to Segments

| Feature | Target Segment | Key Metric |
|---|---|---|
| Song reactions & comments | Social Sharers | % of shares kept in-app vs. external |
| Listening Rooms | Community Seekers | Monthly active room participants |
| Friend Feed | Both | D7/D30 retention lift |

### 4. Prioritization (RICE)
- **Song Reactions** — RICE 8.5 (high reach × high impact × high confidence / medium effort) → Phase 1
- **Listening Rooms** — RICE 7.0 (medium reach × very high impact / high effort) → Phase 1
- **Social Discovery Feed** — RICE 9.0 but requires critical mass first → Phase 3

---

## Features Built in This Prototype

### Friend Feed
- Post what you're listening to with a caption
- Like posts — counters update in real time
- Emoji reactions (🔥 ❤️ ✨) — toggle on/off
- Comment on any post — full comment thread, add your own

### Listening Rooms
- Create a room — name it, set public/private
- Join any live room — full experience: album art, live progress bar, play/pause controls
- Live room chat — type messages, auto-reply simulation shows the social dynamic
- Leave room — seamlessly returns to the rooms list

### Activity Feed
- Real-time friend activity (likes, comments, room joins)
- Tap any item to "play" the track

### Now Playing Bar
- Persistent across all views (authentic Spotify UX)
- Play/pause toggle, seekable progress bar

---

## Success Metrics I'd Track

| Metric | Target | Why |
|---|---|---|
| **DASI** (Daily Active Social Interactions) | North Star | Captures health of the entire social layer |
| D30 retention lift | +8% for social-engaged users | Social features should increase stickiness |
| In-app share rate | 40%+ of shares stay in Spotify | Directly validates Social Sharer pain point |
| Room session length | 15+ min average | Proxy for community health |
| NPS delta | +5 pts vs. control group | Social features should drive advocacy |

---

## Risks & Mitigations

| Risk | Mitigation |
|---|---|
| Toxicity / spam in comments | AI moderation + community guidelines + flagging |
| Privacy concerns | Opt-in by default, granular controls per post |
| Cannibalization of passive listening | Monitor solo listening metrics, don't force social |
| Infrastructure at scale | Invite-only beta → gradual rollout |

---

## Tech Stack (Prototype)
Single-file HTML/CSS/JS — no dependencies, no build step required. Designed to be portfolio-ready and instantly runnable.

**If built for real:**
- Frontend: React + TypeScript
- Real-time: WebSockets (room chat) + WebRTC (synchronized playback)
- Backend: Node.js + Spotify Web API
- Auth: Spotify OAuth
- Infra: AWS / GCP with CDN for global low-latency

---

## How to Run

```bash
# Option 1: Just open it
open spotify-circles.html

# Option 2: Local server
npx serve .
# → http://localhost:3000/spotify-circles.html
```

---
*Built as a PM portfolio project. Concept, research framework, and prototype by Rahul Adusumalli*
