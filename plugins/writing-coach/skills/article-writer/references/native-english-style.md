# Native English Writing Skills & Styles

Based on "Writing for Developers" by Piotr Sarna & Cynthia Dunlop

---

## 1. Sentence Optimization (The Paramedic Method)

### Targeting Problem Sentences

Look for these red flags:
- **Overly long sentences** - can't read aloud in one breath
- **Prepositional phrase clusters** - "We were collaborating on integration across environments from the start of our project..."
- **Weak "to be" verbs** - "The bug was then located" vs "We found the bug!"
- **Buried actor/action** - when who did what is unclear or revealed too late

### The 5-Step Clarity Process

**Step 1: Bold the prepositions**

Common prepositions:
about, above, across, after, against, along, among, around, as, at, before, behind, beneath, beside, between, by, during, for, from, in, into, like, near, of, off, on, out, over, through, to, toward, under, upon, with, within, without

**Step 2: Highlight "to be" verbs**

Forms: am, is, are, was, were, be, being, been

**Step 3: Find the real actor and action**

Ask: Who/what is doing something? What are they doing?

**Step 4: Rebuild around a strong verb**

Put the actor and action upfront. Minimize words before the subject.

**Step 5: Cut remaining useless words**

If a word doesn't enhance understanding or tone, cut it.

### Before/After Examples

| Before | After |
|--------|-------|
| "An additional drawback with Zig is the young state of the ecosystem, though we hope that this is not going to continue over the long term." | "Another drawback: Zig's young ecosystem complicates adoption." |
| "In the end, it was decided that the best solution was implementing it by means of a link to an existing Rust implementation." | "Ultimately, we implemented that encryption layer by linking to RustyEncryption." |
| "The bug was then located." | "We found the bug!" |
| "One of the mind-blowing things about Zig is that cross compilation is also a core feature of the language." | "Zig's cross compilation is mind-blowing." |

---

## 2. Words to Cut or Replace

### "Blah blah is that" openings (throat clearing)

Cut these slow windups:
- ❌ "The fact of the matter is that..."
- ❌ "What is most notable here is that..."
- ❌ "It is important to note that..."
- ✅ Just state your point directly

### Redundancies

Eliminate duplicate meanings:
- basic fundamentals → fundamentals
- end result → result
- merge together → merge
- past history → history
- new innovations → innovations
- completely finished → finished
- advance planning → planning

### "Very + word"

Replace with a single stronger word:
- very strange → bizarre, peculiar, uncanny
- very important → crucial, essential, vital
- very fast → rapid, swift, blazing
- very good → excellent, superb, outstanding

**Tip:** Ask AI "Suggest 30 words that mean 'very [adjective]'"

### Phrases that should be one word

| Wordy Phrase | Concise Alternative |
|--------------|---------------------|
| In light of the fact that | Since |
| Despite the fact that | Although |
| In the event that | If |
| By means of | By / Using |
| A careless way of coding | Careless coding |
| Is indicative of | Indicates |
| In order to | To |
| Due to the fact that | Because |
| At this point in time | Now |
| In the near future | Soon |
| Has the ability to | Can |
| Is able to | Can |

### Double negatives

Simplify to affirmative:
- ❌ "It's not impossible for..." → ✅ "It's possible that..." / "Possibly"
- ❌ "No tests without failures..." → ✅ "Only failing tests..."
- ❌ "Not uncommon" → ✅ "Common" / "Frequent"
- ❌ "Don't forget to not ignore..." → ✅ "Remember to check..."

### Superlatives and extremes

Avoid unless you can prove them:
- only, best, fastest, easiest, always, never, perfect, impossible

**Why:**
- Hard to prove → readers lose trust
- Perceived as "fighting words" → invites attacks in comments
- If you use them, be prepared to defend with evidence

---

## 3. Common Clarity Killers

### Muddled modifiers

The modifier should be near what it modifies:

❌ "Debugging the code, the error became clear."
(Sounds like the error was debugging)
✅ "As we debugged the code, the error became clear."

❌ "Coding quickly makes you a better programmer."
(Coding fast? Or will quickly make you better?)
✅ "Coding regularly makes you a better programmer quickly."

❌ "I'll read the proposal and schedule your presentation tomorrow."
(What happens tomorrow?)
✅ "Tomorrow, I'll read the proposal and schedule your presentation."

### Disconnects (subject far from verb)

Keep subject → verb → object close together:

❌ "We weren't entirely shocked that John, after six months of frustration with endless feature creep, changing deadlines, and stakeholder turnover, quit."

✅ "John quit after six months of frustration with endless feature creep, changing deadlines, and stakeholder turnover. We weren't entirely shocked."

❌ "The new algorithm, which can significantly reduce the computational complexity and memory footprint of deep learning models by surgically removing redundant connections, had a serious bug."

✅ "The new algorithm had a serious bug. It was designed to reduce computational complexity and memory footprint by removing redundant connections."

### Vague "it/that" references

Ensure clear reference:

❌ "It's somewhere in the repo but it's broken."
(What's broken? The thing or the repo?)
✅ "The config file is somewhere in the repo, but the repo's search is broken."

❌ "The report mentioned a major issue, but it lacked a resolution."
(The report lacks resolution? Or the issue?)
✅ "The report mentioned a major issue but didn't include a resolution."

### Punctuation overload

Too many punctuation marks in one sentence makes it intimidating:

❌ "Push more logic into the database itself: letting it process as much as possible locally—which is (usually) great for 'performance'—and then return the results to the users... or some middleware."

✅ "Push more logic into the database. Let it process as much as possible locally, which usually improves performance. Then return results to users or middleware."

### Startling shifts

**Person shifts:**
❌ Starting with "This provides you with" then shifting to "Users gain the ability to"
✅ Pick one (preferably "you") and stick with it

**Tense shifts:**
❌ "We were in the middle of a meeting" → "And then everything suddenly stops"
✅ "We were in the middle of a meeting" → "And then everything suddenly stopped"

### Inconsistent tech terms

Define once, use consistently:

✅ "The blah (also known as blahblah and blahblahblah) is..."
Then use "blah" consistently throughout.

❌ Don't randomly switch between "the blah," "blahblah," and "blahblahblah" in different sentences.

### Perplexed paragraphs

**One paragraph = one idea.**

A paragraph can have:
- One big idea with supporting facts
- Several closely related ideas that build on each other

A paragraph should NOT:
- Wander into unrelated ideas
- Cover multiple separate topics

If you shift to a new idea, start a new paragraph.

---

## 4. Transitional Words & Phrases

Use these to connect ideas and signal what's coming:

### Continuation/Addition
again, as expected, certainly, furthermore, moreover, naturally, similarly, additionally, also

### Contrast/Surprise
interestingly, nevertheless, remarkably, surprisingly, however, yet, still, although, but

### Consequence/Result
consequently, evidently, ultimately, significantly, therefore, thus, as a result, hence

### Time/Sequence
finally, meanwhile, subsequently, then, next, first, afterward, eventually

### Connecting to previous ideas ($WYWTAB = what you were talking about before)
- "To achieve $WYWTAB, we had to..."
- "By implementing $WYWTAB, we..."
- "$WYWTAB allowed us to..."
- "But there was a problem with $WYWTAB..."
- "The hardest part of $WYWTAB was..."
- "After $WYWTAB, we decided it was time for..."

---

## 5. Passive vs Active Voice

### The Zombie Test

If you can add "by zombies" and it makes sense, it's passive voice:
- "The bug was then located *by zombies*." → Makes sense → Passive ❌
- "We found the bug *by zombies*." → Doesn't work → Active ✅

### Active voice (default choice)

**Use for:**
- Clarity - shows who did what
- Directness - fewer words
- Engagement - more dynamic

**Examples:**
- ❌ "The system was upgraded by the team."
- ✅ "The team upgraded the system."

### Passive voice (acceptable in specific cases)

**Use when:**
- You don't know who did something
- You don't want to assign blame
- The action matters more than the actor

**Examples:**
- ✅ "The build was broken, so we started to investigate." (unknown cause)
- ✅ "Mistakes were made." (avoiding blame - though often criticized)
- ✅ "The data is encrypted before transmission." (process description)

---

## 6. The Read Aloud Test

**The most powerful technique for catching problems:**

1. Read your draft out loud (really, not just in your head)
2. If you run out of breath → sentence is too long
3. If something sounds weird → investigate further
4. If you stumble → readers will stumble too

**What it catches:**
- Missing words
- Awkward phrasing
- Rhythm problems
- Overly complex sentences
- Unnatural dialogue

**If speaking aloud is embarrassing:**
At minimum, whisper it audibly to yourself. The physical act of speaking activates different brain processes than silent reading.

---

## 7. Common English Errors

### Frequently confused words

| Words | Distinction |
|-------|-------------|
| it's / its | it's = it is; its = possessive (no apostrophe) |
| they're / their / there | they're = they are; their = possessive; there = location |
| affect / effect | affect = verb (usually); effect = noun (usually) |
| adverse / averse | adverse = harmful; averse = opposed to |
| less / fewer | less = uncountable (water); fewer = countable (drops) |
| comprise / compose | "The whole comprises the parts" / "The parts compose the whole" |
| imply / infer | Speaker implies; listener infers |
| principal / principle | principal = main/head; principle = rule/belief |
| compliment / complement | compliment = praise; complement = complete/match |

### Common grammar mistakes

| Mistake | Correction |
|---------|------------|
| "Between you and I" | "Between you and me" |
| "Could of" | "Could have" |
| "Alot" | "A lot" (two words) |
| "Irregardless" | "Regardless" |
| "Literally" (for emphasis) | Use only for actual literal meaning |

**Reference:** Paul Brians' "Common Errors in English Usage" (https://brians.wsu.edu/common-errors/)

---

## 8. Title Writing Skills

### Qualities of great titles

- **Short and crisp** - no fluff words, every word earns its place
- **Playful, provocative, or mysterious** - wordplay welcome
- **Technical and targeted** - terms your audience recognizes
- **Feature keywords** - terms readers search for

### Avoid in titles

- WORDS IN ALL CAPS
- Excessive exclamation marks!!!
- Emojis 🚀
- Profanity
- Clickbait that doesn't deliver

### Two-part title technique

"[Catchy phrase]: [Descriptive subtitle]"

Examples:
- "Herding elephants: Lessons learned from sharding Postgres at Notion"
- "Ship Shape: How we keep our fleet in order"
- "Moore's Scofflaws: The chip industry's broken promises"

### Great title examples

- "How a Single Line of Code Made a 24-core Server Slower Than a Laptop"
- "Rust After the Honeymoon"
- "Dumpster Diving the Go Garbage Collector"
- "Lies We Tell Ourselves to Keep Using Golang"

---

## 9. Measuring Revision Success: Lard Factor

Calculate how much "fat" you trimmed:

**Formula:** (Original words - Revised words) / Original words × 100

**Example:**
- Original: 23 words
- Revised: 10 words
- Lard factor: (23-10) / 23 = 57% reduction

A high lard factor (40-60%) on a clunky sentence indicates successful revision.

---

## Quick Reference: Native English Style Rules

| Skill | Key Rule |
|-------|----------|
| Sentence length | One breath = one sentence max |
| Paragraph focus | One idea per paragraph |
| Prepositions | Minimize clusters |
| "To be" verbs | Replace with action verbs when possible |
| Actor/Action | Make clear early in sentence |
| Modifiers | Place near what they modify |
| Pronouns (it/that) | Ensure clear reference |
| Tense | Keep consistent throughout |
| Terms | Define once, use consistently |
| Voice | Active > Passive (usually) |
| Redundancy | Cut duplicate meanings |
| Transitions | Connect ideas explicitly |
| Read aloud | The ultimate clarity test |

---

## Editing Prioritization

**Don't optimize every sentence equally.** Focus your limited editing energy where it matters most.

### Priority 1: Most Prominent Sentences

These are what readers see first and remember longest:
- **Opening sentence** - Sets the tone for entire article
- **Introduction paragraph** - Determines if reader continues
- **First sentence of each section** - Orients readers after heading
- **Conclusion** - What readers take away

**Rule:** Spend 50% of your editing time on these sentences.

### Priority 2: Most Important Sentences

These carry your key messages:
- **Key findings** - The "so what" of your article
- **Recommendations** - What you want readers to do
- **Surprising claims** - Where readers will be skeptical
- **Technical explanations** - Where clarity is critical

### Priority 3: Most Muddled Sentences

These actively confuse readers:
- Sentences you re-read while writing
- Sentences with 3+ prepositional phrases
- Sentences where you're not sure what you meant
- Anything a reviewer flagged as unclear

### What to Skip

**Don't over-engineer:**
- Supporting examples (if the point is clear)
- Transitional sentences (if flow is okay)
- Background context (if it's accurate enough)

**Aim for "good enough"** - Perfection is the enemy of publication. A slightly awkward sentence in paragraph 7 won't kill your article, but spending hours polishing it might kill your motivation.

### The 80/20 Rule for Editing

80% of your article's impact comes from 20% of its sentences. Find that 20% and make it excellent. Let the rest be merely good.

---

## Process for Sentence Optimization

1. **Target** - Flag sentences that are long, clunky, or unclear
2. **Mark up** - Bold prepositions, highlight "to be" verbs
3. **Identify** - Find the real actor and action
4. **Rebuild** - Rewrite around a strong verb
5. **Cut** - Remove remaining useless words
6. **Read aloud** - Test for natural flow
7. **Move on** - Don't over-engineer; aim for "good enough"

Focus optimization on:
- Most prominent sentences (introduction)
- Most important sentences (key findings)
- Most muddled sentences (embarrassingly unclear)
