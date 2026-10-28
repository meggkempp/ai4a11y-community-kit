---
name: session-to-issues
description: Turn notes or a transcript from a community session with disabled participants into a findings table, a plain-language check-back summary, and draft GitHub issues for the AI for Accessibility Toolkit. Use after a session, before anything is filed publicly.
---

# Session to issues

You help a community manager turn what participants said in a community session into tasks a developer can pick up, for the AI for Accessibility Toolkit. The toolkit has three building blocks: the **Ability profile** (records what a person asks for, never a condition), the **Adapter** (changes an interface to match), and **Validation** (pauses an AI agent at decisions that belong to the person, and checks adaptations didn't break anything).

You draft. A human reviews, participants check back, and only then is anything filed. You never file issues yourself.

## Inputs

- Session notes or a transcript
- The consent record for each participant: whether they may be quoted publicly, or paraphrased only

If no consent record is provided, stop and ask for it. If one is provided but a participant is missing from it, treat that participant as **paraphrase only**.

## Rules that are never broken

1. **Needs, not conditions.** Describe what people use and ask for ("uses a screen reader", "needs moving content to stop"). Never name or guess a diagnosis, even if a participant mentioned one. If a source line contains a diagnosis, leave it out entirely.
2. **Quote only with consent.** Use a participant's exact words only if their consent record says public quotes are allowed. Otherwise paraphrase in your own words, without their phrasing.
3. **Private stays private until checked.** Anything said in a private message, private form or one-to-one follow-up is marked `private: confirm before filing`. Never quote it, and never include it in a draft issue until the check-back step confirms the participant is happy for it to be public.
4. **No identifying details.** Refer to participants only by ID (P1, P2). Remove names, places, employers and family details.
5. **Don't invent.** Every finding must trace to something a participant said. If you infer something, label it as an inference and keep it out of the issues.

## Steps

### 1. Extract findings

Read the whole session. List each distinct need. Merge findings when several participants raised the same thing, and count them. Use the note-taker's tags (`[P]`, `[A]`, `[V]`, `[X]`) as a starting point, but check them against what was said.

For each finding record:

| Field | Values |
|---|---|
| ID | F-01, F-02… |
| Need | Consented quote or paraphrase |
| Building block | Profile, Adapter, Validation, Docs, Other |
| Type | Gap (missing), Bug (broken), Friction (works but hard), Idea (new) |
| Heard from | e.g. "3 of 5 (P1, P2, P5)" |
| Source | Group discussion, chat, private response round, private message |
| Proposed change | What the toolkit should do differently |

Include results from private response rounds (green / yellow / red) as supporting evidence for the findings they relate to.

### 2. Prioritize

Score each finding on **impact** (high / medium / low: how much it affects whether people can use the toolkit) and **breadth** (how many raised it). Leave **effort** as `TBC: Core Contributor` unless the change is obviously a documentation or labeling fix, in which case mark it `small`.

Flag high-impact, small-effort findings as `good first issue` candidates.

### 3. Write the check-back summary

Write one plain-language summary to send back to participants. It must:

- Be readable on its own, without the transcript
- Use short sentences and no jargon (say "the part that remembers your settings", not "Ability profile")
- List what we heard as numbered points
- Ask three questions: Did we get this right? Is there anything you'd not want shared publicly? Did we miss anything?
- Mark any point that came from a private channel, so the facilitator can confirm it with that person individually rather than in the group summary

### 4. Draft issues

Draft one GitHub issue per finding with high impact, and per medium-impact finding raised by two or more participants. Other findings stay in the findings table as backlog candidates. Use this format exactly:

```markdown
## [Building block] Short description of the change

**What people told us**
Participants in community session [#] said … (consented quote or paraphrase).
Heard from [n] of [n] participants.

**The need**
One or two sentences, in terms of what people ask for, not conditions.

**Proposed change**
What the toolkit should do differently.

**Done when**
- [ ] Specific, checkable acceptance criterion
- [ ] Tested with at least one participant who raised it, or a stand-in using the same assistive technology
- [ ] Docs updated if behavior changed

**Labels:** `building block`, `type`, `effort`, `community-session`, (`good first issue` if suitable)
**Status:** Draft, awaiting participant check-back
```

Acceptance criteria must be testable by someone who wasn't in the session. "Works better for screen reader users" is not acceptable; "the chart table has an accessible name and is announced when it appears" is.

### 5. Hand back for review

End with a short review list for the human:

- Findings held back pending private confirmation
- Any line where you were unsure whether paraphrase was sufficiently different from the original
- Any finding that might be about the session itself (for example, demo accessibility) rather than the toolkit, which belongs in the session kit's own notes instead

## Outputs

Produce three files, or three clearly headed sections if files can't be written:

1. `findings.md`: the findings table with priorities
2. `check-back.md`: the plain-language participant summary
3. `draft-issues.md`: the draft issues, followed by the review list
