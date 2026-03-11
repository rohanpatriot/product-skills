# Slice Releases From a Story Map

This workflow guides you through slicing your story map into releases. Slicing is the practice of drawing horizontal lines across the map — each line separates one release from the next. Everything above the first line is Release 1. Everything between the first and second lines is Release 2. And so on.

The most important release is Release 1: the walking skeleton. This workflow starts there.

You should have a story map with activities, tasks, and stories before starting this workflow. If you don't, go to `workflows/build-map.md` and `workflows/generate-stories.md` first.

---

## What a Slice Is

A release slice is a **horizontal cut** across the entire map. It includes the topmost story (or few stories) from every task column — a thin layer that spans the full width of the map.

**A slice is NOT:**
- A set of features selected from one part of the map
- All the stories from one activity or one task
- A feature-complete implementation of any single area

**A slice IS:**
- A thin layer that covers the entire user journey from left to right
- Enough to let a user accomplish their goal, even if only barely
- The thinnest possible version of every step in the backbone

This is the "mile wide, inch deep" principle in action. You go wide across the entire journey before you go deep on any part of it.

---

## Before You Start

**Who should be in the room for release slicing:**
- Product owner or PM (to make in/out decisions)
- Engineering lead or architect (to validate what is feasible per release)
- Designer (to ensure the user experience is coherent per release)
- A stakeholder with business authority (to validate that each release serves a business need)

**What you need:**
- A story map with at minimum: backbone (activities), tasks, and rough stories
- Sticky notes or tape in a different color to draw release lines
- 60–90 minutes minimum

**The key question for every release:**
> "Can a user accomplish their goal with ONLY what is above this line?"

---

## Step 1: Review the Full Map With Stakeholders

Before drawing any lines, walk stakeholders through the complete map. This is not a presentation — it is a tour. Walk from left to right. Name each activity. Name the tasks beneath it. Let stakeholders ask questions.

**AskUserQuestion:** "Have all stakeholders seen the full story map? If not, walk them through it now before drawing any release lines. What questions or concerns come up as you walk through the backbone?"

**What to listen for during the walk-through:**
- Activities or tasks that are missing from the map
- Stakeholders who see something unexpected (that means an assumption needs to surface)
- Disagreements about what belongs in the backbone vs. what is optional
- Stakeholders who point to a card and say "that's the most important thing" — note those

**Correct the map before slicing:**
If stakeholders identify missing activities or tasks, add them now. Slicing a wrong map produces wrong release plans. The review step is not optional.

**Output of this step:** A map that all stakeholders have seen and agree is structurally correct. Gaps and disagreements are surfaced before release lines are drawn.

---

## Step 2: Draw the Walking Skeleton Line (Release 1)

The walking skeleton is the thinnest end-to-end slice through the entire system. It is the topmost story from each task — or in some cases, only the essential tasks from each activity.

**AskUserQuestion:** "Looking at your map — what is the absolute minimum set of stories, spanning the full backbone from left to right, that would let a user [state the goal]? What must be true for a user to go end-to-end, even if the experience is rough?"

**How to identify the walking skeleton:**

Work left-to-right across the backbone. For each activity, ask:
- What is the one task a user absolutely must be able to do in this activity?
- What is the thinnest possible version of that task?

The answers form your walking skeleton.

**Walking skeleton example — time tracking and invoicing app:**
```
Activity: Log Time
→ Walking skeleton story: "As a designer, I can manually add a time entry with a project name and duration"

Activity: Review Logged Time
→ Walking skeleton story: "As a designer, I can view a list of my time entries for the current month"

Activity: Create Invoice
→ Walking skeleton story: "As a designer, I can create an invoice that pulls in my logged time entries"

Activity: Send Invoice
→ Walking skeleton story: "As a designer, I can send my invoice to a client email address"

Activity: Track Payment
→ Walking skeleton story: "As a designer, I can manually mark an invoice as paid"
```

**Draw the line:**
Place a horizontal line (tape, a bold card, or a digital boundary) across the entire map, just below the stories you've identified as the walking skeleton. Everything above this line is Release 1.

**What the walking skeleton is NOT:**
- A polished, production-ready release
- A feature-complete version of any single activity
- The "nice to have" version of anything
- A release with all error states handled

**What it IS:**
- End-to-end functional
- Enough for a real user to accomplish their goal, even if inelegantly
- The minimal proof that the full user journey is possible

**Output of this step:** A release line drawn across the entire map. Everything above the line is the walking skeleton — Release 1.

---

## Step 3: Validate Release 1 — Can a User Accomplish Their Goal With ONLY What Is Above This Line?

This is the most critical question in the workflow. Walk through the walking skeleton end-to-end. Narrate it aloud: "A user opens the app, they do [activity 1 top story], then [activity 2 top story], then..."

**AskUserQuestion:** "Walk me through the user journey using ONLY the stories above the Release 1 line. At each step, ask: can the user actually proceed? Is there anything missing that would block them? Does the story at the end of this walk let them achieve [the goal]?"

**Signs the walking skeleton is missing something:**
- You cannot narrate the journey without referencing a story below the line
- There is a step where the user would be stuck (missing data, missing UI, missing action)
- The user cannot complete the final activity (they cannot achieve the goal)
- The walking skeleton assumes backend infrastructure that isn't in the line

**Signs the walking skeleton is too thick:**
- Multiple stories per task are above the line in the same activity
- You included error states, advanced variations, or edge cases above the line
- Release 1 feels like "the full product, just done quickly"

**If the walking skeleton fails validation:**
- Add the minimum missing story to Release 1
- Remove any story that is not strictly necessary for end-to-end function
- Re-narrate until the user journey is coherent end-to-end

**Output of this step:** Confidence that Release 1 — and only Release 1 — lets a user accomplish the stated goal.

---

## Step 4: Define Release 2 and Beyond

Release 2 adds depth, not new journeys. It takes the thin walking skeleton and makes it better — adding the next most important stories beneath each task.

**AskUserQuestion:** "With Release 1 scoped, what should come next? For each activity in the backbone — what stories immediately below the Release 1 line are most important for making the experience meaningfully better for real users?"

**How to scope Release 2:**

Work through the map activity by activity. For each activity:
- Look at the stories below the Release 1 line
- Ask: "Which stories here would make the biggest difference to actual users?"
- Pull those stories into Release 2

**Release 2 is NOT:**
- Everything that didn't make Release 1
- A second feature set (a new journey)
- The "nice to have" release

**Release 2 IS:**
- Meaningful depth added to the existing journey
- Stories that improve the quality, reliability, or completeness of what Release 1 established
- Something that delivers meaningfully more value than Release 1 on its own

**Avoid the "feature addition" trap:**
Teams often treat Release 2 as "the features we didn't have time to do in Release 1." That is not a release strategy — that is a backlog. Release 2 should be driven by what users need most after experiencing Release 1, not by what was left over.

**Draw the Release 2 line:**
Place a second horizontal line across the map, below the first. Everything between line 1 and line 2 is Release 2.

**How many releases should the map have?**
See `references/slicing-principles.md`. In general: 3–5 release slices for a map that covers a significant product area. Fewer than 3 suggests you are not thinking far enough ahead. More than 6 suggests your releases are too thin or your map is too large.

**Output of this step:** A Release 2 line drawn on the map, with stories between the two lines representing the next meaningful increment of value.

---

## Step 5: Validate Each Release — Does It Deliver Meaningful Value on Its Own?

Each release must stand on its own. Ask this question for every release you've drawn:

> "If we shipped only this release and then stopped — would users be better off than before? Would this release accomplish something meaningful for them?"

**AskUserQuestion:** "For each release on the map — if this were the last release you shipped, would it be worth having shipped at all? Does it deliver something real to users, or is it just scaffolding for the next release?"

**Validation questions per release:**

*Release 1 (Walking Skeleton):*
- Can a user accomplish the stated goal?
- Is it usable, even if rough?
- Would a real user be willing to try this to accomplish something they care about?

*Release 2+:*
- Does this release make the product meaningfully better, not just marginally better?
- Could a user who has never seen Release 1 use this release and achieve the goal?
- Would you be comfortable showing this to a real customer?

**Red flags:**
- A release that only completes something started in a previous release (Release 2 completes a feature started in Release 1 — that means Release 1 was too thin)
- A release where the only thing delivered is backend infrastructure (no user-visible value)
- A release that only serves internal users or ops teams (valuable, but not a user-facing release — it may need a separate track)

**Output of this step:** Each release validated as independently meaningful. Release lines adjusted if any release fails validation.

---

## Step 6: Name Each Release by the Outcome It Enables

Release names should describe what users can do — not what features are in the release.

**AskUserQuestion:** "What would you call each release? Try to name it by the outcome it enables for users, not the features it contains. Finish this sentence for each release: 'After this release, users can finally ___.' That sentence is your release name."

**Good release names:**
- "Send your first invoice" (not "Invoice creation v1")
- "Get paid end-to-end" (not "Payment tracking + invoice status")
- "Manage your team's time" (not "Multi-user support")

**Weak release names:**
- "Phase 1" — describes sequence, not value
- "MVP" — describes development stage, not user outcome
- "Core features" — describes product completeness, not user capability

**Why naming matters:**
Release names are communication tools. When a stakeholder asks "what are we building next?", the answer "Send your first invoice" is more compelling and more clarifying than "Invoice creation module." Names that describe outcomes create alignment around value, not features.

**Output of this step:** Each release labeled with an outcome-focused name on the map.

---

## Common Slicing Mistakes

**Mistake 1: Drawing the walking skeleton line vertically instead of horizontally.**
A vertical slice selects all stories from one or two activities. That is not a release — it is a feature silo. Users cannot accomplish their goal with only one activity's features. Slices must be horizontal.

**Mistake 2: Putting everything in Release 1.**
If your Release 1 line is at the bottom of the map, you haven't sliced — you've just labeled the whole map "Release 1." This happens when stakeholders resist trade-offs. The fix: ask, "What is the thinnest version of this that a user would actually use?" and draw the line there.

**Mistake 3: Treating the walking skeleton as the "rough" version of every feature.**
The walking skeleton is not a rough version of anything — it is the minimum set of stories that spans the full journey. Rough versions of every feature is a thick Release 1 in disguise.

**Mistake 4: Skipping validation.**
Drawing lines without narrating the journey produces releases that look good on paper but break in practice. Always walk through each release aloud.

**Mistake 5: Naming releases by sprint number or quarter.**
"Q2 Release" tells no one what value is being delivered. Name releases by outcome.

**Mistake 6: Backend stories that aren't stories.**
Infrastructure work — API setup, database schema, third-party integrations — often gets stuffed into Release 1 as "stories." These are tasks, not user stories. They have no user-visible outcome. Track them separately from the user story map, or represent them as dependencies on real stories.

---

## Validation Checklist

Before finalizing release slices, run through this checklist:

**Walking Skeleton (Release 1):**
- [ ] Covers the full backbone from left to right
- [ ] A user can accomplish the stated goal using only Release 1 stories
- [ ] No stories below the line are needed to make Release 1 functional
- [ ] No advanced features, edge cases, or polish above the line that can wait

**All Releases:**
- [ ] Each release is named by user outcome, not features
- [ ] Each release adds depth to the existing journey (not a new, unrelated journey)
- [ ] Each release delivers independently meaningful value
- [ ] Dependencies between stories are respected across release lines
- [ ] Engineering has validated that each release is scoped feasibly
