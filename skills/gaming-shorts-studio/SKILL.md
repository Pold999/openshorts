
---
name: gaming-shorts-studio
description: Analyze, improve, debug and extend Gaming Shorts Studio using OpenShorts as a technical reference. Focus on content-aware clip selection, truthful hooks, short-form storytelling, subtitles, FFmpeg rendering, Gemini API reliability and automated tests.
---

# Gaming Shorts Studio Development Skill

## Objective

Develop a reliable AI-powered gaming shorts editor that produces engaging vertical clips from authorized YouTube videos, Twitch VODs and local recordings.

## Core principles

1. Prioritize genuine storytelling over random movement or loud audio.
2. Use visual and audio understanding to identify meaningful moments.
3. Generate truthful, specific hooks grounded in the source footage.
4. Reject weak clips instead of forcing a fixed number of exports.
5. Preserve important gameplay elements and streamer facecams.
6. Use subtitles, zooms and effects only when they improve clarity or impact.
7. Never claim that a viral score guarantees views.

## Video analysis

- Use Gemini or another configured multimodal model to analyze candidate scenes.
- Identify the setup, payoff, reactions and context.
- Assign explainable editorial scores.
- Preserve source timestamps.
- Avoid fabricated events or dialogue.
- Cache completed analyses to reduce repeated API calls.

## Video editing

- Produce vertical 9:16 MP4 exports.
- Support 720x1280 and 1080x1920.
- Create accurate, synchronized captions.
- Use adaptive editing based on scene type.
- Generate meaningful A/B variants.
- Validate audio, duration, aspect ratio and output integrity.

## Reliability

- Handle yt-dlp HTTP errors.
- Support compatible JavaScript runtimes such as Deno.
- Implement API timeouts, retries and model fallback.
- Persist downloaded sources and analysis results.
- Keep secrets in environment variables.
- Provide detailed logs and visible progress.

## Development workflow

1. Inspect the existing project before modifications.
2. Identify the root cause of defects.
3. Propose the smallest reliable implementation.
4. Implement changes without breaking existing functionality.
5. Run automated tests and media export checks.
6. Review the output video quality.
7. Document limitations and remaining problems.

## OpenShorts integration

Use the OpenShorts repository as a reference for:

- clip selection and quality scoring
- subtitles and captions
- face tracking and video layouts
- editing and rendering
- automated test architecture

Inspect source licenses and compatibility before copying code.
Do not assume OpenShorts APIs are compatible with Gaming Shorts Studio.

## Safety and publishing

Only download, edit and publish content when the user has permission.
Never expose API keys or other secrets.
Require explicit authorization before publishing videos.
