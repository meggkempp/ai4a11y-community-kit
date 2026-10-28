# AI for Accessibility: Community Kit

**From what disabled people say to tasks developers can build.**

A community session kit and Claude skill for the [AI for Accessibility Toolkit](https://github.com/AI-for-Accessibility-Collective/AI-for-Accessibility-Toolkit). It covers the full path from a paid, accessible session with disabled participants to well-scoped GitHub issues a new open-source contributor can pick up, with consent and participant check-back built in at every step.

## Why this exists

The toolkit's goal is software that adapts to each person, rather than asking people to adapt to it. That only works if what people actually need reaches the developers building it, in a form they can act on. Too often, findings from research sessions stay in notes.

This repo closes that gap, and applies the toolkit's own principles to the research process:

| The toolkit… | This kit… |
|---|---|
| Records what a person asks for, never a condition | Screens and writes findings by needs and tools, never diagnoses |
| Lets the person choose every change | Gives participants a private way to answer and control over what is quoted |
| Pauses an AI agent at decisions that belong to the person | Checks every finding back with participants before anything is made public |

## What's inside

```
session-kit/                  How to run a session, step by step
  README.md                   Principles and field notes
  01-plan-and-recruit.md      Recruiting, layered consent, access, pay, safety
  02-discussion-guide.md      A 60-75 minute guide mapped to the toolkit's loop
  03-synthesis-template.md    From session notes to GitHub issues

skills/session-to-issues/     A Claude skill that drafts the findings, the
  SKILL.md                    participant summary and the GitHub issues

examples/mock-session-01/     A worked example, start to finish
  transcript.md               A fictional five-person session
  findings.md                 16 findings, prioritized
  check-back.md               The plain-language summary sent to participants
  draft-issues.md             9 draft issues and a review list
```

## Start here

- **New to the kit?** Read [`session-kit/README.md`](session-kit/README.md).
- **Want to see it work?** Read [`examples/mock-session-01/draft-issues.md`](examples/mock-session-01/draft-issues.md), then trace any issue back through `findings.md` to `transcript.md`.
- **Looking for something to build?** The worked example includes a `good first issue`: giving generated chart tables an accessible name, so voice control users can reach them.

## Using the skill

The skill drafts; people decide. It never files issues itself, and it holds back anything said privately until the participant confirms it can be shared.

To use it, add the `skills/session-to-issues` folder to Claude as a skill, or ask Claude Code to follow `skills/session-to-issues/SKILL.md`. Give it two things:

1. Your session notes or transcript
2. Each participant's consent record (quote, or paraphrase only)

It returns a findings table, a participant check-back summary and draft issues, in the toolkit's issue format.

**Rules it never breaks:** needs not conditions; quotes only with consent; private stays private until confirmed; no identifying details; nothing invented.

## Where the practices come from

The kit draws on my research for Catholic Relief Services' ReMiND prenatal care app in Uttar Pradesh, India, where I led recruiting, consent, research, design and validation with low-vision and low-literacy residents alongside community health workers. Layered consent and private response options both come from that work. More in [`session-kit/README.md`](session-kit/README.md#field-notes-where-these-practices-come-from).

## Status

A working draft, built independently to support the AI for Accessibility Collective's community work. It is not an official Collective project. The example session is fictional; no real participant's words appear in this repo.

Feedback, issues and pull requests are welcome.

## About

Made by **Meg Kemp**, design researcher and founder of [Alma Major](https://www.almamajor.com/), a behavioral insight studio. [LinkedIn](https://www.linkedin.com/in/meghan-kemp/)

## License

[Apache License 2.0](LICENSE), matching the AI for Accessibility Toolkit, so anything here can be folded into it.
