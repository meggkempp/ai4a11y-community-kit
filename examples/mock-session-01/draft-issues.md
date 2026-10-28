# Mock session 01: draft issues

> Output of the `session-to-issues` skill. **Drafts only**, awaiting participant check-back and human review. Fictional session.

---

## [Validation] Always pause before decisions involving money, with a short summary of what changes

**What people told us**
Participants in community session 1 said an AI agent should always stop before a decision involving money, such as renewing or changing a subscription. They asked for the difference to be explained briefly. P1: "Not a giant comparison table." P4: "Anything involving money, stop."
Heard from 4 of 5 participants.

**The need**
People want any spending or plan change to wait for their decision, explained in a way that is quick to take in with their tools.

**Proposed change**
Make payments, purchases and plan changes a default pause point in the Validation agent. The pause includes a short plain-language summary of what changes (cost, features gained, features lost).

**Done when**
- [ ] Any action classed as a payment, purchase or plan change triggers a pause by default, with no setting that silently disables it
- [ ] The summary states cost difference and features gained or lost in no more than three short sentences
- [ ] The summary is readable by screen reader and contains no table by default
- [ ] Tested with at least one participant who raised it, or a stand-in using the same assistive technology
- [ ] Docs updated to list default pause points

**Labels:** `validation`, `gap`, `effort: TBC`, `community-session`
**Status:** Draft, awaiting participant check-back

---

## [Profile] Let preferences follow the person across the apps and devices they allow

**What people told us**
Participants in community session 1 described setting up text size and captions again on every site and device. P5: "I set it up on my laptop, then my phone is completely different, then my daughter's tablet."
Heard from 3 of 5 participants.

**The need**
People want to set their preferences once and have them apply wherever they choose.

**Proposed change**
Document and test the path for a profile to be shared across devices, starting with text size and captions, only with apps the person has allowed.

**Done when**
- [ ] Text size and caption preferences set in one allowed app are applied in a second allowed app on a different device
- [ ] An app the person has not allowed receives nothing
- [ ] Tested with at least one participant who raised it, or a stand-in using the same assistive technology
- [ ] Docs include a step-by-step example of cross-device use

**Labels:** `profile`, `gap`, `effort: TBC`, `community-session`
**Status:** Draft, awaiting participant check-back
**Note:** Cross-app sharing drew the most hesitation in the session. Pair with the plain-language profile view and storage explainer issues below.

---

## [Validation] A prominent undo for every adaptation

**What people told us**
Participants in community session 1 asked for a clear way to reverse changes. P5: "An undo button. A big obvious one." Two participants described software updates that changed their settings and took days to recover from.
Heard from 2 of 5 participants.

**The need**
People need to get back to how things were, immediately and without hunting for a setting.

**Proposed change**
Every adaptation can be undone in one action, restoring the exact previous state.

**Done when**
- [ ] Each applied adaptation can be reversed with a single action reachable by keyboard, screen reader and voice control
- [ ] Undo restores the exact previous state, including settings the adaptation changed indirectly
- [ ] The undo control is announced when an adaptation is applied
- [ ] Tested with at least one participant who raised it, or a stand-in using the same assistive technology
- [ ] Docs updated

**Labels:** `validation`, `adapter`, `gap`, `effort: TBC`, `community-session`
**Status:** Draft, awaiting participant check-back

---

## [Adapter] Larger text pushes the site's navigation out of view

**What people told us**
Participants in community session 1 said that with the larger-text adaptation on, a news site's menu moved beneath the article, the same problem they have with manual zoom. Two participants gave the larger-text adaptation a "not sure" vote for this reason.
Heard from 2 of 5 participants.

**The need**
People who enlarge text need the site's navigation to stay visible and reachable.

**Proposed change**
After applying larger text, the adapter (or the Validation agent's breakage check) confirms primary navigation is still visible and reachable, and adjusts layout if not.

**Done when**
- [ ] On the example news test page, navigation remains visible and reachable at 200% and 400% text size
- [ ] The Validation agent flags the adaptation if navigation becomes hidden
- [ ] Tested with at least one participant who raised it, or a stand-in using screen magnification
- [ ] Docs updated

**Labels:** `adapter`, `bug`, `effort: TBC`, `community-session`
**Status:** Draft, awaiting participant check-back

---

## [Adapter] Give generated chart tables an accessible name

**What people told us**
Participants in community session 1 said the table created from a chart could not be reached with voice control. P4: "The new table had no name, so I couldn't jump to it by saying anything."
Heard from 1 of 5 participants.

**The need**
People using voice control or a screen reader need to find and move to the generated table by name.

**Proposed change**
Give each generated table an accessible name based on the original chart's title, falling back to "Chart data table" if the chart has no title.

**Done when**
- [ ] The generated table has an accessible name matching the chart title
- [ ] Without a chart title, the table is named "Chart data table"
- [ ] The table can be reached by voice command using its name, and is listed by name in screen reader table navigation
- [ ] Tested with voice control and at least one screen reader
- [ ] Docs updated

**Labels:** `adapter`, `bug`, `effort: small`, `community-session`, `good first issue`
**Status:** Draft, awaiting participant check-back

---

## [Adapter] Announce each adaptation when it is applied

**What people told us**
Participants in community session 1 said they only found a converted chart table by accident. P1: "it didn't tell me the table was there," and in closing asked to be told whenever something changes.
Heard from 1 of 5 participants, raised twice.

**The need**
People need to know when the interface has changed, and what changed.

**Proposed change**
Each adaptation announces itself briefly when applied, through the person's assistive technology, with a pointer to undo.

**Done when**
- [ ] Each adaptation triggers a short announcement (one sentence) that screen readers read out
- [ ] The announcement names what changed and how to undo it
- [ ] Announcements do not repeat on every page load once the person has acknowledged them
- [ ] Tested with at least one screen reader
- [ ] Docs updated

**Labels:** `adapter`, `bug`, `effort: TBC`, `community-session`
**Status:** Draft, awaiting participant check-back

---

## [Profile] Plain-language view of what the profile remembers, with delete

**What people told us**
Participants in community session 1 said they would want to see everything the profile has remembered, in plain words, and delete any of it.
Heard from 1 of 5 participants, supported by two "not sure" votes on sharing preferences between apps.

**The need**
People need to see and control what is remembered before they are comfortable letting it follow them.

**Proposed change**
A plain-language view listing each remembered preference, which apps can see it, and a delete control for each.

**Done when**
- [ ] Every stored preference is listed in plain language (e.g. "Larger text: on")
- [ ] Each item shows which apps can read it
- [ ] Each item can be deleted individually, and deletion removes it from all apps
- [ ] The view works with screen readers, voice control and keyboard alone
- [ ] Docs updated

**Labels:** `profile`, `gap`, `effort: TBC`, `community-session`
**Status:** Draft, awaiting participant check-back

---

## [Profile] Let each person choose how automatic changes should be

**What people told us**
Participants in community session 1 disagreed about whether changes should happen automatically. P5 wanted to be asked the first time, then have it happen automatically. P1 wanted changes to be automatic but announced. Another participant wanted to be asked every time, after past experiences with tools that changed things uninvited.
Heard from 3 of 5 participants.

**The need**
People differ in how much control they want over each change, and one default will not suit everyone.

**Proposed change**
Store a per-person preference in the profile: always ask, ask once then apply, or apply automatically with notice.

**Done when**
- [ ] The three options can be set in the profile
- [ ] Adapters respect the setting
- [ ] The default is "always ask" until the person chooses otherwise
- [ ] Docs updated

**Labels:** `profile`, `adapter`, `idea`, `effort: TBC`, `community-session`
**Status:** Draft, awaiting participant check-back

---

## [Docs] Explain simply where the profile is kept, before asking for consent

**What people told us**
Participants in community session 1 said they would need a simple explanation of where their profile is kept before agreeing. P5: "I'd need someone to explain that to me simply before I said yes." P1 wanted to be able to take the profile with them.
Heard from 2 of 5 participants.

**The need**
People need to understand where their information lives in order to give real consent.

**Proposed change**
A short plain-language explainer, shown before consent, covering where the profile is kept, who can see it, and how to take it elsewhere or delete it.

**Done when**
- [ ] Explainer is under 150 words and written in plain language
- [ ] It is shown before any consent request in the sample onboarding service
- [ ] Available as text and readable by screen reader
- [ ] Reviewed by at least one participant

**Labels:** `docs`, `profile`, `gap`, `effort: small`, `community-session`
**Status:** Draft, awaiting participant check-back

---

## Review list for the community manager

- **Held pending private confirmation:** F-04 (separate work and home profiles, from P3's private message). Confirm with P3 before drafting.
- **Consent check:** P2 and P3 agreed to paraphrase only. Their points appear above as paraphrase only, including P2's line about enlarging text on every site, which is not quoted anywhere.
- **Session, not toolkit:** F-16 (captions lagging behind the demo) belongs in the session kit's notes. Suggest adding "test caption sync before demos" to `01-plan-and-recruit.md`.
- **Inference to check:** the storage explainer issue assumes the sample onboarding service is where consent is asked; confirm with the Core Contributor.
