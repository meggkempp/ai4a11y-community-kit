# Mock session 01: findings

> Output of the `session-to-issues` skill run on `transcript.md`. Fictional session; see the transcript for consent records.

## Findings table

| ID | Need | Block | Type | Heard from | Source | Proposed change | Impact | Effort |
|---|---|---|---|---|---|---|---|---|
| F-01 | Settings like text size and captions have to be set up again on every site and every device. P5: "I set it up on my laptop, then my phone is completely different, then my daughter's tablet." | Profile | Gap | 3 of 5 (P2, P3, P5) | Group, chat | Let preferences follow the person across the apps and devices they allow | High | TBC: Core Contributor |
| F-02 | People want to see, in plain words, everything the profile has remembered, and delete any of it. | Profile | Gap | 1 of 5 (P2), supported by yellow votes from P2, P4 | Group, response round | A plain-language view of the profile with per-item delete | High | TBC |
| F-03 | The profile should record the tools someone uses, not imply why. P4: "Not that I have a disability. Just that I use voice." Concern that employers or insurers could infer a condition. | Profile | Gap | 1 of 5 (P4) | Group | State and test that no stored field or combination of fields describes a condition | Medium | TBC |
| F-04 | Separate profiles for different parts of life, such as work and home. | Profile | Idea | 1 of 5 | **Private: confirm before filing** | Not drafted | — | — |
| F-05 | Before agreeing, people need a simple explanation of where their profile is kept, and the ability to take it with them. P5: "I'd need someone to explain that to me simply before I said yes." | Profile, Docs | Gap | 2 of 5 (P1, P5) | Group | A plain-language explainer shown before consent; profile export | Medium | Small (explainer), TBC (export) |
| F-06 | With larger text on, the site's menu is pushed under the article or off the screen, the same problem as manual zoom. | Adapter | Bug | 2 of 5 (P2, P4 yellow votes) | Group, response round | Larger-text adapter checks that navigation stays visible and reachable | High | TBC |
| F-07 | When a chart becomes a table, nothing tells the person it happened; they find it by accident. P1: "it didn't tell me the table was there." P1 also asked to be told about every change. | Adapter | Bug | 1 of 5 (P1), repeated in closing | Group | Announce each adaptation briefly when it is applied | High | TBC |
| F-08 | The generated chart table has no name, so voice control users can't navigate to it. P4: "The new table had no name, so I couldn't jump to it by saying anything." | Adapter | Bug | 1 of 5 (P4), supported by P4 yellow vote | Group, response round | Give generated tables an accessible name based on the chart title | High | Small: **good first issue** |
| F-09 | Many buttons are icons with no name, so they can't be spoken in voice control. | Adapter | Idea | 1 of 5 (P4) | Group | Explore an adapter that adds names to unlabeled icon buttons | Medium | TBC |
| F-10 | People differ on whether changes should happen automatically. P5: suggested first, then automatic once agreed. P1: automatic, but say what changed. P2 (paraphrase): always suggest, after past bad experiences with tools that changed things uninvited. | Adapter, Profile | Idea | 3 of 5 (P1, P2, P5) | Group | Store each person's choice (always ask, ask once, automatic with notice) in the profile | Medium | TBC |
| F-11 | An AI agent should always stop before a decision involving money, and explain the difference briefly, without a large comparison table. | Validation | Gap | 4 of 5 (P1, P3, P4, P5) | Group, chat | Make payments and plan changes a default pause point; require a short plain-language summary of what changes | High | TBC |
| F-12 | Confirmation requests should come in the person's preferred way, such as a written message they can read when ready, rather than a sound or call. | Validation | Gap | 1 of 5 (P3) | Chat | Read the preferred confirmation channel from the profile | Medium | TBC |
| F-13 | Confirmations should wait; some people need longer to decide. P5: "Don't time out on me." | Validation | Gap | 1 of 5 (P5) | Group | No default timeout on confirmation requests | Medium | TBC |
| F-14 | People need a clear way to reverse a change. P5: "An undo button. A big obvious one." P2 and P5 described updates that changed their settings and took days to recover from. | Validation, Adapter | Gap | 2 of 5 (P2, P5) | Group | A prominent undo for every adaptation, restoring the previous state | High | TBC |
| F-15 | Some people want a structured version of a page, with clear headings, rather than the visual layout. P1: "give me the structured version, not the pretty version." | Adapter | Idea | 1 of 5 (P1) | Group | Explore a structure-first adapter | Low | TBC |
| F-16 | Captions lagged behind the demo, so a text-only participant couldn't follow it. | Other: session | — | 1 of 5 | **Private form** | Session kit note, not a toolkit task | — | — |

## Response round evidence

| Statement | Green | Yellow | Red |
|---|---|---|---|
| Comfortable with preferences following me between apps | P1, P5 | P2, P4 | P3 (private: only if they choose the apps) |
| Larger text adapter | P5 | P2 (menu breaks), P4 | — |
| Charts as tables | P1, P2, P3 | P4 (can't reach by voice) | — |
| Reduced motion | P2, P3, P4, P5 | — | — |

**Reading the round:** reduced motion worked for everyone it applied to, and is not a priority for change. Cross-app profiles drew the most hesitation, which supports prioritizing F-02 (seeing and deleting what's remembered) and F-05 (explaining where it's kept) alongside F-01.

## Priority order for drafting

1. F-11 Stop before money decisions (4 of 5)
2. F-01 Preferences across apps and devices (3 of 5)
3. F-14 Undo (2 of 5)
4. F-06 Larger text hides navigation (2 of 5)
5. F-08 Name generated tables: **good first issue**
6. F-07 Announce adaptations
7. F-02 Plain-language profile view
8. F-10 Per-person automation preference (medium, 3 of 5)
9. F-05 Explain where the profile is kept (medium, 2 of 5)

Backlog candidates, not drafted: F-03, F-09, F-12, F-13, F-15. Held: F-04 (private). Session note: F-16.
