

### Iteration 1, Phase 1
**QA Failure Lesson:**

*   **Specific Failure:** `index.html` lacked complete JavaScript for 'random quote' and 'search' features; `quotes` array contained fewer than 50 unique quotes, directly violating project requirements.
*   **Root Cause:** Inadequate adherence to the full project specification and insufficient internal validation against all defined criteria before submitting to QA.
*   **Next Iteration Action:** Implement a mandatory "definition of done" checklist. Conduct thorough pre-QA self-review, explicitly verifying all specified features, data counts, and functional requirements.


### Iteration 1, Phase 1
*   **Game code and/or accompanying documentation failed to meet QA's functional and completeness criteria.** Specific defects or missing elements led to rejection.
*   **Inadequate definition of "done" for a "Hybrid (Code + Documents)" project.** Acceptance criteria for both code functionality and documentation quality were either unclear or not rigorously applied pre-QA.
*   **Establish explicit, measurable acceptance criteria for *all* deliverables (code, documentation, deployment readiness) *before* development begins.** Integrate pre-QA checklists into the development workflow.


### Iteration 1, Phase 1
**QA Rejected: Revision Routing** indicates a critical process failure, not a product bug.

*   **Specific Failure:** Incorrect or unapproved build submitted for QA, or the revision submission/routing process itself was non-compliant. This signifies a breakdown in the dev-to-QA handoff.
*   **Root Cause:** Absence of a formalized, enforced version control and build submission protocol. No clear, documented process for tagging QA-ready builds, routing them, or tracking integrated feedback.
*   **Next Iteration:** Implement strict Git tagging for QA builds (e.g., `v1.0-qa-ready`). Establish a mandatory build submission checklist. Utilize project management tools for formal QA ticket creation, feedback routing, and revision tracking.


### Iteration 1, Phase 1
*   **Specific Failure:** GitHub Pages deployment rejected. Content routing/presentation issues prevented v1 shipment.
*   **Root Cause:** Inadequate understanding and testing of GitHub Pages' base path and routing requirements. Local development environment did not accurately simulate deployment environment.
*   **Next Iteration:** Implement pre-deployment checks for GitHub Pages base path/routing. Develop and test locally using a configuration mirroring the GitHub Pages environment. Prioritize deployment environment compatibility from project inception.


### Iteration 2, Phase 1
**QA Rejected: Revision Routing**

*   **What specifically went wrong:** Iteration 2 failed QA due to incorrect revision routing. The submission process prevented proper review, not product quality.
*   **Root cause:** Lack of a clear, documented, and enforced protocol for submitting completed work to QA. Team members did not follow or were unaware of the correct routing procedure.
*   **What the team must do differently:** Establish and mandate a precise, step-by-step QA submission and routing process. Conduct immediate training to ensure all developers understand and adhere to the new protocol for future iterations.


### Iteration 2, Phase 1
**QA Rejected — Revision Routing**

*   **Specific Failure:** Iteration 2 rejected due to "Revision Routing" failure, indicating a breakdown in the process for re-submitting fixes or revised features to QA.
*   **Root Cause:** Absence of a clear, documented, and communicated workflow for handling post-feedback revisions and re-entry into the QA pipeline. Developers lacked explicit guidance on re-submission protocols.
*   **Next Iteration Action:** Implement a mandatory, documented QA re-submission protocol. This includes specific steps for developers to follow when addressing feedback, ensuring proper versioning, and clear communication channels for re-testing.


### Iteration 1, Phase 1
**QA Rejected — Revision Routing:**

*   **Task revision routing logic failed QA.** Users could not submit revisions, assignees were not notified, and task states did not update correctly after review/revision cycles.
*   **Root cause: Incomplete workflow definition.** Ambiguous requirements led to partial implementation and inadequate test coverage for critical state transitions and notification triggers.
*   **Next iteration: Detailed workflow diagrams.** Define explicit task states, revision loops, notification rules, and assignee responsibilities. Implement comprehensive test cases for all transitions and edge scenarios.
