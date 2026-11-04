# Assignment 06 — Accessibility Testing (Project VITAL)

**Due: Tuesday, November 17, 2026, 11:59 PM ET**  
**Total: 100 points**

## Goal
Evaluate the accessibility of your team's OpenEMR workflow (patient registration, appointment scheduling, or vital signs) using WCAG 2.2, manual keyboard/form testing, automated scans, evidence-based findings, and CI regression testing. Use only your isolated Project VITAL environment and synthetic data.

## Requirements
1. **Plan (15):** Identify task, browser/environment, initial/error/completion states, and at least eight checks across POUR. Map checks to applicable WCAG 2.2 criteria.
2. **Manual testing (20):** Navigate without a mouse; inspect focus order/visibility, labels, errors, dynamic states, and 200% zoom. Report at least six observations, including two on error/dynamic states.
3. **Automated scan (15):** Run axe DevTools, Accessibility Insights, Lighthouse, or axe-core; record tool/version, states, findings and at least three manual verification checks. Explain scanner limitations.
4. **Findings (15):** Document at least three evidence-based defects, risks, or passing checks, including steps, expected/actual, impact, WCAG mapping (or uncertainty), severity, and recommendation. Never invent violations.
5. **Automation (15):** Implement at least two executable accessibility regression checks. At least one must exercise a relevant OpenEMR screen or its rendered DOM locally. CI fixtures may supplement but not replace live workflow evidence.
6. **CI experiment (10):** Add `.github/workflows/accessibility-tests.yml`; demonstrate GREEN → RED → GREEN by temporarily breaking a team-owned HTML fixture (e.g., removing an input label). Include commit/run links and restore the fixture.
7. **Reflection (5):** Explain accessibility vs usability, scan limitations, highest-impact barrier, why automated passing is not WCAG AA conformance, and next tests.
8. **Reproducibility (5):** Provide clear setup, commands, versions, sanitized evidence and links.

## Submission
In `assignment-06/`, submit `README.md`, `accessibility-plan.md`, `manual-test-report.md`, `automated-scan-report.md`, `accessibility-defects.md`, `automation.md`, `ci-report.md`, `reflection.md`, tests, and optional fixtures/evidence. Add the workflow in `.github/workflows/`.

Tag the final submission `assignment-06` and push the tag. Never commit patient information, credentials, or intentional accessibility regressions.

## Important boundaries
Do not test public or production healthcare systems. Do not claim to simulate disability or represent disabled users. A clean automated scan does not prove accessibility compliance. Do not modify production OpenEMR code merely to pass a test.

References: [WCAG 2.2](https://www.w3.org/TR/WCAG22/), [W3C Easy Checks](https://www.w3.org/WAI/test-evaluate/preliminary/), [Playwright accessibility testing](https://playwright.dev/docs/accessibility-testing).
