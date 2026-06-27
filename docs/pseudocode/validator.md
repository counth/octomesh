# Validator

## Purpose

The Validator ensures that work completed by workers is correct before it becomes part of the final result.

---

## Responsibilities

- Receive completed tasks
- Verify the computation
- Compare results with other validators
- Vote on validity
- Report the decision to the Coordinator

---

## Pseudocode

```text
START Validator

WHILE connected

    WAIT for completed task

    RECEIVE task result

    VERIFY computation

    COMPARE with validator network

    IF consensus reached THEN

        SEND VALID

    ELSE

        SEND INVALID

    END IF

END WHILE
```