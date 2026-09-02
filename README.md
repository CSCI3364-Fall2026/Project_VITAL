# Project VITAL — CSCI3364 Fall 2026

**Software Testing, Quality and Security**  
**Boston College — Fall 2026**

## Project VITAL

**VITAL: Verification, Integration, Testing, Accessibility & Lifecycle**

Project VITAL is the semester-long software testing project for CSCI3364.

Throughout the semester, you will work with a substantial real-world open-source software system, **OpenEMR**, and progressively apply different software testing and quality-assurance techniques to it.

The purpose of the project is not to become an OpenEMR or PHP developer. Instead, you will learn how to understand, test, evaluate, and provide evidence about the quality of a software system that you did not build yourself.

A central principle of this course is:

> **A test that passes is not automatically a successful testing result, and a test that fails is not automatically an unsuccessful result.**

Your work should connect:

**requirements → risks → test design → evidence → conclusions**

---

## Current Assignment

### Assignment 1 — System Exploration

**Status: RELEASED**

Assignment instructions:

[`assignments/01-system-exploration/README.md`](assignments/01-system-exploration/README.md)

Only assignments officially released in this repository should be considered active course assignments.

Additional assignments will be released progressively during the semester.

---

## How the Course Repository Works

This repository contains the official Project VITAL materials for **CSCI3364 Fall 2026**.

You will use two types of repositories during the semester:

### 1. Course Repository

This repository:

`CSCI3364-Fall2026/Project_VITAL`

contains:

- official assignment instructions;
- Project VITAL documentation;
- the reproducible course environment;
- setup and submission instructions; and
- testing infrastructure released for current assignments.

Do **not** submit your team's work directly to this repository.

### 2. Team Repository

Each team will receive a separate **private GitHub repository** for its Project VITAL work.

Your team repository is where you will:

- write tests and testing infrastructure;
- store required diagrams and documentation;
- record testing evidence;
- collaborate using Git and GitHub; and
- create the tagged versions required for assignment submission.

Team repositories must remain private unless the instructor explicitly states otherwise.

---

## Getting Started

Start with:

1. [`docs/STUDENT_SETUP.md`](docs/STUDENT_SETUP.md)
2. [`docs/STUDENT_SUBMISSION_GUIDE.md`](docs/STUDENT_SUBMISSION_GUIDE.md)
3. [`assignments/01-system-exploration/README.md`](assignments/01-system-exploration/README.md)

The OpenEMR environment is located in:

`environment/`

Follow the course setup instructions rather than installing or configuring a different OpenEMR version independently.

---

## System Under Test

Project VITAL uses a **pinned OpenEMR release** running in an isolated Docker-based environment.

OpenEMR is not included directly in this repository. The Project VITAL environment retrieves the designated version so that teams work from a reproducible baseline.

The system is being used strictly for educational software-testing activities.

---

## Data, Privacy, and Safety

Project VITAL follows a data-minimization and controlled-testing approach.

### You may:

- use the Project VITAL course environment;
- use synthetic course data;
- perform testing specifically authorized by an assignment; and
- experiment within your team's designated environment and repository.

### You may not:

- use real patient data or Protected Health Information (PHI);
- test production healthcare systems;
- test Boston College production systems;
- test third-party systems without explicit authorization;
- upload real patient information to GitHub or generative-AI systems; or
- perform security testing outside the scope explicitly authorized by the course.

When an assignment introduces additional testing restrictions, those restrictions are part of the assignment requirements.

---

## Generative AI

Generative AI may be used when permitted by the course and individual assignment instructions.

Using AI does **not** remove your responsibility for understanding, evaluating, testing, and defending the work you submit.

AI-generated tests, explanations, code, or recommendations should be treated as artifacts that require evaluation rather than as automatically correct answers.

Specific AI-use and documentation requirements will be provided with course activities and assignments.

---

## Repository Structure

The contents of this repository will grow as assignments are released.

```text
Project_VITAL/
├── assignments/
│   └── 01-system-exploration/
├── data/
├── docs/
│   ├── STUDENT_SETUP.md
│   └── STUDENT_SUBMISSION_GUIDE.md
├── environment/
├── rubrics/
└── tests/
