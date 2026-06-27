# OctoMesh Job Model

## Purpose

A job is the main unit of work submitted to OctoMesh.

The coordinator receives a job, breaks it into smaller tasks, assigns those tasks to workers, verifies the results, and combines them into a final output.

---

## Job Lifecycle

1. Client submits a job.
2. Coordinator validates the job.
3. Coordinator splits the job into tasks.
4. Scheduler assigns tasks to workers.
5. Workers execute tasks.
6. Verifier checks the results.
7. Aggregator combines verified results.
8. Final result is returned to the client.

---

## Job Structure

Every job contains:

- Job ID
- Job Type
- Input Data
- Task Size
- Priority
- Status
- Created Time
- Deadline
- Verification Method

---

## Example

```json
{
  "job_id": "job_001",
  "job_type": "number_sum",
  "input_data": [1,2,3,4,5],
  "task_size": 2,
  "priority": "normal",
  "status": "pending",
  "verification_method": "replication"
}
```

---

## Job Status

- Pending
- Splitting
- Scheduled
- Running
- Verifying
- Completed
- Failed
- Cancelled

---

## Relationship Between Jobs and Tasks

One job may contain many tasks.

```text
Job
├── Task 1
├── Task 2
├── Task 3
└── Task 4
```

The coordinator is responsible for dividing jobs into tasks.

---

## Verification

Task results may be verified by:

- Running the same task on multiple workers
- Comparing outputs
- Checking hashes
- Using worker reputation

---

## Design Principles

A job should be:

- Easy to split
- Easy to schedule
- Easy to verify
- Easy to retry
- Easy to aggregate

---

## Version

Document Version: 0.1

Status: Draft