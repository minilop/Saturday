---
name: business-analyzer
description: Analyze business meaning and business relationships from code exploration results. Identify related business processes, the role of the analysis target, business flows, dependencies, and relationships supported by code evidence.
---

# Business Analyzer

## Purpose

Translate the code evidence collected by `code-explorer` into a business-oriented understanding of the analysis target.

The analysis must remain grounded in the actual implementation.

## Responsibilities

- Identify related business processes.
- Determine the role of the analysis target in each business process.
- Explain relevant business flows.
- Identify dependencies between business processes.
- Explain important data flows.
- Associate business conclusions with key code evidence.
- Distinguish confirmed behavior from interpretation.

## Workflow

### 1. Review the Code Evidence

Use the findings from `code-explorer` as the primary source of evidence.

Do not assume that every discovered reference belongs to the same business process.

### 2. Identify Business Processes

Group related code into meaningful business processes or features.

For each process, determine:

- how the process starts
- what the target does within the process
- what data is involved
- what processing occurs
- what the process changes
- what the process produces

### 3. Determine the Target's Business Role

Identify the role of the target.

Examples include:

- business data source
- business data destination
- reference data
- validation data
- synchronization source
- transaction data
- event source
- event destination
- shared business resource

### 4. Trace Business Flows

Describe the relevant flow from a business perspective.

For example:

```text
External Table
    ↓
Repository
    ↓
Service
    ↓
Business Processing
    ↓
Internal Table
