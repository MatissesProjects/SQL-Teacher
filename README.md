# SQL Teacher (SQL Buddy)

A lightweight, browser-based interactive SQL learning tool that runs entirely locally using WebAssembly.

## Overview

**SQL Teacher** (also known as SQL Buddy) is a single-file application designed to help users learn and practice SQL queries without needing to set up a database server. It leverages `sql.js` to run a fully functional SQLite database directly in your web browser.

## New Features (v2.0)

-   **✅ Smart Validation:** The "Check Answer" button runs your query and compares the actual results with the expected solution, giving you instant verification.
-   **🏆 Progress Tracking:** Your completed lessons are saved locally. Look for the green checkmarks in the sidebar!
-   **👩‍🏫 Teacher Mode (Import Curriculum):** You can now load custom lesson plans (JSON files). Great for teachers creating specific assignments for students.
-   **🖥️ Presentation Mode:** A dedicated button to hide the sidebar and increase font sizes, perfect for projecting in a classroom.

## Standard Features

- **Zero Setup:** Just open the file in your browser. No server, node.js, or database installation required.
- **Interactive SQL Editor:** Write and execute queries with instant feedback.
- **Built-in Curriculum:** Structured lessons covering Foundations, Basics, Keys, Aggregation, Joins, and more.
- **Visual Schema:** See table structures, primary keys, and foreign keys at a glance.
- **Local Persistence:** Your custom snippets are saved to your browser's local storage.
- **Responsive UI:** Clean, dark-themed interface styled with Tailwind CSS.

## Getting Started

1.  Clone this repository or download the `index.html` file.
2.  Open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari).
3.  **To Learn:** Click a lesson in the sidebar. Read the task, write your SQL, and click "Check Answer".
4.  **To Teach:** Create a JSON curriculum file (see format below) and use the Upload icon in the sidebar header to load it.

## Custom Curriculum Format (JSON)

Teachers can create a `.json` file with the following structure to load their own lessons:

```json
{
  "curriculum": [
    {
      "category": "My Custom Module",
      "lessons": [
        { 
          "title": "Find the Gold", 
          "task": "Select all items with color 'Gold'", 
          "solution": "SELECT * FROM items WHERE color = 'Gold'" 
        }
      ]
    }
  ],
  "initSql": "CREATE TABLE items (id INT, color TEXT); INSERT INTO items VALUES (1, 'Gold');",
  "schema": {
    "items": { "id": { "type": "INT", "key": "PK" }, "color": { "type": "TEXT" } }
  }
}
```

## Tech Stack

-   **Core:** HTML5, Vanilla JavaScript
-   **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN)
-   **Icons:** [Lucide](https://lucide.dev/)
-   **Database Engine:** [sql.js](https://sql.js.org/) (SQLite compiled to WebAssembly)
