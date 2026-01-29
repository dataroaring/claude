# SEO & Metadata Skills

Based on "Writing for Developers" by Piotr Sarna & Cynthia Dunlop

---

## Keywords Strategy

### Selecting Your Keywords

Identify 3-5 keywords for your article:
- Mix of: one broad popular term + specialized qualifiers
- Example: "Rust" (broad) + "async, performance, profiling" (specific)

Think: What would your target reader search for when exploring this topic?

### Using Google Trends (https://trends.google.com/)

Compare terms to determine:
- Which term is searched more often
- Rising vs declining interest
- Related terms people are searching for
- Seasonal spikes (e.g., around conferences)

**Tips:**
- Expand timeframe to 2+ years for trend patterns
- Choose "topics" over "search terms" when available (more accurate)
- Check "Related Queries" for additional topic ideas

**Search operators:**
- Quotation marks: `"streaming data"` - exact phrase only
- Plus sign: `Postgres + PostgreSQL` - either term
- Minus sign: `Rust -movie` - exclude results containing "movie"

### Where to Use Keywords

Once you've identified your keywords, include them in:
- Title (at the beginning if possible)
- Headings and subheadings
- Meta description
- URL
- ALT text for images
- Body text (naturally, not forced)

---

## Title Tag Optimization

The `<title>` tag determines:
- Browser tab title
- Bookmark text
- Social media link previews
- Search result titles (usually)

### Guidelines

- Keep under 50-60 characters (browsers truncate beyond this)
- Put important keywords at the START
- Can add brand name at end if space permits
- Must be similar to H1 (search engines penalize mismatches)

### Techniques

**Shorten if needed:**
- Replace "and" with "&"
- Replace long em dashes (—) with pipes (|) or colons (:)

**Add brand if short enough:**
- "We Built a Migrator with Zig | ACME blog" (59 chars)

### Examples

**Good:**
```
We Built a Postgres to FakeDB Migrator with Zig | ACME blog
```
- Keywords (Postgres, FakeDB, Zig) appear early
- Brand added at end
- 59 characters

**Bad:**
```
Why and How the ACME Engineering Team Decided to Build a New Data Migrator (Postgres to FakeDB) with Zig
```
- Keywords (Postgres, FakeDB, Zig) get cut off
- Too much preamble before the important words

---

## Meta Description

The `<meta name="description">` tag determines:
- Link preview blurbs
- Search result descriptions (often)
- First impression for deciding whether to click

### Guidelines

- ~150 characters max
- Clear, compelling description of what reader gets
- Include keywords naturally
- Focus on reader value, not author credentials
- Don't accept auto-generated defaults—craft it carefully

Google bolds the user's search terms in result descriptions, so including keywords helps your result stand out.

### Examples

**Good:**
```
ACME built a Postgres to FakeDB data migration tool in Zig. Learn how Zig compared to C, C++ & Rust and access the open source tool.
```
- Keywords appear early
- States what reader will get
- Mentions open source (reader value)

**Bad:**
```
In this article, ACME staff engineer PretendPiotr shares his experiences creating a new data migration tool that enables faster migrations from Postgres to FakeDB. And he built it in Zig.
```
- Keywords (Postgres, FakeDB, Zig) get cut off
- Loaded with words reader doesn't care about
- All about the author, not what's in it for reader

---

## URL Structure

### Guidelines

- Use lowercase throughout
- Separate words with hyphens (not underscores)
- Include your keywords
- Keep it clean and short
- Avoid dates in URL (makes content seem stale)

URL length doesn't affect search ranking, but clean URLs look more professional.

### Examples

**Good:**
```
/postgres-fakedb-migrator-zig
```

**Bad:**
```
/we_built_a_postgres_to_fakedb_migrator_with_zig
```
- Underscores instead of hyphens
- Unnecessarily long

**Bad:**
```
/database-zigzagging
```
- "Zig" keyword not recognizable as separate word

---

## Hyperlinks

### What Text to Hyperlink

**NEVER hyperlink:**
- "here" or "click here"
- Raw URLs
- Generic phrases ("learn more", "read this")

**ALWAYS hyperlink:**
- Descriptive text about the linked content

### Why This Matters

1. **Helps readers** decide if they want to click
2. **Helps search engines** understand content relationships
3. **Critical for accessibility** - screen readers often list links out of context

Imagine a visually impaired reader hearing: "here, click here, here, read more, here..." vs. "RustyEncryption library, Zig documentation, performance benchmark results..."

### Examples

**Good:**
```
Ultimately, we implemented that encryption layer by linking to RustyEncryption.
                                                              ^^^^^^^^^^^^^^^^ (hyperlinked)
```

**Bad:**
```
Ultimately, we implemented that encryption layer by linking to RustyEncryption, which you can access here.
                                                                                                     ^^^^ (hyperlinked)
```

### Always Verify

Before publishing:
- Click every link to confirm it works
- Verify links lead to expected pages
- Check that documentation links haven't moved (they frequently do)

---

## Image Metadata

### File Names

**Use descriptive names:**
- ✅ `zig-star-history.png`
- ✅ `postgres-fakedb-architecture.png`
- ❌ `IMG123.png`
- ❌ `screenshot.png`

### ALT Text

ALT text is critical for:
- Accessibility (screen readers)
- SEO (search engines)
- Fallback when images fail to load

**Guidelines:**
- Describe what the image shows
- Under 125 characters (screen reader cutoff)
- Include relevant keywords naturally
- Skip ALT text for purely decorative images

**Example:**
```
ALT: "The ziglang/zig GitHub star history from 2016 to 2024. Between 2022 & 2024, the stars surged from 10K to 30K."
```

**Avoid:**
- "This image shows..."
- "Screenshot of..."
- Just listing keywords without context

---

## Tags/Topics (Platform-Specific)

For platforms like Medium, consider both:

### Relevance
- Is your article truly about this topic?
- Would someone following this tag find value in your article?
- Fleeting mention ≠ deserving a tag

### Reach
- How many followers does this tag have?
- How many competing articles?
- Big fish in small pond vs. small fish in big pond

### Strategy

Mix:
- Specialized tags (your core audience, less competition)
- 1-2 broad tags (exposure to wider audience)

Example for a Zig + Postgres article:
- "Zig" (core, small but dedicated audience)
- "Postgresql" (relevant, moderate audience)
- "Programming" (broad, 6.9M followers)

---

## Featured/Thumbnail Images

### Why It Matters

Without a featured image, your article appears as a "sad gray box" when shared on social media. Even if YOU upload an image when sharing, others who share your article won't.

### Setting the Image

Set `og:image` metadata (Open Graph protocol) to ensure your preferred image displays on social shares.

Many platforms auto-set this when you specify a "Featured Image."

### What to Use

Good options:
- Flame graphs
- Data visualizations
- Code screenshots (decorative, not functional)
- Architecture diagrams
- Article screenshot (if not into graphics)
- Brand logo (if recognizable)

### Testing

Use LinkedIn Post Inspector (https://www.linkedin.com/post-inspector) to:
- Preview how your post will look
- See which metadata is being used
- Identify what to fix

---

## Open Graph Metadata

Open Graph (created by Facebook) controls social media previews.

### Basic Tags

```html
<meta property="og:site_name" content="http://www.mysite.com">
<meta property="og:locale" content="en-us">
<meta property="og:type" content="article">
<meta property="og:url" content="https://www.mysite.com/my/great-article">
<meta property="og:title" content="My great title">
<meta property="og:image" content="http://www.mysite.com/img/thumbnail.png">
```

### Twitter/X Cards

```html
<meta property="twitter:site" content="@my_handle">
<meta property="twitter:title" content="My great title">
<meta property="twitter:card" content="This is the best article ever.">
<meta property="twitter:image" content="http://www.mysite.com/img/thumbnail.png">
```

---

## Pre-Publish Checklist

- [ ] Keywords identified (3-5 terms)
- [ ] Title tag under 60 characters, keywords at start
- [ ] Meta description compelling, under 150 characters
- [ ] URL clean, lowercase, hyphens, includes keywords
- [ ] All hyperlinks tested and working
- [ ] Hyperlink text is descriptive (not "here")
- [ ] Images have descriptive file names
- [ ] Images have ALT text under 125 characters
- [ ] Tags/topics selected (relevance + reach)
- [ ] Featured image set (og:image)
- [ ] Social preview tested (LinkedIn Post Inspector)
