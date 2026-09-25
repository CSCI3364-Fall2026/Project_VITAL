# Project VITAL Assignments — Fall 2026

This directory contains the assignments currently released for **CSCI3364 — Software Testing, Quality and Security**.

Assignments are released progressively during the semester.

## Currently Released

### Assignment 1 — System Exploration

**Status: RELEASED**

Instructions:

[Assignment 1 — System Exploration](01-system-exploration/README.md)

---

### Assignment 2 — System Architecture

**Status: RELEASED**

Instructions:

[Assignment 2 — System Architecture](02-system-architecture/README.md)

Assignment 2 builds directly on the observations and testing opportunities developed in Assignment 1.

Students investigate one focused OpenEMR workflow and trace it through:

- user-visible behavior;
- HTTP requests and endpoints;
- C4 architecture models;
- relevant source-code components;
- database tables and relationships;
- important dependencies;
- architecture-informed testing decisions.

---

### Assignment 3 — Unit Testing and Continuous Integration

**Status: RELEASED**

Instructions:

[Assignment 3 — Unit Testing and Continuous Integration](03-unit-testing-ci/README.md)

Assignment 3 builds directly on the architectural evidence developed in Assignment 2.

Students will:

- return to the workflow investigated in Assignment 2;
- identify and justify a small testable unit from the relevant implementation;
- evaluate dependencies and testability;
- study existing OpenEMR tests;
- design six meaningful unit tests, including normal, boundary, invalid/error, and risk-based cases;
- include parameterized/data-driven testing where appropriate;
- run tests locally using the provided isolated PHPUnit environment;
- demonstrate a deliberate **GREEN → RED → GREEN** cycle;
- run the same tests automatically with GitHub Actions;
- explain what their unit tests establish — and what still requires integration, system, or acceptance testing.

The private team repositories contain the Assignment 3 workspace and validated unit-testing/CI infrastructure. The public Assignment 3 README remains the authoritative assignment specification.

Complete each assignment according to its README and the course submission guidelines.

## Future Assignments

Additional Project VITAL assignments will be added to this directory when they are officially released.

Only assignments present in the official course repository should be considered released.