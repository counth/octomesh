# Worker

## Purpose

A Worker is any device participating in the OctoMesh network. Workers receive tasks from the Coordinator, execute them, and return the results.

---

## Responsibilities

- Wait for work
- Receive a task
- Download required resources
- Execute the computation
- Generate proof of execution
- Return the result

---

## Pseudocode

```text
START Worker

WHILE connected

    WAIT for task

    RECEIVE task

    DOWNLOAD required resources

    EXECUTE computation

    CREATE proof

    SEND result to Coordinator

END WHILE
```