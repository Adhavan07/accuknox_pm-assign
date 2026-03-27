# AccuKnox — Product Management Trainee Assignment

**Problem chosen:** [2] Alert Triage Workflow  
**Candidate:** Adhavan  

---

## Problem Statement

Security engineers at AccuKnox receive 50–200 cloud security alerts per day across
multiple AWS, GCP, and Kubernetes environments. Triage happens across disconnected
tools — engineers context-switch between the alert console, AWS CloudTrail, runbooks,
and Slack just to investigate a single alert. This inflates MTTR, buries critical
alerts under noise, and means the same pattern gets re-investigated from scratch
every time it recurs.

---

## Solution — 3-Screen Triage Workflow

| Screen | What it does |
|--------|-------------|
| Alert Queue | Risk-scored feed (1–10) sorted by severity × blast radius × data sensitivity |
| Investigation Panel | Inline context: CloudTrail timeline, blast radius, similar past alerts, compliance violations |
| Resolution Playbook | Pre-populated step-by-step playbook with CLI commands, progress tracking, audit log |

---

## Figma Wireframes

[View wireframes →](<https://www.figma.com/proto/NOmUwYAoB0DdtVIwybL04y/Accuknox_Assignment?node-id=1-7&p=f&t=z65bGbLX8e564wZ0-1&scaling=scale-down&content-scaling=responsive&page-id=0%3A1>)

---

## Files in this repo

| File | Description |
|------|-------------|
| `AccuKnox_Alert_Triage_Writeup.docx` | 1-page write-up with RICE prioritization, success metrics, edge cases, and dev action items |

---

## Key Design Decisions

- **Risk score** combines severity + data classification + blast radius + asset criticality — engineers triage by number, not intuition
- **Investigation panel** surfaces CloudTrail data inline — zero context switching to AWS console
- **Playbook** is pre-populated from past resolutions — institutional memory baked into the product
- **Compliance auto-mapping** (CIS, SOC 2, PCI-DSS) adds enterprise value with minimal engineering effort

---

## Success Metrics

- MTTR reduced by ≥ 30% in 90 days  
- Critical alert acknowledgement within 15 min > 90%  
- 60%+ of alerts resolved via playbook steps  
- Context switches per alert session: 4–6 tools → ≤ 1

---

## Tech Background

AWS · Kubernetes · Prometheus · Grafana · DevOps
