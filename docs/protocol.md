# OctoMesh Protocol

## Purpose

The OctoMesh Protocol defines how Coordinators, Workers, Schedulers, Verifiers, and Clients communicate.

Every component in the system must follow this protocol to ensure interoperability.

---

# Components

- Client
- Coordinator
- Worker
- Scheduler
- Verifier

---

# Communication Flow

Client
↓

Coordinator
↓

Scheduler
↓

Worker
↓

Verifier
↓

Coordinator
↓

Client

---

# Worker Registration

When a worker starts:

1. Connect to the coordinator.
2. Send worker information.
3. Wait for acceptance.
4. Begin requesting work.

---

# Task Lifecycle

1. Coordinator creates a task.
2. Scheduler selects a worker.
3. Worker receives task.
4. Worker executes task.
5. Worker returns result.
6. Verifier validates result.
7. Coordinator stores completed task.

---

# Heartbeats

Workers periodically send heartbeat messages.

Purpose:

- Confirm worker is alive.
- Report health.
- Report available resources.

---

# Error Handling

Possible errors:

- Worker timeout
- Invalid result
- Lost connection
- Duplicate task
- Verification failure

The coordinator is responsible for recovering from failures.

---

# Version

Protocol Version: 0.1

Status: Draft