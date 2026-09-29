# Peer Review Standards & Process

## Overview

The IPhySims peer review process ensures that every simulation in our repository meets the highest standards of scientific accuracy, code quality, reproducibility, and educational value. This document outlines the complete review process and evaluation criteria.

---

## Review Criteria

All submissions are evaluated on four dimensions, each scored on a scale of 1–5:

### 1. Scientific Accuracy (Weight: 40%)

| Score | Description |
|-------|-------------|
| **5** | Perfectly implements established physics; validated against analytical/experimental results with documented error analysis |
| **4** | Correct physics; minor approximations well-justified; results consistent with known solutions |
| **3** | Generally correct physics; some simplifications that are documented; results approximately correct |
| **2** | Physics contains errors or unjustified assumptions; results deviate significantly from expected values |
| **1** | Fundamental physics errors; results are incorrect or misleading |

**Reviewers should verify:**
- Correctness of governing equations and physical models
- Appropriateness of numerical methods for the problem
- Proper handling of boundary/initial conditions
- Valid approximations and their documented justification
- Comparison with analytical solutions or experimental data where available
- Correct units and dimensional consistency
- Proper treatment of significant figures and numerical precision

### 2. Code Quality (Weight: 25%)

| Score | Description |
|-------|-------------|
| **5** | Exceptionally clean, well-documented code; follows best practices; comprehensive tests; excellent dependency management |
| **4** | Clean code with good documentation; some tests; reasonable dependencies |
| **3** | Readable code with basic documentation; minimal tests; acceptable dependencies |
| **2** | Poorly structured code; insufficient documentation; no tests; problematic dependencies |
| **1** | Unreadable or unmaintainable code; no documentation; broken dependencies |

**Reviewers should verify:**
- Code readability and organization
- Inline documentation and comments
- External documentation (README, API docs)
- Unit tests and integration tests
- Dependency management (minimal, pinned versions)
- Error handling and edge cases
- Performance considerations
- Adherence to language-specific conventions
- Open-source license compliance

### 3. Reproducibility (Weight: 20%)

| Score | Description |
|-------|-------------|
| **5** | Fully reproducible on multiple platforms; containerized; clear execution instructions; deterministic results |
| **4** | Reproducible on at least 2 platforms; clear instructions; consistent results |
| **3** | Reproducible on one platform with documented setup; minor variations acceptable |
| **2** | Difficult to reproduce; unclear instructions; inconsistent results |
| **1** | Cannot be reproduced; missing critical information |

**Reviewers should verify:**
- Clear installation/setup instructions
- Documented dependencies and versions
- Execution instructions for running the simulation
- Expected output and how to verify correctness
- Platform compatibility (OS, hardware requirements)
- Deterministic behavior (or documented stochastic behavior)
- Container/virtual environment support (Docker, conda, etc.)

### 4. Educational Value (Weight: 15%)

| Score | Description |
|-------|-------------|
| **5** | Excellent educational resource; comprehensive documentation; tutorials; suitable for stated level; visually clear |
| **4** | Good educational value; adequate documentation; some learning materials provided |
| **3** | Basic educational utility; minimal documentation; limited learning materials |
| **2** | Limited educational value; poor documentation; unclear target audience |
| **1** | No educational value; no documentation; not suitable for learning |

**Reviewers should verify:**
- Target audience is clearly stated
- Documentation explains the physics being demonstrated
- Parameters are clearly explained
- Output/visualization is clear and interpretable
- Tutorials or example use cases are provided
- Common misconceptions are addressed
- Connections to physical intuition are made

---

## Review Process

### Step 1: Submission

The author submits a simulation via the IPhySims submission portal (GitHub Issues or dedicated form). Required materials:

- [ ] Source code (complete and runnable)
- [ ] README with description, physics background, and usage instructions
- [ ] Open-source license file
- [ ] Documentation of dependencies
- [ ] Example input/output
- [ ] Target physics domain and educational level
- [ ] Any validation data or comparisons

### Step 2: Initial Screening (1–3 days)

A technical staff member performs a preliminary check:
- All required materials are present
- Code runs without errors
- Basic functionality matches description
- License is acceptable
- No obvious scientific errors

**Outcome**: Pass → Proceed to peer review | Fail → Returned to author with feedback

### Step 3: Peer Review (14–21 days)

Two independent reviewers with domain expertise evaluate the simulation:
- Each reviewer scores all four criteria
- Reviewers provide detailed written feedback
- Reviewers recommend: Accept / Minor Revision / Major Revision / Reject

**Reviewer Assignment Criteria:**
- Domain expertise matching the simulation's physics area
- No conflict of interest with the author
- Active reviewer status maintained

### Step 4: Author Revision (14–30 days)

The author addresses reviewer comments:
- Respond to each comment individually
- Make requested changes or explain why changes are not appropriate
- Submit revised version with change log

### Step 5: Editorial Decision (3–7 days)

The Editorial Board reviews the submission, reviews, and author responses:
- **Accept**: Simulation meets all standards; proceed to publication
- **Conditional Accept**: Minor changes required; no further review needed
- **Major Revision**: Significant issues remain; another review cycle needed
- **Reject**: Simulation does not meet standards; provide constructive feedback

### Step 6: Publication (1–3 days)

Accepted simulations are:
- Added to the IPhySims repository
- Assigned a DOI (Digital Object Identifier)
- Tagged with physics domain and educational level
- Given the IPhySims Verified badge
- Announced on social media and newsletter

---

## Decision Thresholds

### Acceptance Criteria
A simulation is accepted if:
- **Scientific Accuracy** ≥ 4.0 (weighted average)
- **Code Quality** ≥ 3.5
- **Reproducibility** ≥ 3.5
- **Educational Value** ≥ 3.0
- **Overall Weighted Score** ≥ 3.7

### Rejection Criteria
A simulation is rejected if:
- Any criterion scores below 2.0
- Scientific Accuracy scores below 3.0
- Overall weighted score below 3.0
- Reviewers unanimously recommend rejection

---

## Reviewer Guidelines

### Reviewer Responsibilities
1. Complete reviews within the assigned timeframe (14–21 days)
2. Provide constructive, respectful feedback
3. Disclose any conflicts of interest immediately
4. Maintain confidentiality of the submission during review
5. Score objectively based on the established criteria
6. Provide specific, actionable suggestions for improvement

### Conflict of Interest
Reviewers must recuse themselves if:
- They are a co-author or collaborator of the submitter
- They work at the same institution as the submitter
- They have a personal relationship that could bias their judgment
- They have a financial interest in the simulation's success

### Review Quality Standards
Reviews should be:
- **Specific**: Cite particular code sections, equations, or documentation
- **Constructive**: Suggest improvements, not just point out problems
- **Respectful**: Maintain professional, collegial tone
- **Thorough**: Address all evaluation criteria
- **Fair**: Evaluate based on stated criteria, not personal preference

---

## Post-Publication

### Updates and Versioning
- Authors may submit updated versions of accepted simulations
- Major updates require re-review
- Minor updates (bug fixes, documentation) are reviewed by the Technical Director
- All versions are archived for reproducibility

### Corrections and Retractions
- Errors discovered post-publication are addressed through corrections
- Serious errors that invalidate results may lead to retraction
- Retractions are documented transparently with explanations

### Community Feedback
- Users may submit feedback on curated simulations
- Persistent issues may trigger re-review
- Community ratings supplement (but do not replace) editorial review

---

## Appeals Process

Authors who disagree with an editorial decision may:
1. Submit a formal appeal to the Technical Director within 30 days
2. Provide a detailed response to the review concerns
3. Request re-evaluation by a different set of reviewers
4. The Technical Director will make a final decision within 14 days

---

## Review Timeline Summary

| Step | Duration | Responsible Party |
|------|----------|-------------------|
| Submission | — | Author |
| Initial Screening | 1–3 days | Technical Staff |
| Peer Review | 14–21 days | Reviewers (×2) |
| Author Revision | 14–30 days | Author |
| Editorial Decision | 3–7 days | Editorial Board |
| Publication | 1–3 days | Technical Staff |
| **Total (typical)** | **33–64 days** | — |

---

## Appendix: Review Template

```markdown
# Peer Review Report

## Submission Information
- **Title**: 
- **Author(s)**: 
- **Domain**: 
- **Date Reviewed**: 

## Scores

| Criterion | Score (1–5) | Weight | Weighted |
|-----------|-------------|--------|----------|
| Scientific Accuracy | | 40% | |
| Code Quality | | 25% | |
| Reproducibility | | 20% | |
| Educational Value | | 15% | |
| **Overall** | | | **/5** |

## Detailed Comments

### Scientific Accuracy
[Detailed comments on physics correctness]

### Code Quality
[Detailed comments on code structure, documentation, tests]

### Reproducibility
[Comments on setup instructions, dependencies, execution]

### Educational Value
[Comments on documentation, target audience, learning materials]

## Summary
[Overall assessment and recommendation]

## Recommendation
- [ ] Accept
- [ ] Minor Revision
- [ ] Major Revision
- [ ] Reject

## Confidential Notes (for Editorial Board only)
[Any additional concerns or comments]
```

---

*This document is maintained by the IPhySims Editorial Board. Last updated: 2025.*
