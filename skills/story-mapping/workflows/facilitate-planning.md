# Facilitate a Story Mapping Session

This workflow guides you through facilitating a story mapping session with stakeholders — from pre-session setup through closing decisions. Story mapping sessions are collaboration tools, not presentations. The facilitator's job is to create the conditions for shared understanding, not to present a finished artifact.

The most common mistake facilitators make: building the map before the session and then presenting it. Do not do this. Build the map with stakeholders in the room.

---

## Pre-Session: Preparation

### Materials

**In-person:**
- Sticky notes in at least 3 colors (activity color, task color, story color)
- Markers (Sharpies — ballpoint pens are too small to read from a distance)
- A long horizontal surface: whiteboard, wall, or butcher paper on a table
- Tape or dots to mark release lines
- A camera or phone to photograph the map at the end

**Remote:**
- Miro, FigJam, or MURAL (all work; Miro is the most common)
- Pre-set sticky note colors and a frame large enough to expand horizontally
- A shared timer if you are running timed activities
- Screen sharing with annotation enabled for all participants
- A backup document (Google Doc or Notion) for capturing decisions that don't fit on the map

**Do NOT use:**
- PowerPoint to present the map
- A Jira board as a substitute for a map
- Spreadsheets for story capture during the session (kills the narrative structure)

---

### Room Setup

**In-person:**
- Clear a wall or large whiteboard — at minimum 8 feet wide, ideally 12+ feet
- Label the top left of the space with the user description and goal
- Pre-draw three horizontal zones with tape or a marker: "Backbone (Activities)," "Tasks," "Stories"
- Place stacks of each sticky color at the table — enough that people can grab them without asking

**Remote:**
- Set up the Miro/FigJam board before the session with:
  - A header section: User + Goal
  - A labeled row for Activities (backbone)
  - Blank space below for tasks and stories
  - Color legend in the top corner
- Send the board link in the calendar invite so participants can orient before the session

---

### Who to Invite

**Always invite:**
- The product owner or PM (has product authority)
- At least one engineer (reality check on what is feasible)
- At least one designer (if design exists or is planned)

**Invite when available:**
- A real customer or user (most powerful input you can have)
- A researcher who can speak for users
- A customer-facing team member (support, sales, success)
- A technical stakeholder whose team will be affected by the decisions

**Do NOT invite:**
- Everyone. Large groups make story mapping sessions slow and political.
- People who are there to observe but not participate. Everyone in the room should be expected to contribute.
- More than 8–10 people. If you have more stakeholders than that, run two sessions and reconcile afterward.

---

### Time Estimates

| Session Type | Duration |
|---|---|
| Build backbone only (first map) | 60–90 minutes |
| Build backbone + story-storm one activity | 90–120 minutes |
| Full map: backbone + tasks + stories | 2.5–4 hours (with breaks) |
| Release slicing session (map already built) | 60–90 minutes |
| Full session: build map + slice releases | 4–6 hours (half day) |

**Do not run more than 90 minutes without a break.** Mapping is cognitively demanding. After 90 minutes, contributions decline sharply.

---

### Pre-Session Homework

Send to all participants before the session:

1. **The user description** — one sentence: who are we mapping for?
2. **The goal** — one sentence: what is this user trying to accomplish?
3. **A question to think about:** "What does the user do between [start state] and [achieving the goal]? What are the major phases?"

Do NOT send a pre-built map. If participants see a draft map before the session, they will react to it rather than build from first principles. You lose the shared discovery.

**AskUserQuestion:** "Before you schedule the session — have you defined the user and goal? Can you articulate them in one sentence each? Those two pieces of information should be agreed on before anyone enters the room."

---

## Opening the Session (15–20 minutes)

### Frame the Session

Start by stating:
1. Who you are mapping for (the user)
2. What the user is trying to accomplish (the goal)
3. What you will produce today (a story map — not a spec, not a backlog)
4. How the map will be used (to plan releases, create shared understanding, drive conversation)

**Script:**
> "Today we're building a story map for [user type]. Our goal is to map what [user] does to [achieve their goal]. We're not writing requirements. We're not committing to a roadmap. We're building shared understanding — a map of the user's journey that we'll use to make release decisions together."

### Explain the Backbone (5 minutes)

Before anyone writes a sticky note, explain the three levels of the map:

1. **Activities (top row):** The big chunks of what the user does — "Find a flight," "Book accommodation." These go left-to-right in user-time order. This is the backbone.
2. **Tasks (middle rows):** The steps within each activity — "Search by date," "Filter results." More specific than activities.
3. **Stories (bottom rows):** Specific variations of how a user might do a task — "As a traveler, I can filter by airline." These go top-to-bottom by priority.

**Show a simple example:**
Draw a 3-activity example on the board (not related to your actual project — a familiar example like "Order food online" or "Plan a trip") to illustrate the structure before you start mapping your actual product.

### Set Expectations

> "There are no wrong answers. If you write a task that's too granular, we'll cluster it. If you write an activity that's too broad, we'll split it. Just write what you think and we'll organize it together."

> "We're going to move fast. Don't labor over wording. Use verb + noun: 'Track time,' 'Send invoice,' 'View history.' We can refine later."

---

## Walking Through the Backbone (30–45 minutes)

### Generate Activities (15 minutes)

**Give everyone sticky notes.** Ask participants to independently write activities on sticky notes — one activity per note, verb + noun format. Give them 5 minutes, then bring them to the wall.

**AskUserQuestion:** "Let's start generating activities. Everyone write down what [user] does from the moment they start until they achieve [the goal]. Major phases only — verb and noun, one per sticky. You have 5 minutes."

**Cluster and sequence:**
After the individual generation phase, bring stickies to the board. Group similar ones together. Sequence the groups left-to-right. Read the backbone aloud to the group.

**Expect disagreement here.** Disagreement about what belongs on the backbone is the most valuable conversation you will have in the session. Two people who disagree about whether "Manage Account" is one activity or three are surfacing a real product question.

**Facilitate the disagreement — don't resolve it by authority:**
> "It sounds like there's a question about whether 'Set Up Profile' and 'Manage Settings' are the same thing or different. Let's talk about that — do these feel like the same phase of the user's journey or different phases?"

### Get Stakeholders to Correct and Add

After an initial backbone is on the board, read it aloud end-to-end and ask:
- "Does this feel like the right sequence?"
- "Is anything missing?"
- "Does anything on this board not belong?"

**AskUserQuestion:** "Now that we have a first backbone — read it left to right. Does this tell the full story of what [user] does to [achieve the goal]? What's missing? What's in the wrong place?"

**Common corrections at this stage:**
- An activity that comes before the first one on the board (onboarding, authentication, account setup)
- A step that happens after the last activity (follow-up, confirmation, recurring action)
- Two activities that should be merged (they describe the same phase)
- One activity that should be split (it's actually two distinct phases)

---

## Discussion Zone: In/Out Per Release (30–45 minutes)

Once the backbone is established and tasks are filled in, it is time to discuss what goes in each release.

**Do not start this conversation until tasks are on the board.** Release discussions without tasks degenerate into vague arguments about features. Tasks give the discussion specificity.

### Surface Disagreement

Release discussions surface the most important disagreements in a product team. Your job as facilitator is to make disagreement visible and productive — not to suppress it.

**When two stakeholders disagree:**
1. Name the disagreement explicitly: "I'm hearing two views here — [person A] thinks this must be in Release 1, [person B] thinks it can wait. Let's understand why."
2. Ask for the user need behind each position: "Who are you imagining when you say this has to be in Release 1?"
3. Check for a false dilemma: "Is there a thinner version of this that satisfies both concerns?"

**The "must have vs. nice to have" conversation:**
Ask stakeholders to rate each task with a simple vote: thumbs up (must be in Release 1), sideways (could wait), thumbs down (clearly future). Do this for each activity. The votes create visible disagreement to discuss.

**AskUserQuestion:** "For each activity in the backbone — is there a story here that is absolutely required for a user to accomplish [the goal] end-to-end? Or can this activity be simplified or deferred in Release 1?"

### Validate the Walking Skeleton as a Group

Once you have a candidate Release 1, narrate the user journey aloud using only the Release 1 stories:

> "OK — let's walk through what a user can do with only what's above this line. They open the app. First they [Release 1 story from Activity 1]. Then they [Release 1 story from Activity 2]. Then..."

Ask the group: "Does a user successfully achieve [the goal] using only this? Does anything break?"

---

## Gap Detection: What's Missing From the Map?

After the backbone is built and initial release lines are drawn, run a gap detection pass.

**AskUserQuestion:** "Looking at the full map — is there anything that users need to do that isn't on the map at all? Think about: error recovery, account management, notification and confirmation steps, help and onboarding, recurring actions."

**Common gaps to check for:**

*Authentication and onboarding:*
How does a new user get started? Is that on the map? If the first activity assumes an existing account, what creates that account?

*Error and recovery states:*
What happens when something goes wrong? Are there tasks on the map for recovery? (These usually belong in stories, not backbone tasks, but they need to exist somewhere.)

*Notifications and confirmation:*
Does the user need to be notified that something happened? Does the map capture that?

*Recurring actions:*
If the user does this journey repeatedly, is there anything that differs on the second time through?

*Supporting roles:*
Does someone else need to do something to enable this user's journey? (An admin sets up the account, an ops team confirms the order, a support agent resolves an issue.) Those activities are not on this map but they may be dependencies.

**Add gaps to the map:**
If a gap is real and important, add a sticky note for it. If it is an edge case or a future concern, note it elsewhere and return to it.

---

## Closing the Session (20–30 minutes)

### Capture Decisions

Before the session ends, write down every significant decision made during the session. Decisions include:
- What is in and out of Release 1
- Activities or tasks that were intentionally deferred
- Disagreements that were resolved and how
- Open questions that were NOT resolved

**AskUserQuestion:** "Before we close — what decisions did we make today that need to be recorded? What is still an open question that needs a follow-up?"

**Decision log template:**
```
Decision: [what was decided]
Rationale: [why this decision was made]
Owner: [who is responsible for acting on it]
Open question: [what we still need to answer]
```

### Photograph and Archive the Map

**In-person:** Photograph the map immediately. Label each activity and the release lines in the photo caption. Send the photo to all participants within 30 minutes of the session ending.

**Remote:** Export the board. Share the link with view access to all participants. Take a screenshot of the current state as a timestamp.

### Assign Owners and Next Steps

Every action that comes out of the session needs an owner and a deadline.

Common next steps:
- Story-storm the top activities in Release 1 (who, by when?)
- Validate the walking skeleton with a real user (who sets that up?)
- Return with engineering estimates for Release 1 stories (who, by when?)
- Follow up on open questions (who owns each question?)

**Do not leave the session without owners on every action.** Unmet actions disappear.

---

## Facilitation Tips

### Remote Sessions

**Remote mapping is harder than in-person.** Expect sessions to run 20–30% longer and produce 20–30% less output per session.

**Tips for remote facilitation:**
- Use timers. Remote sessions drift without visible countdowns. Show a timer on screen.
- Require cameras on. Participants with cameras off disengage faster.
- Use breakout rooms for subgroup discussions, then bring findings back to the main board.
- Do shorter sessions more frequently. A 90-minute remote session is as effective as a 2-hour in-person session.
- Rotate facilitation: ask participants to take turns reading sticky notes aloud. Passive listening kills remote sessions.

**Remote tool tips for Miro:**
- Use voting features for "must have / can wait" decisions
- Use the built-in timer for timed activities
- Use sticky note reactions (thumbs up/down) as a quick signal of agreement
- Lock the backbone after it is established so participants don't accidentally move it

### In-Person Sessions

- Stand up. Sessions run better standing — people move, point, and engage more physically.
- Let participants write their own stickies. The act of writing creates ownership.
- If someone is dominating: "Let's hear from someone who hasn't spoken yet about this."
- If someone is disengaged: give them a specific job — "Can you read back the backbone left-to-right for us?"
- If the session bogs down: move to the next activity and come back. Don't let one card stop the session.

### Handling Common Problems

**"This map is already out of date."**
That is fine. Maps are never perfectly current. Update the relevant section and move on.

**"We need to map [new topic] that isn't on the board."**
Capture it on a parking lot sticky. Finish the current map before expanding scope.

**"Engineering says this isn't feasible in Release 1."**
This is the most valuable conversation in the session. Work through it: "What is the feasible version of this story that still lets the user accomplish their goal?" Don't remove the story — simplify it.

**"We can't agree on the backbone."**
Split the disagreement: run two versions of the backbone for 10 minutes, then compare. The act of seeing two alternatives usually resolves the disagreement faster than arguing about the first version.
