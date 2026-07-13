# Learn SQL

This is a browser-based practice course for learning SQL from first queries
through joins, summaries, subqueries, and controlled table changes. It also
includes a small Python-to-SQL bridge.

This is Book 2 of the learning route. Start with
[Book 1, Learn Python Data Preparation](https://tidyweb.github.io/tidyweb-learn-python-data-preparation/)
if you first need to learn how to prepare a clean table for SQL.

## Start here

Open [`index.html`](index.html), then choose **Learner's Guide**. The guide
shows the route through the chapters and links to the practice labs.

You can also open the guide directly:

[`guide/html/SQLBolt Compressed Map.html`](guide/html/SQLBolt%20Compressed%20Map.html)

## Suggested route

1. Read the learner's guide overview.
2. Work through Chapters 1 to 6 in order.
3. Use the practice labs to repeat each group of ideas.
4. Use the reference pages when a piece of syntax needs a reminder.
5. Try the Coffee Python SQL Bridge after the SQL foundations are familiar.

## If you downloaded the project

Keep the folder structure together, including `datasets/`. The normal guide
pages can be read as local files, but the Python-to-SQL bridge loads its
bundled CSV through the browser and works best from a small local server. The
bridge also needs an internet connection to load its in-browser Python and SQL
engines.

From the project folder, run:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000/>. Stop the server with `Ctrl+C` when you
finish.

## What is included

- `guide/` — the learner's guide, chapters, references, and logo
- `exercises/` — interactive SQL practice labs and the Python-to-SQL bridge
- `datasets/` — the CSV files used by the exercises
- `shared/` — navigation used by the learner pages
- `* Lab Cheat Sheet.html` — optional answer references for the practice labs
