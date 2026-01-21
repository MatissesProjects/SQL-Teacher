# SQL Teacher (SQL Buddy)

A lightweight, browser-based interactive SQL learning tool that runs entirely locally using WebAssembly.

![SQL Buddy Interface](https://via.placeholder.com/800x450?text=SQL+Buddy+Interface+Preview)

## Overview

**SQL Teacher** (also known as SQL Buddy) is a single-file application designed to help users learn and practice SQL queries without needing to set up a database server. It leverages `sql.js` to run a fully functional SQLite database directly in your web browser.

## Features

- **Zero Setup:** Just open the file in your browser. No server, node.js, or database installation required.
- **Interactive SQL Editor:** Write and execute queries with instant feedback.
- **Built-in Curriculum:** Structured lessons covering:
  - Foundations (SELECT, LIMIT, DISTINCT)
  - Basics (WHERE, LIKE)
  - Keys & Relationships (PK, FK)
  - Aggregation (COUNT, GROUP BY, AVG)
  - Joins (INNER, LEFT, MULTIPLE)
  - Data Modification (INSERT, UPDATE)
- **Visual Schema:** See table structures, primary keys, and foreign keys at a glance.
- **Local Persistence:** Your custom snippets are saved to your browser's local storage.
- **Responsive UI:** Clean, dark-themed interface styled with Tailwind CSS.

## Getting Started

1.  Clone this repository or download the `index.html` file.
2.  Open `index.html` in any modern web browser (Chrome, Firefox, Edge, Safari).
3.  Start with the "Curriculum" on the left sidebar or create a "New Snippet" to practice freely.

## Tech Stack

-   **Core:** HTML5, Vanilla JavaScript
-   **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN)
-   **Icons:** [Lucide](https://lucide.dev/)
-   **Database Engine:** [sql.js](https://sql.js.org/) (SQLite compiled to WebAssembly)
