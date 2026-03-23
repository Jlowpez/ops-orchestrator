# ops-orchestrator

> Multi-agent operations orchestrator — the capstone of a 5-agent agentic AI platform.

![CI](https://github.com/Jlowpez/ops-orchestrator/actions/workflows/ci.yml/badge.svg)
![Phase](https://img.shields.io/badge/phase-5__in__development-3b82f6)
![Status](https://img.shields.io/badge/status-placeholder-yellow)

## Status

Active development begins **Week 34 (Phase 5)**. This repo is the capstone of the portfolio — full platform launch, portfolio site, and NVIDIA NCP-AAI exam at completion.

## What This Agent Does

`ops-orchestrator` is the top-level router for the entire agent platform. It classifies incoming requests, dispatches them to the appropriate specialist agent (or chains of agents), manages end-to-end workflow state, and returns a unified response. The portfolio site also lives here.

## Agentic Pattern: Orchestrator / Router Agent

An intent classifier routes requests to one of four specialist agents. Multi-step workflows (e.g., new request → intake → procedure lookup → work order creation) are managed as sequential chains with shared state. A supervisor layer handles error recovery and retries.

## Evaluation Targets

| Metric | Target | Method |
|--------|--------|--------|
| E2E Success Rate | ≥85% | 20 end-to-end scenarios |
| Routing Accuracy | ≥95% | 50 varied requests |
| Full Pipeline Latency | <30s | Automated timing |

## The Full Platform

This orchestrator connects all five agents. At Phase 5 completion, `agent-core` goes public and the full system is visible E2E.

| Agent | Pattern | Status |
|-------|---------|--------|
| [knowledge-navigator](https://github.com/Jlowpez/knowledge-navigator) | RAG Agent | 🔄 Active |
| [intake-agent](https://github.com/Jlowpez/intake-agent) | Structured Output | ⏳ Phase 2 |
| [compliance-checker](https://github.com/Jlowpez/compliance-checker) | Multi-Agent Pipeline | ⏳ Phase 3 |
| [workload-scheduler](https://github.com/Jlowpez/workload-scheduler) | Planner-Executor | ⏳ Phase 4 |
| **ops-orchestrator** | Orchestrator | ⏳ Phase 5 |

## Production Path

At go-live: connect each specialist agent to your organization's data sources via the DAL config. The routing logic, workflow chains, and orchestration layer are unchanged.
