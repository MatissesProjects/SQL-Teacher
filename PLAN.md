# SQL-Teacher Improvement Plan

## Goal
Enhance the existing single-file SQL learning tool to better support teaching multiple students in a classroom or workshop setting.

## Core Philosophy
- **Local-First:** Maintain the "no setup" advantage. Everything runs in the browser.
- **Teacher-Centric:** Empower the teacher to customize content and present effectively.
- **Student-Centric:** Provide better feedback and progress tracking.

## Phase 1: Interactive Learning & Validation (High Priority)
Currently, the tool only shows the solution text. We need active learning validation.
- [ ] **Result Comparison:** Implement a "Check Answer" button that runs both the user's query and the hidden solution query, then compares the result sets (rows and columns) to verify correctness.
- [ ] **Feedback UI:** Display success/failure messages (e.g., "Correct! 5 rows returned." or "Incorrect. Expected 5 rows, got 3.").

## Phase 2: Progress Tracking
Students need to know where they stand.
- [ ] **Lesson Status:** Track "Completed" status for each lesson in `localStorage`.
- [ ] **Visual Indicators:** Add checkmarks (✓) next to completed lessons in the sidebar.
- [ ] **Reset Progress:** Option to clear progress for a fresh start.

## Phase 3: Content Flexibility (The "Teacher" Feature)
Allow the user (teacher) to modify what is being taught without editing HTML code.
- [ ] **Import Curriculum:** Add a feature to upload a JSON file containing a custom lesson plan (Categories -> Lessons -> Tasks/Solutions).
- [ ] **Export Curriculum:** (Optional) If we build an in-app editor, allow exporting the modified state.
- [ ] **Custom Init SQL:** Allow the curriculum file to also define the database schema (INIT_SQL) so teachers can use their own datasets (e.g., a Library DB instead of the default Store DB).

## Phase 4: Classroom/Presentation Tools
- [ ] **Presentation Mode:** A toggle button to hide the sidebar, maximize the editor/result area, and increase font sizes for projector viewing.
- [ ] **Student Export:** Allow students to "Export Progress" (a JSON summary of their completed lessons and code) to submit to the teacher.

## Technical Tasks
1.  **Refactor:** Extract `CURRICULUM`, `INIT_SQL`, and `SCHEMA` handling to be more dynamic (reloadable).
2.  **Implementation:** Build the Validation Logic.
3.  **UI Update:** Add the "Check" button and Progress markers.
4.  **File I/O:** Implement JSON reading/writing for curriculum loading.

## Future Ideas (Backlog)
-   In-browser schema builder/editor.
-   Multi-tab query editor.
-   Visual Query Builder (Drag and drop).
