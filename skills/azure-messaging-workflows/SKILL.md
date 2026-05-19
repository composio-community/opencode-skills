---
name: azure-messaging-workflows
description: Workflow for building scalable messaging systems on Microsoft Azure using queues, event-driven architecture, pub/sub systems, service buses, and cloud-native communication patterns.
---

# Azure Messaging Workflows

## Overview

This skill enables Claude to design, implement, and manage messaging systems using Microsoft Azure cloud services.

The workflow focuses on:
- asynchronous communication
- event-driven architecture
- queue systems
- publish/subscribe messaging
- distributed workflows
- scalable cloud communication
- reliable message delivery
- cloud-native integration systems

The goal is to build messaging pipelines that are:
- scalable
- fault-tolerant
- loosely coupled
- event-driven
- production-ready

This workflow emphasizes reliability, observability, and scalability across distributed systems.

---

# Setup

Before starting:

1. Create an Azure account:
   https://azure.microsoft.com

2. Install Azure CLI:

```bash
npm install -g azure-cli
```

or follow:
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli

3. Login to Azure:

```bash
az login
```

4. Create Azure resources.

Recommended services:
- Azure Service Bus
- Azure Queue Storage
- Azure Event Grid
- Azure Event Hubs
- Azure Functions

Recommended tools:
- VS Code
- Azure Portal
- Azure CLI
- Docker
- GitHub Actions

Optional:
- Kubernetes
- Terraform
- Monitoring dashboards
- Distributed tracing systems

---

# Inputs Required

- Messaging requirements
- Event workflows
- Application architecture
- Throughput expectations
- Reliability requirements

Optional:
- Existing microservices
- API systems
- Queue consumers
- Monitoring systems

---

# When to Use This Skill

Use this skill when:
- building distributed systems
- implementing async workflows
- decoupling microservices
- processing events at scale
- creating pub/sub architectures
- managing cloud event pipelines
- scaling backend communication systems
- improving reliability in cloud applications

---

# When NOT to Use

Do NOT use this skill for:
- tiny monolithic applications
- fully synchronous workflows
- systems without distributed communication needs
- single-process local-only applications

---

# Example Use Case

> Build an event-driven order processing pipeline using Azure messaging services.

Claude should:

1. Design queue architecture
2. Configure message routing
3. Implement producers and consumers
4. Handle retries and failures
5. Monitor event flow
6. Ensure message durability
7. Scale consumers dynamically

Final result should:
- remain fault tolerant
- scale efficiently
- support async processing
- improve system reliability
- reduce service coupling

---

# Core Azure Messaging Principles

## 1. Prefer Asynchronous Communication

Messaging systems should reduce direct service dependencies.

Instead of:
- tightly coupled API chains
- blocking communication

Use:
- queues
- events
- pub/sub systems
- background processing

Asynchronous systems improve:
- scalability
- reliability
- resilience

---

## 2. Design for Failure

Distributed systems fail regularly.

Claude should proactively handle:
- retries
- dead-letter queues
- duplicate events
- timeouts
- consumer crashes
- transient cloud failures

Reliable systems require:
- graceful recovery
- observability
- fault tolerance

---

## 3. Choose the Correct Azure Service

Different Azure messaging tools solve different problems.

### Azure Service Bus
Best for:
- enterprise messaging
- ordered delivery
- reliable queues
- transactions

### Azure Queue Storage
Best for:
- simple queue workflows
- lightweight async tasks
- cost-efficient messaging

### Azure Event Grid
Best for:
- event routing
- reactive cloud workflows
- serverless integrations

### Azure Event Hubs
Best for:
- high-throughput event streaming
- telemetry pipelines
- analytics ingestion

Claude should choose services based on:
- throughput
- reliability
- ordering requirements
- architecture goals

---

## 4. Keep Services Loosely Coupled

Messaging systems should:
- isolate services
- reduce dependencies
- improve scalability
- allow independent deployment

Good decoupling improves:
- maintainability
- resilience
- deployment flexibility

Avoid:
- tightly synchronized services
- shared state coupling
- fragile orchestration chains

---

## 5. Monitor Everything

Messaging systems require observability.

Claude should help implement:
- logging
- tracing
- queue monitoring
- failure alerts
- retry tracking
- throughput analytics

Good observability improves:
- debugging
- scaling
- operational reliability

---

# Workflow

## 1. Define Messaging Architecture

Start by identifying:
- producers
- consumers
- event types
- queue requirements
- throughput expectations

Define:
- synchronous vs asynchronous boundaries
- retry policies
- delivery guarantees
- scaling strategy

---

## 2. Select Azure Messaging Services

Choose:
- Service Bus
- Queue Storage
- Event Grid
- Event Hubs

based on:
- event volume
- ordering requirements
- durability
- architecture complexity

Claude should optimize for:
- reliability
- scalability
- operational simplicity

---

## 3. Configure Queues & Topics

Create:
- queues
- subscriptions
- topics
- routing rules

Configure:
- retry policies
- dead-letter queues
- message TTL
- scaling settings

Ensure:
- fault tolerance
- delivery reliability
- predictable routing behavior

---

## 4. Build Producers & Consumers

Implement:
- message publishers
- queue consumers
- event handlers
- background workers

Validate:
- serialization consistency
- idempotency
- retry safety
- throughput handling

Avoid:
- fragile message parsing
- blocking workflows
- unsafe retries

---

## 5. Handle Failures Gracefully

Implement:
- retries
- dead-letter handling
- fallback systems
- timeout management
- monitoring alerts

Claude should proactively prevent:
- infinite retry loops
- message loss
- silent failures
- duplicate processing bugs

---

## 6. Monitor & Scale

Track:
- queue depth
- processing latency
- failure rates
- throughput
- consumer health

Scale:
- worker instances
- event processors
- serverless consumers

Ensure:
- stable processing under load
- operational visibility
- efficient resource usage

---

## 7. Validate Production Readiness

Before deployment validate:
- retry behavior
- dead-letter handling
- observability
- scaling behavior
- security configuration

Ensure:
- systems remain fault tolerant
- workflows scale predictably
- failures remain recoverable

---

# Output Expectations

The final output should include:
- scalable messaging architecture
- Azure-native queue systems
- reliable event processing workflows
- observability pipelines
- fault-tolerant distributed communication
- production-ready cloud messaging systems

The workflow itself should remain:
- scalable
- resilient
- loosely coupled
- observable
- cloud-native

---

# Execution Strategy (for AI agents)

The agent should:

1. Prefer asynchronous communication patterns
2. Design for distributed system failures
3. Select Azure messaging services intentionally
4. Maintain loose service coupling
5. Implement strong observability systems
6. Optimize for scalable cloud-native communication

The workflow should optimize for:
- reliability
- scalability
- resilience
- operational visibility
- distributed system stability

---

# Best Practices

- Use queues to decouple services
- Implement retries carefully
- Always configure dead-letter queues
- Monitor message flow continuously
- Keep consumers idempotent
- Validate scaling behavior early
- Prioritize observability in distributed systems

---

# Notes

- Asynchronous systems scale significantly better than tightly coupled architectures
- Reliable messaging systems require strong failure handling
- Observability is critical for distributed cloud systems
- Azure messaging services solve different scalability and reliability problems
- Loosely coupled systems improve deployment flexibility and resilience
