# Give Claude a Workflow

> **Coherent Code Skills · Episode 01**
> Vibes don't ship. Workflow does.

A 5-minute walkthrough that installs the [`cd-skills`](https://github.com/Coherence-Daddy/cd-skills) plugin into your Claude Code, lights up the canonical loop, and walks you through one full pass — context → brainstorm → plan → execute → review → ship — on a real task in your repo.

## Watch the tutorial

→ **[coherencedaddy.com/tutorials/give-claude-a-workflow](https://coherencedaddy.com/tutorials/give-claude-a-workflow)** — 11 slides, ~5 min read.

## Hand it off to Claude

The companion copy-paste install prompt (in [`prompts/copy-paste-prompt.md`](prompts/copy-paste-prompt.md)) does the entire setup + your first loop pass end-to-end:

- Runs `/plugin marketplace add` and `/plugin install` for you.
- Confirms the SessionStart hook fired and all 12 skills loaded.
- Drives `cd:context` on your current repo to produce the *know / assume / verify* block.
- Asks you for one small dogfood task and walks the full loop on it.
- Stops at every gate. Never picks the integration option for you on `cd:ship`.

Drop the prompt into Claude Code. It walks you through install → smoke test → one real loop pass with a checklist that updates after every step.

## What's in this repo

```
.
├── index.html                       ← The 11-slide presentation (self-contained, no build step)
├── cd-face-coral.png                ← Brand monogram referenced by the sidebar
├── og.png                           ← Open Graph card for social unfurl
├── prompts/
│   └── copy-paste-prompt.md         ← The companion install prompt — paste into Claude
└── README.md                        ← This file
```

## The twelve skills (in 30 seconds)

```
Workflow phases:    context → brainstorm → plan → execute → review → ship
Cross-cutting:      tdd · parallel · debug · worktree · memory
Meta:               new-skill
```

Each skill is a single `SKILL.md` with a hard gate, a numbered checklist, and a forced handoff. The agent can't drift past a gate without your approval.

## The canonical loop, in one screen

```
cd:context      load memory + git + key files; produce know/assume/verify
   ↓
cd:brainstorm   one-question-at-a-time dialogue; spec saved + committed
   ↓
cd:plan         spec becomes checkbox plan; you approve, plan committed
   ↓
cd:execute      one step at a time, with quoted verify output per step
   ↓
cd:review       self-review then dispatch the code-reviewer agent
   ↓
cd:ship         full verify, then YOU pick: merge / PR / push / stop
```

Run that loop on a small task once. The hour you'd usually spend untangling a half-baked diff disappears.

## License

MIT — copy, fork, remix. The plugin itself ([`cd-skills`](https://github.com/Coherence-Daddy/cd-skills)) is also MIT.

## More from Coherence Daddy

- **[cd-skills](https://github.com/Coherence-Daddy/cd-skills)** — the plugin this tutorial installs. 12 skills, MIT, no telemetry.
- **[Give Claude an Organized Brain](https://github.com/Coherence-Daddy/give-claude-an-organized-brain)** — Coherent Obsidian Skills · 01. Adopt kepano-style frontmatter graphs in your Obsidian vault.
- **[Use Ollama to Enhance Claude](https://github.com/Coherence-Daddy/use-ollama-to-enhance-claude)** — pair Anthropic Claude Desktop with Claude Code routed through Ollama. Cuts Claude Code spend ~90%.
- **[Give Obsidian a Memory](https://github.com/Coherence-Daddy/give-obsidian-a-memory)** — wire Claude Desktop into an Obsidian vault via MCP, with Ollama embedding locally. One-click installer.
- **[More tutorials →](https://coherencedaddy.com/tutorials)**

---

🟠 [coherencedaddy.com](https://coherencedaddy.com)
