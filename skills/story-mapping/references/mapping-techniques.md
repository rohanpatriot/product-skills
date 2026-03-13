# Mapping Techniques

Practical techniques for running effective story mapping sessions. This reference covers facilitation mechanics, tool choices, session structure, and judgment calls that come up repeatedly in real mapping sessions.

---

## How to Run a Mapping Session: Facilitation Steps

Story mapping sessions follow a consistent arc, regardless of how much time you have.

### The Arc

1. **Frame** (5–10 minutes): State the user, the goal, and the structure of the map. Do a quick example with an unrelated domain so participants understand the three levels before they start writing.

2. **Generate backbone** (15–20 minutes): Everyone writes activities independently on sticky notes. Bring them to the board. Cluster and sequence. Read aloud. Correct.

3. **Generate tasks** (20–40 minutes): Work through each activity one at a time. Generate tasks beneath each one. Use the same independent-then-cluster technique.

4. **Story-storm key tasks** (20–40 minutes): Pick the most critical tasks — usually the first task under the first few activities — and generate stories beneath them. Do not story-storm every task in one session.

5. **Slice releases** (20–30 minutes): With backbone and tasks visible, draw release lines. Use the walking skeleton test for Release 1. Validate each release by narrating the journey.

6. **Capture and close** (15–20 minutes): Photograph the map. Record decisions. Assign owners for next steps. Identify open questions.

### Timing Guidelines

- Do not skip the framing. Five minutes of framing saves 30 minutes of confusion.
- Do not start release slicing until the backbone AND tasks are on the board. Release slicing without tasks produces vague arguments.
- Do not let story-storming expand to cover every task in the first session. Go deep on the most critical, shallow on the rest.

### The Facilitator's Job

The facilitator is not the expert on the map. The facilitator creates the conditions for the group to build shared understanding together.

Facilitation behaviors that work:
- Ask more than you tell
- Name disagreements explicitly instead of resolving them by authority
- Give people time to write before asking them to speak (independent generation → group discussion)
- Read the map back to the group regularly — "here's what I'm hearing"
- Keep the session moving — timeboxes, parking lots, and explicit deferrals keep pace up

Facilitation behaviors that don't work:
- Building the map before the session and presenting it
- Letting one person dominate the sticky note placement
- Resolving disagreements by saying "let's table that for later" without a plan to return
- Treating the map as a document to be correct rather than a conversation to be had

---

## Remote vs. In-Person: Tools and Trade-offs

### Remote Mapping Tools

**Miro** is the most widely used tool for remote story mapping. Its advantages:
- Infinite canvas expands left-to-right naturally
- Sticky notes are fast to create, move, and color
- Voting features work well for "must have / can wait" exercises
- Frames can be used to separate map sections
- Templates exist specifically for story mapping

**FigJam** is lightweight and visually clean. Better for smaller maps or teams that already live in Figma. Less powerful voting/facilitation features than Miro.

**MURAL** is similar to Miro in capability, with slightly better facilitation templates. Either works.

**What remote tools cannot replace:**
- The peripheral awareness of an in-person map (you see the whole thing at once, not just your viewport)
- The physical act of walking up to the wall and placing a card (which creates ownership)
- Side conversations between participants while the map is being built

### In-Person Mapping: Sticky Notes and Walls

**The case for physical:**
Nothing beats a wall covered in sticky notes for a team in the same room. The whole map is visible at once. People walk up to it. They point. They rearrange. The tactile, physical engagement produces a different kind of conversation than digital tools.

**Sticky note conventions:**
- Use three distinct colors: one for activities, one for tasks, one for stories
- Write one item per sticky note
- Write large — Sharpie, not ballpoint. Cards need to be readable from 6 feet away
- Use a consistent verb + noun format

**Wall surface options (in order of preference):**
1. Whiteboard — easy to annotate, easy to photograph
2. Painted wall — stickies adhere well, requires tape to mark release lines
3. Butcher paper on a table — works but loses the vertical dimension
4. Glass — stickies adhere well but glare can make photography difficult

### Digital After Physical

If you run a physical session, digitize the map immediately afterward. The photograph captures the artifact; a digital tool captures the ability to update it.

Recommended workflow:
1. Photograph the physical map before leaving the room
2. Recreate in Miro or FigJam within 24 hours
3. Share the digital version with all participants for corrections
4. Use the digital version for all future sessions

---

## Handling Disagreement During Mapping

Disagreement during mapping is a feature, not a bug. The map surfaces disagreements that would otherwise emerge later — in a sprint, during a design review, or after shipping.

### Types of Disagreement

**Scope disagreement:** "Should [activity] be on this map at all?"
Handle by returning to the user and goal. Does this activity help the user accomplish the stated goal? If yes, it belongs. If not, it does not.

**Abstraction disagreement:** "Is this an activity or a task?"
Handle pragmatically. Put it in the position that makes the backbone read coherently. Abstraction debates are usually resolvable by reading the backbone aloud and asking "does this level feel right?"

**Prioritization disagreement:** "This must be in Release 1." "No, it can wait."
This is the most valuable disagreement. Do not suppress it. Ask both parties to describe the user they are imagining. Often they are imagining different users, or different moments in the user's journey, and both are correct. The disagreement reveals a need to either split the map (different users) or clarify the goal (scoping question).

**Feasibility disagreement:** "We can't build this in Release 1." "We have to."
This disagreement belongs in the session, not after it. Ask engineering to articulate what they can build in the timeframe, then ask if there is a thinner version of the story that achieves the same user outcome. Usually there is.

### Techniques for Productive Disagreement

**"Two-column test":** When two parties disagree on what Release 1 contains, write both versions side by side and narrate each one. Often the act of narrating makes one clearly superior.

**"User test":** When parties disagree on whether a story is necessary, ask: "If we shipped without this, what would a user do?" If the answer is "they'd be stuck" or "they'd give up," it is essential. If the answer is "they'd work around it," it can wait.

**"Parking lot":** When a disagreement cannot be resolved in the session, name it explicitly, put it on a parking lot sticky, assign an owner, and move on. Do not let unresolvable debates stop the session.

---

## When the Map Gets Too Big

Maps grow. A map that starts with 6 activities can expand to 12 as tasks are added and activities are split. Large maps are hard to work with.

### Signs the Map Is Too Big

- The backbone no longer fits on one wall or one screen
- Activities are at radically different levels of abstraction
- Tasks have become activities and no one has renamed them
- The map covers more than one distinct user type
- The map spans more than one distinct user goal

### Fixes

**Split by user type:** If your map contains activities for two distinct user types (e.g., "Admin sets up account" and "End user logs in"), split them into two separate maps. Each map should have one user type and one goal.

**Raise the level of the backbone:** If your backbone has 12 activities, some of them are probably too granular. Merge adjacent activities that represent the same phase of the user journey. The backbone should have 4–8 activities. More than 8 usually means the backbone is at the task level.

**Split by user goal:** If the map covers two distinct goals ("Get paid for work this month" and "Manage ongoing client relationships"), split into two maps. Each map should cover one goal.

**Collapse the body:** If the map is large because the story body is deep (dozens of stories per task), that is fine — do not collapse stories just because the map is large. But do archive stories that are clearly far-future and not relevant to the current planning cycle.

---

## Splitting Activities That Are Too Broad

An activity is too broad if:
- It has more than 10–12 tasks beneath it
- The tasks beneath it seem to belong to different phases of the user's journey
- Stakeholders cannot agree on what belongs in it

**How to split:**
1. List all tasks beneath the activity
2. Ask: "Do these tasks fall into two or three natural sub-phases?"
3. Name those sub-phases and promote them to activities
4. Distribute the tasks to the appropriate new activities

**Example:**
"Manage Account" (too broad, 15 tasks beneath it) →
- "Set Up Profile" (tasks: add name, upload photo, set timezone, connect integrations)
- "Configure Billing" (tasks: add payment method, set invoice settings, manage subscription)
- "Manage Team" (tasks: invite team member, set permissions, remove member)

---

## Merging Activities That Are Too Granular

An activity is too granular if:
- It has only 1–2 tasks beneath it and they are very simple
- It is hard to distinguish from an adjacent activity
- It sounds like a task, not a phase

**How to merge:**
1. Read the two candidate activities aloud: "First the user does [A], then the user does [B]."
2. Ask: "Do these feel like two phases of the journey, or one phase described in two steps?"
3. If they are one phase, pick the better name and merge the tasks underneath it.

**Example:**
"Start Timer" and "Stop Timer" (too granular, each has 2 tasks) →
"Track Time" (tasks: start timer, name entry, tag project, stop timer, manually add entry)

---

## How to Know When the Backbone Is Complete

The backbone is complete when:

1. **You can narrate it.** Read the activities left-to-right. Does it tell a complete story of the user accomplishing their goal? No gaps, no missing phases?

2. **Every activity contributes to the goal.** Remove each activity and ask: "Can the user still accomplish the goal?" If yes, it may not belong on the backbone. If no, it is essential.

3. **No task is hiding an activity.** Look at the tasks beneath each activity. If any task feels as large or important as the activity itself, it might be a hidden activity that needs to be promoted.

4. **The walking skeleton is coherent.** Take the first task from each activity and narrate the walking skeleton. Can the user go end-to-end? If yes, the backbone is complete enough to build from.

---

## Color Coding Conventions

Consistent color coding is essential for making maps readable at a glance. There is no universal standard, but the following conventions are common:

| Color | Usage |
|---|---|
| Yellow | Activities (backbone) |
| Blue | Tasks |
| Green | Stories |
| Orange or Red | Blocked stories, dependencies, or critical risks |
| Pink | Questions or open items |
| Purple | Stories for a second user type |

**In remote tools:**
Miro and FigJam allow you to set sticky note colors per level. Set them at the start of the session so everyone uses the same colors automatically.

**Multi-user-type maps:**
If you must show two user types on the same map, use a second story color (e.g., green for primary user, purple for secondary user). This is a signal the map is getting complex — consider whether a separate map would be clearer.

---

## How Long Sessions Should Run

| Goal | Recommended Duration |
|---|---|
| Backbone only | 60 minutes |
| Backbone + tasks for all activities | 90–120 minutes |
| Backbone + tasks + stories for top activities | 2.5–3 hours |
| Full map + release slicing | 4–5 hours (half day with breaks) |
| Remote sessions | Add 20–30% to in-person estimates |

**Do not run more than 90 minutes without a 10-minute break.** After 90 minutes, contribution quality drops sharply.

**Timeboxing individual activities:**
- Backbone generation: 15 minutes
- Task generation per activity: 8–10 minutes
- Story-storming per task: 10 minutes
- Release slicing: 30 minutes

---

## Who Should Be in the Room

**Core team (always):**
- Product owner or PM — decision-making authority
- One engineer — feasibility and technical reality
- Designer (if the product has a UI being designed)

**Value-adds (invite when possible):**
- A real customer or user — the most powerful input
- A researcher who has spoken with users recently
- A customer-facing team member (support, sales, success) who can represent user behavior patterns

**Do not invite:**
- More than 8–10 people total
- Passive observers — everyone in the room should participate
- People who will veto decisions without contributing to the map
- Multiple levels of management from the same org — the hierarchy dynamics suppress honest contribution

**The "right size" test:** Can everyone in the room see the map clearly and reach the wall to place a sticky note? If not, the group is too large.
