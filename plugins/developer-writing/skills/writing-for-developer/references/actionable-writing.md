# Actionable Writing (Don't Make Reader Think)

Based on reviewer feedback and "Writing for Developers" principles.

---

## The Problem

Abstract writing forces readers to do the thinking themselves. They must interpret requirements, imagine scenarios, and figure out when advice applies to them.

Actionable writing does the thinking for readers. It provides:
- Specific conditions and thresholds
- Recognition signals they can observe
- Decision criteria they can apply immediately
- Concrete examples, not abstract descriptions

---

## Transform Abstract → Actionable

### General Transformations

| Abstract (Avoid) | Actionable (Write) |
|------------------|-------------------|
| "Consider your scaling requirements" | "If you have >10M rows, use partitioning" |
| "Performance may vary" | "Expect 50-200ms latency depending on query complexity" |
| "Teams often struggle with X" | "You'll hit this wall when daily inserts exceed 1M" |
| "There are several approaches" | "Use approach A for reads, approach B for writes" |
| "This depends on your needs" | "For OLTP: use X. For OLAP: use Y" |
| "At scale, problems emerge" | "Above 100GB, expect 2x query time without indexes" |
| "Eventually consistency issues arise" | "With >5 replicas, expect 50-100ms sync delays" |

### Replacing "It Depends"

Every "it depends" should be followed by specific conditions:

**Before:**
> "Whether to use caching depends on your workload."

**After:**
> "Use caching when:
> - Read/write ratio exceeds 10:1
> - Same queries repeat within 5-minute windows
> - You can tolerate 30-second stale data"

### Replacing Vague Adjectives

| Vague | Specific |
|-------|----------|
| "fast" | "<100ms" or "3x faster than baseline" |
| "large" | ">1TB" or ">10M rows" |
| "many" | "5-10" or "typically 8" |
| "significant" | "40% improvement" or "$50K/month savings" |
| "often" | "in 70% of cases" or "3 out of 4 teams" |
| "sometimes" | "when X condition is true" |

---

## The "How Do I Know When?" Test

For every claim, ask: "How does the reader know when this applies to them?"

### Examples

**Fails the test:**
> "At some point, you'll need to scale your database."

**Passes the test:**
> "Scale your database when:
> - Query latency exceeds 500ms for simple lookups
> - Storage hits 80% capacity
> - Connection pool exhaustion occurs more than once per week"

**Fails the test:**
> "Performance will degrade over time."

**Passes the test:**
> "Watch for these degradation signals:
> - Queries that took 10ms now take 100ms+
> - Increased CPU during off-peak hours
> - Growing query queue depth in monitoring"

---

## Don't List Requirements—Provide Decision Criteria

Listing requirements forces readers to evaluate whether they match. Decision criteria let them act immediately.

### Requirements (Avoid)

> "Requirements for this solution:
> - High availability
> - Low latency
> - Horizontal scalability
> - Cost efficiency"

**Problem:** Reader must interpret each term and assess their own needs.

### Decision Criteria (Write)

> "Choose this solution if:
> - You need <100ms read latency
> - You can tolerate eventual consistency (up to 5 seconds)
> - Your data grows >100GB/month
> - Budget allows $2-5K/month for infrastructure"

**Benefit:** Reader can immediately check each criterion against their situation.

---

## Don't Describe Problems—Show Recognition Signals

Abstract problem descriptions require interpretation. Recognition signals are observable.

### Abstract Description (Avoid)

> "Query performance can degrade over time as data accumulates, especially with complex joins and insufficient indexing."

**Problem:** Reader doesn't know what "degraded performance" looks like or how to detect it.

### Recognition Signals (Write)

> "Your queries are degrading when you observe:
> - Simple SELECT by ID taking >50ms (should be <10ms)
> - EXPLAIN plans showing sequential scans on tables >1M rows
> - Connection timeouts increasing week-over-week
> - Dashboard load times doubling quarter-over-quarter"

**Benefit:** Reader can check their monitoring right now.

---

## Don't Describe Solutions—Show Implementation

Describing what a solution does is less useful than showing how to implement it.

### Description (Avoid)

> "Connection pooling helps manage database connections efficiently by reusing existing connections rather than creating new ones."

### Implementation (Write)

> "Add connection pooling:
>
> ```python
> # Install: pip install sqlalchemy
> from sqlalchemy import create_engine
> engine = create_engine(
>     'postgresql://user:pass@host/db',
>     pool_size=20,          # concurrent connections
>     max_overflow=10,       # burst capacity
>     pool_timeout=30        # wait time for connection
> )
> ```
>
> Set pool_size to your typical concurrent query count. Start with 20 and adjust based on monitoring."

---

## Actionable Writing Checklist

For each section of your article, verify:

- [ ] Every "it depends" is followed by specific conditions
- [ ] Numbers replace words like "fast," "many," "large"
- [ ] Reader can take action without additional research
- [ ] Recognition signals provided, not just problem descriptions
- [ ] Decision criteria given, not just requirements listed
- [ ] Thresholds are specific (">1M rows" not "large datasets")
- [ ] Time-based triggers are quantified ("weekly" not "regularly")
- [ ] Examples are concrete, not hypothetical

---

## Quick Transformations

### From Abstract Advice

**Before:**
> "Consider implementing caching for frequently accessed data."

**After:**
> "Add Redis caching for data accessed >100 times/minute. Start with a 5-minute TTL and adjust based on staleness tolerance."

### From Vague Warnings

**Before:**
> "Be careful with this approach as it can cause issues at scale."

**After:**
> "This approach breaks above 10K requests/second. At that point, switch to the batch processing pattern described in Section 3."

### From General Recommendations

**Before:**
> "You should monitor your system for performance issues."

**After:**
> "Set up these three alerts:
> 1. P99 latency > 500ms (immediate investigation)
> 2. Error rate > 1% (on-call notification)
> 3. CPU > 80% sustained for 10 minutes (capacity planning trigger)"

---

## The Cognitive Load Principle

Every abstract statement adds cognitive load. Readers must:
1. Interpret your meaning
2. Apply it to their situation
3. Decide if it's relevant
4. Figure out what to do

Actionable statements reduce this to:
1. Check if condition applies
2. Take specified action

**Goal:** Minimize the gap between reading and doing.

---

## Testing Your Writing

### The "What Do I Do?" Test

After each paragraph, ask: "If I were the reader, would I know exactly what to do next?"

If the answer is "it depends," you haven't been specific enough.

### The "Number Check"

Scan your article for vague quantity words: many, few, large, small, fast, slow, often, sometimes.

Each one should either:
- Be replaced with a specific number
- Include conditions that make it specific

### The "Action Verb Check"

Actionable writing uses action verbs: configure, set, add, enable, run, check.

Abstract writing uses state verbs: is, has, exists, contains, provides.

If a section has more state verbs than action verbs, rewrite it to focus on what the reader should do.
