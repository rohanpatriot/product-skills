# Map Opportunities Workflow

I'll guide you through customer interviewing, experience mapping, and building an Opportunity Solution Tree rooted in real customer evidence.

## When to Use

- After setting a product outcome (from [set-outcomes.md](set-outcomes.md))
- When the team needs to understand the customer's experience related to their outcome
- When the Opportunity Solution Tree is empty or thin
- When the team is operating on assumptions instead of customer evidence

## Prerequisites

Read [frameworks.md](../references/frameworks.md) for Experience Map, Interview Snapshot, and Opportunity Solution Tree frameworks. Read [techniques.md](../references/techniques.md) for Continuous Interviewing, Story-Based Interviewing, and Interview Snapshot Synthesis methods. Read [anti-patterns.md](../references/anti-patterns.md) for Interviewing and Opportunity Mapping anti-patterns.

## The Process

### Step 1: Create the Initial Experience Map

Use `AskUserQuestion` to understand the starting context:

**Question:** "What experience are your customers going through that relates to your outcome?"

**Follow-ups:**
- What is the customer trying to accomplish?
- What are the major steps they take today?
- Where do you think they struggle most? (Mark these as assumptions to validate)

Draft an initial experience map:

```
Customer goal: [What the customer is trying to accomplish]

[Step 1: ___] → [Step 2: ___] → [Step 3: ___] → [Step 4: ___] → [Step 5: ___]
```

Mark this as a hypothesis — it will be refined through interviews. Annotate any steps that are assumed rather than observed.

### Step 2: Set Up Continuous Interviewing

I'll walk you through establishing a sustainable interview cadence:

1. **Recruit:** How will you find customers to interview?
   - In-product prompt ("Help us improve — chat for 20 minutes?")
   - Automated scheduling (Calendly or similar)
   - Customer success referrals
   - Existing research panel
2. **Schedule:** Set a recurring weekly time slot that all trio members can attend
3. **Target:** Which customers are most relevant to your outcome?
   - Current users experiencing the mapped journey
   - Churned users who abandoned the journey
   - Prospective users who haven't started yet
4. **Prepare:** Create an interview guide using the story-based interviewing technique

Interview guide skeleton:

```
Opening: "Tell me about the last time you [activity related to outcome]."

Follow the story:
- "What happened next?"
- "You mentioned [friction point]. Tell me more about that."
- "How did that feel?"
- "How are you handling that today?"

Close:
- "If you could wave a magic wand, what would change about this experience?"
- "Is there anything I didn't ask about that you think is important?"
```

### Step 3: Conduct Interviews and Create Snapshots

For each interview:

1. All available trio members attend
2. One person leads the interview, others take notes
3. Follow the story — don't stick rigidly to the guide
4. Within one hour of the interview, fill out the snapshot:

```
Interview Snapshot: [Customer ID/Name]    Date: [Date]

Quick Facts:
- [Relevant context about this customer]

Opportunities Identified:
- [Opportunity 1: customer need, pain point, or desire]
- [Opportunity 2]
- [Opportunity 3]

Key Quotes:
- "[Direct quote illustrating an opportunity]"
- "[Direct quote]"

Experience Insights:
[What we learned about their journey — how does this update our experience map?]

Surprises:
[What we didn't expect]
```

5. Update the experience map with new steps, needs, pain points, or desires discovered
6. Add opportunities to the Opportunity Solution Tree

### Step 4: Build the Opportunity Solution Tree

As interviews accumulate (aim for at least 5-10 before heavy structuring):

1. **Start the tree:** Place your desired outcome at the top
2. **Add opportunities:** Each opportunity from interview snapshots goes on the tree
3. **Structure hierarchically:**
   - Group related opportunities under parent nodes
   - Ask: "Is this a sub-opportunity of something already on the tree?"
   - Example: "Can't find relevant products" might be a child of "Shopping experience is overwhelming"
4. **Label branches:** Give parent opportunities descriptive names
5. **Track frequency:** Note how many interviews surfaced each opportunity (frequency signals importance)

```
[Desired Outcome: Increase activation rate]
        |
    -------------------------
    |           |           |
[Onboarding   [Value       [Trust
 confusing]    unclear]     lacking]
    |                |
  -----            -----
  |   |            |   |
[Too  [Jargon    [No    [Benefits
many   heavy]    proof    not
steps]           of       visible]
                 value]
```

### Step 5: Validate and Enrich the Tree

Continue weekly interviews to:

- **Validate:** Do new interviews reinforce existing opportunities? (Frequency builds confidence)
- **Discover:** Do new interviews reveal opportunities not yet on the tree? (Add them)
- **Refine:** Do new interviews suggest restructuring? (Move opportunities, merge duplicates, split overly broad ones)
- **Deepen:** Do new interviews add nuance to known opportunities? (Add detail, quotes, context)

The tree should change every week. If it hasn't changed in two weeks, you're either not interviewing or not synthesizing effectively.

### Step 6: Select a Target Opportunity

When the tree has at least 10-15 opportunities across multiple branches:

1. Identify candidate opportunities (specific enough to generate solutions for)
2. Evaluate using structured criteria:

| Criterion | Opportunity A | Opportunity B | Opportunity C |
|-----------|--------------|--------------|--------------|
| Frequency (how many customers?) | | | |
| Intensity (how much does it matter?) | | | |
| Connection to outcome | | | |
| Feasibility | | | |

3. Compare candidates as a trio — use the compare-and-contrast framework
4. Select one target opportunity
5. Commit to this opportunity for a discovery cycle (2-4 weeks)

Use `AskUserQuestion` to present the top candidates and discuss with the user.

## Output

By the end of this workflow, the team should have:

- A validated experience map populated from customer interviews
- At least 5 interview snapshots
- An Opportunity Solution Tree with 10-15+ opportunities structured hierarchically
- A selected target opportunity to focus solution generation on

## What Comes Next

With a target opportunity selected, move to [ideate-solutions.md](ideate-solutions.md) to generate and compare solutions.

## Common Failure Modes

1. **Rushing to solutions** before the opportunity space is rich enough
2. **Mapping assumptions** instead of interview-sourced opportunities
3. **Flat list** instead of hierarchical tree structure
4. **Stopping interviews** after a few — the tree should grow continuously
5. **PM-only interviews** — the whole trio needs direct customer contact
6. **Solutions as opportunities** — "We need a better X" is a solution, not an opportunity
