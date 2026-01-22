# SQL Teacher (SQL Buddy)

A lightweight, browser-based interactive SQL learning tool that runs entirely locally using WebAssembly.

## Overview

**SQL Teacher** (also known as SQL Buddy) is a single-file application designed to help users learn and practice SQL queries without needing to set up a database server. It leverages `sql.js` to run a fully functional SQLite database directly in your web browser.

## Key Features

-   **Educational Explanations:** Every lesson now includes a "Learn" section that explains the SQL concepts before you tackle the challenge.
-   **Smart Validation:** The "Check Answer" button runs your query and compares results with the solution for instant verification.
-   **Snippet Management:** Use the dedicated "Save as Snippet" button to store your favorite queries or work-in-progress scripts.
-   **Interactive Curriculum:** Structured lessons covering everything from Foundations and Basics to Aggregation, Joins, and Data Modification.
-   **Hover-to-Reveal Sidebar:** A sleek, auto-hiding sidebar that stays out of your way while you work, revealing the Curriculum and Schema only when you need them.
-   **Import/Export:** Export your progress as JSON or import custom curriculum files created by teachers.
-   **Visual Schema:** A collapsible schema viewer that shows table structures, Primary Keys, and Foreign Keys at a glance.
-   **Zero Setup:** Runs entirely in the browser using WebAssembly. No database or server installation required.

## Getting Started

1. Currently hosted at [sqlbuddy.matissetec.dev](https://sqlbuddy.matissetec.dev/) if you want to try without downloading

or host it locally

1.  Clone this repository or download the `index.html` file.
2.  Open `index.html` in any modern web browser.
3.  **To Learn:** Hover over the left edge of the screen to reveal the sidebar. Select a lesson, read the "Learn" context, and complete the "Challenge".
4.  **To Practice:** Write custom queries in the editor and use the "Save" icon to keep them in your "Saved Snippets" list.

## Custom Curriculum Format (JSON)

Teachers can create a `.json` file with the following structure:

```json
{
  "curriculum": [
    {
      "category": "My Custom Module",
      "lessons": [
        { 
          "title": "Find the Gold", 
          "explanation": "The WHERE clause filters data based on conditions.",
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
-   **Styling:** [Tailwind CSS](https://tailwindcss.com/)
-   **Icons:** [Lucide](https://lucide.dev/)
-   **Database Engine:** [sql.js](https://sql.js.org/) (SQLite via WebAssembly)
