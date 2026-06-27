# Coordinator

## Purpose

The Coordinator is the brain of OctoMesh. It receives a large job, breaks it into smaller tasks, sends those tasks to workers, checks the results, and returns the final answer.

## Pseudocode

```text
START Coordinator

WHILE system is running

    IF new task arrives THEN
        receive task
        split task into subtasks
        give each subtask an ID
        place subtasks in task queue
    END IF

    IF worker is available THEN
        assign next subtask to worker
    END IF

    IF worker returns result THEN
        send result to validator

        IF result is valid THEN
            store result
            increase worker reputation
        ELSE
            return subtask to queue
            decrease worker reputation
        END IF
    END IF

    IF all subtasks are complete THEN
        merge results
        return final answer
    END IF

END WHILE
```