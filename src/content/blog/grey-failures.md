---
title: 'Grey Failures: The Silent Killers of Distributed Systems'
description: 'Your monitoring is lying to you. Health checks pass, dashboards are green, but users are still having a bad time.'
pubDate: 'Feb 12 2026'
---

Your monitoring is lying to you.

Health checks pass. Dashboards are green. Alerts are silent.

But users are still having a bad time.

Welcome to **grey failures** — the silent killers of distributed systems.

## What Are Grey Failures?

Grey failures happen when:

- A server is "up" but responding slowly
- Network is working but dropping 2% of packets
- CPU is fine but one core is degraded
- The instance passes health checks but fails real requests

Traditional monitoring misses these because it asks: **"Is this thing alive?"**

The right question: **"Is this thing useful?"**

## How We Detect Grey Failures at Scale

### 1. Multi-signal detection

Don't trust just the instance. Compare instance metrics + client metrics.

If clients see errors but the instance looks fine — that's your grey failure.

The instance says "I'm healthy!" while users say "This is broken!" Trust the users.

### 2. Latency is a signal, not just errors

Errors are obvious. Latency creep is subtle.

A p99 that slowly climbs is often a grey failure brewing. By the time it becomes an error, you've already impacted users for minutes or hours.

### 3. Automate the response

By the time a human notices, users have suffered for 15+ minutes.

We got detection down to <4 minutes through automation. The system detects, validates, and begins mitigation before a human even knows there's a problem.

---

## The Key Insight

Grey failures are invisible to traditional monitoring because they exist in the space between "working" and "broken."

A server can be 95% healthy and still cause pain for the 5% of requests that hit the degraded path.

Your system probably has grey failures right now.

The question is: **do you know where?**

---

## How to Start Finding Them

1. **Compare perspectives**: What does the instance think? What do clients see? Discrepancies are clues.

2. **Watch latency distributions**: Not just averages — look at p95, p99. That's where grey failures hide.

3. **Track error locality**: Are errors coming from everywhere, or concentrated on specific instances?

4. **Automate detection**: Humans are too slow. Build systems that watch for you.

Grey failures are the problems that make you say "everything looks fine, but users are complaining." Once you learn to see them, you'll find them everywhere.
