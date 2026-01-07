# Repo Health Audit Pipeline

This pipeline analyzes how a repository evolves over time to surface
design risk, decay, and ownership gaps.

## 1. Inventory & Baseline
Purpose: Establish what exists and how it has changed.

Scripts:
- triage_scan.py
- cherry_pick_filter.py

Outputs:
- Full artifact inventory
- Change frequency
- Last-modified timelines

---

## 2. Change & Churn Analysis
Purpose: Identify where risk concentrates through repeated change.

Scripts:
- triage_group_by_date.py
- triage_heatmap.py

Outputs:
- Change clustering
- Hot paths vs ignored paths
- Silent risk accumulation

---

## 3. Narrative Extraction
Purpose: Convert raw signals into human-readable risk narratives.

Scripts:
- swbst_extractor.py
- cow_extractor.py
- backlog_ticket_generator.py

Outputs:
- Risk stories
- Refactor / archive candidates
- “Do not ship” indicators

---

## 4. Agent & Automation Health (Optional Module)
Purpose: Assess automation reliability and governance drift.

Scripts:
- agent_check.py
- agent_launcher.py
- auto_monitor.py

Outputs:
- Agent health signals
- Automation fragility warnings
- Governance gaps

---

## 5. Audit Findings
Purpose: Produce evidence leaders can act on.

Outputs:
- Ranked findings
- Ownership gaps
- Structural risk summaries
