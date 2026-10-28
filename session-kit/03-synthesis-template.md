# Step 3: From findings to tasks

A session is finished when its findings are on the toolkit's to-do list as tasks a developer can pick up. This page takes notes from a session to published tasks in four steps.

```
Session notes → Findings table → Check-back with participants → Tasks on GitHub
```

## 1. Fill in the findings table

One row per distinct need. Merge rows when several participants raised the same thing, and record how many.

| ID | Need, in participant's words (or paraphrase) | Building block | Type | Heard from | Proposed change |
|---|---|---|---|---|---|
| F-01 | "I make the text bigger on every site, every single time." | Profile | Gap | 4 of 5 | Remember text size across apps the person allows |
| F-02 | | | | | |

**Building block:** Profile, Adapter, Validation, Docs, or Other.
**Type:** Gap (missing), Bug (broken), Friction (works but hard), Idea (new possibility).
**Rule:** describe needs, never conditions. "Uses a screen reader," not a diagnosis.
**Rule:** quote only participants who consented to quotes; otherwise paraphrase.

## 2. Prioritize

For each finding, score:

- **Impact:** how much it affects whether people can use the toolkit (high / medium / low)
- **Breadth:** how many participants raised it
- **Effort:** a rough guess from the Core Contributor (small / medium / large)

High impact and small effort become candidates for `good first issue`, since they are the best way to bring a new open-source contributor in.

## 3. Check back with participants

Before anything goes public, send each participant a short plain-language summary of what we heard, in the format they asked for. Ask:

- Did we get this right?
- Is there anything here you would not want shared publicly?
- Anything we missed?

Allow at least five working days. Change or remove findings based on the answers. This step mirrors the toolkit's Validation agent: the interpretation is checked with the person before anyone acts on it.

## 4. Write the task

Each finding that survives check-back becomes one GitHub issue, using this template:

```markdown
**Title:** [Building block] Short description of the change
e.g. [Profile] Remember text size across apps the person allows

**What people told us**
Participants in community session [#] said ... (paraphrase or consented quote).
Heard from [n] of [n] participants.

**The need**
One or two sentences, in terms of what people ask for, not conditions.

**Proposed change**
What the toolkit should do differently.

**Done when**
- [ ] Specific, checkable acceptance criterion
- [ ] Tested with at least one participant who raised it, or a stand-in using the same assistive technology
- [ ] Docs updated if behavior changed

**Labels:** building block, type, effort, `community-session`, `good first issue` if suitable
**Session:** link to the anonymized session summary
```

## 5. Close the loop

- Tell participants which tasks came from their session, in their preferred format
- When a task is completed, tell them again and invite them to try the change
- Record in the monthly progress note: sessions held, findings, tasks filed, tasks completed
