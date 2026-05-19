---
name: azure-observability-workflows
description: Workflow for implementing observability systems on Microsoft Azure using logging, monitoring, tracing, telemetry, metrics, dashboards, and production-grade cloud diagnostics.
---

# Azure Observability Workflows

## Overview

This skill enables Claude to design and implement observability systems for applications running on Microsoft Azure.

The workflow focuses on:
- distributed tracing
- centralized logging
- metrics collection
- cloud monitoring
- telemetry pipelines
- incident diagnostics
- alerting systems
- production visibility

The goal is to make cloud systems:
- observable
- debuggable
- measurable
- reliable
- production-ready

Instead of reacting to failures after they happen, observability systems should proactively surface:
- bottlenecks
- errors
- degraded performance
- unusual system behavior
- infrastructure instability

This workflow prioritizes operational visibility and debugging quality across distributed systems.

---

# Setup

Before starting:

1. Create an Azure account:
   https://azure.microsoft.com

2. Install Azure CLI:

```bash
az login
```

3. Enable Azure monitoring services.

Recommended Azure services:
- Azure Monitor
- Application Insights
- Log Analytics
- Azure Dashboard
- Azure Alerts

Recommended tools:
- VS Code
- Azure Portal
- Grafana
- OpenTelemetry
- Docker
- Kubernetes (optional)

Optional:
- Prometheus
- Jaeger
- Azure Managed Grafana
- Distributed tracing systems

---

# Inputs Required

- Application architecture
- Cloud infrastructure
- Deployment environment
- Service dependencies
- Monitoring objectives

Optional:
- Existing telemetry systems
- Logging pipelines
- Kubernetes clusters
- Incident history

---

# When to Use This Skill

Use this skill when:
- deploying production applications
- debugging distributed systems
- monitoring cloud infrastructure
- tracking application performance
- diagnosing incidents
- implementing SRE workflows
- scaling microservices
- improving operational reliability

---

# When NOT to Use

Do NOT use this skill for:
- disposable prototypes
- tiny local-only applications
- systems with no production requirements
- workflows without operational monitoring needs

---

# Example Use Case

> Build observability infrastructure for a distributed Azure microservices platform.

Claude should:

1. Configure telemetry pipelines
2. Enable distributed tracing
3. Centralize logs
4. Create monitoring dashboards
5. Configure alerts
6. Track infrastructure health
7. Diagnose failures proactively

Final result should:
- improve debugging speed
- surface production issues quickly
- increase operational visibility
- support scalable cloud monitoring
- improve reliability and uptime

---

# Core Observability Principles

## 1. Logs Alone Are Not Enough

Modern observability requires:
- logs
- metrics
- traces
- telemetry
- distributed context

Claude should combine:
- application logs
- infrastructure metrics
- request traces
- dependency monitoring

Good observability systems provide:
- visibility
- diagnostics
- operational understanding

---

## 2. Distributed Systems Require Distributed Tracing

Microservices introduce:
- request chains
- async communication
- hidden bottlenecks
- cross-service failures

Claude should implement:
- trace correlation
- request IDs
- distributed spans
- dependency tracking

Distributed tracing improves:
- debugging speed
- bottleneck detection
- root-cause analysis

---

## 3. Centralize Monitoring

Observability data should remain centralized.

Recommended systems:
- Azure Monitor
- Application Insights
- Log Analytics
- Grafana dashboards

Centralization improves:
- debugging
- incident response
- operational visibility

Avoid:
- fragmented logging systems
- isolated metrics
- disconnected dashboards

---

## 4. Monitor What Matters

Not all metrics are equally valuable.

Claude should prioritize:
- latency
- error rates
- throughput
- resource utilization
- request failures
- dependency health

Avoid:
- noisy dashboards
- vanity metrics
- excessive telemetry without purpose

Good monitoring improves:
- reliability
- scaling decisions
- incident detection

---

## 5. Alerts Should Be Actionable

Bad alerting systems create:
- alert fatigue
- ignored notifications
- operational chaos

Claude should configure alerts for:
- real incidents
- meaningful thresholds
- actionable failures
- production-impacting issues

Good alerts improve:
- operational response
- uptime
- debugging speed

---

# Workflow

## 1. Analyze System Architecture

Start by identifying:
- services
- APIs
- databases
- queues
- infrastructure dependencies

Determine:
- critical workflows
- failure points
- performance bottlenecks
- observability gaps

Understand:
- request flow
- service boundaries
- scaling behavior

---

## 2. Configure Telemetry Collection

Enable:
- application logging
- infrastructure metrics
- distributed traces
- dependency monitoring

Use:
- Application Insights
- Azure Monitor
- OpenTelemetry

Validate:
- telemetry consistency
- trace propagation
- correlation IDs

---

## 3. Centralize Logs & Metrics

Route:
- logs
- traces
- metrics
- diagnostics

into centralized systems.

Recommended:
- Log Analytics
- Azure Monitor
- Grafana

Ensure:
- searchable logs
- structured telemetry
- consistent formatting

---

## 4. Implement Distributed Tracing

Track:
- requests
- service dependencies
- API calls
- async workflows

Use:
- trace IDs
- span relationships
- request correlation

Distributed tracing improves:
- debugging
- latency analysis
- dependency visibility

---

## 5. Create Dashboards

Build dashboards for:
- infrastructure health
- application performance
- error tracking
- queue processing
- API latency
- service dependencies

Dashboards should remain:
- readable
- actionable
- operationally useful

Avoid:
- cluttered dashboards
- excessive graphs
- irrelevant metrics

---

## 6. Configure Alerts

Create alerts for:
- service downtime
- latency spikes
- high failure rates
- queue backlogs
- resource exhaustion

Alerts should:
- reduce noise
- remain actionable
- trigger appropriate escalation

---

## 7. Validate Production Observability

Before deployment validate:
- logs are searchable
- traces propagate correctly
- metrics update consistently
- alerts trigger correctly
- dashboards remain readable

Ensure:
- incidents can be diagnosed quickly
- telemetry remains reliable
- systems stay observable under load

---

# Output Expectations

The final output should include:
- centralized observability systems
- distributed tracing pipelines
- actionable monitoring dashboards
- production telemetry systems
- scalable diagnostics infrastructure
- cloud-native operational visibility

The workflow itself should remain:
- scalable
- observable
- production-focused
- debugging-friendly
- operationally reliable

---

# Execution Strategy (for AI agents)

The agent should:

1. Treat observability as foundational infrastructure
2. Centralize telemetry aggressively
3. Implement distributed tracing consistently
4. Prioritize actionable monitoring
5. Reduce alert noise proactively
6. Optimize for operational visibility and debugging quality

The workflow should optimize for:
- reliability
- debugging speed
- operational clarity
- incident response quality
- cloud scalability

---

# Best Practices

- Use structured logging consistently
- Implement distributed tracing early
- Centralize metrics and logs
- Monitor latency and error rates closely
- Keep dashboards actionable
- Avoid alert fatigue
- Validate observability under production load

---

# Notes

- Distributed tracing dramatically improves debugging in microservices
- Observability quality strongly affects operational reliability
- Actionable dashboards outperform noisy telemetry systems
- Good alerting reduces operational burnout significantly
- Observability systems should evolve continuously with infrastructure growth
