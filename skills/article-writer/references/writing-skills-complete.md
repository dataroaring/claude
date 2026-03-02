# Complete 14 Writing Skills Reference

Based on "Writing for Developers" by Piotr Sarna & Cynthia Dunlop

---

## Pre-Writing Skills

### Skill 1: Goal Definition

Before writing anything, establish two sentences that never get published:

1. **"The goal of this article is to..."**
   - Be specific about what the reader will gain
   - Example: "The goal of this article is to help backend developers understand when to choose Redis over PostgreSQL for caching"

2. **"My perspective is interesting because..."**
   - What makes YOU the right person to write this?
   - Example: "My perspective is interesting because I migrated our 10M user system from PostgreSQL to Redis caching and learned hard lessons"

Also identify:
- **Target reader**: Who specifically will read this?
- **Prior knowledge**: What do they already know?
- **Why they care**: What problem does this solve for them?
- **Desired outcome**: What should they think or do differently?

---

### Skill 2: Pattern Selection

Match your content to the appropriate structure:

| If your content is about... | Use this pattern |
|----------------------------|------------------|
| Finding and fixing a tricky bug | Bug Hunt |
| Migrating to a new language/framework | Rewrote It in X |
| A significant technical project | How We Built It |
| Hard-won wisdom from experience | Lessons Learned |
| Your opinion on industry direction | Thoughts on Trends |
| Educational content featuring your product | Non-markety Product Perspectives |
| Performance data and comparisons | Benchmarks and Test Results |

See `patterns.md` for detailed guidance on each pattern.

---

## Writing Skills

### Skill 3: Evidence-Based Claims

Every arguable statement needs support. Transform weak claims into strong ones:

| Weak Claim | Strong Alternative |
|------------|-------------------|
| "Impressive performance" | "Reduced latency from 200ms to 15ms (92% improvement)" |
| "X is better than Y" | Show side-by-side code comparison with metrics |
| "It's difficult" | "Required understanding 3 undocumented APIs and debugging race conditions" |
| "Migration is simple" | "Migration takes 4 steps: 1) Export config... 2) Run migration script... 3) Verify data... 4) Switch traffic" |
| "We improved reliability" | "Uptime went from 99.2% to 99.95%, reducing incidents from 12/month to 2/month" |

**Rule of thumb**: If a skeptical reader would ask "How do you know?" or "Prove it", you need evidence.

---

### Skill 4: Conversational Voice

Write like you're explaining to a smart colleague over lunch:

**Pronouns:**
- Use "I" or "we" for yourself
- Use "you" for the reader
- Avoid passive voice where possible

**Tone:**
- Contractions are fine ("don't", "it's", "we've")
- Be authentic - share frustrations, mistakes, uncertainties
- Don't try to sound impressive - be clear instead

**Examples:**

❌ "The system was optimized by the engineering team"
✅ "We optimized the system"

❌ "One might consider implementing caching"
✅ "Consider adding caching here"

❌ "The results were unexpected"
✅ "I didn't expect this result - here's why it surprised me"

---

### Skill 5: Single-Idea Paragraphs

**One idea per paragraph.** When you move to a new idea, start a new paragraph.

**Sentence length test:** Read the sentence aloud. If you run out of breath, it's too long. Break it up.

**Verb optimization:**
- Replace weak "to be" verbs with action verbs
- ❌ "The function is responsible for parsing"
- ✅ "The function parses"

**Trim prepositional phrase chains:**
- ❌ "In the process of the implementation of the feature"
- ✅ "While implementing the feature"

---

### Skill 6: Scannability

Readers scan before they read. Make scanning easy:

**Headings:**
- Use headings every 2+ scrolls of content
- Make headings descriptive (not "Introduction" but "Why We Chose Rust")
- Use heading hierarchy (H2, H3, H4) consistently

**Visual breaks:**
- No paragraph blocks longer than 5-6 lines
- Use bullet points for lists of 3+ items
- Use tables for comparisons
- Bold key terms and phrases

**Key points:**
- Front-load important information
- Put the main point in the first sentence of each section
- Don't bury the lede

---

### Skill 7: Show Don't Tell

Replace descriptions with demonstrations:

**Code examples:**
- Legible (proper formatting)
- Syntax highlighted
- Copy-pasteable (no line numbers in code blocks)
- Minimal - show only what's relevant

**Diagrams:**
- Architecture for system overviews
- Flowcharts for processes
- Sequence diagrams for interactions

**Specific numbers:**
- ❌ "Significantly faster"
- ✅ "3.2x faster (from 450ms to 140ms)"

**Real examples:**
- Draw from your actual experience
- Name specific technologies, not "a database"
- Reference real scenarios, not hypotheticals

---

## Review Skills

### Skill 8: Facts Check

For each arguable statement, ask:

1. **Is it supported by evidence?**
   - Numbers, code, benchmarks, citations?
   - Or just opinion presented as fact?

2. **Would a skeptical reader trust this?**
   - Is the evidence sufficient?
   - Is the source credible?

3. **Are specifics provided?**
   - Vague: "It performs well"
   - Specific: "Handles 10K requests/second with p99 latency under 50ms"

**Action:** Flag every unsupported claim. Either add evidence or soften to opinion ("In my experience..." or "I believe...").

---

### Skill 9: Focus Check

For every paragraph, ask:

1. **Does this advance the stated goal?**
   - Return to your goal statement from Skill 1
   - If the paragraph doesn't serve the goal, cut it

2. **Can this be cut without losing value?**
   - If removing it wouldn't hurt the article, remove it
   - When in doubt, cut it out

3. **Is there off-topic rambling?**
   - Tangents that don't serve the reader
   - Background that isn't necessary
   - Showing off knowledge that isn't relevant

**Action:** Be ruthless. Cut anything that doesn't serve the reader's goal.

---

### Skill 10: Flow Check

Evaluate the overall structure:

1. **Logical progression?**
   - Does the article build from start to finish?
   - Would reordering sections help?

2. **Smooth transitions?**
   - Can readers follow from one section to the next?
   - Are there jarring jumps?

3. **No getting lost?**
   - Would a reader know where they are?
   - Does each section connect to what came before?

**Action:** Read the article as if you know nothing about the topic. Where do you get confused?

---

### Skill 11: Component Review

Check each component:

| Component | Questions |
|-----------|-----------|
| **Title** | Under 60 characters? Keywords upfront? Intriguing but not clickbait? |
| **Introduction** | States what reader will get? Explains why your perspective matters? Hooks the reader? |
| **Headings** | Descriptive and scannable? Would a reader understand the article from headings alone? |
| **Ending** | Ties up the article? Provides clear next steps or path forward? Memorable? |
| **Code** | Legible? Syntax highlighted? Copy-pasteable? Minimal and relevant? |
| **Visuals** | Helpful (not decorative)? Properly sized? Alt text for accessibility? |

---

### Skill 12: Pattern-Specific Review

Apply criteria specific to your chosen pattern:

See `pattern-reviews.md` for detailed checklists for:
- Bug Hunt
- Rewrote It in X
- How We Built It
- Lessons Learned
- Thoughts on Trends
- Non-markety Product Perspectives
- Benchmarks and Test Results

---

### Skill 13: Pre-Publish Verification

Technical checks before publishing:

- [ ] Title renders well in template/preview
- [ ] All links work (click every one)
- [ ] Code is legible and copy-pasteable
- [ ] Images properly sized (not stretched, not tiny)
- [ ] Keywords in meta description
- [ ] URL is clean and includes keywords
- [ ] No embarrassing typos in title/headings
- [ ] Author info is correct
- [ ] Publication date is correct

**Action:** Actually click through the preview. Don't assume it looks right.

---

### Skill 14: Self-Review Test

Final gut-check questions:

1. **Would I share this if someone else wrote it?**
   - Honestly - is it good enough to recommend?

2. **Can a skeptical reader trust my claims?**
   - Did I back up everything with evidence?

3. **Does every section advance my stated goal?**
   - No fluff, no tangents, no showing off?

4. **Is the key takeaway clear within the first few paragraphs?**
   - Would a busy reader get value from just the intro?

5. **Have I shown my work, not just stated conclusions?**
   - Did I explain WHY, not just WHAT?

**Action:** If any answer is "no", revise before publishing.

---

## Quick Reference Summary

| # | Skill | Phase | Key Question |
|---|-------|-------|--------------|
| 1 | Goal Definition | Pre-Writing | What's the goal and why me? |
| 2 | Pattern Selection | Pre-Writing | Which structure fits? |
| 3 | Evidence-Based Claims | Writing | Can I prove this? |
| 4 | Conversational Voice | Writing | Does this sound human? |
| 5 | Single-Idea Paragraphs | Writing | Is this clear and concise? |
| 6 | Scannability | Writing | Can readers scan this? |
| 7 | Show Don't Tell | Writing | Am I showing, not telling? |
| 8 | Facts Check | Review | Is every claim supported? |
| 9 | Focus Check | Review | Does this serve the goal? |
| 10 | Flow Check | Review | Does this flow logically? |
| 11 | Component Review | Review | Are all parts polished? |
| 12 | Pattern-Specific Review | Review | Does it fit the pattern? |
| 13 | Pre-Publish Verification | Review | Is it technically ready? |
| 14 | Self-Review Test | Review | Would I share this? |
