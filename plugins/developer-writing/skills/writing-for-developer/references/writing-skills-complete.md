# Technical Article Writing Skills

Based on "Writing for Developers" by Piotr Sarna & Cynthia Dunlop

---

## Topic Selection (Before Everything Else)

Selecting a promising topic is the **single most important task**. A catchy title, eloquent sentences, solid code examples—none of that matters if you're not covering a topic that fits both you and your readers.

### The 3 Ps Test

Does your topic meet at least one of the 3 Ps?

| P | Question | Examples |
|---|----------|----------|
| **Proud of** | What accomplishments are you eager to show off? | Impressive feature, architectural breakthrough, performance improvement |
| **Pained by** | What challenges caused constant headaches? | Debugging nightmare, migration struggle, scaling crisis |
| **Passionate about** | What else gets your blood racing? | Technology opinion, industry trend, tool comparison |

**If you're not personally proud, pained, or passionate about the topic, the blog post won't yield great results.**

### Topic Idea Sources

**From your daily work:**
- That cool thing you implemented
- Security incident post-mortem
- How infrastructure survived (or didn't survive) a traffic spike
- Bug hunting stories
- Difficult design decisions
- Architectural shifts and tradeoffs
- Epic failures and lessons learned

**From industry conversations:**
- Challenging the status quo
- Controversial opinions backed by experience
- Predictions and analysis
- Book/tool reviews

**For your users:**
- Clarifications of confusing features
- Common mistakes to avoid
- Unexpected use cases

### Test Your Topic Idea

**Quick test:** Float it as a social media post. If it takes off, that's a good indicator. If it doesn't strike a chord, try variations before giving up.

### Topic Ideas Checklist

- [ ] Passes at least one of the 3 Ps
- [ ] You have unique insight or experience on this topic
- [ ] Target readers would genuinely care about this
- [ ] You can provide specific details, not just generalities
- [ ] It hasn't been covered better by someone more qualified

---

## Pre-Writing Skills

### 1. Goal Definition
Write two sentences that never get published:
- "The goal of this article is to..."
- "My perspective is interesting because..."

Also identify:
- Who is your target reader?
- What do they already know?
- Why would they care?
- What should they think or do differently after reading?

### 2. Pattern Selection
Match your content to the appropriate blog post structure:

| If your content is about... | Use this pattern |
|----------------------------|------------------|
| Finding and fixing a tricky bug | Bug Hunt |
| Migrating to a new language/framework | Rewrote It in X |
| A significant technical project | How We Built It |
| Hard-won wisdom from experience | Lessons Learned |
| Your opinion on industry direction | Thoughts on Trends |
| Educational content featuring your product | Non-markety Product Perspectives |
| Performance data and comparisons | Benchmarks and Test Results |

---

## Writing Skills

### 3. Evidence-Based Claims
Support every arguable statement with specifics:

| Weak | Strong |
|------|--------|
| "Impressive performance" | Show benchmark numbers |
| "X is better than Y" | Show code comparison |
| "It's difficult" | Explain specific challenges |
| "Migration is simple" | Detail the actual steps |

### 4. Conversational Voice
- Use "I/we" for yourself, "you" for the reader
- Contractions are fine
- Share frustrations, mistakes, what you don't know
- Be authentic, not robotic
- Write like talking to colleagues over lunch

### 5. Single-Idea Paragraphs
- One idea per paragraph
- If you run out of breath reading aloud, the sentence is too long
- Replace weak "to be" verbs with action verbs
- Trim prepositional phrase chains

### 6. Scannability
- Use headings every 2+ scrolls of content
- Bold key points
- Use lists and tables where appropriate
- No massive paragraph blocks

### 7. Show Don't Tell
- Include code examples (legible, syntax-highlighted)
- Add diagrams for architecture/flow
- Provide specific numbers, not vague claims
- Use real examples from your experience

### 8. Actionable Writing (Don't Make Reader Think)

**The Problem:** Abstract descriptions force readers to do the thinking. Actionable writing does the thinking for them.

**Transform Abstract → Actionable:**

| Abstract (Avoid) | Actionable (Write) |
|------------------|-------------------|
| "Consider your scaling requirements" | "If you have >10M rows, use partitioning" |
| "Performance may vary" | "Expect 50-200ms latency depending on query complexity" |
| "Teams often struggle with X" | "You'll hit this wall when your daily inserts exceed 1M" |
| "There are several approaches" | "Use approach A for reads, approach B for writes" |
| "This depends on your needs" | "For OLTP: use X. For OLAP: use Y" |

**The "How Do I Know When?" Test:**

For every claim, ask: "How does the reader know when this applies to them?"

- ❌ "At some point, you'll need to scale"
- ✅ "When query latency exceeds 500ms or storage hits 80%, it's time to scale"

**Don't List Requirements—Provide Decision Criteria:**

- ❌ "Requirements: high availability, low latency, scalability"
- ✅ "Choose this if you need <100ms reads and can tolerate eventual consistency"

**Don't Describe Problems—Show Recognition Signals:**

- ❌ "Query performance can degrade over time"
- ✅ "Watch for: queries that took 10ms now taking 100ms, increased CPU during off-peak hours"

**Actionable Writing Checklist:**

- [ ] Every "it depends" is followed by specific conditions
- [ ] Numbers replace words like "fast," "many," "large"
- [ ] Reader can take action without additional research
- [ ] Recognition signals provided, not just problem descriptions
- [ ] Decision criteria given, not just requirements listed

---

## Review Skills

### 9. Facts Check
Ask for each arguable statement:
- Is it supported by evidence?
- Are there specific numbers, code examples, benchmarks?
- Would a skeptical reader trust this?

### 10. Focus Check
For every paragraph ask:
- Does this advance the stated goal?
- Can this be cut without losing value?
- Is there off-topic rambling?

### 11. Flow Check
- Is there logical progression from start to end?
- Are transitions smooth between sections?
- Would a reader get lost anywhere?

### 12. Component Review

| Component | Review Questions |
|-----------|-----------------|
| **Title** | Short (<60 chars)? Keywords upfront? Intriguing? |
| **Introduction** | States what reader gets? Why your perspective matters? |
| **Headings** | Descriptive and scannable? |
| **Ending** | Ties up nicely? Clear path forward? |
| **Code** | Legible? Syntax highlighted? Copy-pasteable? |
| **Visuals** | Helpful? Properly sized? |

#### Title Deep Dive

**The Process:**
- Generate at least 10 title variations (don't overwrite, keep all ideas)
- Mix and match elements from different variations
- Spend at least a few minutes on title even if you skip other optimization

**Title Must-Haves:**
- Intrigue target readers without misleading them
- Catch attention in a random list (think Hacker News)
- Feature at least one searchable keyword

**Don't Bury Differentiators:**
If your article has something surprising, counterintuitive, or unique—feature it in the title.

**Never Tease Without Delivering:**
If you promise "shocking truth," deliver it. Broken promises = snarky comments + lost future readers.

**Ad Blocker / Clickbait Filters (Avoid):**
- WORDS IN ALL CAPS
- Excessive exclamation marks!!!
- Emojis in titles
- Profanity
- Hyperlinks in title

**Effective Title Qualities:**
- Short and crisp (no fluff words)
- Playful, provocative, or mysterious
- Technical and targeted (something broader audience wouldn't "get")

**Two-Part Title Strategy:**
"[Catchy phrase]: [Descriptive subtitle]"
- "Herding elephants: Lessons learned from sharding Postgres at Notion"
- "Moore's Scofflaws: [subtitle]"

#### Introduction Deep Dive

**What Readers Want to Know:**
- What exactly they'll get from reading
- What angle you're taking on the topic
- How it compares to everything else they've read
- If you seem qualified to address this topic
- If it's worth their time

**Be Upfront and Transparent:**
- Don't trick readers—let uninterested ones leave early
- They'll appreciate you saved their time
- You'll avoid flames from mismatched expectations

**Target Reader Context:**
- Provide soft landing with brief descriptions when introducing concepts
- Use hyperlinks to abstract away details for advanced readers
- Offer learning options for those who need background
- Don't go into hyperlink overload

**Every Word Counts:**
Think hard about every sentence (ideally every word) in your introduction. This is the one place where over-engineering is justified.

#### Ending Deep Dive

**Summary/Takeaways:**
- Synthesize main ideas (don't repeat every point)
- Touch on why it all matters
- Makes it easy for readers to share your key points
- Revisit threads from introduction to close the loop

**Implications/Extrapolation (The "So What"):**
- Place your work in broader industry context
- How does your specific work tie into the broader tech world?
- Conversation starter for comment section

**What's Next (For You):**
- Transparency about future work
- Builds anticipation for next blog post
- Projects rarely have clear endings

**Next Steps (For Them):**
- Invite feedback or contribution
- Give them a way to apply what they learned
- Offer paths to learn more
- End by giving something AND asking for something

### 13. Pattern-Specific Review

**For Story-Driven Posts (Bug Hunt, Lessons Learned):**
- Does it build tension/interest progressively?
- Are the struggles and false leads included?
- Is the resolution satisfying and educational?

**For Comparison Posts (Rewrote It in X, Benchmarks):**
- Are before/after clearly shown side-by-side?
- Are tradeoffs acknowledged honestly?
- Can results be reproduced?

**For Educational Posts (How We Built It):**
- Is the "why" explained, not just the "what"?
- Are key decisions and tradeoffs covered?
- Is there enough context for someone unfamiliar?

**For Opinion Posts (Thoughts on Trends):**
- Is your credibility established?
- Is the position clear and defensible?
- Are counterarguments addressed?

**For Product Posts (Non-markety):**
- Is the content valuable even without the product?
- Is the product mention natural, not forced?
- Is marketing fluff eliminated?

### 14. Pre-Publish Verification
- [ ] Title renders well in template
- [ ] All links work
- [ ] Code is legible and copy-pasteable
- [ ] Images properly sized
- [ ] Keywords in meta description
- [ ] URL is clean and includes keywords
- [ ] Read the whole thing aloud - what sounds clunky?

### 15. Self-Review Test
Ask yourself:
1. Would I share this if someone else wrote it?
2. Can a skeptical reader trust my claims?
3. Does every section advance my stated goal?
4. Is the key takeaway clear within the first few paragraphs?
5. Have I shown my work, not just stated conclusions?

---

## Working with Reviewers

### Selecting Your Reviewers

**Ideal combination:**
- **Technical reviewer** - Someone who knows the subject matter deeply
- **Clarity reviewer** - Someone unfamiliar with the topic (catches assumptions)

**Consider:**
- Do they have time and willingness?
- Will they give honest feedback (not just "looks good")?
- Do they represent your target audience?

### When to Start Review

Ask yourself:
1. **How important/controversial is the topic?** - Higher stakes = more review cycles
2. **Do you have a true "blocker" question?** - Something you can't proceed without answering
3. **Have you done what you intended?** - Check against your goal statement
4. **Will there be time for another cycle?** - Don't send for review the night before deadline

### Preparing Your Reviewers

**Provide background:**
- What's the goal of this article?
- Who's the target reader?
- What stage is the draft in?

**Specify what you want:**
- "Focus on technical accuracy" vs "Focus on clarity and flow"
- "Is the argument convincing?" vs "Is this easy to understand?"
- Highlight specific sections you're uncertain about
- Note what's NOT ready for review (if applicable)

### Responding to Comments

**Do:**
- Thank reviewers for their time
- Address every comment (even if just "noted" or "keeping as-is because...")
- Ask clarifying questions if feedback is unclear
- Consider the feedback, don't just react

**Don't:**
- Argue with every suggestion
- Ignore feedback you don't like
- Make reviewers feel their time was wasted

### Special Cases

**Non-native English speakers:**
- Find a native speaker for at least one review pass
- Focus on idioms and phrasing that might sound "off"

**Don't know who to ask:**
- Writing communities and forums
- Colleagues in adjacent teams
- Professional editors (for high-stakes posts)

---

## Quick Reference: All Skills

| # | Skill Name | Phase |
|---|------------|-------|
| 0 | Topic Selection (3 Ps Test) | Before Everything |
| 1 | Goal Definition | Pre-Writing |
| 2 | Pattern Selection | Pre-Writing |
| 3 | Evidence-Based Claims | Writing |
| 4 | Conversational Voice | Writing |
| 5 | Single-Idea Paragraphs | Writing |
| 6 | Scannability | Writing |
| 7 | Show Don't Tell | Writing |
| 8 | Actionable Writing | Writing |
| 9 | Facts Check | Review |
| 10 | Focus Check | Review |
| 11 | Flow Check | Review |
| 12 | Component Review (Title, Intro, Ending) | Review |
| 13 | Pattern-Specific Review | Review |
| 14 | Pre-Publish Verification | Review |
| 15 | Self-Review Test | Review |
| 16 | Working with Reviewers | Collaboration |

---

## Human Voice (Avoiding AI-Sounding Writing)

### What Makes Writing Sound Human

**Be Authentic and Relatable:**
- Share your background when relevant
- Reveal what was going through your head during triumphs and tribulations
- Admit worries, frustrations, mistakes, and imperfections
- Be open about what you don't (yet) know
- Poke fun at yourself

**Write in Your Own Voice:**
- Use words you'd normally use (don't raid the thesaurus)
- Match your natural sentence length and complexity
- Let your tone show (enthusiastic, sarcastic, witty, reserved)
- Contractions and colloquialisms are fine if that's how you speak

**Test:** If a close friend read your article, would they recognize your personality?

### AI-Generated Writing Red Flags

| Red Flag | Description |
|----------|-------------|
| Unusually dense metaphors | High density of themed references maintained throughout |
| Overly flowery language | Consistently ornate/poetic prose |
| Lack of specific technical details | No concrete examples or real experience |
| Perfect thematic consistency | Theme maintained flawlessly without natural drift |
| Artificial emotional arc | Predictable: curiosity → challenge → triumph |
| Too-perfect structure | Follows idealized template |
| No genuine personal anecdotes | Missing specific, idiosyncratic details |
| **Excessive em dashes** | Multiple em dashes (—) per paragraph is a classic AI tell |

### Punctuation as AI Signal

**Em dashes are a red flag.** AI-generated content often overuses em dashes (—) as a crutch for connecting ideas. Human writers rarely use more than 1-2 em dashes per article.

**Fix em dash overuse:**
| Instead of | Write |
|------------|-------|
| "The system—which handles millions of requests—was failing" | "The system handles millions of requests. It was failing." |
| "We tried Redis—a popular choice—but it didn't fit" | "We tried Redis, a popular choice, but it didn't fit" |
| "Performance improved—dramatically—after the fix" | "Performance improved dramatically after the fix" |

**Rules:**
- Limit em dashes to 1-2 per entire article
- Replace with periods, commas, or parentheses
- If you see 3+ em dashes, rewrite those sentences
- Colons often work better for introducing explanations

### How to Sound More Human

**DO:**
- Include specific, idiosyncratic details from real experience
- Let your writing have natural variation in tone
- Include concrete technical details (code, numbers, commands)
- Share genuine personal anecdotes with messy, real-world details
- Allow natural drift in theme and style

**DON'T:**
- Maintain artificially consistent metaphors throughout
- Use perfectly structured emotional arcs
- Write prose that's consistently ornate
- Hit predictable narrative beats
- Remove all the "messy" human elements

### Human-Voice Checklist

- [ ] Includes at least one admitted uncertainty or mistake
- [ ] Has specific technical details (not just generalities)
- [ ] Contains a genuine personal anecdote with specific details
- [ ] Voice varies naturally (not perfectly consistent)
- [ ] Emotional moments feel earned, not manufactured
- [ ] Would pass the "friend recognition" test
- [ ] Contains at least one self-deprecating comment

### Examples

**AI-sounding (avoid):**
> "Zig was like a breath of fresh air in a smog-choked C++ cave. Gone were the cryptic templates and memory management migraines."

**Human-sounding (aim for):**
> "Zig lets you dereference null pointers and use freed memory. This led to long debugging sessions—just us, gdb, and the ninth cup of coffee—but it was comforting to see all the existing tools just work."

### Quick Transformations

| Instead of | Write |
|------------|-------|
| "We solved the problem" | "After three false starts and one embarrassing typo, we finally figured it out" |
| "Performance improved significantly" | "Latency dropped from 200ms to 15ms—I refreshed the dashboard three times because I didn't believe it" |
| "This approach is optimal" | "I'm not 100% sure this is the best approach, but it's working well so far" |
| "We chose Redis" | "We debated Redis vs Memcached for a week. Redis won because half the team already knew it—pragmatism over perfection" |

---

## Native English Style (Sentence Optimization)

### The Paramedic Method: 5-Step Clarity Process

**Step 1:** Bold the prepositions (of, in, for, with, by, to, from, etc.)
**Step 2:** Highlight "to be" verbs (is, was, are, were, be, being, been)
**Step 3:** Find the real actor and action
**Step 4:** Rebuild around a strong verb
**Step 5:** Cut remaining useless words

### Problem Sentence Red Flags

- Can't read aloud in one breath → too long
- Prepositional phrase clusters → "We were collaborating on integration across environments from the start..."
- Weak "to be" verbs → "The bug was located" vs "We found the bug!"
- Buried actor/action → who did what is unclear

### Before/After Examples

| Before | After |
|--------|-------|
| "An additional drawback with Zig is the young state of the ecosystem" | "Another drawback: Zig's young ecosystem complicates adoption" |
| "In the end, it was decided that the best solution was implementing it by means of a link" | "Ultimately, we implemented it by linking to..." |
| "The bug was then located" | "We found the bug!" |

### Words to Cut or Replace

**Throat clearing (cut entirely):**
- "The fact of the matter is that..."
- "What is most notable here is that..."
- "It is important to note that..."

**Redundancies (pick one):**
- basic fundamentals → fundamentals
- end result → result
- past history → history
- new innovations → innovations

**Wordy phrases → concise:**
| Wordy | Concise |
|-------|---------|
| In light of the fact that | Since |
| Despite the fact that | Although |
| In the event that | If |
| By means of | By/Using |
| In order to | To |
| At this point in time | Now |
| Has the ability to | Can |

**"Very + word" → single stronger word:**
- very important → crucial
- very fast → rapid
- very strange → bizarre

**Double negatives (simplify to affirmative):**
- ❌ "It's not impossible" → ✅ "It's possible" or "Possibly"
- ❌ "No tests without failures" → ✅ "Only failing tests"
- ❌ "Not uncommon" → ✅ "Common" or "Frequent"

**Superlatives and extremes (avoid unless provable):**

Words to avoid: only, best, fastest, easiest, always, never, perfect, impossible

**Why:**
- Hard to prove → readers lose trust
- Perceived as "fighting words" → invites comment section attacks
- If you use them, be prepared to defend with evidence

| Instead of | Write |
|------------|-------|
| "The fastest database" | "Achieved 50K QPS in our benchmark" |
| "Always use X" | "In most cases, X works well because..." |
| "The only solution" | "The approach we chose" |
| "Never do Y" | "Y can cause problems when..." |

### Clarity Killers to Avoid

**Muddled modifiers:**
- ❌ "Debugging the code, the error became clear" (error was debugging?)
- ✅ "As we debugged, the error became clear"

**Subject-verb disconnect:**
- ❌ "We weren't shocked that John, after six months of frustration with feature creep, changing deadlines, and stakeholder turnover, quit."
- ✅ "John quit after six months of frustration. We weren't shocked."

**Vague "it/that":**
- ❌ "It's in the repo but it's broken" (what's broken?)
- ✅ "The config is in the repo, but the search is broken"

**Startling shifts:**
- Don't switch between "you" and "users"
- Don't switch verb tense mid-paragraph

**One paragraph = one idea**

### Passive vs Active Voice

**Zombie test:** If you can add "by zombies" and it makes sense, it's passive.
- "The bug was located *by zombies*" → Passive ❌
- "We found the bug *by zombies*" → Doesn't work → Active ✅

**Use active voice (default):** clearer, more direct
**Passive is OK when:** actor unknown, blame avoided, or process described

### Transitional Words

**Continuation:** moreover, furthermore, additionally, similarly
**Contrast:** however, nevertheless, surprisingly, yet
**Consequence:** therefore, consequently, thus, as a result
**Connection:** "To achieve X, we...", "But there was a problem with X...", "The hardest part of X was..."

### The Read Aloud Test

**Most powerful technique:**
1. Read your draft out loud (really!)
2. Out of breath? → Sentence too long
3. Sounds weird? → Investigate
4. Stumble? → Readers will too

### Common English Errors

| Confused | Distinction |
|----------|-------------|
| it's / its | it's = it is; its = possessive |
| affect / effect | affect = verb; effect = noun |
| less / fewer | less = uncountable; fewer = countable |
| they're / their / there | they're = they are; their = possessive; there = location |

### Lard Factor (Measuring Success)

Formula: (Original words - Revised words) / Original words × 100

Example: 23 words → 10 words = (23-10)/23 = **57% reduction**

### Quick Reference: Style Rules

| Rule | Key Point |
|------|-----------|
| Sentence length | One breath max |
| Paragraph | One idea |
| Prepositions | Minimize clusters |
| "To be" verbs | Replace with action verbs |
| Actor/Action | Make clear early |
| Modifiers | Place near what they modify |
| Pronouns | Ensure clear reference |
| Tense | Keep consistent |
| Terms | Define once, use consistently |
| Voice | Active > Passive |
| Read aloud | The ultimate test |

---

## SEO & Metadata Skills

### Keywords Strategy

**Select 3-5 keywords:**
- Mix of: one broad popular term + specialized qualifiers
- Example: "Rust" (broad) + "async, performance, profiling" (specific)
- Think: What would your target reader search for?

**Use Google Trends (https://trends.google.com/):**
- Compare similar terms to find which is searched more
- Check rising vs declining interest
- Look at "Related Queries" for additional topics

### Title Tag Optimization

- Keep under 50-60 characters (browsers truncate)
- Put important keywords at the START
- Can add brand name at end if space permits

**Good:** `We Built a Postgres to FakeDB Migrator with Zig | ACME blog`
**Bad:** `Why and How the ACME Team Decided to Build...` (keywords cut off)

### Meta Description

- ~150 characters max
- Clear, compelling description of what reader gets
- Include keywords naturally
- Don't accept auto-generated defaults

**Good:** `ACME built a Postgres to FakeDB migration tool in Zig. Learn how Zig compared to C, C++ & Rust.`
**Bad:** `In this article, ACME staff engineer shares his experiences...` (keywords cut off)

### URL Structure

- Use lowercase + hyphens (not underscores)
- Include your keywords
- Keep it clean and short
- Avoid dates (makes content seem stale)

**Good:** `/postgres-fakedb-migrator-zig`
**Bad:** `/we_built_a_postgres_to_fakedb_migrator_with_zig`

### Hyperlinks

**NEVER hyperlink:** "here", "click here", raw URLs
**ALWAYS hyperlink:** Descriptive text about the linked content

**Good:** `...by linking to **RustyEncryption**` (hyperlinked)
**Bad:** `...which you can access **here**` (hyperlinked)

**Why:** Screen readers list links out of context; descriptive text helps accessibility.

### Image Metadata

**File names:** Use descriptive names (`zig-star-history.png` not `IMG123.png`)

**ALT text:**
- Describe what image shows
- Under 125 characters
- Include relevant keywords
- Skip for purely decorative images

### Tags/Topics

Consider both:
- **Relevance** - Is your article truly about this topic?
- **Reach** - How many followers does this tag have?

Strategy: Mix specialized tags (core audience) + 1-2 broad tags (exposure)

### Featured Images

- Always set `og:image` metadata
- Avoid the "sad gray box" on social shares
- Test with LinkedIn Post Inspector

### SEO Pre-Publish Checklist

- [ ] Keywords identified (3-5 terms)
- [ ] Title tag under 60 chars, keywords at start
- [ ] Meta description under 150 chars, compelling
- [ ] URL clean with keywords
- [ ] All hyperlinks working and descriptive
- [ ] Images have ALT text
- [ ] Featured image set

---

## Visual & Code Presentation Skills

### Headings

**Keep them short:** Shortest words that orient readers
**Put key words first:** Readers scan left to right
**Proper hierarchy:** H1 >> H2 >> H3 >> H4 (don't skip levels)

**Bad:** `Configuration A vs Configuration B: Throughput`
**Good:** `Throughput Results`

### Images

**Always add captions** - Explains what image shows
**Consider color-blindness** - 8% of men are color-blind; don't rely solely on color
**Check image rights** - Get permission, not forgiveness (violations cost thousands)
**Size appropriately** - Aim for <100KB, ensure labels are readable

### Code Examples

**Must be:**
- **Shareable** - Get clearance for closed-source code
- **Well-vetted** - No embarrassing mistakes
- **Realistic** - Compiles, secure (people copy-paste!)
- **Concise** - Omit irrelevant parts (use ... for omitted code)

**Display requirements:**
- Syntax highlighting (specify language)
- Legible in light AND dark mode
- Copy-pasteable (never images of code)
- Wrap at 80-120 characters
- Check indentation preserved

**Better options:**
- GitHub gists (easy embedding)
- Interactive playgrounds (Stackblitz, Sandpack)
- Link to full repo for context

### Tables

- Use for comparing multiple items
- Keep simple (complex tables break)
- Clear, short column headers
- Preview rendering

### Lists

- Use bullets for unordered, numbers for sequential
- Keep items parallel in structure
- Max 2 levels of nesting
- Preview rendering

### Visual Pre-Publish Checklist

- [ ] Title doesn't wrap awkwardly
- [ ] Headings short, keywords first
- [ ] Code has syntax highlighting
- [ ] Code copy-paste works correctly
- [ ] Images properly sized, readable labels
- [ ] Images have ALT text
- [ ] Tables/lists render correctly
- [ ] Checked on mobile
