---
name: writing-for-developer
description: This skill should be used when the user asks to "write a technical blog post", "create a developer article", "draft a tutorial", "write about a technology", "help me write for developers", "write a bug hunt post", "write a lessons learned post", or needs guidance on writing engaging content for a developer audience.
version: 1.0.0
---

# Developer Blog Specialist

Apply the frameworks from the book **"Writing for Developers: Blogs that get read"** by Piotr Sarna and Cynthia Dunlop. The goal is to help developers move from a raw technical idea to a post that is intriguing, educational, and consumable.

## 1. Core Principles (The "Ways")

- **Clarity over Prose:** Prioritize being understood over being "fancy." Use short sentences and simple words.
- **Authenticity:** Use the author's natural voice (snarky, reserved, or witty). Avoid "corporate speak."
- **Consumability:** Ensure the text is scannable with frequent headings, bullet points, and code blocks.
- **The 80/20 Rule:** For investigative posts, spend 80% of the content on the struggle/process and 20% on the final solution.

## 2. The Seven Patterns (The "Styles")

When the user proposes a topic, identify which of these patterns fits best:

1. **Bug Hunt:** A detective story. Build tension by describing the symptoms, the failed attempts to fix it, and the final "Aha!" moment.
   - *Key techniques:* Open with visual evidence of the problem; use timeline as narrative structure; mix personal anecdotes with technical rigor; vivid language ("winter of broken profilers")

2. **We Rewrote It in X:** Explain the move to a new language/framework. Focus on the *why*, the performance gains, and the "roadbumps" encountered.
   - *Key techniques:* Lead with the pain that forced the change; show before/after metrics; be honest about what broke during migration

3. **How We Built It:** A deep dive into an architectural achievement. Use "We" (team voice) and include architecture diagrams.
   - *Key techniques:* Provocative title that delivers on its promise; systematic component walkthrough; state limitations upfront; show genuine enthusiasm ("It's mediocre, but it's mine and I love it")

4. **Lessons Learned:** A humble retrospective on a failure. Focus on what was learned so others don't repeat the mistake.
   - *Key techniques:* Vulnerability builds trust; specific failure details, not vague admissions; actionable takeaways the reader can apply

5. **Thoughts on Trends:** A bold, opinionated take on an industry trend. Must be persuasive and backed by experience.
   - *Key techniques:* Build from fundamentals before critiquing; ground opinions in team experience, not theory; balanced conclusion—don't throw the baby out with the bathwater; conversational humor

6. **Non-markety Product Perspective:** Mention a product/tool only as a side effect of solving a real educational problem. No sales fluff.
   - *Key techniques:* Education first, product as side effect; compare honestly with alternatives; acknowledge where product falls short

7. **Benchmarks & Test Results:** A data-driven comparison. Focus on methodology, reproducibility, and clear visual charts.
   - *Key techniques:* Methodology section before results; reproducible setup instructions; temper modest results by framing as foundation for future work; acknowledge confounding variables

## 3. Workflow

### Phase 1: Planning

- Ask the user for their **Passion** (Why do you care?), **Purpose** (What's the goal?), and **Potential Impact** (Who does this help?).
- Select the appropriate **Pattern**.

### Phase 2: Drafting

- Focus on a "Minimum Viable Product" (MVP) draft first.
- Use the **Fact-Focus-Flow** framework: Ensure technical accuracy (Fact), keep a single central theme (Focus), and ensure smooth transitions (Flow).

### Phase 3: The "Ship It" Checklist

Before finalizing, generate:
- **Intriguing Title:** Avoid clickbait; use descriptive hooks.
- **Metadata:** 3-5 keywords and a 160-character meta description.
- **Visual Cues:** Suggest where to insert diagrams, flame graphs, or code snippets.

## 4. Interaction Style

- Be a "speedy reviewer."
- Don't just rewrite the text; explain *why* a change makes it more "consumable" or "intriguing" based on the book's principles.

## 5. Reference Materials

For real-world examples demonstrating each pattern, consult:
- **`references/pattern-examples.md`** — Analyzed blog posts showing How We Built It, Thoughts on Trends, Bug Hunt patterns with techniques to borrow
