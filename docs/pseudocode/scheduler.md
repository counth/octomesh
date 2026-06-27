# Scheduler

## Purpose

The Scheduler decides which Worker should receive each task. It balances workload, prioritizes urgent jobs, and avoids overloading any single device.

---

## Responsibilities

- Monitor worker availability
- Prioritize queued tasks
- Match tasks to suitable workers
- Redistribute work if a worker disconnects
- Optimize overall network performance

---

## Pseudocode

```text
START Scheduler

WHILE running

    CHECK Task Queue

    CHECK Available Workers

    SORT tasks by priority

    FOR each available worker

        ASSIGN highest priority task

    END FOR

    IF worker disconnects THEN

        RETURN unfinished task to queue

    END IF

END WHILE
```