# Anti-Patterns

Seventeen common mistakes in Jobs-to-be-Done practice, organized by the activity where they occur. Each anti-pattern covers: what practitioners do wrong, why it fails, and the fix.

---

## Table of Contents

- [Interview Anti-Patterns](#interview-anti-patterns)
- [Job Statement Anti-Patterns](#job-statement-anti-patterns)
- [Forces Analysis Anti-Patterns](#forces-analysis-anti-patterns)
- [Strategy and Application Anti-Patterns](#strategy-and-application-anti-patterns)

---

## Interview Anti-Patterns

### 1. Asking About Future Behavior

**The mistake:** Asking hypothetical questions: "Would you use this feature?" "How much would you pay for X?" "If we built Y, would that solve your problem?"

**Why it fails:** People are systematically wrong about predicting their own future behavior. The gap between stated preference and revealed preference is not random error — it's structural. In an interview, people want to be helpful. They tell you what they think you want to hear, or what they think they should want. Neither is valid research data. "Would you use a feature that automatically organized your calendar?" sounds compelling but predicts nothing about whether they'd actually change their behavior.

**The fix:** Stay entirely in the past. "How are you solving this today?" "What did you do the last time this happened?" "Walk me through the last time you tried to [task]." Past behavior is the only valid predictor of future behavior. Real stories with real events are what JTBD is built on.

---

### 2. Leading Questions

**The mistake:** Asking questions that suggest the answer: "So that was really frustrating, right?" "Was the main issue the cost?" "Did you feel like the old product wasn't keeping up with your needs?"

**Why it fails:** Customers are not adversarial. They're trying to be helpful. When a question suggests an interpretation, customers tend to confirm it — not because it's true, but because they want to cooperate. You're getting their agreement with your hypothesis, not their actual experience. Every leading question makes your data slightly less trustworthy until eventually you're hearing your own assumptions reflected back at you.

**The fix:** Use neutral follow-ups: "Tell me more." "What happened next?" "What was that like?" "What did you actually do?" These keep the story moving without steering it. If you notice yourself about to say "So you felt like...", stop and ask "What were you feeling in that moment?" instead.

---

### 3. Skipping the Struggling Moment

**The mistake:** Opening an interview by asking about the product or the purchase decision, rather than digging back to the first sign that something wasn't working.

**Why it fails:** The struggling moment is the cause. The purchase is the effect. If you start at the purchase and work forward, you're analyzing the downstream behavior without understanding what drove it. You learn what happened but not why it happened. The struggling moment is where Push forces originate — and Push is the primary driver of most switching decisions.

**The fix:** Before asking about the purchase or the new product, ask: "Before you ever thought about changing anything — what was the first moment you remember thinking 'something about this isn't working'?" Probe until you have a specific event, not a vague feeling. Everything else flows from there.

---

### 4. Synthesizing Too Early

**The mistake:** Drawing conclusions during the interview, then asking questions that probe those conclusions rather than following the customer's story.

**Why it fails:** Once you form a hypothesis, confirmation bias takes over. Your follow-up questions probe for evidence that confirms the hypothesis and ignore evidence that contradicts it. You hear the customer's story as evidence for your theory rather than as its own object. Customers also respond to the implicit agenda — they sense what you're looking for and give you more of it.

**The fix:** Think of the interview as documentation, not analysis. Your job is to capture the story. Flag things that seem important in your notes, but don't act on them during the interview. Synthesis happens after, not during. Give yourself 30 minutes after the interview before reviewing your notes — the distance helps.

---

### 5. Recruiting Non-Switchers

**The mistake:** Interviewing customers who didn't make a real decision — people who had the product imposed on them, who renewed by default, or who barely remember why they signed up.

**Why it fails:** JTBD is a theory of switching. It explains why people make deliberate decisions to change from one solution to another. Customers who didn't make an active switch can't tell you about the forces that drive switching. They have no struggling moment, no passive looking phase, no deciding moment. Their story is too thin to yield insight.

**The fix:** Screen specifically for deliberate switchers. Recruiting criteria: "Did you evaluate alternatives before choosing this product? Did you switch from something you were using before?" If they say "I don't know, I just signed up" — thank them and move on. You need people who made a real decision and remember it.

---

### 6. Presenting Solutions During the Interview

**The mistake:** Describing potential solutions mid-interview to see if the customer reacts positively. "We're thinking of building X — would that help?" or "What if we made Y easier?"

**Why it fails:** The moment you put a solution in the room, the interview shifts from a timeline reconstruction to a product evaluation. The customer is now thinking about your solution rather than their own experience. You lose the rest of the causal story — because they're focused on evaluating what you've shown them rather than telling you what actually happened. You've converted a discovery interview into a usability or preference session.

**The fix:** Keep solutions out of the interview entirely. Your job is to understand the job, the forces, and the timeline — full stop. If the customer asks "are you going to build something to fix this?", redirect: "We might be, but for now I just want to understand your experience. Tell me more about..."

---

### 7. Interviewing Only Satisfied Customers

**The mistake:** Conducting switch interviews exclusively with current happy customers, avoiding churned or dissatisfied customers.

**Why it fails:** Satisfied customers tell you why your product works for them. Churned customers tell you what jobs your product failed to do. Both stories are necessary for a complete understanding. If you only hear from satisfied customers, you build a picture of the job that is systematically biased toward the jobs your product already does well. You miss the jobs it's failing at — which is exactly where growth comes from.

**The fix:** Design a research program with deliberate balance: current satisfied customers, recent churned customers, and customers who considered you but chose a competitor. Each population answers a different question about demand.

---

## Job Statement Anti-Patterns

### 8. Conflating the Job with the Solution

**The mistake:** Writing job statements that describe a solution rather than the underlying job. "When I need to manage my projects, I want to use project management software, so I can track progress."

**Why it fails:** A job statement that contains a solution is circular. It tells you what to build (project management software) before you've understood what progress the customer is trying to make. It forecloses exploration of alternative solutions. And it produces false validation — of course customers who bought project management software want project management software. That tells you nothing.

**The fix:** The motivation component of the job statement should describe a progress the customer wants to make, expressed independently of any solution. Ask: "Could the customer make this progress without my product?" If yes — that's closer to the job. "I want to always know where a project stands without having to chase people for updates" is a job. "I want to use a dashboard" is a solution preference.

---

### 9. Ignoring the Emotional Job

**The mistake:** Writing job statements that capture only the functional dimension and ignore the emotional and social jobs entirely.

**Why it fails:** Functional job statements produce functional solutions — incremental improvements to what the product already does. But switching decisions are rarely driven by functional improvements alone. The switch happens when a customer's emotional or social job isn't being served, or when a new solution promises to serve it better. Ignoring these dimensions leads to products that work well technically but don't win customers.

**The fix:** Always document all three dimensions. After writing the functional statement, ask: "What feeling is this customer trying to reach or escape?" and "How do they want to be seen — by others or by themselves — when this job is done?" The emotional and social jobs often predict switching behavior more accurately than the functional job.

---

### 10. Deriving the Job Statement from One Interview

**The mistake:** Conducting one switch interview, writing a job statement from it, and treating that statement as validated.

**Why it fails:** One interview is one data point. That customer's struggling moment, their specific forces, their exact situation — all of these are particular to them. They may be representative or they may be an outlier. You cannot know until you have data from multiple interviews. Building a strategy on a single job statement is building on sand.

**The fix:** Write a draft job statement after each interview, but treat it explicitly as a hypothesis. After 5 interviews, compare the draft statements. If they converge — if the situation, motivation, and expected outcome are consistent across customers — the statement is gaining validity. If they diverge significantly, you may be looking at multiple distinct segments with different jobs.

---

## Forces Analysis Anti-Patterns

### 11. Ignoring the Firing Decision

**The mistake:** Focusing the JTBD analysis entirely on why customers hired your product, without investigating why they fire it or what they fired before hiring you.

**Why it fails:** The firing decision is the other half of the story. What did the customer fire to make room for hiring you? What job was the old solution doing — and how did it fail? Without this, you don't understand the full competitive landscape. And without understanding why customers fire you, you can't prevent churn or design for better little hire.

**The fix:** Every switch interview should capture what was fired. "What were you using before you switched to us?" and "When did you finally decide to stop using that — what was the last straw?" And for churn interviews: "What finally made you decide to stop using us? What are you doing instead now?"

---

### 12. Treating All Four Forces as Equally Important

**The mistake:** Documenting all four forces as present, assigning them equal weight, and concluding that the switch happened because all four were engaged.

**Why it fails:** In most switching decisions, one or two forces dominate. Understanding which force dominated is the strategic finding. If Push dominates, your customers are escaping problems more than pursuing your vision — and you're at risk of being used until someone else solves the problem better. If Anxiety dominates, your biggest opportunity is risk reduction and credibility, not feature improvement. If Habit dominates, switching cost reduction is the highest-leverage investment. Treating all forces as equal produces no clear strategic implication.

**The fix:** After mapping all four forces, explicitly assess dominance. "Of these four forces, which one, if removed, would have stopped the switch from happening? Which one, if increased, would have accelerated it?" The answers to those two questions are your strategic insights.

---

### 13. Building the Forces Map from Assumptions

**The mistake:** Drawing a forces diagram based on what you think customers feel rather than what interview data shows.

**Why it fails:** Internal teams almost always overestimate Pull (they believe their product is more compelling than it is), underestimate Anxiety (they don't see the fear their product creates), and miss the specific source of Push (they substitute a general market problem for the customer's specific struggling moment). A forces map built from assumptions confirms existing beliefs and produces no new insight.

**The fix:** Every element of the forces map should trace to a specific customer quote from a real interview. If you can't cite a quote for a force, you don't have evidence for it. Mark it as a hypothesis and design an interview question to test it.

---

## Strategy and Application Anti-Patterns

### 14. Using Surveys Instead of Interviews

**The mistake:** Attempting to do JTBD analysis through surveys, NPS questions, or quantitative behavioral data rather than timeline interviews.

**Why it fails:** JTBD is a causal theory. It explains why customers make the decisions they do. Causation requires narrative — the sequence of events, the forces that built and resolved, the specific moment when something tipped. Surveys can tell you what happened (what customers think of your product, whether they'd recommend it) but not why it happened. The struggling moment, the passive looking phase, the deciding moment — these are all invisible to surveys.

**The fix:** Interviews are non-negotiable for JTBD. Quantitative data can help you identify which customers to interview (customers who churned, customers who just converted, customers whose usage dropped) but cannot replace the interview. Use surveys to find the switchers; use interviews to understand them.

---

### 15. Treating JTBD as a One-Time Exercise

**The mistake:** Conducting JTBD research once (during initial product definition or a major strategy review) and treating the findings as permanent.

**Why it fails:** Jobs are stable, but the situations that trigger jobs, the forces that drive switching, and the competing solutions that serve jobs all change. New competitors emerge. Customers' circumstances shift. The context in which the struggling moment arises evolves. A forces map from three years ago may be structurally correct but tactically outdated.

**The fix:** Treat JTBD research as a continuous practice alongside discovery. Run at least one switch interview per month, even when you think you already understand the job. The incremental learning compounds. And when you see unexpected changes in acquisition, churn, or engagement patterns, conduct a fresh round of interviews rather than speculating about the cause.

---

### 16. Confusing Job Segments with Demographic Segments

**The mistake:** Equating JTBD segmentation with demographic segmentation. "Our JTBD analysis shows that millennials hire our product for X."

**Why it fails:** Demographics do not cause jobs. Age, gender, income, and industry are correlations at best. Two 35-year-old product managers at similar companies can hire your product for completely different jobs depending on their specific circumstances. And two people from entirely different demographic profiles may share the exact same struggling moment and hire your product for the same job. Demographic segmentation produces marketing personas. Job segmentation produces product strategy.

**The fix:** Segment by the situation that creates the job, not by the person who has the job. "When a first-time manager is responsible for a decision they don't have enough information to make" is a situation-based segment. "Product managers at mid-sized SaaS companies" is a demographic segment. The first tells you what to build and how to position it; the second tells you who to reach.

---

### 17. Testing Features When You Should Be Testing Jobs

**The mistake:** Using JTBD research to validate specific features ("We learned about the job, now let's test whether Feature X does the job") rather than using it to question whether you're addressing the right job at all.

**Why it fails:** Feature testing assumes the job is well understood and confirmed. If the job statement is wrong — if you've misidentified the situation, the motivation, or the expected outcome — all the feature testing in the world won't reveal it. You'll optimise solutions to the wrong problem. This is how products get better and better at something fewer and fewer customers care about.

**The fix:** Before testing features, test the job statement. Run validation interviews: "Here's what we believe is the job you're hiring our product for. Does that resonate? Is that the progress you're trying to make?" If customers consistently reframe or correct the job statement, fix it before building anything. Job testing is cheaper than feature testing.
