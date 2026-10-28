# Hachimo plugin

Connects your agent to [Hachimo](https://mcp.hachimo.protoductai.com), an English-learning app for iPhone, through Hachimo's hosted MCP server at `https://mcp.hachimo.protoductai.com/mcp`.

This plugin works in Cursor and Grok Bot. It contains one MCP server and one skill (`get-started`). It has no commands, hooks or local code.

## Requirements

- A Hachimo account (the one you use in the Hachimo iPhone app).
- An active Hachimo Pro subscription. Without Pro, every tool returns a short message saying Pro is required.

## Connect

1. Install the plugin from the marketplace.
2. When the agent first calls Hachimo, a sign-in page opens. Sign in with your Hachimo account and approve access. Hachimo uses OAuth 2.1 with PKCE and dynamic client registration, so there is no API key to paste.
3. To disconnect, remove the plugin.

## Try it

- "Show my Hachimo plan for today."
- "Give me one Hachimo review card without the answer."
- "Save this lesson to Hachimo as today's materials."

## Tools

| Tool | What it does | Changes data |
|---|---|---|
| `get_today_plan` | Read today's study plan and progress | No |
| `save_today_plan` | Create or replace today's study plan | Yes |
| `adjust_today_plan` | Shrink today's plan to a shorter time budget | Yes |
| `start_lesson` | Start a task from today's plan and get its lesson prompt | Yes |
| `complete_lesson` | Record a finished lesson: score, summary, mistakes and new words | Yes |
| `preview_lesson_bundle` | Show exactly what a lesson save would register, without saving | No |
| `save_lesson_bundle` | Save a lesson record, review cards and materials after you confirm the preview | Yes |
| `create_learning_assignment` | Create a vocabulary list, practice quiz or pronunciation test | Yes |
| `get_learning_assignment` | Open a learning activity by ID | No |
| `submit_learning_assignment` | Save the results of a finished learning activity | Yes |
| `add_srs_items` | Save vocabulary to your review deck | Yes |
| `get_srs_queue` | Get review cards due now (fronts only) | No |
| `reveal_srs_answer` | Reveal a card's answer after you have tried it | No |
| `submit_srs_review` | Record how well you remembered a card | Yes |
| `get_progress` | Read XP, streaks, weekly chart data and badges | No |
| `get_learner_profile` | Read your level, goal, interests, weaknesses and daily minutes | No |
| `update_learner_profile` | Update parts of your learner profile | Yes |

## Privacy

Hachimo only reads and writes your own learning data: today's plan, lesson records, review cards, practice activities, progress and learner profile. It previews a lesson before saving it, never reveals a review answer before you try, and does not access your email, calendar, files or chat history.

- Privacy policy: https://mcp.hachimo.protoductai.com/privacy
- Terms: https://mcp.hachimo.protoductai.com/terms
- Support: https://mcp.hachimo.protoductai.com/support (support@protoductai.com)

## License

MIT. See [LICENSE](LICENSE). The license covers the files in this repository, not the Hachimo service.
