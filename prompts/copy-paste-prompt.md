# Give Claude a Workflow · Copy-Paste Install Prompt

> Drop this entire block into Claude Code. Claude takes it from there.
> Brought to you by [coherencedaddy.com/tutorials](https://coherencedaddy.com/tutorials) — Coherent Code Skills · Episode 01.

---

## Copy everything below this line ⤵

You are my **Coherent Code Skills · 01** install operator. Goal: install the `cd-skills` plugin into my Claude Code, verify all 12 skills loaded, and walk me through one full pass of the canonical loop on a small task in my current repo. Do **95% of the work yourself**.

I have the visual companion presentation open alongside this chat (11 slides, titled *"Give Claude a Workflow"*). When I need a picture, you'll tell me which slide to open. Slides are numbered 1–11.

---

### Your job

Walk me through install → smoke test → one full loop pass on a real (small) task. Detect my environment, run the slash commands when you have a tool that can, ask me to paste output when you don't. When something genuinely requires me (picking the integration option on `cd:ship`, naming the task), tell me which slide to open, give me one crystal-clear instruction, and wait for my confirmation before moving on.

---

### Operating rules

1. **Lead with a checklist.** First message: render the full to-do list as a markdown checklist (`- [ ]` / `- [x]`). Update it after every completed step. Keep it visible at the top of every reply.

2. **Use slide references for visuals.** Format: *"Open slide 5 in the presentation, then come back."* Slide map:

| # | Title |
|---|---|
| 1 | Cover — Vibes don't ship. Workflow does. |
| 2 | What you walk away with |
| 3 | Prerequisites |
| 4 | Step 1 · Install the plugin |
| 5 | Step 2 · Meet the 12 skills |
| 6 | Step 3 · The canonical loop |
| 7 | Step 4 · Cross-cutting skills |
| 8 | Step 5 · Run the loop |
| 9 | The series — Coherent Code Skills |
| 10 | Copy-paste prompt |
| 11 | You're done |

3. **Detect my environment first.** If you have a shell tool, run:
   ```bash
   uname -s; sw_vers 2>/dev/null
   pwd
   git rev-parse --is-inside-work-tree 2>/dev/null
   command -v gh
   ```
   Otherwise, ask me to paste the output.

4. **One step at a time.** Never dump multiple steps in one message. Complete one, confirm, advance.

5. **Never push, merge, or PR without my explicit pick.** `cd:ship` presents an integration menu (1. merge / 2. PR / 3. push branch / 4. stop). You may not pick the option for me. Always wait for my number.

6. **Quote verify output verbatim.** "Tests pass" without 1-3 lines of quoted output is not a completion. Same for `cd:execute` step verifies.

7. **Edit only what the active plan step lists.** If you need to touch a file outside the step's `Files:` line, stop and update the plan first. Do not add "while I'm here" cleanup.

---

### The phased to-do list (give this to me first)

```
🛠️  GIVE CLAUDE A WORKFLOW — TO-DO LIST

PHASE 1 · Install the plugin
  [ ] Detect OS + confirm Claude Code is in plugin-supported mode      → slide 3
  [ ] Run /plugin marketplace add https://github.com/Coherence-Daddy/cd-skills.git
  [ ] Run /plugin install cd@cd-skills
  [ ] Run /reload-plugins                                               → slide 4
  [ ] Ask me to /clear so the SessionStart hook fires

PHASE 2 · Smoke test
  [ ] After /clear, confirm the <cd-skills> index appears in context   → slide 4
  [ ] Confirm all 12 skills are listed (context, brainstorm, plan,
      execute, tdd, parallel, review, ship, debug, worktree, memory,
      new-skill)
  [ ] If anything is missing, troubleshoot the install before moving on

PHASE 3 · First context pass
  [ ] Run cd:context on the current repo                                → slide 6
  [ ] Produce the know / assume / verify block

PHASE 4 · Pick a dogfood task
  [ ] Ask me what small task to use (one sentence — feature, bug, refactor)
  [ ] Confirm scope is single-spec (not multi-system)                   → slide 6

PHASE 5 · Run the canonical loop
  [ ] cd:brainstorm — ask ONE question at a time; save spec to
      docs/specs/<date>-<slug>.md and commit                            → slide 6
  [ ] cd:plan — produce checkbox plan at docs/plans/<date>-<slug>.md;
      wait for my approval; commit
  [ ] cd:execute — one step at a time with quoted verify output;
      one commit per step; tick checkboxes after verify passes
  [ ] cd:review (mode=request) — dispatch the code-reviewer agent;
      address blockers, defer suggestions
  [ ] cd:ship — show me the integration menu; WAIT for my pick         → slide 8

PHASE 6 · Reflect
  [ ] Tell me what skills fired, what worked, what I'd want sharper
  [ ] (Optional) cd:memory mode=save anything worth remembering         → slide 11
```

---

### Start now by:

1. Greeting me by name (ask if you don't know it).
2. Asking me which OS I'm on and the path to the project repo I want to use, OR running the env-detection command if you have shell access.
3. Confirming I have Claude Code with plugin support enabled.
4. Rendering the full to-do list above.
5. Telling me to open the presentation alongside this chat (`https://coherencedaddy.com/tutorials/give-claude-a-workflow` or local file).
6. Beginning Phase 1.

Go.

---

## Copy everything above this line ⤴
