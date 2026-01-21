# SQL-Teacher Improvement Plan

## Goal
Enhance the existing single-file SQL learning tool to better support teaching multiple students in a classroom or workshop setting.

## Core Philosophy
- **Local-First:** Maintain the "no setup" advantage. Everything runs in the browser.
- **Teacher-Centric:** Empower the teacher to customize content and present effectively.
- **Student-Centric:** Provide better feedback and progress tracking.

## Phase 1: Interactive Learning & Validation (Completed)
- [x] **Result Comparison:** Implemented "Check Answer" button.
- [x] **Feedback UI:** Added success/failure messages.

## Phase 2: Progress Tracking (Completed)
- [x] **Lesson Status:** Tracking completed lessons in `localStorage`.
- [x] **Visual Indicators:** Added checkmarks next to completed lessons.

## Phase 3: Content Flexibility (The "Teacher" Feature) (Completed)
- [x] **Import Curriculum:** Added JSON import for custom lesson plans.
- [x] **Custom Init SQL:** Supported in the import format.

## Phase 4: Classroom/Presentation Tools (In Progress)
- [x] **Presentation Mode:** Added toggle for sidebar/font size.
- [ ] **Student Export:** Allow students to "Export Progress" (a JSON summary of their completed lessons and code) to submit to the teacher.

## Phase 5: Student Aids (New)
- [ ] **SQL Cheat Sheet:** A reference modal with common SQL syntax patterns.
- [ ] **Friendly Error Messages:** Intercept raw SQL errors and provide helpful hints (e.g., "Did you mean 'WHERE' instead of 'WERE'?").

## Technical Tasks
1.  **Student Export:** Add button and `exportProgress` function.
2.  **Cheat Sheet:** Add Modal HTML and toggle logic.
3.  **Error Handling:** Enhance `runQuery` catch block with regex-based hints.

## Future Ideas (Backlog)
-   In-browser schema builder/editor.
-   Multi-tab query editor.
-   Visual Query Builder (Drag and drop).