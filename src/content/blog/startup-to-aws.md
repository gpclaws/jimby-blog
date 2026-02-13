---
title: 'From Startup to AWS: What 1M Instances Taught Me'
description: 'I went from a startup with 100M users to AWS managing 1M instances. Here is what surprised me.'
pubDate: 'Feb 12 2026'
---

I went from a startup with 100M users to AWS managing 1M instances. Here's what surprised me.

At **Hike Messenger**, we moved FAST.

- Built a dating feature backend in 1 week
- Shipped India's first UPI payments on chat
- "Move fast, fix things later"

Then I joined AWS.

---

At AWS, I learned: **speed without reliability is just chaos waiting to happen.**

Managing infrastructure at 1M instance scale taught me three lessons:

## 1. Automation isn't optional — it's survival

We reduced incident response from 40 minutes to 5 minutes. Not by working faster. By building systems that respond for us.

When you're at scale, humans can't keep up. The only way to survive is to automate the predictable so you can focus on the unknown.

## 2. "Works on my machine" doesn't scale

What works for 1,000 instances will break at 100,000. What works at 100,000 will break at 1M.

You have to design for the scale you haven't hit yet. This means:
- Testing failure modes before they happen
- Building health systems that see problems before users do
- Assuming every component will fail, and designing for it

## 3. The best features are invisible

Health systems, grey failure detection, automated recovery — users don't see these.

But they feel it when they're missing.

The best reliability work is invisible work. If users notice your reliability system, it has already failed.

---

## The biggest shift?

**Startup:** "How fast can we ship?"

**AWS:** "How do we ship fast AND sleep at night?"

Both matter. The best engineers know when to optimize for which.

The lesson I carry: **Speed and reliability aren't opposites. They're partners.** When you build systems that let you move fast *safely*, you get the best of both worlds.
