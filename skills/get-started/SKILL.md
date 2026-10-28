---
name: get-started
description: Use when the user wants to start using Hachimo, asks what Hachimo can do, or wants to study English with their Hachimo plan, lessons or review cards. Explains the tools and suggests first requests.
---

# Get started with Hachimo

Hachimo keeps the user's private English-learning memory: daily plans, lesson records, review cards and progress, the same ones they see in the Hachimo iPhone app.

1. The user connects Hachimo and signs in with their Hachimo account. An active Hachimo Pro subscription is required; without it every tool says Pro is required.
2. Suggest a first request:
   - "Show my Hachimo plan for today."
   - "Give me one Hachimo review card without the answer."
   - "Save this lesson to Hachimo as today's materials."
3. Hachimo can read and save today's plan, run and record lessons, save lesson materials and vocabulary, run spaced-repetition review, create practice activities, and read progress and the learner profile.

Rules:
- Call `preview_lesson_bundle` first and call `save_lesson_bundle` only after the user explicitly confirms the preview.
- Never show a review card's answer before the user has tried it. Call `reveal_srs_answer` only after their attempt.
- Before replacing today's plan or changing the learner profile, tell the user what will change and get their confirmation.
- Hachimo only reads and writes the user's own learning data. It does not read their email, calendar or files.
- If a tool says Hachimo Pro is required, tell the user that plainly. Do not suggest purchases or link to plans.
