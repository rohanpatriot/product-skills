# Build a Story Map

This workflow guides you through building a story map from scratch using Jeff Patton's methodology. A story map is not a documentation exercise — it is a shared understanding tool. Build it with people in the room, not before they arrive.

The map has a simple structure: activities across the top (the backbone), tasks beneath each activity arranged left-to-right by sequence, and stories beneath each task arranged top-to-bottom by priority.

---

## Before You Start

**Who should be in the room:**
- The person who knows the users best (researcher, PM, designer)
- Someone who will build what you map (engineer or tech lead)
- At minimum 2 people — mapping alone produces a weaker map and no shared understanding

**What you need:**
- Sticky notes or a digital whiteboard (Miro, FigJam, MURAL)
- Three colors: one for activities, one for tasks, one for stories
- 60–90 minutes for an initial backbone pass
- A blank horizontal surface with room to spread left-to-right

**What you are NOT doing:**
- Writing requirements
- Building a backlog
- Defining acceptance criteria (that comes later)
- Estimating anything

---

## Step 1: Identify the User

Before you write a single sticky note, you must know who you are mapping for.

Story maps describe the experience of a specific user doing a specific thing. If you start mapping without naming the user, you will produce a map that describes the system, not the user. That is the most common mistake.

**AskUserQuestion:** "Who is the primary user this map is for? Describe them in one or two sentences — their role, their context, and what they care about."

**What a good answer looks like:**
> "A freelance graphic designer who bills clients by the hour. She uses our tool to log time against projects and send invoices at the end of each month."

**What a weak answer looks like:**
> "Our users." (Too broad — you will map for no one.)
> "Admins and end users." (Two users — map them separately.)

**If the user names multiple user types:**
Pick one to start. Map one user type at a time. If you map "admins AND end users" simultaneously, you will conflate their journeys and your backbone will be incoherent. Finish one map, then build a second for the other user type, or clearly separate their lanes.

**Output of this step:** A one-sentence user description written at the top of your map. Keep it visible throughout the session.

Example header:
> **User:** Freelance graphic designer who logs time and invoices clients monthly.

---

## Step 2: Frame the Goal

Every story map tells a story about a user accomplishing a goal. Before mapping the steps, name the goal.

The goal is not a feature. The goal is not "use our product." The goal is what the user is trying to accomplish in their life or work — the outcome they are seeking.

**AskUserQuestion:** "What is this user trying to accomplish? Finish this sentence: 'At the end of this journey, the user has successfully ___.' State it in terms of their outcome, not your product."

**Good goal statements:**
> "The user has been paid for the work they did this month."
> "The user has found and booked a flight that fits their schedule and budget."
> "The user has onboarded their first paying customer."

**Weak goal statements:**
> "The user has used our invoicing feature." (That's a product action, not a user goal.)
> "The user has completed the workflow." (Too vague — which workflow?)

**Why this matters:**
The goal defines the scope of the map. Activities in the backbone should all contribute to achieving this goal. If an activity does not help the user achieve their goal, it does not belong on this map.

Write the goal at the top of your map, next to the user description. It is your north star for every decision you make during mapping.

**Output of this step:**
> **User:** Freelance graphic designer
> **Goal:** Has been paid for the work she did this month.

---

## Step 3: Map Activities Across the Top (The Backbone)

Activities are the top level of the map. They are the high-level things your user does to accomplish their goal — chunked at a meaningful level of abstraction. Activities go left-to-right in the order the user actually does them.

The backbone is the spine of your map. Everything else hangs off it.

**AskUserQuestion:** "Walk me through what this user does, from the moment they start until they achieve their goal. What are the major phases or stages of their journey? Don't go into detail yet — just name the big chunks."

**How to identify activities:**
- Think in phases, not steps. "Track time" is an activity. "Click the start button" is too granular.
- Use verb + noun format: "Find a flight," "Book accommodation," "Log time," "Send invoice."
- Activities should feel roughly equivalent in scope. If one is vastly larger than the others, it probably needs to be split.
- Aim for 4–8 activities to start. Fewer than 4 suggests you are mapping a single activity, not a full journey. More than 12 suggests your activities are too granular or your goal is too broad.

**Example backbone for a time tracking and invoicing user:**
```
[ Log Time ] → [ Review Logged Time ] → [ Create Invoice ] → [ Send Invoice ] → [ Track Payment ]
```

**Example backbone for a traveler booking a flight:**
```
[ Plan Trip ] → [ Search Flights ] → [ Select Flight ] → [ Book Flight ] → [ Prepare for Travel ]
```

**Common mistakes at this step:**
- Writing tasks as activities. "Click 'New Entry'" is a task, not an activity. Activities are bigger.
- Jumping straight to "how the system works" instead of "what the user does." Map the user, not the UI.
- Including activities that happen before the user journey starts or after the goal is achieved. Scope your backbone to the goal you defined in Step 2.

**How to sequence activities:**
Read your backbone left-to-right like a sentence. "First the user does X, then Y, then Z." If that narrative makes sense, your sequence is right. If you find yourself saying "well, sometimes they do Y before X," that is a signal — note it, but keep the most common path as your baseline.

**Output of this step:** 4–8 activity cards across the top of your map, in left-to-right user-time order.

---

## Step 4: Break Activities Into Tasks

Tasks are the steps within each activity. They are more specific than activities but still describe what the user does — not what the system does.

Work through each activity from left to right. For each activity, ask: "What does the user actually do when they are doing this activity?"

**AskUserQuestion:** "Let's take your first activity: [Activity Name]. What specific steps or actions does the user take when doing this? Don't worry about priority or completeness yet — just brainstorm."

**Task format:**
Tasks use the same verb + noun format as activities, but at a finer grain.

For the activity "Log Time":
```
- Start a timer
- Name the time entry
- Tag the project
- Add a description
- Stop the timer
- Manually add an entry
- Edit a logged entry
- Delete an entry
```

For the activity "Send Invoice":
```
- Preview the invoice
- Adjust line items
- Add payment terms
- Send via email
- Copy a shareable link
```

**How detailed should tasks be?**
Tasks should describe discrete actions the user takes. A good test: could you build a UI flow around each task? If a task is too vague to imagine a UI for, it is still an activity. If a task describes a single button click, it is probably too granular — combine it with adjacent steps.

**Timebox this step:** Spend no more than 10 minutes per activity. You will refine later. The goal is coverage, not completeness.

**Output of this step:** 4–8 task cards beneath each activity, written on a different color from activities.

---

## Step 5: Arrange Tasks Left-to-Right Within Each Activity

Within each activity, tasks should be arranged in the sequence a user typically performs them. This is a light sort — don't over-engineer it.

**AskUserQuestion:** "Looking at the tasks under [Activity Name] — is there a natural order in which users typically do these? What comes first?"

**Sequencing rules:**
- Left is earlier in the user's flow, right is later.
- If tasks can happen in any order, place the most common or critical path first.
- If a task is optional or rare, move it to the right. Rare tasks will typically fall below the release line later.

**Why sequencing tasks matters:**
When you draw release slices later, the left-to-right order of tasks within an activity helps you identify the minimum viable path. The first task in each activity is usually the one that must be in Release 1.

**Common mistakes:**
- Arranging tasks by how you build them (backend first, frontend second). Arrange by how the user experiences them.
- Over-sorting: if two tasks are genuinely parallel, don't force an order. Leave them side by side.

**Output of this step:** Tasks within each activity arranged in rough user-time order, left-to-right.

---

## Step 6: Review and Refine the Backbone

With tasks filled in, step back and look at your backbone again. Now that you can see what lives beneath each activity, the backbone often needs adjustment.

**AskUserQuestion:** "Now that we can see the tasks, does the backbone still make sense? Are any activities too broad? Too narrow? Missing?"

**What to look for:**

**Activities that are too broad:** If one activity has 15+ tasks beneath it and others have 3–4, the large one probably contains 2–3 distinct activities. Split it.
- "Manage Account" with 20 tasks → Split into "Set Up Profile," "Configure Billing," "Manage Team"

**Activities that are too narrow:** If two adjacent activities each have only 2–3 tasks and are hard to distinguish from each other, merge them.
- "Start Timer" and "Stop Timer" → Merge into "Track Time"

**Missing activities:** Walk the map left-to-right and ask: "Is there anything a user has to do between [Activity A] and [Activity B] that we haven't captured?" Common omissions: onboarding, authentication, notification/confirmation steps, error recovery.

**Sequence mistakes:** Does the left-to-right order still reflect how users actually move through the journey? Correct sequence errors now — they will confuse everyone during release planning.

**Output of this step:** A refined backbone with activities at consistent levels of abstraction, in correct sequence.

---

## Step 7: Sanity Check — Can a User Accomplish Their Goal With Just the Backbone?

This is the most important check before you move to story generation or release planning.

Read your backbone activities left-to-right. Imagine a user doing only the first task under each activity — the simplest possible version of each step. Can they achieve the goal you named in Step 2?

**AskUserQuestion:** "If we built the bare minimum version of every activity on the backbone — just enough to do each step — could a user [state the goal]? What is missing or broken in that narrative?"

**What you are looking for:**
- Gaps where the user cannot progress without a task you haven't mapped yet
- Activities that are prerequisites but haven't been included
- Dead ends where the user's journey breaks

**This is the walking skeleton test:**
The walking skeleton is the thinnest slice that lets a user go end-to-end. If your backbone cannot support even a skeletal walk-through, you have gaps to fill before you can plan a Release 1.

**What to do if the sanity check fails:**
- Add the missing activity or task to the backbone
- Revisit whether the goal is scoped correctly (maybe the goal is too ambitious for this map)
- Check whether you are missing a user type whose actions enable this user's goal (e.g., an admin must set something up before an end user can proceed)

**Output of this step:** Confidence that the backbone tells a complete enough story for a user to accomplish their goal — even if only barely.

---

## After the Map Is Built

Once you have a backbone with tasks, you are ready to move to the next phase. Depending on your team's needs:

- **Generate stories** → Go to [generate-stories.md](./generate-stories.md)
- **Slice releases** → Go to [slice-releases.md](./slice-releases.md)
- **Facilitate with stakeholders** → Go to [facilitate-planning.md](./facilitate-planning.md)

**What to do with the physical map:**
If you built on sticky notes, photograph it immediately. Label each activity and its tasks. If you built digitally, export a snapshot and share it with everyone who was in the room. The map is a shared artifact — it belongs to the whole team, not to the person who facilitated.

**The map is never done:**
Expect to revise the map after every significant discovery. A good map reflects current understanding, not final truth. When your understanding of users changes, update the map.

---

## Quick Reference: Patton's Vocabulary

| Term | Definition | Example |
|------|-----------|---------|
| Activity | High-level user goal-stage | "Send Invoice" |
| Task | Step within an activity | "Preview invoice before sending" |
| Story | Specific way to accomplish a task | "As a designer, I can preview my invoice as a PDF" |
| Backbone | Top row: all activities in sequence | The horizontal spine of the map |
| Walking skeleton | Thinnest end-to-end slice | The minimum that proves the journey works |

---

## Common Mistakes Summary

1. **Starting with tasks, not activities.** You skip the backbone and end up with a pile of cards with no narrative structure.
2. **Mapping the system, not the user.** Your backbone says "Database writes record" instead of "User saves entry."
3. **Mapping multiple user types simultaneously.** The map becomes incoherent because different users have different goals.
4. **Treating the map as done after Step 1.** The backbone is a starting point, not a deliverable.
5. **Over-detailing too early.** Spend 60 minutes on the backbone before going deep on any activity.
