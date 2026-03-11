# Generate User Stories From a Map

This workflow guides you through generating user stories from a completed story map. Stories live at the bottom level of the map — beneath activities (backbone) and tasks. They describe specific ways a user might accomplish a task, and they vary by user need, context, or capability.

You should have a backbone with tasks before starting this workflow. If you don't, go to [build-map.md](build-map.md) first.

---

## What a Story Is (and Is Not)

In Patton's framing, a **user story** is not a requirement. It is a placeholder for a conversation. Stories are written to create dialogue about what to build — not to specify what to build.

A story has three parts:
1. **A card** — the written story, usually in the format: *As a [user], I can [action] so that [outcome].*
2. **A conversation** — the discussion that happens when the team works on the story.
3. **Confirmation** — the acceptance criteria that confirm the story is done.

Stories beneath a task represent **variations**: different ways the user might accomplish that task, for different users, contexts, or situations. The most essential variation goes on top. Rare, edge-case, or advanced variations go lower.

---

## Before You Start

**What you need:**
- A story map with backbone (activities) and tasks filled in
- At minimum: the PM or product owner + one engineer
- Optionally: a designer, a researcher, or a customer

**What you are NOT doing in this workflow:**
- Estimating stories
- Assigning stories to sprints
- Writing exhaustive requirements
- Making final prioritization decisions (you will arrange by rough priority, but formal decisions come during release slicing)

---

## Step 1: Pick a Task to Story-Storm

Story-storming is Patton's term for generating all the possible stories for a given task. You do not story-storm every task at once — that produces an overwhelming map. Pick a task, story-storm it, then move on.

**AskUserQuestion:** "Which task do you want to story-storm first? I recommend starting with the most critical task in your first activity — the one that is definitely in Release 1. Which task is that?"

**How to choose which task to story-storm:**
- Start with tasks that are in or near Release 1 — you need the stories to plan delivery.
- Avoid story-storming tasks that are clearly far-future. Generate those stories when they become relevant.
- If you are unsure, story-storm the tasks on the left side of the backbone first (they come earlier in the user journey and are usually higher priority).

**Output of this step:** One specific task selected for story-storming.

---

## Step 2: Brainstorm All Possible Stories for That Task

This is the generative phase. Do not filter. Write a card for every variation you can think of.

**AskUserQuestion:** "For the task '[Task Name]' — what are all the different ways a user might do this? Think about: different user types, different situations, edge cases, error states, power user variations, accessibility needs, and minimum viable versions."

**Prompts to drive story generation:**

*Who might need to do this differently?*
- A first-time user vs. a power user
- A mobile user vs. a desktop user
- An admin vs. an end user
- A user with accessibility needs

*What could go wrong?*
- What if the data is missing or invalid?
- What if the user makes a mistake?
- What if the connection drops?

*What are the variations?*
- The simple case (most users, most of the time)
- The complex case (edge cases, unusual inputs)
- The advanced case (power user shortcuts, bulk actions)

*What does the user need to know?*
- Confirmation that something worked
- Feedback that something failed
- Guidance when they are stuck

**Example — Task: "Send Invoice"**

Story-stormed variations:
```
- As a designer, I can send an invoice to a client via email directly from the app
- As a designer, I can copy a shareable payment link and send it myself
- As a designer, I can schedule an invoice to send on a future date
- As a designer, I can send a reminder for an unpaid invoice
- As a designer, I can resend an invoice that was lost or not received
- As a designer, I can see a confirmation that the invoice was delivered
- As a designer, I see a helpful error if my client's email is invalid
- As a designer, I can send the same invoice to multiple contacts at one client
- As a designer, I can preview the email my client will receive before sending
- As a designer, I can include a personalized message with my invoice
- As a designer with slow internet, I can still send an invoice if my connection drops
```

**How many stories per task?**
Typically 5–12. Fewer than 5 usually means you stopped too early. More than 15 suggests you may be conflating multiple tasks or the task is scoped too broadly.

**Output of this step:** A set of story cards for the selected task — quantity doesn't matter yet, coverage does.

---

## Step 3: Arrange Stories Vertically by Priority

Now you sort. Arrange story cards top-to-bottom within the task column. The most essential story — the one without which the task is completely non-functional — goes on top.

**AskUserQuestion:** "Looking at all the stories for '[Task Name]' — which one is absolutely required for a user to accomplish this task at all? That goes on top. Which ones are nice-to-have, edge cases, or advanced features? Those go toward the bottom."

**How to sort:**
- **Top:** The minimum viable story. If this is missing, the task cannot be done at all.
- **Middle:** Important variations that most users will need, but are not strictly required for a first release.
- **Bottom:** Edge cases, power user features, error states, accessibility variations, rarely-used paths.

**Example — "Send Invoice" sorted:**
```
1. (TOP) Send invoice to client via email — ESSENTIAL
2. Preview email before sending — HIGH VALUE
3. Confirmation that invoice was delivered — HIGH VALUE
4. Helpful error if email is invalid — HIGH VALUE
5. Resend a lost invoice — MEDIUM VALUE
6. Include personalized message — MEDIUM VALUE
7. Send to multiple contacts — LOWER VALUE
8. Copy shareable link — LOWER VALUE
9. Schedule invoice for future date — LOW / FUTURE
10. Send reminder for unpaid invoice — LOW / FUTURE (may belong to a different task)
```

**The sorting conversation:**
Sorting stories almost always produces disagreement. That is the point. The disagreement surfaces different assumptions about what users need. Surface and resolve those disagreements now, not during a sprint.

**Output of this step:** Stories arranged top-to-bottom by priority, with the essential story on top.

---

## Step 4: Write Acceptance Criteria for Top Stories

Stories near the top of each column — especially those in Release 1 — need acceptance criteria before they go to an engineer. Stories at the bottom can wait.

**AskUserQuestion:** "For the top story in '[Task Name]' — what does 'done' look like? What must be true for this story to be considered complete? Think about: what the user sees, what the system does, and what edge cases must be handled."

**Acceptance criteria format:**
Use the "Given / When / Then" format or a simple checklist — whichever your team prefers. The goal is shared understanding, not format compliance.

**Given/When/Then format:**
```
Given: [the user's starting state]
When: [the user takes this action]
Then: [the expected outcome]
```

**Example — "As a designer, I can send an invoice to a client via email":**
```
Given: I have created an invoice and added at least one line item
When: I click "Send Invoice" and enter my client's email address
Then: My client receives an email with the invoice attached as a PDF

Given: I enter an email address with an invalid format
When: I click "Send Invoice"
Then: I see an inline error message before the invoice is sent

Given: The invoice sends successfully
When: I return to my invoice list
Then: The invoice status shows "Sent" with the send timestamp
```

**Checklist format (simpler alternative):**
```
- [ ] User can enter a client email address
- [ ] Invoice is sent as a PDF attachment
- [ ] Client email is validated before sending
- [ ] Invoice status updates to "Sent" after successful delivery
- [ ] User sees confirmation message after sending
- [ ] Error state if delivery fails
```

**How many acceptance criteria per story?**
3–6 is typical. Fewer than 3 usually means the story is underdefined. More than 8 usually means the story should be split.

**When to skip acceptance criteria:**
Stories in the bottom half of the column — deep in future releases — do not need acceptance criteria yet. Write them when the story becomes ready to build.

**Output of this step:** Acceptance criteria written for the top 2–3 stories in each task column.

---

## Step 5: Tag Dependencies Between Stories

Some stories cannot be built until another story is done. Surface these dependencies now so they don't create surprises during delivery.

**AskUserQuestion:** "Looking at the stories for '[Task Name]' — are any of these stories dependent on another story being built first? Either within this task or elsewhere on the map?"

**How to identify dependencies:**
- Story B assumes infrastructure or data that Story A creates (e.g., "Send reminder" depends on "Track payment status")
- Story B is a variation of Story A and shares the same UI component (e.g., "Edit invoice" depends on "View invoice")
- Story B requires a backend service that Story A initiates (e.g., "Preview PDF" depends on "Generate PDF")

**How to tag dependencies:**
On a physical map: draw a line or arrow between the two cards.
On a digital map: use a connector tool or add a note on the card: "Depends on: [Story Name]."

**What to do with dependencies:**
Dependencies affect sequencing in your release plan. If Story B depends on Story A, Story A must either be in the same release or an earlier release. Surface these before you draw release lines.

**Common dependency trap:**
Treating everything as dependent on everything else. Be ruthless: if a story can be built independently, it is independent. Over-tagging dependencies creates false constraints.

**Output of this step:** Critical dependencies tagged between stories, surfacing sequencing constraints.

---

## Step 6: Add Context — Who Does This Story Serve and What Is the Outcome

A story without context is just a task in disguise. The best stories include explicit context about the user and the outcome they are seeking.

**AskUserQuestion:** "For each top story in this task — who specifically benefits from this story being built? And what do they accomplish because of it? Is it the same user across all stories, or do some stories serve different user types?"

**Story format with context:**
```
As a [specific user in a specific context],
I can [take this action]
so that [I achieve this outcome].
```

**Good story with context:**
> "As a freelance designer who just completed a project, I can send an invoice directly from the app so that I don't have to switch to email to send it manually."

**Weak story without context:**
> "As a user, I can send an invoice."

**Why context matters:**
Context-free stories hide assumptions. When an engineer builds a context-free story, they fill in the missing context themselves — sometimes incorrectly. Context in the story ensures everyone is building for the same user and the same situation.

**Outcome-focused stories:**
The "so that" clause is the most important part of the story. It states what the user achieves. If you cannot write a meaningful "so that" clause, the story may be technically necessary but not user-valuable — that is a signal to examine whether it belongs in the map at all.

**Output of this step:** Top stories revised to include user context and explicit outcome in the "so that" clause.

---

## Story Template

Use this template when writing stories:

```
Story: As a [user in context], I can [action] so that [outcome].

Acceptance Criteria:
- Given: [starting state]
- When: [user action]
- Then: [expected result]

Dependencies: [list any stories this depends on, or "none"]
Serves: [user type]
Release: [tentative: Release 1 / Release 2 / Future]
```

---

## When to Stop Story-Storming

**Stop story-storming for a task when:**
- You have covered the most common user situations
- You have identified the essential top story
- You have at least rough acceptance criteria for Release 1 stories
- The team agrees they understand the task well enough to build it

**Do not stop story-storming because:**
- You ran out of time (it is better to have fewer tasks fully story-stormed than all tasks superficially covered)
- The stories seem obvious (even obvious stories benefit from written acceptance criteria)

---

## After Stories Are Generated

Once you have stories generated and roughly sorted, you are ready for:

- **Release slicing** → Go to `workflows/slice-releases.md`
- **Facilitation with stakeholders** → Go to `workflows/facilitate-planning.md`

**What to do with the stories:**
Stories do not move into a sprint backlog until a release line has been drawn. The map — not a ticket tracker — is the source of truth until you formally pull stories into delivery. Keeping stories in the map context maintains their narrative structure. Once they are exported to Jira or Linear as isolated tickets, the narrative is lost.

---

## Common Mistakes in Story Generation

1. **Writing acceptance criteria that describe implementation.** "The system queries the database" is not acceptance criteria. "The user sees their invoice status update" is.
2. **Generating stories for every task before refining any.** Go deep on the most important tasks. Wide and shallow story generation produces a large map with no useful detail.
3. **Skipping the "so that" clause.** Stories without outcomes are features in disguise. They invite build-first thinking instead of outcome-first thinking.
4. **Over-splitting stories to make them small.** A story should be small enough to discuss and build in a sprint, but large enough to deliver value. A story that says "Add send button to invoice screen" is too small — it delivers no user value alone.
5. **Treating sorted stories as final priority.** The sort in Step 3 is for organizing the map, not for committing to a roadmap. Formal prioritization happens during release slicing with stakeholders in the room.
