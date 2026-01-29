# Pattern Examples: Real-World Blog Posts

Curated examples demonstrating each pattern from "Writing for Developers."

---

## How We Built It

### "A Search Engine in 80 Lines of Python"
**URL:** https://www.alexmolas.com/2024/02/05/a-search-engine-in-80-lines.html

**Why it works:**
- Progresses through components: crawler → inverted index → BM25 ranking → FastAPI UI
- Shows real constraints (async optimization: 20 min → 20 seconds)
- Honest about limitations—lists missing features rather than overselling
- Frames purpose philosophically ("bringing back the glory of the little guys")

**Techniques to borrow:**
- Slightly provocative title that delivers on its promise
- Balance technical depth with accessibility
- Acknowledge what's *not* included

---

### "I Have Written a JVM in Rust"
**URL:** https://andreabergia.com/blog/2023/07/i-have-written-a-jvm-in-rust/

**Why it works:**
- Opens with honest scope (what works, what doesn't)
- Systematic exploration: parsing → execution → values → bytecode → GC
- Personal voice: "It's quite mediocre, but it's mine and I love it"
- Diagrams for complex concepts (garbage collection)

**Techniques to borrow:**
- Lead with capabilities *and* limitations upfront
- Show genuine enthusiasm for the craft
- Use Rust's features as narrative elements (Result type solving control flow)

---

## Thoughts on Trends

### "Async Rust"
**URL:** https://bitbashing.io/async-rust.html

**Why it works:**
- Builds from fundamentals (why concurrency matters) before critiquing
- Catalogs specific pain points: lifetimes, `Arc`, `Pin`, recursive functions
- Balanced: acknowledges Rust's strengths while arguing async isn't the win it seems
- Conversational humor ("going to plaid," "Mickey Mouse games")

**Techniques to borrow:**
- Ground opinions in team experience, not theory
- Progress from accessible concepts to specific friction
- End with nuance—don't throw the baby out with the bathwater

---

### "Python Gets a JIT"
**URL:** https://tonybaloney.github.io/posts/python-gets-a-jit.html

**Why it works:**
- Progressive understanding: starts with crude interpreter loop
- Explains *why* this approach (copy-and-patch) vs alternatives
- Tempers disappointment (2-9% gains) by framing as foundation for future
- Technical depth (assembly, templates) remains accessible

**Techniques to borrow:**
- Compare approaches to highlight tradeoffs
- Frame modest results optimistically when justified
- Use "most people haven't heard of this" as teaching hook

---

## Bug Hunt (with Historical Narrative)

### "The Return of the Frame Pointers"
**URL:** https://www.brendangregg.com/blog/2024-03-17/the-return-of-the-frame-pointers.html

**Why it works:**
- Opens with the problem: broken flame graph image
- 20-year chronological arc: removal → broken profilers → resolution
- Personal anecdotes (Netflix, Sun Microsystems) ground the technical
- Vivid language: "winter of broken profilers"

**Techniques to borrow:**
- Start with visual evidence of the problem
- Use timeline as narrative structure
- Mix corporate experience with technical rigor
- Include future predictions to spark curiosity

---

## Pattern Identification Quick Reference

| Blog | Primary Pattern | Secondary |
|------|-----------------|-----------|
| Search Engine in 80 Lines | How We Built It | — |
| JVM in Rust | How We Built It | — |
| Async Rust | Thoughts on Trends | Lessons Learned |
| Python Gets a JIT | Thoughts on Trends | How We Built It |
| Return of Frame Pointers | Bug Hunt | Thoughts on Trends |
