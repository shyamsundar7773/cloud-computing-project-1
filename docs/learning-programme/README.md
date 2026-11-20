# Learning programme guide

## Purpose

The ten-module syllabus builds one integrated **Retail Business Cloud Operations & Data Platform** for the fictional online retailer ShopSphere. The supplied `Cloud_Data_IT_Career_Launch_Phased_Syllabus.pdf` is the authoritative source for formal module titles, sequence, phase titles, and coverage. Module 0 is onboarding; it is not an eleventh formal module.

The shared system grows from business requirements and system fundamentals, through networking, Linux, relational data, Python, Git/API integration, Azure fundamentals, cloud operations, and an end-to-end data pipeline, to final testing, documentation, and job readiness. Cloud service selection and any resource creation require a separate security/cost review.

## Required module-by-module rotation

Complete one module in this order before moving to the next:

`1A.1 -> 1B.1 -> 1C.1 -> 1D.1 -> 1A.2 -> 1B.2 -> 1C.2 -> 1D.2 -> ... -> 1A.10 -> 1B.10 -> 1C.10 -> 1D.10`

The tracks are **A - Project Building**, **B - Technical Learning**, **C - Business Understanding**, and **D - Interview Preparation**. Each module workspace reproduces its exact syllabus phase names and scope. No lesson or assessment is completed by creating its folder.

## What the learner demonstrates

For each sub-phase, keep evidence of the objective, practical work, inputs/outputs, dependencies, expected and actual results, normal/failure testing where applicable, business outcome, troubleshooting, independent explanation, assessment, and revision. The learner, not generated files, is the basis for completion. Explain what was built, why, how it works, and its limits; reproduce the work and answer follow-up questions.

## Where work belongs

- `docs/modules/` - module and phase indexes, work instructions, and learner records
- `docs/templates/` - reusable sub-phase, assessment, and troubleshooting records
- `src/`, `tests/`, `database/`, `api/`, `cloud/` - future project code/configuration as introduced by the syllabus
- `data/sample/` - synthetic or explicitly approved source samples; `data/processed/` - generated outputs
- `operations/` - runbooks and sanitized operational records; do not commit runtime logs or secrets
- `notes/`, `assessments/`, `evidence/` - learner-owned notes, assessment records, and sanitized verification evidence

Keep personal credentials, real customer/personal data, private keys, `.env`, and machine-specific exports out of version control. Record evidence with enough context to reproduce it, but redact secrets and sensitive values.

## Progress status definitions

- **NOT STARTED** - no learner activity recorded.
- **IN PROGRESS** - learning/practice is underway.
- **BLOCKED** - a prerequisite or user action prevents progress; record it.
- **IMPLEMENTED BUT NOT VERIFIED** - an artifact exists but checks have not passed.
- **VERIFIED** - practical checks passed; learner assessment may still be pending.
- **LEARNER ASSESSMENT PENDING** - work is verified but independent explanation/review remains.
- **NEEDS REVISION** - assessment or evidence identifies a gap; record a correction and retest.
- **COMPLETED** - practical evidence, assessment, independent explanation, and revision review are all complete.

Use [the tracker](progress-tracker.md) as the current summary and the phase record template for detail. Keep failed attempts and corrections; do not replace them with a success-only account.

## Official module map

| Module | Syllabus title | Workspace |
|---:|---|---|
| 1 | IT AND SYSTEM FUNDAMENTALS | [Module workspace](../modules/module-01-it-and-system-fundamentals/README.md) |
| 2 | NETWORKING FUNDAMENTALS | [Module workspace](../modules/module-02-networking-fundamentals/README.md) |
| 3 | LINUX AND COMMAND-LINE OPERATIONS | [Module workspace](../modules/module-03-linux-and-command-line-operations/README.md) |
| 4 | SQL AND DATABASE OPERATIONS | [Module workspace](../modules/module-04-sql-and-database-operations/README.md) |
| 5 | PYTHON PROGRAMMING | [Module workspace](../modules/module-05-python-programming/README.md) |
| 6 | GIT, GITHUB, REST APIs AND INTEGRATION | [Module workspace](../modules/module-06-git-github-rest-apis-and-integration/README.md) |
| 7 | CLOUD COMPUTING AND AZURE FUNDAMENTALS | [Module workspace](../modules/module-07-cloud-computing-and-azure-fundamentals/README.md) |
| 8 | CLOUD OPERATIONS, SECURITY AND MONITORING | [Module workspace](../modules/module-08-cloud-operations-security-and-monitoring/README.md) |
| 9 | DATA ENGINEERING AND ETL INTEGRATION | [Module workspace](../modules/module-09-data-engineering-and-etl-integration/README.md) |
| 10 | TESTING, DOCUMENTATION AND JOB READINESS | [Module workspace](../modules/module-10-testing-documentation-and-job-readiness/README.md) |

## Resume procedure

1. Open the tracker and choose the earliest incomplete sub-phase in the required rotation.
2. Read its module/phase index and the exact syllabus section.
3. Set the status to IN PROGRESS and agree on a bounded practical task before implementation.
4. Save the activity record and sanitized evidence in that phase workspace.
5. Test, explain, assess, record mistakes/root cause, and complete a revision task.
6. Update the tracker only after the learner's evidence meets the status definition.
