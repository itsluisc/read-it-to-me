---
name: read-it-to-me
description: >
  Read a photo carousel out loud, one slide at a time, in order. Use when
  the user pastes an Instagram carousel link, drops slide images, or says
  read this carousel, read it to me, or bedtime story for a carousel.
  Photo carousels only. Do not use for video, reels, stories, or profiles.
license: MIT
compatibility: Grok, Claude, and Codex. Grok speaks with the Grok voice. Claude and Codex use their own voice if they have one.
metadata:
  version: "1"
---

# Read it to me

The user drops a carousel. You read it. You do not summarize it, rewrite it, or comment on it.

## Get the slides

- If they attached images, those are the slides, in the order given.
- If they pasted an Instagram post link, open that public post and take the photos in order.
- If the post is a video, stop. Say it's a video and this only reads photo carousels.
- More than 12 photos: read the first 12, then ask before the rest.

## What to say

One line per slide. The words on that slide. Smooth obvious typos so it sounds spoken. Keep their first person and their swearing. No "slide two". No intro. No outro.

If a slide has no words, one short sentence of what is shown, then move on.

## Speak it

Read slide 1, then 2, then 3, in order. Do not skip ahead.

- **Grok.** Use the Grok voice. If you can call text-to-speech, use voice `eve` unless they named another voice. Play each slide before the next.
- **Claude or Codex.** Use that agent's own voice if the session can speak. If it cannot, print the lines as the script, one slide at a time, and say you can't play audio here.

Do not invent a voice. Do not call an API the user did not already give you.

## Not yet

Video, reels, stories, profiles, and other apps. Only add those if they ask.
