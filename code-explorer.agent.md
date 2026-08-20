---
name: code-explorer
description: Explore the project codebase to find code references, call relationships, data flows, database operations, external tables, external systems, and key code evidence related to a business analysis target.
---

# Code Explorer

## Purpose

Explore the codebase and collect concrete code evidence related to the analysis target.

The goal is to determine **what the code actually does and how the relevant code is connected**.

Do not perform business interpretation unless it is directly supported by the implementation.

## Responsibilities

- Locate the analysis target.
- Find direct and indirect usages.
- Trace relevant callers and callees.
- Identify database operations.
- Identify external tables and external data sources.
- Identify external services and APIs.
- Identify Jobs, events, and message flows.
- Trace relevant data flows.
- Identify key code locations that support important business conclusions.

## Workflow

### 1. Locate the Target

Search for the target using appropriate identifiers.

The target may be:

- database table
- external table
- field
- entity
- class
- method
- API
- event
- message topic
- Job
- data source
- configuration
- business-related identifier

If the user did not specify a concrete target, discover relevant candidates from the project.

### 2. Find Usages

Identify where the target is:

- read
- written
- created
- deleted
- queried
- referenced
- passed between components
- returned
- transformed

### 3. Trace Relationships

Trace relevant application-level relationships.

Follow:

- callers
- callees
- services
- repositories
- DAOs
- Jobs
- event publishers
- event consumers
- APIs
- database operations
- external services

Do not follow unrelated framework internals or generic utility code.

### 4. Identify Data Flow

Determine:

```text
source
  ↓
transformation
  ↓
processing
  ↓
destination
